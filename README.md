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
vi depot_i/app/controllers/line_items_controller.rb
vi depot_i/app/views/carts/show.html.erb
vi depot_i/app/models/line_item.rb
vi depot_i/app/models/cart.rb
vi depot_i/app/assets/stylesheets/carts.css.scss
vi depot_i/app/views/carts/show.html.erb
cp depot_i depot_j
vi depot_j/app/views/carts/show.html.erb
vi depot_j/app/views/line_items/_line_item.html.erb
vi depot_j/app/views/carts/_cart.html.erb
cp depot_j depot_k
vi depot_k/app/app/viewws/carts/show.html.erb
vi depot_k/app/views/layouts/application.html.erb
vi depot_k/app/controllers/store_controller.rb
vi depot_k/app/assets/stylesheets/carts.css.scss
vi depot_k/app/assets/stylesheets/layout.css.scss
vi depot_k/app/controllers/line_items_controller.rb
cp depot_k depot_l
vi depot_l/app/views/store/index.html.erb
vi depot_l/app/controllers/line_items_controller.rb
vi depot_l/app/views/line_items/create.js.erb
cp depot_l depot_m
vi depot_m/app/assets/javascripts/application.js
vi depot_m/app/controllers/line_items_controller.rb
vi depot_m/app/views/line_items/line_item.html.erb
vi depot_m/app/views/line_items/create.js.erb

vi depot_m/app/assets/javascripts/application.js
vi depot_m/app/controllers/line_items_controller.rb
vi depot_m/app/views/line_items/_line_item.html.erb

vi depot_m/app/views/line_items/create.js.erb
cp depot_m depot_n
vi depot_n/app/views/line_items/create.js.erb
ls -p app
ls -p app/helpers
vi depot_n/app/views/layouts/application.html.erb
vi depot_n/app/helpers/application_helper.rb
vi depot_n/app/controllers/carts_controller.rb
vi depot_n/app/views/store/index.html.erb
vi depot_n/app/assets/javascripts/store.js.coffee
rake test
cp depot_n depot_o
vi depot_o/app/views/layouts/application.html.erb
vi depot_o/test/functional/line_items_controllers_test.rb
vi depot_o/test/functional/line_items_controller_test.rb
vi depot_o/test/functional/store_controller_test.rb

rails g scaffold order name:string address:test email:string apy_type:string
rails db:migrate
vi depot_o/app/views/carts/_cart.html.erb
vi depot_o/app/controllers/orders_controller.rb
vi depot_o/test/functional/orders_controller_test.rb
vi depot_o/app/views/orders/new.html.erb
vi depot_o/app/views/orders/_form.html.erb
vi depot_o/app/models/order.rb
vi depot_o/app/assets/stylesheets/layout.css.scss
vi depot_o/app/models/order.rb
vi depot_o/test/fixtures/orders.yml
vi depot_o/test/fixtures/line_items.yml
vi depot_o/app/models/line_item.rb
vi depot_o/app/models/order.rb
vi depot_o/app/controllers/orders_controller.rb
cp depot_o depot_p
vi depot_p/app/models/orders.rb
vi depot_p/test/functional/orders_controller_test.rb
vi sqlite3 -line db/development.sqlite3
vi select * from orders;
vi select * from line_items;
vi depot_p/app/views/line_items/create.js.erb
vi depot_p/app/controllers/products_controller.rb
vi depot_p/app/views/products/who_bought.atom.builder
vi depot_p/app/models/product.rb
vi depot_p/config/routes.rb
curl --silent http://localhost:3000/products/3/who_bought.atom
cp depot_p depot_q
vi Gemfile
bundle install
vi depot_q/script/load_orders.rb
rails runner script/load_orders.rb
vi depot_q/app/controllers/orders_controller.rb
vi depot_q/app/views/orders/index.html.erb

rails g mailer OrderNotifier received shipped
vi depot_q/app/mailers/order_notifier.rb
vi depot_q/app/views/order_notifier/received.text.erb
vi depot_q/app/views/line_items/_line_item.text.erb
cp depot_q depot_r
vi depot_r/app/mailers/order_notifier.rb
vi depot_r/app/controllers/orders_controller.rb
vi depot_r/app/mailers/order_notifier.rb
vi depot_r/app/views/order_notifier/shipped.html.erb
vi depot_r/app/views/line_items/_line_item.html.erb
vi depot_r/test/functional/order_notifier_test.rb

rails g integration_test user_stories
vi depot_r/test/integration/user_stories_test.rb
vi depot_r/test/integration/user_stories_test.rb
vi depot_r/test/integration/user_stories_test.rb
vi depot_r/test/integraion/user_stories_test.rb
vi depot_r/testintegration/user_stories_test.rb
vi depot_r/test/integraion/user_stories_test.rb
vi depot_r/test/integration/user_stories_test.rb
vi depot_r/test/integration/user_stories_test.rb
rails g scaffold User name:string password_digest:string
rails db:migrate
vi depot_r/app/models/user.rb
vi depot_r/app/controllers/users_controller.rb
vi depot_r/app/controllers/users_controller.rb
vi depot_r/app/controllers/users_controller.rb
vi depot_r/app/views/users/index.html.erb
vi depot_r/app/views/users/_form.html.erb
sqlite3 -line db/development.sqlite3 "select * from users"
vi depot_r/test/functional/users_controller_test.rb
rails g controller Sessions new create destroy
rails g controller Admin index
vi depot_r/app/controllers/sessions_controller.rb
vi depot_r/app/views/sessions/new.html.erb
vi depot_r/app/controllers/sessions_controller.rb
vi depot_r/app/controllers/admin_controller.rb
vi depot_r/config/routes.rb
vi depot_r/test/functional/sessions_controller_test.rb
vi depot_r/test/fixtures/users.yml
vi depot_r/app/controllers/application_controller.rb
vi depot_r/app/controllers/store_controller.rb
vi depot_r/app/controllers/session_controller.rb
vi depot_r/app/controllers/carts_controller.rb
vi depot_r/app/controllers/line_items_controller.rb
vi depot_r/app/controllers/orders_controller.rb
cp depot_r depot_s
vi depot_s/test/test_helper.rb
vi depot_r/app/views/layouts/application.html.erb
rails c
User.create{name: 'tky', password: 'secret', passord_confirmation: 'secret'}
User.count
vi depot_s/app/models/user.rb
vi depot_s/app/controllers/users_controller.rb

vi depot_s/config/initializers/i18n.rb
vi depot_s/config/routes.rb
vi depot_s/app/controllers/application_controller.rb
vi depot_s/app/views/layouts/application.html.erb
vi depot_s/config/locales/en.yml
vi depot_s/config/locales/es.yml
vi depot_s/app/views/store/index.html.erb
vi depot_s/config/locales/en.yml
vi depot_s/config/locales/es.yml
vi depot_s/app/views/carts/_carts.html.erb
vi depot_s/config/locales/en.yml
vi depot_s/config/locales/es.yml
vi depot_s/config/locales/en.yml
vi depot_s/config/locales/es.yml
vi depot_s/app/views/orders/new.html.erb
vi depot_s/app/views/orders/_form.html.erb
vi depot_s/config/locales/en.yml
vi depot_s/config/locales/es.yml
vi depot_s/config/locales/es.yml
cp depot_s depot_t
vi depot_t/app/views/orders/_form.html.erb
vi depot_t/config/locales/es.yml
vi depot_t/app/controllers/orders_controller.rb
vi depot_t/config/locales/en.yml
vi depot_t/config/locales/es.yml
vi depot_t/app/views/alyoutsapplication.html.erb
vi depot_t/app/controllers/store_controller.rb
vi depot_t/app/assets/stylesheets/layout.css.scss
```

```sh
gem install passenger
passenger-install-apache2-module

apachectl -V | grep HTTPD_ROOT
apachectl -V | grep SERVER_CONFIG_FILE
sudo apachectl restart
touch tmp/restart.txt

vi depot_t/Gemfile

mysql -u root
CREATE DATABASE depot production;
GRANT ALL PRIVILLEGES ON depot_production.* \
TO 'tky'@'localhost' IDENTIFIED BY 'password';

rails db:setup RAILS_ENV="production"
mysql depot_production
create table dummy(i int);
drop table dummy;

mkdir -p ~/git/depot.git
cd ~/git/depot.git
git --bare init
test -e ~/.ssh/id_dsa.pub || ssh-keygen -t dsa
cat ~/.ssh/d_dsa.pub >> ~/.ssh/authorized_keys2

vi depot_t/Gemfile

cd apptky
git init
git add .
git commit -m "1st"

bundle pack
git add Gemfile.lock vendor/cache
git commit -m "bundle gems"

git remote add origin ssh://tky@host/~/git/depot.git
git push origin master

capify .

vi depot_t/Capfile
vi depot_t/config/deploy.rb

cap deploy:setup
cap deploy:check
cap deploy:migrations

git add .
git commit -m "ad cap files"
gi tpush -u origin master
cap deploy
cap deploy:rollback

vagrant ssh
cd/home/rubys/work/depot/
tail -f log/production.log
cd /home/rubys/work/depot/
rails console production
p = Product.find_by_title("Pragmatic Version Control")
p.price = 32.95
p.save

vi config/environments/production.rb


```

```
```



```
```

```
```

```
```


