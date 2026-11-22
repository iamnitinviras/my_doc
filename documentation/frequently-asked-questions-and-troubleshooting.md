# Frequently asked questions and troubleshooting

Laravel Script sells Laravel code. This page answers common questions about buying, downloading, installing and updating scripts, and lists fixes for typical installation problems. For step-by-step setup, see \[Installing a script\] and for usage rights, see \[License and usage terms\]. Those pages are listed in the outline; check their final titles before publishing.

{% hint style="warning" %}
Needs verification: The material does not list real customer questions or known installation errors. Replace the general questions below with the ones customers actually ask, and add any confirmed error messages.
{% endhint %}

## Buying and downloading

### What do I get when I buy a script?

Each purchase includes the script's source code. Check the product page on [https://laravelscripts.net/](https://laravelscripts.net/) for the exact contents of each package.

{% hint style="warning" %}
Needs verification: Confirm what each package includes (source files, documentation, database files, sample data) and whether a purchase covers one site or several.
{% endhint %}

### How do I download my script after purchase?

{% hint style="warning" %}
Needs verification: Describe where the download link appears (order confirmation email, account page, or other), how long the link stays valid, and whether there is a download limit.
{% endhint %}

### Can I get a refund?

{% hint style="warning" %}
Needs verification: Confirm the refund policy, including the time window and conditions. Do not publish this answer until it is confirmed.
{% endhint %}

## Updates

### Are updates free?

{% hint style="warning" %}
Needs verification: Confirm whether updates to purchased scripts are free, for how long, and whether major versions cost extra.
{% endhint %}

### How are updates delivered?

{% hint style="warning" %}
Needs verification: Confirm the delivery method (email notification, account download, or other) and whether you need to re-download the full package or can apply a patch.
{% endhint %}

### Should I back up before updating?

Yes. Before you replace any files, back up your application files and your database. Keep your own changes, such as custom views or configuration values, in a separate place so you can compare them with the new version.

{% hint style="info" %}
Tip: Test updates on a local or staging copy of your site before applying them to a live site.
{% endhint %}

## Installation troubleshooting

Most installation problems with Laravel applications come from a short list of causes. Work through the checks below in order.

### Blank page or a 500 Internal Server Error

1. Turn on error display in a local environment only, then read the message in `storage/logs/laravel.log`.
2. Check that the `storage` and `bootstrap/cache` directories are writable by the web server.
3. Check that your `.env` file exists and that the application key is set.

{% hint style="warning" %}
Needs verification: Confirm the exact commands for generating the application key and clearing caches, and the PHP version the script requires.
{% endhint %}

### "No application encryption key has been specified"

The `APP_KEY` value in `.env` is empty. Generate a key and add it to the file, then reload the page. Do not share your key, because anyone with it can decrypt session data and cookies.

### Database connection refused

- Check the `DB_HOST`, `DB_DATABASE`, `DB_USERNAME` and `DB_PASSWORD` values in `.env`.
- Confirm that the database server is running and that the user has access to the database.
- Clear the configuration cache after you change `.env`.

{% hint style="warning" %}
Needs verification: Confirm the database types the script supports and any required database version.
{% endhint %}

### Missing tables or migration errors

The database has not been set up. Run the migrations included with the script, then import any seed data the package provides.

{% hint style="warning" %}
Needs verification: Confirm the migration and seeding steps and whether the package includes an SQL file as an alternative.
{% endhint %}

### Permission denied errors

Give the web server user write access to `storage` and `bootstrap/cache`. Avoid setting permissions to 777 on production servers.

### Changes to `.env` have no effect

Cached configuration may still be in use. Clear the configuration cache and reload the page.

## Getting support

{% hint style="warning" %}
Needs verification: Describe how to contact support (email, form, or other channel), what information to include in a request (purchase reference, PHP version, error log excerpt), and the response times offered. If no support is offered, say so.
{% endhint %}

When you contact support, include:

- Your purchase reference or order email
- The script name and version
- Your PHP and Laravel versions
- The exact error message and the relevant lines from `storage/logs/laravel.log`
- The steps you followed before the problem appeared

{% hint style="info" %}
Tip: Remove passwords and application keys from any log or configuration you send.
{% endhint %}

## Still stuck?

If your problem is not listed here, check the \[Installing a script\] page for the full setup steps, and review the \[License and usage terms\] page to confirm what you may do with the code.
