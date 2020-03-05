# Resume

**First Name:** Gleb

**Last Name:** Gundilovich

**Sex:** Male

**Age:** 20

## Contact Info

**Telegram:** @gleboha

**VK:** https://vk.com/id255341470

## Skills

* Basic JavaScript
* Knockout JS
* HTML
* CSS
* Java
* PHP
* Magento 2
* Python
* MySQL

## Code Examples

```javascript
define([
    'uiComponent',
    'ko',
    'jquery',
    'Magento_Checkout/js/model/quote',

], function (Component, ko, $, quote) {
    'use strict';
    return Component.extend({
        
        initialize: function () {
            this.additionalField = ko.observable();
            this._super();
            return this;
        },

        onSubmit: function() {
            quote.shippingAddress().extensionAttributes = {};
            quote.shippingAddress().extensionAttributes.additionalField = this.additionalField;

            $.ajax({
                url: '/magento2/rest/V1/test-checkout/post',
                type: "POST",
                data: ko.toJSON({param: quote.shippingAddress()}),
                contentType: "application/json"
            });

            return true;
        }
    });
});
```
## Experience

I have a little experience in developing modules for Magento 2.2.4.
Also I was developing a small online store, it was a project for the university (Backend - PHP, Frontend - HTML, CSS).

## Education

Main:
* Belarusian National Technical University

Online:
* Learn JavaScript
* HTMLAcademy
* JavaRush

## English

I practice my English by reading technical literature and communicating in English with my friends.