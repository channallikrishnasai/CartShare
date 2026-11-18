# CartShare

**Good things, shared.** CartShare is a responsive, room-based group-shopping prototype for roommates, work teams, and travel groups. It combines a 250-product quick-shop catalog, a shared cart, room activity, delivery progress, and a print-ready group receipt.

## Start the app

CartShare uses plain HTML, CSS, and JavaScript. There is no build step or package install.

1. Open `index.html` in a current browser.
2. Enter a name and create a room, or join using an invite code.
3. Search or browse the shop below the cart and add products with one tap.

For the most consistent browser-storage behavior, serve the folder locally:

```bash
python -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000).

## Shop and cart features

- **250 catalog items** arranged into ten aisles, with 25 products per aisle: Fresh fruit, Vegetables, Dairy & eggs, Bakery, Snacks & sweets, Drinks, Pantry staples, Personal care, Home essentials, and Meat & seafood.
- Search by product name or aisle; browse aisle filters; sort by popularity, name, or price.
- Save and remove products from the persistent **Saved** aisle.
- Load catalog picks in manageable batches and add any product in one tap.
- Enter custom items and prices; use quick-add buttons for common essentials.
- See a running cart total and progress toward the sample $75 free-delivery threshold.
- Review who added each cart item, remove items, or clear the cart.
- See recent room activity and print a clean, itemized group receipt.
- Copy the room invite code and open the room dialog to create or join a room.

## 15-second teaser and website walkthrough

Open [cartshare-teaser-15s.html](assets/video/cartshare-teaser-15s.html) and press **Export 15 sec video** to record the fast-cut 1280×720 animated teaser with its voiceover as a WebM file. Use **Preview** to play it first. The included Zira narration is [cartshare-teaser-15s.wav](assets/video/cartshare-teaser-15s.wav), with its transcript in [teaser-15s-voiceover.txt](assets/video/teaser-15s-voiceover.txt).

For a live site demo, follow the [two-minute website walkthrough script](assets/video/website-walkthrough-script-2min.txt). It includes timed cues for showing the room, 250-item catalog, search and favorites, shared cart, receipt, and implementation.

## 40-second animated explainer

Open [cartshare-explainer.html](assets/video/cartshare-explainer.html), press **Export 40 second video**, and let the animation finish. The page records its animated canvas and the included narration together as a WebM video. If a local save endpoint is unavailable, the browser downloads `CartShare-Animated-Explainer.webm` when export finishes. Use **Play with voiceover** to preview it first.

The narration is also available separately as [cartshare-voiceover.wav](assets/video/cartshare-voiceover.wav), with its text in [voiceover-script.txt](assets/video/voiceover-script.txt). It uses the locally installed Microsoft Zira voice and is about 41 seconds long.

## File layout

```text
CartShare/
├── index.html                       # Shopping room and catalog markup
├── css/
│   └── styles.css                   # Responsive, depth-rich UI and print styling
├── js/
│   └── app.js                       # Catalog, room, cart, search, and saved products
├── assets/
│   └── video/
│       ├── cartshare-explainer.html # Animated video player and WebM exporter
│       ├── cartshare-voiceover.wav  # Narration track
│       └── voiceover-script.txt     # Narration transcript
└── README.md
```

## Product photos

Every catalog card uses a real product-category photograph from Pexels, loaded at a smaller web size from its image CDN. Each aisle rotates across a small set of representative photos, so cards show real aisle imagery rather than an exact manufacturer package for every individual product. An emoji remains available if an image fails to load. An internet connection is needed to display the photos.

Credits are included even though Pexels does not require them. Photos are used under the [Pexels License](https://www.pexels.com/license/); do not present the photographers or any depicted brand as endorsing CartShare.

- **Fruit:** [Olena Bohovyk](https://www.pexels.com/photo/bowl-of-fruits-on-white-surface-7004906/), [alleksana](https://www.pexels.com/photo/bananas-on-white-background-4114143/), [Bora C](https://www.pexels.com/photo/assorted-fresh-fruit-in-containers-on-white-background-35439977/), [Paolo Bici](https://www.pexels.com/photo/fresh-fruit-bowl-with-kiwi-orange-and-apple-36659537/)
- **Vegetables:** [Polina Tankilevitch](https://www.pexels.com/photo/close-up-shot-of-fresh-vegetables-on-a-white-surface-5719953/), [cottonbro studio](https://www.pexels.com/photo/top-view-of-fresh-vegetables-on-white-surface-6823594/), [Tima Miroshnichenko](https://www.pexels.com/photo/fresh-fruits-and-vegetables-on-white-surface-7879834/)
- **Dairy & eggs:** [RDNE Stock project](https://www.pexels.com/photo/dairy-products-on-white-surface-8964258/), [Towfiqu barbhuiya](https://www.pexels.com/photo/ingredients-preparing-on-table-11363573/)
- **Bakery:** [Mariana Kurnyk](https://www.pexels.com/photo/flatlay-photography-of-variety-of-breads-1775053/), [Hanna Pad](https://www.pexels.com/photo/bread-on-white-ceramic-plate-7214788/), [Kerim Eveyik](https://www.pexels.com/photo/artisanal-sourdough-bread-held-by-baker-36930940/)
- **Snacks & sweets:** [Pavel Danilyuk](https://www.pexels.com/photo/delicious-chips-and-cookies-on-wooden-surface-8111369/), [Nothing Ahead](https://www.pexels.com/photo/area-with-corn-snacks-and-potato-chips-in-supermarket-7451961/)
- **Drinks:** [Berna](https://www.pexels.com/photo/bottles-of-water-and-orange-juice-lying-on-a-white-sheet-26791666/), [Polina Tankilevitch](https://www.pexels.com/photo/lemon-juice-in-clear-plastic-bottle-4443460/), [Khadijah Karaca](https://www.pexels.com/photo/close-up-shot-of-milk-being-poured-into-a-glass-with-coffee-17497894/)
- **Pantry:** [MART PRODUCTION](https://www.pexels.com/photo/ingredients-ready-to-use-8108163/), [Antonius Ferret](https://www.pexels.com/photo/meal-ingredients-on-table-6223120/)
- **Personal care:** [Tara Winstead](https://www.pexels.com/photo/soap-and-skincare-products-on-a-white-surface-6690916/), [ROMAN ODINTSOV](https://www.pexels.com/photo/close-up-shot-of-skincare-products-7691164/), [Tara Winstead](https://www.pexels.com/photo/cosmetic-products-on-a-white-background-6682969/)
- **Home essentials:** [Anna Shvets](https://www.pexels.com/photo/cleaning-products-on-white-background-5217896/), [Polina Tankilevitch](https://www.pexels.com/photo/cleaning-materials-on-white-surface-4440525/)
- **Meat & seafood:** [Julia Filirovska](https://www.pexels.com/photo/raw-meat-on-display-in-supermarket-8251004/), [Los Muertos Crew](https://www.pexels.com/photo/raw-meat-on-a-tray-8477074/), [Geraud Pfeiffer](https://www.pexels.com/photo/plates-with-various-raw-meat-with-spices-on-table-6607314/)

## How the prototype works

- Cart and room data are saved in browser `localStorage` under `cartshare-v1`.
- Favorite products use `cartshare-favorites`.
- The browser `storage` event refreshes other tabs that share the same local origin and browser profile.
- The cart and item list print using the stylesheet’s print rules.
- The live-looking room members are demo profiles; the app does not authenticate real members.

## Known limits

This is a front-end prototype rather than a production multi-user service. Room codes do not create server-side rooms, and different devices or browser profiles cannot see each other’s changes. Real cross-device collaboration needs authentication and a shared real-time backend such as Firebase or Supabase. Product prices and the $75 delivery threshold are sample data defined in `js/app.js`; there is no retailer inventory or delivery integration.

## Publish as a static site

The project can be hosted from its root on GitHub Pages, Netlify, or Vercel. No build command is needed. Keep the relative `css/styles.css` and `js/app.js` paths if deploying to a project subpath.


