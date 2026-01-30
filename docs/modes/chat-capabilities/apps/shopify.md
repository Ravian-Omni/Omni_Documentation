# Shopify in Chat Mode

Connecting Shopify lets you **manage products, orders, customers, and inventory directly from chat**, handling store operations without switching apps.

Use it for order fulfillment, product updates, customer service, and sales analysis.

---

## What Shopify can do

Once Shopify is connected (Settings → Connections → Shopify), you can:

- Create/update products, variants, collections, and inventory.
- Process orders: fulfill, refund, tag, update customer info.
- Manage customers: create profiles, note interactions, segment lists.
- Retrieve sales data, abandoned checkouts, analytics.
- Handle discounts, shipping, and store settings.

!!! note
    Actions respect your Shopify permissions and store status (draft/live products).

---

## 1. Product management

### Create/update products and inventory

**Capabilities:** Create/update Product/Variant, manage inventory levels, collections.  

**What it does:** Adds products, updates pricing/stock, organizes into collections.

1. Add new product

    ```text title="Prompt – new product"
    Create a Shopify Product "Wireless Headphones Pro – Matte Black".
    Price: $129.99, Cost: $45.00, SKU: "WH-PRO-BLK".
    Variants: Size M/L (same price), Inventory: 50 units.
    Add description: "Premium noise‑cancelling with 30h battery."
    Put in "Electronics/Audio" collection. Make it available for sale.
    ```

2. Bulk price update

    ```text title="Prompt – update pricing"
    Find all Products tagged "winter-sale" with price > $50.
    Apply 25% discount to variants, round to nearest dollar.
    Update inventory description to note the sale price.
    Show before/after prices for the top 5 by revenue.
    ```

---

## 2. Order fulfillment and service

### Process orders and refunds

**Capabilities:** List/update orders, fulfill shipments, issue refunds, add tags/notes.  

**What it does:** Handles fulfillment workflow and customer support.

1. Fulfill recent orders

    ```text title="Prompt – ship orders"
    Find my unfulfilled Orders from the last 2 days where
    financial_status = "paid" and total_weight > 0.
    Fulfill each with tracking number "USPS 9400 1000 0000 0000 0000 00"
    (carrier: USPS, method: Priority Mail).
    Add note: "Shipped Jan 30 – expect delivery by Feb 2."
    ```

2. Process refund

    ```text title="Prompt – customer refund"
    For Order #1234567890 (the one with "defective headphones"),
    issue full refund ($129.99) to original payment method.
    Tag order "refunded-customer-service", add note:
    "Full refund issued due to defective unit. Apology email sent."
    ```

---

## 3. Customer profiles and segments

### Manage customers and lists

**Capabilities:** Create/update Customer records, add notes/tags, segment lists.  

**What it does:** Builds customer profiles and segments.

1. Create VIP customer

    ```text title="Prompt – new customer"
    Create Shopify Customer "Sarah Chen" email: sarah@techco.com,
    Phone: +1-555-9876, Accepts Marketing: yes.
    Note: "VIP – enterprise prospect, referred by Jordan Lee".
    Tag: "high-value-lead", add to "VIP Pipeline" customer group.
    Default address: 123 Tech St, San Francisco.
    ```

2. Segment analysis

    ```text title="Prompt – customer segments"
    Query Customers who:
    -  Ordered > $500 lifetime
    -  No orders in last 90 days
    -  Accepts marketing emails

    List top 10 by LTV with last order date.
    Suggest win-back discount codes for each.
    ```

---

## 4. Sales and analytics

### Retrieve reports and checkouts

**Capabilities:** List orders/checkouts, sales reports, abandoned cart recovery.  

**What it does:** Surfaces store performance and recovery opportunities.

1. Daily sales report

    ```text title="Prompt – sales summary"
    Show Orders from today grouped by product collection:
    -  Count, total revenue, average order value
    -  Top 3 products by units sold
    -  Payment methods breakdown

    Compare to yesterday's same metrics.
    ```

2. Abandoned checkout recovery

    ```text title="Prompt – cart recovery"
    List 5 most recent abandoned checkouts (> $100, < 24h old).
    For each: customer email, cart contents, total, abandoned time.
    Generate personalized recovery email text for the highest value one.
    ```

---

## 5. Discounts and promotions

### Create discount codes

**Capabilities:** Create/update Price Rules/Discount Codes.  

**What it does:** Launches promotions and coupons.

1. Flash sale code

```text title="Prompt – discount code"
Create Shopify discount code "FLASH25" – 25% off sitewide,
minimum purchase $75, valid for 48 hours, unlimited uses.
Target collections: exclude "clearance".
Auto‑apply to cart for first 100 uses.
```

---

## Best practices for Shopify

- **Reference specific IDs.** Use order numbers, product SKUs, customer emails for precision.  
- **Preview bulk actions.** Ask to "list first" before fulfilling/refunding multiple orders.  
- **Check inventory/stock.** Confirm levels before bulk updates.  
- **Combine with email.** Flow: analyze abandoned carts → create discount → send recovery emails → fulfill recovered orders.

To connect Shopify, open **Settings → Connections → Shopify**, enter your store domain and access token. Then run prompts directly from Chat Mode.