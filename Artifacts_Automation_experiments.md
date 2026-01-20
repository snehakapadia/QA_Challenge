## **Automation Experiments**

E2E 
Test Scenario high prio
1.Customer can configure a parcel -> Fill recipient detils -> Packet size ->Click on Add to shopping cart-> Verify view cart -> Click on to check out -> check redirection of page-> 
Fill sender details-> Fill payment method & valid discount code -> Verify cart again-> Click on BUy now-> Check Order confirmation / success state (Shipping label cretaed.
(Playwright or Cypress framework with Page object model) or can covered manually iitially.

Integration 
1. During checkout cart total and payment details are sent to the payment gateway for processing.
       Verify:
       Payment request succeeds (200 OK) for valid transactions.
       Payment failures (insufficient funds, 401 unauthorized, 402 declined) are handled correctly.
2. When a customer selects parcel size, destination country and delivery option the pricing service calculates the correct price.
       Verify:
       API returns 200 OK with correct pricing details.
       Invalid input returns 4xx errors (e.g., 400 for invalid country/size).
       Service failures return 5xx errors and the UI handles it gracefully without incorrect totals.
   Can cover in playwright frameowrk
   
Api test 
1. Cart API Test (Add / Edit / Delete Items)
       Scenario:Add, edit, or delete a parcel from the cart using the cart API.
       Verify:
       Correct 200 OK responses with updated cart state.
       Cart total matches backend calculation.
       Invalid updates return 4xx errors without corrupting cart data.
2. Carrier / Label Generation API Test
       Scenario:Generate shipping label after checkout.
       Verify:
       200 OK returns label URL and tracking number.
       4xx / 5xx errors handled without crashing the system.
       Invalid addresses or unsupported destinations fail gracefully.
   Can cover in playwright frameowrk or any other .

Accessibility test 
User can complete parcel configuration using keyboard only

Mobile 
Cart behavior on mobile ios(Safari) & Android(Chrome etc) . Cart opens/closes reliably. Edit/delete buttons are tappable (not too small)
Visual regression test for Parcel size images on Page . Can check with Browserstack or Lambdatest
