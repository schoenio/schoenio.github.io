---
layout: page
title: WooCommerce Reply-to Customer
meta_title: WooCommerce Reply-to Customer WordPress Plugin
permalink: /woocommerce-reply-to-customer/
---

<div class="value-proposition">
  <div class="plugin-screenshot">
    <img src="https://d2yca1enuxtdrs.cloudfront.net/images/resize/product/1240/ce76d33aeb4bf46daf8de9c4b1bb1722.jpg" alt="Plugin screenshot">
  </div>

  <p>This WooCommerce plugin makes the new order notification email that is sent to the store owner appear to have been sent from the customer's email address. This lets the store owner simply press "reply" within their email client to contact the customer about their new order.</p>

  <p>Your purchase includes one year of support and updates, and the right to use the plugin on up to five domains.</p>

  <p><a href="https://sellfy.com/p/98Kw/" class="btn btn-primary">Buy on Sellfy</a></p>

  <div class="panel" style="max-width: 370px; margin-top: 18px;">
    <p><strong>Happiness promise:</strong> If the plugin doesn't help you, write to hi@schon.io within 30 days of purchase and we'll give you a full refund.</p>
  </div>




</div>

## Documentation

### How to install

1. Unzip the plugin files and place the plugin folder into your WordPress
plugins directory (usually /wp-content/plugins/).

2. Activate the plugin from the WordPress dashboard.

3. Go to WooCommerce Settings and click the "Email" tab. Choose the
submenu item for the email called "New Order (from customer)".

4. Check that the default options are correct and press "Save changes".

If you want to disable WooCommerce's default new order notification email (the
one which is sent from the store owner's email address), click the "New
Order" submenu item, un-check the "Enable this email notification" option
and press "Save changes". Before doing this, check the IMPORTANT NOTE section below.


### Troubleshooting

If you do not receive the new order notification emails after activating this
plugin, please try the following:

- Check that the plugin settings are correct (WooCommerce Settings Email "New Order (from Customer)").

- Check your spam folder. Emails with a spoofed "From" header are somewhat more likely to be binned by spam filters.

- Check your mail server logs. Some mail servers (such as Gmail) refuse to send emails with a spoofed "From" header. If your hosting platform doesn't give you access to your mail server logs, use Mailgun instead (free, ten minute setup via https://wordpress.org/plugins/mailgun/) and inspect the logs via their web interface.


### Important note

This plugin "spoofs" or "fakes" the sender headers to make WooCommerces' new order notification emails appear to have come directly from your customers. This "spoofing" means that emails sent by this plugin are somewhat more likely to be binned by spam filters. Most users do not have problems on this score, but if the reliable receipt of these notification emails is crucial to your business operations, you should leave WooCommerce's default new order notification enabled.


### Support

For support, write to [hi@schon.io](mailto:hi@schon.io). To help us assist you, please include the WooCommerce System Report in your email. To get this, login to WordPress WooCommerce System Status and then press the "Get System Report" button on that page.
