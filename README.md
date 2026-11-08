# inField
A simple yet valuable app that catches all missed calls from clients/customers for small service businesses. Phase 1 features include missed-call text back, lead generation, categorized customer feedback summary, and after a job is completed a automated text thanks customer for business and requests a google review. 

## Mobile SaaS launch notes (iOS fastest path)

- `index.html` now includes iOS/PWA metadata, safe-area handling, manifest support, and service worker registration.
- Set your Supabase Functions base URL at runtime with either:
  - `window.__INFIELD_CONFIG__.supabaseFunctionsBaseUrl`, or
  - `<meta name="infield-supabase-functions-base-url" content="https://your-project.supabase.co/functions/v1">`
- Offline shell files are defined in `service-worker.js`.

### Quickest App Store wrapper path

1. Host this web app over HTTPS.
2. Wrap with Capacitor iOS (`npm init @capacitor/app`, `npx cap add ios`).
3. Point Capacitor webDir to this app output and sync.
4. Add production app icons/splash assets and iOS privacy strings.
5. Build/sign in Xcode and submit to App Store Connect.
