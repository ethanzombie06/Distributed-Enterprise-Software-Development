**Scope:** Use Case 1 - Producer Product Listing and Inventory Management  
**Prioritisation:** MoSCoW (Must, Should, Could)

| ID    | User story                                                                                                                                                                 | Priority | Acceptance criteria                                                                                                    | Status |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- | ---------------------------------------------------------------------------------------------------------------------- | ------ |
| PB-01 | As a registered producer, I want to enter a new product name, description, category, price, quantity, availability period, and farm origin so that I can create a listing. | Must     | All required fields are available and the product details can be submitted.                                            | To do  |
| PB-02 | As a producer, I want the system to validate my product information so that I can correct missing or invalid details.                                                      | Must     | Missing or invalid values are rejected with clear correction messages; valid values pass validation.                   | To do  |
| PB-03 | As a producer, I want to add optional harvest date, allergen, organic certification, and best-before information so that customers receive useful product details.         | Should   | Optional information can be recorded and displayed when provided; invalid dates or certification details are rejected. | To do  |
| PB-04 | As a producer, I want an organic certification claim to be checked by an external or simulated service so that the claim can be trusted.                                   | Must     | A valid certification is accepted; an invalid certification is rejected or marked unverified.                          | To do  |
| PB-05 | As a producer, I want to know when certification verification is unavailable so that I can retry or resolve the issue.                                                     | Must     | Service failure or timeout is recorded and shown as pending or failed; the product is not presented as verified.       | To do  |
| PB-06 | As a producer, I want a successfully validated product to be published so that customers can find it.                                                                      | Must     | A product is published only after mandatory validation succeeds and any required certification check is resolved.      | To do  |
| PB-07 | As a producer, I want to update available quantity so that the listing reflects current stock.                                                                             | Must     | Quantity updates are accepted only when zero or greater; the product becomes unavailable when quantity reaches zero.   | To do  |
| PB-08 | As a producer, I want to update seasonal availability so that customers can order products only during the correct period.                                                 | Must     | The availability period is validated; products outside the period cannot receive new orders.                           | To do  |
| PB-09 | As a customer, I want to see whether a product is available so that I do not try to order unavailable stock.                                                               | Must     | Customers can distinguish available, out-of-stock, out-of-season, pending, and unpublished products.                   | To do  |
| PB-10 | As a producer, I want a replenished product to become available again when it is still in season so that I can resume sales.                                               | Must     | A positive quantity restores availability only when the current date is within the seasonal period.                    | To do  |
| PB-11 | As a marketplace administrator, I want product, stock, validation, and certification changes to be recorded so that issues can be traced.                                  | Should   | Changes include the relevant action, time, user or service, and outcome.                                               | To do  |
| PB-12 | As a customer, I want accurate origin, allergen, best-before, and certification information so that I can make an informed purchase.                                       | Should   | Valid customer-facing information is shown clearly on published product listings.                                      | To do  |
| PB-13 | As a producer, I want listing and stock updates to respond quickly so that I can manage products efficiently.                                                              | Should   | Normal listing submissions and stock updates respond within an agreed target, such as two seconds, under normal load.  | To do  |
| PB-14 | As a customer, I want availability checks to remain reliable when several customers order at the same time so that stock is not oversold.                                  | Must     | Concurrent stock checks and orders complete safely without allowing available quantity to become negative.             | To do  |
| PB-15 | As a producer, I want certification checks to stop waiting after a reasonable time so that an unavailable service cannot block the system indefinitely.                    | Must     | Verification requests have a defined timeout and show pending or failed with a retry or escalation path.               | To do  |

## Suggested delivery order

1. **Foundation:** PB-01, PB-02
2. **Certification and publication:** PB-03, PB-04, PB-05, PB-06
3. **Inventory and seasonal availability:** PB-07, PB-08, PB-10
4. **Performance and reliability:** PB-13, PB-14, PB-15
5. **Customer visibility and traceability:** PB-09, PB-11, PB-12

## Definition of done

- The user story acceptance criteria are met.
- Validation and failure paths have been tested.
- The BPMN process and backlog requirements remain consistent.
- Customer-facing availability reflects stock and seasonal rules.
- Changes are reviewed by the group and recorded in the repository.
