# permalinks-with-selling-plan

## Pre-Load Cart With Subscription/Plan Products Using Permalinks
I believe I figured it out, this url will clear the cart, add items with a selling_plan and then redirect to checkout:
```
https://{SHOP}.myshopify.com/cart/clear?return_to=/cart/add?items[][id]={VARIANT_ID}%26items[][quantity]={QUANTITY}%26items[][selling_plan]={SELLING_PLAN_ID}%26return_to=/checkout
```

To head to the cart page instead of directly to checkout, you can remove the `%26return_to=/checkout`.

```
https://myshop.com/cart/add?id=42021984993480&quantity=1&selling_plan=858226888&return_to=/checkout
```
