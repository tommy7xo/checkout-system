Here is my simple checkout system. It allows to creates discounts of users purchase. I created two types of discounts - product discount and global discount. First one is a change in product price if user adds a particular quantity of products. Second is a discount off the whole purchase when basket value is bigger than provided one. To make it flexible you can create any global discount that you want (or no discount at all). You can also add many product discounts for different products and product quantities and values. To run it type:
> ruby checkout_system.rb

It uses the interface you provided:

```ruby
co = Checkout.new(promotional_rules)
co.scan(item)
co.scan(item)
price = co.total
```

You can checkout products any time, each time a total value will be recalculated.

It the checkout_system.rb I implemented conditions and test examples you provided:

If you spend over £60, then you get 10% off of your purchase.
If you buy 2 or more lavender hearts then the price drops to £8.50.

```
Test data
---------
Basket: 001,002,003
Total price expected: £66.78

Basket: 001,003,001
Total price expected: £36.95

Basket: 001,002,001,003
Total price expected: £73.76
```

Additionally I created specs to test each method of each class.