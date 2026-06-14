# FedEx GraphQL Schema

## Overview

This conceptual GraphQL schema represents the FedEx shipping and logistics platform APIs, covering the full lifecycle of shipment creation, tracking, rating, pickup scheduling, location lookup, and address validation. It is derived from the FedEx REST API surface available at https://developer.fedex.com/ and models the core domain objects, enumerations, and operations offered by the FedEx Web Services API suite.

The schema unifies capabilities across the FedEx Track API, Ship API, Rate API, Address Validation API, Pickup API, Locations API, Authorization API, and the Shipment Visibility Webhook into a single coherent type system.

## Source

- Developer Portal: https://developer.fedex.com/
- Track API: https://developer.fedex.com/api/en-us/catalog/track/v1/docs.html
- Ship API: https://developer.fedex.com/api/en-us/catalog/ship/v1/docs.html
- Rate API: https://developer.fedex.com/api/en-us/catalog/rate/v1/docs.html
- Address Validation API: https://developer.fedex.com/api/en-us/catalog/address-validation/v1/docs.html
- Pickup API: https://developer.fedex.com/api/en-us/catalog/pickup/v1/docs.html
- Locations API: https://developer.fedex.com/api/en-us/catalog/locations/v1/docs.html
- Authorization API: https://developer.fedex.com/api/en-us/catalog/authorization/v1/docs.html
- Shipment Visibility Webhook: https://developer.fedex.com/api/en-us/catalog/svm/v1/docs.html

## Top-Level Operations

### Queries

- `trackShipment(trackingNumber: String!, shipDateBegin: String, shipDateEnd: String): TrackingDetails` — Retrieve current status and event history for a shipment.
- `trackByReference(referenceNumber: String!, accountNumber: String!): [TrackingDetails]` — Track packages using a customer reference number.
- `getRates(rateRequest: RateRequest!): RateReply` — Retrieve rate quotes and transit times for proposed shipments.
- `validateAddress(address: AddressInput!): AddressValidationResult` — Verify and correct a postal address.
- `findLocations(address: AddressInput!, radius: Int, services: [ServiceType]): [ServiceCenter]` — Find nearby FedEx drop-off or service locations.
- `getPickupAvailability(originAddress: AddressInput!, packageCount: Int, weight: WeightInput!): PickupAvailability` — Check if pickup service is available for a given address and package profile.

### Mutations

- `createShipment(request: CreateShipmentRequest!): CreateShipmentReply` — Create a domestic or international shipment and generate a shipping label.
- `cancelShipment(trackingNumber: String!, accountNumber: String!): Boolean` — Cancel a previously created shipment.
- `createReturnShipment(request: ReturnShipmentRequest!): CreateShipmentReply` — Create a return label for a shipment.
- `schedulePickup(request: PickupRequest!): PickupConfirmation` — Schedule a package pickup at an origin address.
- `cancelPickup(confirmationNumber: String!, accountNumber: String!): Boolean` — Cancel a scheduled pickup.
- `registerWebhook(endpoint: String!, events: [WebhookEventType]!, accountNumber: String!): Webhook` — Register a webhook endpoint to receive shipment visibility events.
- `deleteWebhook(webhookId: String!): Boolean` — Remove a registered webhook.
- `generateToken(clientId: String!, clientSecret: String!): Token` — Obtain an OAuth 2.0 access token for API authentication.

## Key Types

- **Shipment / ShipmentDetails / ShipmentRequest / ShipmentResult** — Core shipment lifecycle objects covering creation request, server response, and persistent shipment state.
- **TrackingNumber / TrackingDetails / TrackingEvent / TrackingStatus / TrackingLocation** — Full tracking domain: number representation, aggregated details per package, individual scan events, status codes, and geo-located scan points.
- **SignatureProof / POD** — Proof of delivery and signature capture data returned after confirmed delivery.
- **Label / LabelFormat / LabelSize / ShippingLabel / ClearanceLabel / DangerousLabel** — Label generation types covering format (PDF, PNG, ZPL), size options, and specialized label categories for customs clearance and dangerous goods.
- **Service / ServiceType / ServiceCode** — FedEx service catalog enumeration and metadata (Express, Ground, Freight, SmartPost, International).
- **PackageType / PackageDetails / Weight / Dimensions / Oversize** — Package physical attributes and FedEx packaging classifications.
- **SpecialService / HoldAtLocation / SignatureOption / SaturdayDelivery / AdultSignature / DirectSignature** — Optional service add-ons modifying default delivery behavior.
- **SenderInfo / RecipientInfo** — Contact and address information for shipment origin and destination parties.
- **BillingInfo / ThirdParty / DutiesPayor** — Billing arrangement types supporting sender-pay, recipient-pay, and third-party billing for both transportation and duties/taxes.
- **COD** — Cash on delivery configuration for eligible service types.
- **ReturnLabel / ReturnShipment** — Return logistics objects for pre-paid label generation and reverse logistics tracking.
- **RateRequest / RateReply / RateDetail / DiscountDetail / SurchargeDetail / FuelSurcharge** — Full rating domain: input request, aggregated reply, per-service rate details, applied discounts, and surcharge breakdowns.
- **CommitDetail / DeliveryEstimate** — Commit date/time and estimated delivery window objects returned alongside rate quotes.
- **SmartPost / GroundService / ExpressService / FreightService / InternationalService** — Service-specific option types carrying parameters unique to each FedEx service family.
- **PickupRequest / PickupConfirmation / PickupAvailability** — Pickup scheduling request, confirmation, and availability check objects.
- **DropoffLocation / ServiceCenter** — FedEx physical location types returned by the Locations API.
- **AddressInput / AddressValidationResult / ValidatedAddress** — Address input shape and validation result with residential/commercial classification and corrected address data.
- **APIKey / Token** — Authentication credential types for OAuth 2.0 token issuance and management.
- **Webhook / WebhookEvent / WebhookEventType** — Webhook registration and event payload types for shipment visibility push notifications.

## Access

FedEx APIs require a FedEx Developer Portal account. Access is granted via OAuth 2.0 client credentials (client ID and secret) obtained from a registered developer project. There is no publicly listed pricing; enterprise rates are negotiated through FedEx account contracts.

- Sign Up: https://developer.fedex.com/api/en-us/home.html
- Getting Started: https://developer.fedex.com/api/en-us/get-started.html
