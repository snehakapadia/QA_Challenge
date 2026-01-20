## **Exploratory**

1. Rapid Add / Edit / Delete in Cart
   Add a parcel & quickly change size/delivery option then delete it multiple times.
   Observe if totals, cart state and images update correctly without duplication or stale data.

2. Invalid or Edge Input Testing
   Enter long names, special characters or invalid addresses in recipient or sender details.
   Check that validation errors appear correctly and the system does not crash.

3. Payment & Discount Edge Cases
   Apply invalid, expired or edge-case discount codes.
   Try a payment failure scenario . Ensure errors are clear and cart remains accurate.

4. Cart Persistence Across Refresh / Navigation
   Add items to the cart then refresh the page or navigate away and back.
   Verify that cart contents, totals and configurations are preserved correctly.

## **Understanding the product Answers**

1. This product cares most about ensuring the parcel is configured correctly including the right size, delivery options and destination so the price is accurate and added to        the cart with proper recipient details, sender details & shippment label should generate correctly with payment success.  
       It ensures the cart always reflects the correct items and total cost, allowing safe edits or deletions and that checkout only proceeds when all information is valid           protecting both revenue and customer trust.
2. Primary users of this product are Customers who need to ship parcels. This includes individuals and businesses purchasing shipping labels, configuring parcel sizes and            destinations and paying for deliveries through the platform. 
3. I assumed that each parcel size maps to a specific price and image and that selecting or changing parcel options updates the total correctly in the cart. 
   I assumed the cart always reflects the latest items, edits and deletions and duplicates. I assumed Add to shoping cart only allows proper size, valid reciepient               address.Checkout only allows complete and valid sender and payment information and that payment and label generation interact correctly with carrier APIs like GLS/NXT. 
   I also assumed the page works across desktop and mobile, handles slow networks or mid-flow changes gracefully. I assume Add to shopping card api https://www.gls-              pakete.de/en/private-customers/parcel-shipping/parcel-configuration gives 200 status ok . Also to checkout button triggers https://www.gls-pakete.de/en/private-               customers/parcel-shipping/checkout api post should return 200. 
