## **Application Overview**
This page shows Parcel configuration. Left side is form showing different Parcel sizes(XS,S,M,L,XL) with different rates & respective images. Another form field is Recepient details(Name, Address, Email, Two Delivery options) & 
Add to shopping Cart button . Right side cart will be empty initially however it depends on left side . Once we fill all details & click on Add to shopping cart . It will add 1 or more parcel to cart. Cart will show options including duplicate, Delete,
Edit with which customer can add/modify parcel. Then customer can checkout with Sender details & completeing payment on another page.User is landed on success page with shipping label will get generate after clicking on Buy now. If Payment fails then user will stay on check out page with error details.

## **Required Reflections**

## **Understanding the product Answers**

1. This product cares most about ensuring the parcel is configured correctly including the right size, delivery options and destination so the price is accurate and added to        the cart with proper recipient details, sender details & shippment label should generate correctly with payment success.  
       It ensures the cart always reflects the correct items and total cost, allowing safe edits or deletions and that checkout only proceeds when all information is valid           protecting both revenue and customer trust.
2. Primary users of this product are Customers who need to ship parcels. This includes individuals and businesses purchasing shipping labels, configuring parcel sizes and            destinations and paying for deliveries through the platform. 
3. I assumed that each parcel size maps to a specific price and image and that selecting or changing parcel options updates the total correctly in the cart. 
   I assumed the cart always reflects the latest items, edits and deletions and duplicates. I assumed Add to shoping cart only allows proper size, valid reciepient               address.Checkout only allows complete and valid sender and payment information and that payment and label generation interact correctly with carrier APIs like GLS/NXT. 
   I also assumed the page works across desktop and mobile, handles slow networks or mid-flow changes gracefully. I assume Add to shopping card api https://www.gls-              pakete.de/en/private-customers/parcel-shipping/parcel-configuration gives 200 status ok . Also to checkout button triggers https://www.gls-pakete.de/en/private-               customers/parcel-shipping/checkout api post should return 200. 


## **Quality Risks**
1. For Customers Overpayment or underpayment – Total cost displayed may not match the amount charged.
   - Wrong shipment details – Parcel size, delivery option or recipient address may be incorrect leading to delivery failure.
   - Duplicate orders – Adding the same parcel multiple times by mistake may lead to an issue.
   - Checkout failures – Payment might fail or be blocked even when details are correct.3DS payment getway might show issue.
   - Checkout or Buy Now flow intermittently fails
   - Errors or unclear messages – Validation errors that don’t explain how to fix the problem.
   - Loss of progress – Cart cleared or data lost if the user refreshes the page navigates away or switches devices.
   - Delays – Slow price updates, cart recalculation or label generation leading to abandonment.

For Business: Refunds & customer support  – Failed or incorrect shipments, duplicate orders or  payment errors lead to extra refunds and increased customer support.
Failed or delayed label generation – Carrier integration problems (GLS/NXT API) could block shipping so delaying deliveries.
Customer trust/reputation damage – Confusing totals, incorrect labels or checkout failures reduce trust and retention.
Compliance or legal risk – Incorrect customs data or failed shipments can create regulatory issues.


2. One risk that worries me is customs-related issues. Sometimes parcels may be delayed, returned or blocked because of incorrect documentation, restricted items or sudden customs fees. 
This means customers don’t receive their shipments on time and may face unexpected charges which hurts trust and satisfaction. 
It also creates operational issues for carriers who must handle returns, disputes or additional payments impacting both the business and delivery reliability.


## **Decisions & Trade offs**

1. I focused on ensuring the functionality & API in devtools of E2E flow works fine on mobile & web on different browsers from Parcel configuration to Label generation with          correct details . If negative scenarios showing proper errors. Also i willl check edge cases.
       Finally I made sure core flows—from parcel configuration to add-to-cart and checkout—work reliably so failures don’t propagate and affect orders.
2. I will not try to cover 100% test coverage , small less priority severity tsetcases. Instead i will focus on High risk & high impact scenarios that affect revenue,                payments and label correctness. I did not treat every bug as release-blocking. I prioritized issues based on customer impact.
3. With one more day I would focus on more exploratory testing  , finding more bugs.

## **Use of Tools / AI **

 1. I use AI tools to brainstorm test ideas, risks and edge cases and to gain broader product understanding helping me think through flows and scenarios more effectively.
 2. Accepted high-level ideas, modified them to fit the real system and priorities and rejected anything unrealistic or assumption-based.
 3. Yes as AI is vast it gives some information which is not realistic with product we work so I just ignore it or I give specific question or correct them.
