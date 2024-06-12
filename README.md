# TWIPLA (Visitor Analytics) [UNOFFICIAL]
**Custom Tag Template for server-side Google Tag Manager**

Send pageviews, ecom events and custom events to TWIPLA 

[![Template Status](https://img.shields.io/badge/Community%20Template%20Gallery%20Status-beta-orange)](https://tagmanager.google.com/gallery/#/owners/mbaersch/templates/twipla-tag-server) ![Repo Size](https://img.shields.io/github/repo-size/mbaersch/twipla-tag-server) ![License](https://img.shields.io/github/license/mbaersch/twipla-tag-server)
    
---

## Usage
Install the tag template and add a new *TWIPLA* tag. Enter your Website ID. Per default, the tag sends a page view when loaded with *1* as *Platform* marker (which is similar to regular client-side tagging) and uses the `client_id` value that comes with every GA4 formatted incoming request. 

### Advanced Settings
This section contains additional options that allows enhanced data redaction. You can optionally send an empty referrer and delete any parameters from tracked urls. 

#### Changing Page URL
If you want to collect data from several sources in different paths of the same profile, you can override the page URL with a different value. This option also can be used for further data redaction or enrichment - as well as the option to delete all parameters from the path before sending data to TWIPLA.

#### Define Client ID Source
When the regular `client_id` from incoming requests is not suitable as a TWIPLA fingerprint replacement, define any other variable to populate the *fingerprint* value for the current visitor.

### Event Data Mapping 
Define event category, label and value for all events that are not a `page_view` and trigger this tag in order to fit the TWIPLA event structure (that is similar to former Universal Analytics or current Piwik PRO events). 

NOTE: this feature is not functional yet. 

### E-Commerce Events 
When a standard GA4 ecom event triggers this tag, it will be sent as a TWIPLA ecom event and populates ecom reports there. If you prefer to just keep thise events as custom events in TWIPLA (without product information), use a transformation to change the event name for this tag. The following event names will be treated as ecom events: 

- `add_payment_info` 
- `add_shipping_info`
- `add_to_cart` 
- `add_to_wishlist` 
- `begin_checkout` 
- `generate_lead` 
- `login` 
- `purchase` 
- `refund` 
- `remove_from_cart` 
- `remove_from_wishlist` 
- `share` 
- `sign_up` 
- `view_cart` 
- `view_item` 
- `view_item_list`   
