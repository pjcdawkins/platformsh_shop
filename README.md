# platformsh_shop
Unofficial / experimental / unstable

Sell Platform.sh subscriptions from a Platform.sh Drupal site.

## Installing/using

1. Build the site from the make files.
2. Set up settings.local.php:
   * Set `$conf['platformsh_api_token']` to your API token.
   * Add database credentials.
3. Install the site with the platformsh_shop profile:
  ```
  drush site-install --sites-subdir=default platformsh_shop
  ```
4. Go to the "Platform.sh Subcription" product display node and add it to your cart, and go through the checkout process.
5. To process the synchronization queue, run:
  ```
  drush advancedqueue --all
  ```
