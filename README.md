# book-catalog
My cataloging app for library
V2- includes lookup of English name first.  INcludes owner field


Book Catalog PWA — Setup Guide
What you have
Four files that make up your Book Catalog app:
File	Purpose
index.html	The entire app (UI + logic)
manifest.json	Tells iOS it’s an installable app
sw.js	Service worker — enables offline use
icon.svg	Home screen icon
 
Step 1 — Get a free GitHub account
Go to github.com and sign up for a free account if you don’t have one. Your username will become part of the app URL.
 
Step 2 — Create a new repository
1.	Click the + in the top-right corner → New repository
2.	Name it: book-catalog (or anything you like)
3.	Set it to Public (required for free GitHub Pages hosting)
4.	Check “Add a README file”
5.	Click Create repository
 
Step 3 — Upload the four files
1.	In your new repository, click Add file → Upload files
2.	Drag all four files into the upload area:
–	index.html
–	manifest.json
–	sw.js
–	icon.svg
3.	Click Commit changes
 
Step 4 — Enable GitHub Pages
1.	In your repository, click Settings (top tab)
2.	Scroll down to Pages in the left sidebar
3.	Under Source, choose Deploy from a branch
4.	Set Branch to main, folder to / (root)
5.	Click Save
6.	Wait 1–2 minutes, then refresh — you’ll see a green banner with your URL
Your app URL will be:
https://YOUR-USERNAME.github.io/book-catalog/
 
Step 5 — Install on your iPhone
1.	Open Safari on your iPhone (must be Safari — not Chrome or Firefox)
2.	Navigate to your app URL
3.	Tap the Share button (the box with an arrow at the bottom of Safari)
4.	Scroll down and tap “Add to Home Screen”
5.	Name it “Book Catalog” (or whatever you like) and tap Add
The app icon will appear on your home screen and open like a native app, with no browser bar — full screen, offline-capable.
 
Using the app
Scanning a book
1.	Tap the Scan tab
2.	Tap ▶ Camera — allow camera access when iOS asks
3.	Aim your iPhone at the barcode on the back of the book
4.	The book details will appear automatically
5.	Fill in Location, Subject, Notes as desired
6.	Tap Save Book
Manual ISBN entry
•	Type or paste an ISBN into the text box and tap Go
•	Works for both ISBN-10 and ISBN-13
Browsing and editing
•	Tap the Books tab to see your catalog
•	Use the search bar or filter dropdowns (Location / Subject)
•	Tap any book to view or edit it
Exporting your catalog
1.	Tap the Export tab
2.	Export Full Catalog → saves a CSV with all fields
3.	The CSV goes to your iOS Files app (Downloads folder)
4.	You can then AirDrop it to your Mac, email it, or open in Numbers
Getting book prices (bulk method)
1.	Tap Export ISBNs Only — this creates a small CSV of just ISBNs
2.	Go to bookscouter.com or booktrapper.com
3.	Use their bulk upload tool to get pricing
4.	Download their result CSV
5.	Come back to the Export tab → Import Pricing Data
6.	Choose the downloaded CSV — pricing will be matched by ISBN and saved
 
Keeping your data safe
Your book data lives in your iPhone’s browser storage (IndexedDB). It persists indefinitely but is tied to Safari on that device.
Back up regularly: - Use Export Full Catalog to save a CSV to your Files app - Periodically AirDrop or copy that CSV to your computer - If you ever need to restore, the CSV is your archive (re-import not yet automatic, but all your data is human-readable in the CSV)
 
Updating the app
If you want to make changes or get an updated version: 1. Replace the files on GitHub (upload and commit again) 2. On your iPhone, open the app, then close it fully and reopen 3. The service worker will pick up the changes within a session or two
 
Troubleshooting
Camera won’t start: Make sure you opened the app in Safari (not Chrome). iOS only grants camera access to Safari PWAs.
Book not found: Try entering the ISBN manually. Very old or obscure books may not be in Google Books or Open Library. You can still save the book with manual title/author entry (the title field is editable in the modal).
Data seems missing after iOS update: iOS occasionally clears PWA storage for apps that haven’t been used in a while. Export your CSV regularly as insurance.
