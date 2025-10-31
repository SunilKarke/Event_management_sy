# Event_M — Minimal PHP Event Management

This is a small, minimal event management demo built for XAMPP (Windows). It provides:

- Signup / Login (PHP sessions, bcrypt-hashed passwords)
- Add Event (title, description, datetime)
- List Events on the homepage with server time
- Admin page that shows database contents

Requirements
- XAMPP (Apache + MySQL/MariaDB)
- PHP 7.4+ (common with XAMPP bundles)

Setup
1. Place this `Event_M` folder inside your XAMPP `htdocs` (e.g. `C:\xampp\htdocs\Event_M`).
2. Create a database in MySQL (phpMyAdmin or CLI). For example create a database named `event_m`.
3. Import `init.sql` into the database (phpMyAdmin > Import, or using mysql CLI).
4. Edit `db.php` and set the correct DB credentials (host, user, pass, dbname).
5. Open http://localhost/Event_M/ in your browser.

Notes
- Default DB settings in `db.php` assume `root` with no password and database `event_m`. Update as needed.
- This is a demo; do not use as-is in production without hardening (CSRF tokens, stronger session config, input validation, escaping output where necessary, role management).

Files
- `db.php` — database connection helper
- `init.sql` — SQL to create `users` and `events` tables
- `index.php` — homepage, lists events and shows server time
- `signup.php`, `process_signup.php` — registration
- `login.php`, `process_login.php` — authentication
- `add_event.php`, `process_add_event.php` — add events (requires login)
- `admin.php` — shows raw database tables (requires login)
- `css/style.css` — basic styling
- `header.php`, `footer.php` — included on pages

If you want, I can also wire this to use SQLite instead of MySQL, or add edit/delete for events, or add role-based admin access.
#
