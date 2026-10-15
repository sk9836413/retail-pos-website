---
title: Web stores and Swiggy / Zomato
permalink: /help/ecommerce
---

# Web stores and Swiggy / Zomato

Requires the **Retail POS Pro - E-Commerce** app.

## Web stores (Shopify, WooCommerce, Magento 2, BigCommerce)

1. **Web Stores** → new: platform, shop URL, the store that collects or fulfils the orders, and the paid-online clearing account.
2. **Set API Credentials**: Shopify / Magento / BigCommerce access token, or WooCommerce consumer key and secret.
3. Tick *Sell Online* on the items to publish.
4. Switch on **Sync Items & Prices**, **Sync Inventory** and **Import Paid Orders**, and run **Sync Now** (the job queue repeats it).

Items are linked to web products (**Web Item Links**). Paid web orders become **customer orders** for click & collect or delivery;
the online payment is booked as a deposit. When the order is collected or delivered, the fulfilment goes back to the web store.
**Web Sync Log** shows every sync with errors per item.

## Swiggy / Zomato through UrbanPiper

1. Get an UrbanPiper account linked to your Swiggy and Zomato outlets.
2. Deploy the connector (*AzureConnector* in the download package) to your Azure subscription and set the UrbanPiper webhook to its
   `api/urbanpiper/<web store code>` address with the secret key.
3. **Web Stores** → new store with platform **UrbanPiper**, API credentials, and **Publish Aggregator Web Service**.
4. Optional: *Accept Aggregator Orders Automatically*; and, with the Hospitality app, send online orders straight to the kitchen.

Orders arrive as customer orders. On the customer order card: **Accept (Swiggy / Zomato)**, **Food Ready** and **Handed to Rider** update
the status on the aggregator. Items marked *Sell Online*, their prices and stock are pushed to UrbanPiper.
