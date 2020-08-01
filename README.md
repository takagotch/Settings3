### Settings4
---

```
rails new depot
rails new g scaffold Product title:string description:text image_url:string price:decimal
vi depot_a/db/migrate/202008011235_create_products.rb
rake db:migrate
rails s
vi depot_a/app/views/products/_form.html.rb
rake test
vi depot_a/app/db/seeds.rb
rake db:seed
vi depot_a/app/assets/stylesheets/products.css.scss
vi depot_a/app/views/layouts/application.html.erb
vi depot_a/app/view/products/index.html.erb
curl https://localhost:3000/products
rake db:rollback
vi depot_b/.gitignore

vi depot_b/app/models/product.rb
rake test
vi depot_b/test/functional/products_controller_test.rb
ls test/unit
vi depot_a/test/unit/product_test.rb
vi depot_b/test/unit/product_test.rb
rake test:units
vi depot_c/test/unit/product_test.rb
vi depot_c/test/unit/product_test.rb
vi depot_b/test/fixtures/products/yml
vi depot_c/test/fixtures/products.yml
vi depot_c/test/unit/product_test.rb
vi depot_c/test/unit/product_test.rb

rails g controller Store index
vi depot_d/config/routes.rb
rm public/index.html
vi depot_d/app/controllers/store_controller.rb
vi depot_d/app/views/store/index.html.erb
vi depot_d/app/assets/stylesheets/store.css.scss
vi depot_e/app/views/layouts/application.html.erb
vi depot_e/app/assets/stylesheets/layout.css.scss
vi depot_e/app/views/store/index.html.erb
vi rake test
vi depot_d/test/functional/store_controller_test.rb
vi depot_e/test/functional/store_controller_test.rb
vi depot_e/test/fixtures/products.yml
rake test:functionals

rails g scaffold cart
rake db:migrate
vi depot_f/app/controllers/application_controller.rb
rails g scaffold line_item product_id:integer cart_id:integer
rake db:migrate
vi depot_f/app/models/line_item.rb
vi depot_f/app/models/product.rb
vi depot_f/app/views/store/index.html.erb
vi depot_f/app/assets/stylesheets/store.css.scss
vi depot_f/app/controllers/line_items_controller.rb
vi depot_g/test/functional/line_items_controller_test.rb
rake test:functionals
vi depot_f/app/views/carts/show.html.erb

rails g migration add_quantity_to_line_items quantity:integer
// cp depot_f depot_g
vi depot_g/db/migrate/202008011336__add_quantity_to_line_items.rb
rails db:migrate
vi depot_g/app/models/cart.rb
vi depot_g/app/controllers/line_items_controller.rb
vi depot_g/app/views/carts/show.html.erb
rails g migration combine_item_in_cart
vi depot_g/db/migrate/202008011339_combine_items_in_cart.rb
rails db:migrate
vi depot_g/db/migrate/202008011339_combine_items_in_cart.rb
rails db:migrate
rails db:rollback
cp depot_g depot_h
vi depot_h/app/controllers/carts.controller.rb
curl https://localhost:3000/carts/
vi depot_h/app/views/carts/show.html.erb
vi depot_h/app/controllers/carts_controller.rb
cp depot_h depot_i
vi depot_i/test/functional/carts_controller_test.rb


```

```
```

```
```



```
```

```
```

```
```


