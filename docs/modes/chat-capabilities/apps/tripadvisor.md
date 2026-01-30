# TripAdvisor in Chat Mode

Connecting TripAdvisor lets you **access location details, reviews, photos, hotels, activities, awards, and geos directly from chat** via Content API for travel insights.

Use it for trip planning, hotel research, review analysis, and destination discovery.

---

## What TripAdvisor can do

Once TripAdvisor is connected (Settings → Connections → TripAdvisor), you can:

- Get location details, reviews/photos V2, hotels, activities.
- Retrieve awards, geos (geographies) for areas.

**Auth:** API key.

---

## 1. Location details

### Core info

**Capabilities:** `TRIPADVISOR_GET_LOCATION_DETAILS_V2`.  

**What it does:** Fetches place data.

1. Hotel lookup

```text title="Prompt – property research"
Get details for location ID 12345678 (Paris Hilton).
Include address, ratings, amenities.
```

---

## 2. Reviews analysis

### User feedback

**Capabilities:** `TRIPADVISOR_GET_LOCATION_REVIEWS_V2`.  

**What it does:** Extracts opinions.

1. Recent reviews

```text title="Prompt – sentiment check"
Get reviews V2 for ID 12345678, limit 20, sort recent.
Summarize top complaints/praises.
```

---

## 3. Photos and visuals

### Images

**Capabilities:** `TRIPADVISOR_GET_LOCATION_PHOTOS_V2`.  

**What it does:** Media gallery.

1. Property images

```text title="Prompt – visual tour"
Get photos V2 for location 12345678.
Categories: exterior, rooms, pool.
List top 5 URLs with captions.
```

---

## 4. Hotels and accommodations

### Lodging options

**Capabilities:** `TRIPADVISOR_GET_LOCATION_HOTELS`.  

**What it does:** Hotel listings.

1. Area hotels

```text title="Prompt – stay options"
Get hotels near geo ID 60763 (New York).
Filter 4+ stars, price low-high.
Top 10 by ranking.
```

---

## 5. Activities and attractions

### Things to do

**Capabilities:** `TRIPADVISOR_GET_LOCATION_ACTIVITIES`, `TRIPADVISOR_GET_LOCATION_GEOS`, `TRIPADVISOR_GET_LOCATION_AWARDS`.  

**What it does:** Experiences and accolades.

1. Top attractions

```text title="Prompt – itinerary build"
Get activities for location 12345678.
Geos nearby, awards list.
Recommend 3-day plan.
```

---

## Best practices for TripAdvisor

- **Location ID first.** Search/find ID via geo/tools.  
- **V2 endpoints.** Use for reviews/photos.  
- **Limits respect.** Paginate large results.  
- **Combine travel.** TripAdvisor + Google Maps.

To connect TripAdvisor, open **Settings → Connections → TripAdvisor** (API key auth config). Then run prompts directly from Chat Mode.