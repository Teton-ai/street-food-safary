# Street Food Safari – Mobile Engineer Challenge

Welcome to **Street Food Safari** 🥡🌮🍜

Imagine you’re traveling through vibrant cities around the world, searching for the best street food vendors hidden in corners and alleys. From steaming bowls of ramen in Tokyo to crispy lángos in Budapest, your mission is to build an app that helps hungry travelers discover and explore these vendors.

This challenge is your chance to show how you think about architecture, polish, performance, and user experience when building a real-world mobile app.

## Repository Structure

This repo contains two parts:

- **`/api`**
  A simple Express server that provides street food vendor data, menus, and some fun endpoints. You’ll run this locally to power your app.

- **`/app`**
  This is where your Expo React Native mobile app will live. Create it from scratch inside this folder. The app should run on both iOS and Android.

## Your Task

Build a mobile app using **Expo** (managed) that consumes the Street Food Safari API and provides a smooth, polished experience.

**Requirements:**

- **Navigation**
  - Tabs: `Vendors`, `Favorites`, `About`
  - Vendors → Vendor Details flow

- **Vendor List**
  - Fetch from `/vendors?page=1&limit=20`
  - Infinite scroll + pull-to-refresh
  - Show image, name, cuisine, rating, city, price level
  - Tapping an item → details

- **Vendor Details**
  - Fetch from `/vendors/:id`
  - Show description + menu items
  - Menu items should show small badges (e.g. spicy/vegan)
  - Toggle favorite via `POST /vendors/:id/favorite`

- **Search**
  - Use `/search?q=`
  - Debounced input in a header search bar
  - Filters (Optional): filter vendors by city or cuisine via `/vendors?city=&cuisine=`

- **Slow Path UX**
  - Somewhere in the app (e.g. About screen), call `/slow`
  - Show proper loading state, retry option, and error handling

- **Documentation**
  - Add a README in `/app` explaining:
    - How to run the app
    - Any design/architecture decisions
    - Tradeoffs or extra features you added

## Time Expectation

We estimate this challenge should take around **5 hours**.
You’re welcome to spend more if you want to polish or add extras, but we’ll mainly be looking at:

- How you structure and reason about the app
- How you handle data fetching and state
- Attention to detail in the UI and UX
- How you consider performance

## Getting Started

### API

```bash
cd api
npm install
npm run dev
```

Server runs at <http://localhost:3333>. You can find a Postman collection in the `/postman` folder to explore the endpoints.

## Final Words

This isn’t about cranking out every single feature perfectly—it’s about showing us how you think, how you code, and how you approach building a small but complete app. We’re excited to see your creativity, polish, and engineering choices shine through.

Good luck, and have fun exploring the world of Street Food Safari! 🚀
