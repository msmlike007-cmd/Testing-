# খামার ম্যানেজিং (Khamar Managing)

Mobile-first farm management PWA starter source.

## Run locally
Because service workers require localhost or HTTPS, run a local static server from this folder:
- Python: `python -m http.server 8000`
- Open `http://localhost:8000`

You can also deploy the folder to Netlify, Cloudflare Pages, GitHub Pages, or another static HTTPS host.

## Included
- Bengali / English interface toggle
- Dashboard and animal records
- Feed inventory and low-stock warnings
- Milk logs and production totals
- Breeding date elapsed-day calculation
- Vaccination records and upcoming dates
- Daily tasks and completion toggles
- Income / expense entries and automatic net profit/loss
- Six-month income/expense chart
- Symptom matching information (educational only)
- Calendar, notes, JSON backup and restore
- Local browser storage and PWA offline cache

## Important production setup
This source stores data in the current browser/device using localStorage. It does **not** yet include real Google authentication, multi-device cloud sync, push notifications, or secure cloud file storage. To enable those, create a Firebase project and configure Firebase Authentication (Google provider), Firestore, and Storage; then add security rules that isolate each user's records by authenticated UID. Do not publish secret service credentials in client code.

For reliable production use, migrate localStorage to IndexedDB (for larger images/offline queues) and implement conflict-safe cloud synchronization. Test restore and backup before entering valuable farm records.

Animal symptom matching is informational and is not a veterinary diagnosis. Vaccination schedules must be confirmed by a local veterinarian.
