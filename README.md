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


