# FedEx (fedex)

FedEx is a logistics company that provides shipping and delivery services worldwide. They offer a range of solutions for individuals and businesses, including express shipping, freight services, and e-commerce fulfillment. FedEx publishes a suite of REST APIs covering tracking, shipping, rating, address validation, pickup, locator, trade documents, and post-shipment visibility through their developer portal.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/fedex/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fedex/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Address Validation
- Freight
- Logistics
- Pickup
- Rating
- Shipping
- Tracking
- Webhooks

## Timestamps

- **Created:** 2025-03-01
- **Modified:** 2026-05-04

## APIs

### FedEx Track API

Track API allows customers and partners to retrieve up-to-the-minute package and shipment status, scan events, delivery details, and proof of delivery using tracking numbers, reference numbers, or TCN.

- **Human URL:** [https://developer.fedex.com/api/en-us/catalog/track/v1/docs.html](https://developer.fedex.com/api/en-us/catalog/track/v1/docs.html)
- **Base URL:** `https://apis.fedex.com`

#### Tags

- Tracking
- Shipping
- Logistics

#### Properties

- [Documentation](https://developer.fedex.com/api/en-us/catalog/track/v1/docs.html)
- [Getting Started](https://developer.fedex.com/api/en-us/get-started.html)
- [Postman Collection](collections/fedex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fedex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FedEx Ship API

Ship API lets developers create domestic and international shipments, generate shipping labels, validate addresses, schedule pickups, and manage end-to-end shipment workflows programmatically.

- **Human URL:** [https://developer.fedex.com/api/en-us/catalog/ship/v1/docs.html](https://developer.fedex.com/api/en-us/catalog/ship/v1/docs.html)
- **Base URL:** `https://apis.fedex.com`

#### Tags

- Shipping
- Labels
- Logistics

#### Properties

- [Documentation](https://developer.fedex.com/api/en-us/catalog/ship/v1/docs.html)
- [Postman Collection](collections/fedex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fedex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FedEx Rate API

Rate API returns rate quotes and transit times for FedEx Express, Ground, Freight, and SmartPost services so applications can present pricing and delivery options at checkout or during fulfillment.

- **Human URL:** [https://developer.fedex.com/api/en-us/catalog/rate/v1/docs.html](https://developer.fedex.com/api/en-us/catalog/rate/v1/docs.html)
- **Base URL:** `https://apis.fedex.com`

#### Tags

- Rating
- Shipping
- Pricing

#### Properties

- [Documentation](https://developer.fedex.com/api/en-us/catalog/rate/v1/docs.html)
- [Postman Collection](collections/fedex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fedex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FedEx Address Validation API

Address Validation API verifies postal addresses for deliverability, classifies them as residential or commercial, and corrects common formatting and spelling issues prior to shipment creation.

- **Human URL:** [https://developer.fedex.com/api/en-us/catalog/address-validation/v1/docs.html](https://developer.fedex.com/api/en-us/catalog/address-validation/v1/docs.html)
- **Base URL:** `https://apis.fedex.com`

#### Tags

- Address Validation
- Shipping

#### Properties

- [Documentation](https://developer.fedex.com/api/en-us/catalog/address-validation/v1/docs.html)
- [Postman Collection](collections/fedex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fedex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FedEx Pickup API

Pickup API provides programmatic access to schedule, modify, and cancel package pickups, and to determine pickup availability for a given origin and service combination.

- **Human URL:** [https://developer.fedex.com/api/en-us/catalog/pickup/v1/docs.html](https://developer.fedex.com/api/en-us/catalog/pickup/v1/docs.html)
- **Base URL:** `https://apis.fedex.com`

#### Tags

- Pickup
- Shipping
- Logistics

#### Properties

- [Documentation](https://developer.fedex.com/api/en-us/catalog/pickup/v1/docs.html)
- [Postman Collection](collections/fedex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fedex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FedEx Locations API

Locations API helps applications find FedEx Office, FedEx Ship Center, drop boxes, and authorized ship centers near a given address or coordinate, including hours of operation and supported services.

- **Human URL:** [https://developer.fedex.com/api/en-us/catalog/locations/v1/docs.html](https://developer.fedex.com/api/en-us/catalog/locations/v1/docs.html)
- **Base URL:** `https://apis.fedex.com`

#### Tags

- Locations
- Shipping

#### Properties

- [Documentation](https://developer.fedex.com/api/en-us/catalog/locations/v1/docs.html)
- [Postman Collection](collections/fedex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fedex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FedEx Authorization API

Authorization API issues OAuth 2.0 access tokens used to authenticate all other FedEx API calls. Tokens are obtained via client credentials generated from a FedEx Developer Portal project.

- **Human URL:** [https://developer.fedex.com/api/en-us/catalog/authorization/v1/docs.html](https://developer.fedex.com/api/en-us/catalog/authorization/v1/docs.html)
- **Base URL:** `https://apis.fedex.com`

#### Tags

- Authentication
- OAuth

#### Properties

- [Documentation](https://developer.fedex.com/api/en-us/catalog/authorization/v1/docs.html)
- [Postman Collection](collections/fedex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fedex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### FedEx Shipment Visibility Webhook

Shipment Visibility Webhook pushes near real-time tracking events to a registered HTTPS endpoint, eliminating the need to repeatedly poll the Track API for shipment status changes.

- **Human URL:** [https://developer.fedex.com/api/en-us/catalog/svm/v1/docs.html](https://developer.fedex.com/api/en-us/catalog/svm/v1/docs.html)
- **Base URL:** `https://apis.fedex.com`

#### Tags

- Webhooks
- Tracking
- Shipping

#### Properties

- [Documentation](https://developer.fedex.com/api/en-us/catalog/svm/v1/docs.html)
- [Postman Collection](collections/fedex.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fedex.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/fedex)
- [Website](https://www.fedex.com/)
- [Documentation](https://developer.fedex.com/api/en-us/home.html)
- [Getting Started](https://developer.fedex.com/api/en-us/get-started.html)
- [Catalog](https://developer.fedex.com/api/en-us/catalog.html)
- [Sign Up](https://developer.fedex.com/api/en-us/home.html)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
