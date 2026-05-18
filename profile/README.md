![Logo](./art/logo.png)
# sushilk/supabase

Modern modular Supabase SDK for PHP powered by independent packages.

`sushilk/supabase` acts as the main meta-package that combines all official Supabase PHP ecosystem packages into one seamless developer experience.

---

# ✨ Features

- Modular architecture
- Fluent query builder
- Authentication & JWT
- Storage management
- Realtime subscriptions
- Edge Functions
- AI vector search
- Laravel integration
- Async support
- DTOs & typed responses
- PSR compliant
- Modern PHP 8.3+

---

# 📦 Installation

Install full ecosystem:

```bash
composer require sushilk/supabase
```

---

# 📚 Included Packages

| Package | Purpose |
|---|---|
| `sushilk/supabase-core` | Core HTTP client & configuration |
| `sushilk/supabase-auth` | Authentication |
| `sushilk/supabase-database` | PostgreSQL database APIs |
| `sushilk/supabase-storage` | Object storage |
| `sushilk/supabase-realtime` | Realtime WebSockets |
| `sushilk/supabase-functions` | Edge Functions |
| `sushilk/supabase-vector` | AI vector search |
| `sushilk/supabase-dto` | Typed DTO objects |
| `sushilk/supabase-support` | Helpers & utilities |

---

# 🏗️ Architecture

```txt
sushilk/supabase
│
├── supabase-core
├── supabase-auth
├── supabase-database
├── supabase-storage
├── supabase-realtime
├── supabase-functions
├── supabase-vector
├── supabase-dto
└── supabase-support
```

---

# ⚙️ Composer Dependencies

```json
{
  "require": {
    "php": "^8.3",
    "sushilk/supabase-core": "^1.0",
    "sushilk/supabase-auth": "^1.0",
    "sushilk/supabase-database": "^1.0",
    "sushilk/supabase-storage": "^1.0",
    "sushilk/supabase-realtime": "^1.0",
    "sushilk/supabase-functions": "^1.0",
    "sushilk/supabase-vector": "^1.0",
    "sushilk/supabase-dto": "^1.0",
    "sushilk/supabase-support": "^1.0"
  }
}
```

---

# 🚀 Quick Start

```php
<?php

require 'vendor/autoload.php';

use Sushilk\Supabase\Supabase;

$supabase = new Supabase(
    url: 'https://your-project.supabase.co',
    apiKey: 'your-anon-key'
);
```

---

# 🗄️ Database

```php
$users = $supabase
    ->database()
    ->table('users')
    ->select('*')
    ->execute();
```

Powered by:

```txt
sushilk/supabase-database
```

---

# 🔐 Authentication

```php
$supabase
    ->auth()
    ->signIn([
        'email' => 'john@example.com',
        'password' => 'secret'
    ]);
```

Powered by:

```txt
sushilk/supabase-auth
```

---

# 📦 Storage

```php
$supabase
    ->storage()
    ->bucket('avatars')
    ->upload(
        'avatar.png',
        fopen('avatar.png', 'r')
    );
```

Powered by:

```txt
sushilk/supabase-storage
```

---

# 🔄 Realtime

```php
$supabase
    ->realtime()
    ->channel('messages')
    ->subscribe();
```

Powered by:

```txt
sushilk/supabase-realtime
```

---

# 🌍 Edge Functions

```php
$supabase
    ->functions()
    ->invoke('send-email', [
        'email' => 'john@example.com'
    ]);
```

Powered by:

```txt
sushilk/supabase-functions
```

---

# 🧠 Vector Search

```php
$supabase
    ->vector()
    ->search(
        table: 'documents',
        embedding: [0.12, 0.55, 0.88]
    );
```

Powered by:

```txt
sushilk/supabase-vector
```

---

# 🧩 Laravel Integration

Install Laravel bridge separately:

```bash
composer require sushilk/supabase-laravel
```

Features:

- Service Provider
- Facades
- Config publishing
- Queue integration
- Event support

---

# ⚡ Async Support

```php
$response = $supabase
    ->database()
    ->table('users')
    ->select('*')
    ->async()
    ->execute();
```

---

# 🛡️ Error Handling

```php
try {
    $users = $supabase
        ->database()
        ->table('users')
        ->select('*')
        ->execute();

} catch (\Sushilk\Supabase\Exceptions\SupabaseException $e) {
    echo $e->getMessage();
}
```

---

# 📂 Folder Structure

```txt
src/
├── Supabase.php
├── Contracts/
├── Exceptions/
├── Facades/
├── Traits/
└── Helpers/
```

---

# 🧪 Development

Run tests:

```bash
composer test
```

Run static analysis:

```bash
composer phpstan
composer psalm
```

Run formatting:

```bash
composer pint
```

---

# 🤝 Contributing

1. Fork repository
2. Create feature branch
3. Commit changes
4. Push branch
5. Open PR to `develop`

---

# 🔒 Security

Report vulnerabilities responsibly:

```txt
security@sushilk.dev
```

---

# 📜 License

MIT License

---

# ❤️ Philosophy

Built for developers who want:

- Clean APIs
- Modern architecture
- Scalable applications
- AI-ready infrastructure
- Enterprise-grade reliability
- Exceptional PHP developer experience

---

# 🌐 Links

- GitHub: https://github.com/sushilk/supabase
- Packagist: https://packagist.org/packages/sushilk/supabase
- Supabase: https://supabase.com

---

# ⭐ Support

If this project helps you, consider giving it a GitHub star.
