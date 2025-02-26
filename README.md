# How to use it?

note that to see the translation run in the *plugin popup*, its input must be empty!
go to the plugin settings page, clear the inputs for the names and text and hit save.
this will still show the english test like nothing happened, but the translation will be triggered.

## wpml
if you already have wmpl installed on your site simply go to *string translation* section of the plugin there you will find import/export section. Simply selecte the po file upload it WITH the translations and thats it!

## manual
if your site is already using hebrew an no other languages, there is litle need in wpml. hence you will need to load the translation yourself.
try putting the mo file (the complied version of the po) into the languages folder that is in the gdpr-cookei-compliance plugin

and adding this to `functions.php`

```php
function manual_load_hebrew_translation() {
    load_textdomain(
        'gdpr-cookie-compliance', 
        WP_PLUGIN_DIR . '/gdpr-cookie-compliance/languages/plugin-name-he_IL.mo'
    );
}
add_action('init', 'manual_load_hebrew_translation', 5);
```

