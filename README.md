# Docker

Make sure you have docker installed.

# Run the app

1. `sail -up -d` - bring the docker environment up.
2. `sail composer install` - install PHP packages.
3. `sail npm install` - install npm packages.
4. `sail npm build` - build the frontend

Visit `localhost` on your computer to interact with your app

# Add your URL

Update line `#15` of `app/Http/Controllers/ConnectionController.php` with the URL of your device i.e. change it
from `"devices.zayndev.org"` to your CloudFlare Tunnel url, or any other endpoint that the Blind is
located at:

```$response = Http::withBody($_command)->post("devices.zayndev.org");```
