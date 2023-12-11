### Data Dictionary

`orders` (3.4m rows, 206k users):
* `order_id`: order identifier
* `user_id`: customer identifier
* `eval_set`: which evaluation set this order belongs in (see `SET` described below)
* `order_number`: the order sequence number for this user (1 = first, n = nth)
* `order_dow`: the day of the week the order was placed on
* `order_hour_of_day`: the hour of the day the order was placed on
* `days_since_prior`: days since the last order, capped at 30 (with NAs for `order_number` = 1)

`products` (50k rows):
* `product_id`: product identifier
* `product_name`: name of the product
* `aisle_id`: foreign key
* `department_id`: foreign key

`deptartments` (21 rows):
* `department_id`: department identifier
* `department`: the name of the department

`order_products_prior` (~3.2m orders):
* `order_id`: foreign key
* `product_id`: foreign key
* `add_to_cart_order`: order in which each product was added to cart
* `reordered`: 1 if this product has been ordered by this user in the past, 0 otherwise

`customers` (206K users)
* `user_id`: user identifier
* `First Name`: first name of the customer
* `Surnam`: last name of the customer
* `Gender`: gender of the customer
* `STATE`: resident state of the customer
* `Age`: age of the customer
* `date_joined`: date the customer joined instacart
* `n_dependants`: number of dependents the customer has
* `fam_status`: family status of the customer
* `income`: yearly income of the customer
