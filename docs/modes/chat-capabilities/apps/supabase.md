# Supabase in Chat Mode

Connecting Supabase lets you **query, insert, update, and manage Postgres data directly from chat**, executing SQL operations securely without leaving your conversation.

Use it for data analysis, CRUD operations, schema changes, and real-time updates on your Supabase projects.

---

## What Supabase can do

Once Supabase is connected (Settings → Connections → Supabase), you can:

- Run SELECT, INSERT, UPDATE, DELETE queries with full SQL syntax.
- Analyze data: aggregations, joins, filters, sorting, pagination.
- Manage schema: create/update tables, indexes, functions (with safeguards).
- Handle real-time: subscribe to changes, trigger Edge Functions.
- Bulk operations and data migrations.

!!! warning
    Destructive operations (DELETE, DROP) require explicit confirmation. Always test SELECT queries first.

---

## 1. Query and analyze data

### SELECT queries and aggregations

**Capabilities:** Full SQL SELECT with JOINs, WHERE, GROUP BY, aggregations, pagination.  

**What it does:** Retrieves and summarizes data from tables.

1. Customer summary

    ```text title="Prompt – analyze customers"
    Query my Supabase `customers` table for top 10 customers by total spend:
    SELECT customer_id, name, SUM(order_amount) as lifetime_value
    FROM customers c JOIN orders o ON c.id = o.customer_id
    GROUP BY c.id ORDER BY lifetime_value DESC LIMIT 10;

    Show results as a formatted table.
    ```

2. Sales dashboard

    ```text title="Prompt – monthly sales"
    Run this query on `orders` table:
    SELECT DATE_TRUNC('month', order_date) as month,
    COUNT(*) as order_count, SUM(amount) as revenue
    FROM orders WHERE order_date >= NOW() - INTERVAL '12 months'
    GROUP BY month ORDER BY month DESC;

    Add a trend column showing % change month-over-month.
    ```

---

## 2. Create and update records

### INSERT/UPDATE/DELETE operations

**Capabilities:** INSERT new records, UPDATE existing, DELETE with conditions.  

**What it does:** Modifies data with precise WHERE clauses.

1. Add new orders

    ```text title="Prompt – insert orders"
    INSERT INTO orders (customer_id, product_id, amount, status, order_date)
    VALUES 
    (123, 456, 299.99, 'shipped', NOW()),
    (124, 457, 149.99, 'pending', NOW());

    Confirm exactly how many rows were inserted and show the new order IDs.
    ```

2. Update customer status

    ```text title="Prompt – bulk update"
    UPDATE customers SET status = 'vip', last_contacted = NOW()
    WHERE lifetime_value > 5000 AND last_login > NOW() - INTERVAL '30 days';

    Show me the count of affected rows and a sample of updated records.
    ```

---

## 3. Schema management

### Tables, indexes, functions

**Capabilities:** CREATE/ALTER/DROP TABLE, INDEX, VIEW, FUNCTION (with confirmation).  

**What it does:** Evolves your database structure safely.

1. Create audit table

    ```text title="Prompt – new table"
    CREATE TABLE IF NOT EXISTS audit_logs (
    id SERIAL PRIMARY KEY,
    table_name TEXT NOT NULL,
    record_id UUID,
    action TEXT CHECK (action IN ('INSERT','UPDATE','DELETE')),
    old_data JSONB,
    new_data JSONB,
    user_id UUID,
    created_at TIMESTAMP DEFAULT NOW()
    );

    Confirm the table was created and show its structure.
    ```

2. Add index for performance

    ```text title="Prompt – optimize query"
    CREATE INDEX CONCURRENTLY IF NOT EXISTS idx_orders_customer_date
    ON orders (customer_id, order_date DESC);

    Verify the index exists and suggest if it covers my common sales query.
    ```

---

## 4. Real-time and Edge Functions

### Subscriptions and serverless

**Capabilities:** Real-time channel subscriptions, invoke Edge Functions.  

**What it does:** Listens for changes and triggers functions.

1. Monitor new orders

    ```text title="Prompt – real-time orders"
    Subscribe to INSERT on `orders` table where amount > 1000.
    For each new high-value order, show: customer name, amount, timestamp.
    Keep listening for 5 minutes.
    ```

2. Trigger notification function

    ```text title="Prompt – invoke Edge Function"
    Invoke my `send-sms-notification` Edge Function with payload:
    {
    "customer_id": 123,
    "message": "Your order no-456 has shipped!"
    }

    Show the function response.
    ```

---

## 5. Data migrations and cleanup

### Bulk operations and archiving

**Capabilities:** Complex migrations, DELETE with safeguards.  

**What it does:** Handles data hygiene and transformations.

1. Archive old data

    ```text title="Prompt – data cleanup"
    Find orders older than 2 years with status = 'cancelled'.
    DELETE FROM orders WHERE order_date < NOW() - INTERVAL '2 years'
    AND status = 'cancelled';

    **Confirm first**: Show count and sample records before deleting.
    ```

2. Migrate customer segments

    ```text title="Prompt – segment migration"
    INSERT INTO customer_segments (customer_id, segment, updated_at)
    SELECT id, 
    CASE 
        WHEN lifetime_value > 10000 THEN 'enterprise'
        WHEN lifetime_value > 1000 THEN 'premium'
        ELSE 'standard'
    END,
    NOW()
    FROM customers WHERE segment IS NULL;

    Update original table with new segment and show distribution stats.
    ```

---

## Best practices for Supabase

- **Always test with SELECT.** Verify your WHERE clause returns expected rows before UPDATE/DELETE.  
- **Use LIMIT for safety.** Add LIMIT 10 to exploratory queries.  
- **Explicit schema names.** Prefix tables with schema if not public (e.g., `app.orders`).  
- **Confirm destructive ops.** Phrase as "Show me what will be affected first, then execute."  
- **Combine with analysis tools.** Query → summarize → visualize → export.

To connect Supabase, open **Settings → Connections → Supabase**, enter your project URL and service key. Then run SQL prompts directly from Chat Mode.