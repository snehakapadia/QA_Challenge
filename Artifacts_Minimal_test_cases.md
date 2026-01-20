## **Minimal test cases**

1. Select each parcel size (XS, S, M, L, XL) and verify price, image, parcel size update correctly.
2. Switch parcel size after filling recipient details and ensure recipient form data is not lost.
3. Ensure Add to shopping cart will throw warning message when mandatory recipient data is not filled.
4. Enter edge-case inputs (e.g. House Number as "2342536y57689708" ) . Verify it will show warning "House number can't exceed 10 characters".
5. Verify total cost updates in cart when Parcel size changes, Delivery option changes, Country changes.
6. Add one item and confirm it appears correctly in the cart.
7. Edit parcel size from cart and verify price, size and total recalculate in cart. Save changes & verify save message.
8. Delete item in cart & verify if item got deleted & Total cost change reflected. Verify message of deletion.
9. Refresh the page and verify cart persistence.
10. Duplicate particular item 2 times & check if it gets added in cart with same destination country, size, price.
11. Attempt check out with missing or invalid recipient details.
12. Verify To check out button is disabled when cart is empty.
13. Verify if page gets redirects to link from "parcel-shipping/parcel-configuration" to "parcel-shipping/checkout"
14. Verify Sender form will throw warnings under respective fields if user clicks on save without filling form.
15. Verify if payment option is selected & can able to change to other option in between.
16. Verify discount code field will throw error "This discount code is invalid. Please enter a valid code." if wrong discount code entered.
17. Check APIs are throwing 200 status in network tab of devtools .
