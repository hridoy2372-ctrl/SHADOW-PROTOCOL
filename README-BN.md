# SHADOW PROTOCOL — Cyber Mission

ফ্রি, static, installable PWA cyber-puzzle game. আলাদা framework, server, database বা API লাগে না।

## ফাইল
- `index.html` — সম্পূর্ণ game UI, story, puzzles, Easy/Hardcore logic.
- `manifest.webmanifest` — app name/icon/install metadata.
- `sw.js` — app shell cache/offline support.
- `icons/` — app icons.

## GitHub Pages-এ ফ্রি প্রকাশ
1. GitHub-এ sign in করে `shadow-protocol` নামে **Public** repository তৈরি করো।
2. এই ZIP-এর ভেতরের সব ফাইল ও `icons` ফোল্ডার আপলোড করো; `index.html` অবশ্যই repository root-এ থাকবে।
3. Repository → **Settings → Pages**-এ যাও।
4. **Deploy from a branch** বেছে নাও; branch `main`, folder `/(root)` নির্বাচন করে Save করো।
5. GitHub যে `https://USERNAME.github.io/REPOSITORY/` লিংক প্রকাশ করবে, সেটি খোলো। publish হতে কয়েক মিনিট লাগতে পারে।
6. URL-এ গেমটি একবার চালিয়ে নাও। তারপর Android Chrome-এর `⋮` menu থেকে **Install app** অথবা **Add to Home screen** নির্বাচন করো।
7. একবার সাইট খুলে cache তৈরি হলে service worker-এর জন্য গেমটি অফলাইনে চলার কথা। আপডেটের পর নতুন version লোড করতে internet-এ একবার খুলে নাও।

## ফোনে ব্যবহার
- Local `.html` ফাইল সরাসরি খুললে browser security কারণে install/offline feature সক্রিয় নাও হতে পারে। PWA features পেতে HTTPS URL দিয়ে খোলো।
- PWA ইনস্টল হওয়া মানে এটি Play Store-এর APK নয়; এটি browser-ভিত্তিক installable app।

## InfinityFree
এই version-এ PHP/database প্রয়োজন নেই, তাই GitHub Pages সহজ পছন্দ। ভবিষ্যতে PHP backend দরকার হলে InfinityFree বিবেচনা করা যায়। সেখানে আপলোড করলে সব ফাইল site root/public web folder-এ রাখতে হবে এবং HTTPS enable হওয়ার পর app installability যাচাই করতে হবে।

## গেমের ফিচার
- 8 story missions, Easy + Hardcore modes
- Hardcore 120-second timer, 3 lives, penalties
- XP / level / progress tracking, hints, mission unlocks
- Local browser save (per-device; no cloud account)
- Sound toggle, mobile/desktop responsive layout
- Manifest + service worker for install/offline experience

## সীমাবদ্ধতা
Progress এই browser/device-এর local storage-এ থাকে; আলাদা device-এ sync হয় না। No multiplayer, server leaderboard, Play Store APK, external ads, trackers, or paid APIs.
