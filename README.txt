STITCH LEDGER PWA OWNER PACKAGE

FILES
- index.html: simple mobile-friendly launcher for the existing private tracker.
- manifest.webmanifest and sw.js: PWA shell metadata and offline caching for this launcher only.

DATA AND ACCESS
The tracker URL is the existing private Apps Script deployment. Records live in the existing Google Sheet, not in this package. The user must sign into the Google account that owns/has access to the deployment. Sharing the APK does not grant a different account access. If the owner authorizes another Google account in Apps Script, that account can then access the same Sheet through the app.

AI
Ollama is local to the device where it runs. localhost on a phone means the phone itself, not the laptop. The currently deployed tracker has no AI screen. A local AI draft exists in the project backend source, but it is not deployed; it sends only aggregate figures to Ollama on the laptop. This package does not claim to connect AI to the Sheet or to provide phone AI.

PACKAGING
A PWA needs to be served over HTTPS (or localhost) for install/service-worker support. Do not open index.html as a file and expect PWA installation. A PWA-to-APK converter can instead be pointed directly at the existing HTTPS Apps Script tracker URL if it supports the Google sign-in flow. That is the simplest path to the actual tracker. This folder is a shell/source package; it is not an APK and does not alter the live deployment.
