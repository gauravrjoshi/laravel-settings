# Laravel Settings Manager

A minimal and reusable Laravel package to store key-value settings in your database.

---

## 📦 Installation

Require the package via Composer:

```bash
composer require statelyworld/laravel-settings:dev-main
```

If you encounter the error:
> Could not find a version of package statelyworld/laravel-settings matching your minimum-stability (stable)...

Add the following to your **root project's `composer.json`** before requiring again:

```json
"minimum-stability": "dev",
"prefer-stable": true
```

---

## ✅ What to Do After Installation?

### 1. **Run Migrations**

#### Option 1: Auto-Load Migrations (Recommended)

Run the following to create the `settings` table:

```bash
php artisan migrate
```

#### Option 2: Publish Migration (Optional)

If you prefer to manage the migration file in your own project:

```bash
php artisan vendor:publish --tag=laravel-settings-migrations
php artisan migrate
```

---

## 🚀 Usage Example

### Set a Value

```php
use StatelyWorld\LaravelSettings\Models\Setting;

// Store a setting
Setting::set('site_name', 'My Awesome Website');
```

### Get a Value

```php
use StatelyWorld\LaravelSettings\Models\Setting;

// Retrieve the setting or use a default if not found
$siteName = Setting::get('site_name', 'Default Site Name');
```

---

## 🧑‍💻 Example Use Cases

- Store API keys or tokens
- Enable/disable site features (maintenance mode, promotions)
- Site-wide text configurations (site name, footer text)
- Track process IDs or timestamps
- Store any small settings without adding extra config files

---

## 📂 Package Structure

```
src/
└── Models/
    └── Setting.php
└── SettingServiceProvider.php
database/
└── migrations/
    └── create_settings_table.php
composer.json
README.md
```

---

## ✅ Laravel Version Compatibility

| Laravel Version | Supported |
|-----------------|-----------|
| 9.x             | ✅        |
| 10.x            | ✅        |
| 11.x            | ✅        |

---

## 📝 License

This package is open-sourced software licensed under the [MIT license](LICENSE).

---

## 🙏 Contributing

We welcome contributions. Please fork the repository, make changes, and submit a pull request.

---

## 👨‍💻 Maintainer

- [Gaurav Joshi](https://github.com/gauravrjoshi)
