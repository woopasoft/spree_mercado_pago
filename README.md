Spree Mercado Pago Payment Method
=================================

This project is a fork of: https://github.com/manuca/spree_mercado_pago

Installation
------------

```
gem 'spree_mercado_pago', git: "git@github.com:woopasoft/spree_mercado_pago.git"
```

inside your project run

```
bundle exec rails g spree_mercado_pago:install
```

to import assets and migrations.

Usage
-----

- Add a new payment method in the admin panel of type Spree::PaymentMethod::MercadoPago
- After adding the payment method you will be able to configure your Client ID and Client Secret (provided by Mercado Pago).

IPN
---

For IPN you need to configure the notification URL in Mercado Pago's site. The notification URL will be `http[s]://[your_domain]/mercado_pago/ipn`. Please review Mercado Pago's documentation at http://developers.mercadopago.com/ for the correct place where to configure IPN notification URLs.


Pending Work
------------

- Configurable currency

Testing
-------

- clone this repo
- execute `bundle`
- execute `rake test_app` to build a dummy app directory inside specs
- execute `bundle exec rspec spec`
