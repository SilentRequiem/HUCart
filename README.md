# HUCart iOS Prototype

HUCart is a student-focused iOS shopping prototype built with Swift and SwiftUI. It simulates a multi-store shopping experience where users can sign in, select a store, browse products, manage a cart, complete a simulated checkout, and view local order history.

This project was created as a proof of concept for a larger shopping application. Store information, product data, account data, and orders are handled locally in the app rather than through external retailer APIs, a backend, or a production authentication system.

## Presentation

- https://tinyurl.com/HamCart
- Mirror: https://tinyurl.com/Hucart2

## Features

- Animated splash screen
- Local login and account creation flow
- Store selection between sample retailers
- Store-specific product categories and product detail views
- Quantity selection before adding products to the cart
- Cart totals and item-count tracking
- Simulated checkout
- Local order history 
- Store switching with cart reset
- Custom tab navigation for Home, Cart, Account, and Stores

## Technologies

- Swift
- SwiftUI
- Xcode

## SwiftUI Concepts Used

HUCart uses SwiftUI state management to share and update data across multiple views.

- `@State` for local view state
- `@StateObject` and `ObservableObject` for shared managers
- `@EnvironmentObject` for passing cart data between views
- `@Binding` for shared selections between parent and child views
- `@Published` for cart items, quantities, and order history
- `UUID` and `Identifiable` for model identifiers
- `NavigationStack` and `NavigationLink` for navigation

## App Structure

The project separates the interface and data into several SwiftUI views and models, including:

- `SplashView`
- `LoginView`
- `SignUpView`
- `StoreSelectionView`
- `HomeScreen`
- `ProductDetailView`
- `CartView`
- `AccountView`
- `StoreResetView`
- `MainTabView`
- `CartManager`
- `Store`, `Product`, `CartItem`, `ProductSection`, and `Order` models

## How It Works

1. The app opens with an animated splash screen.
2. Users enter credentials or create a local account.
3. Users select from the included sample stores.
4. The home screen displays locally defined product categories for the selected store.
5. Users can open a product, choose a quantity, and add it to the cart.
6. `CartManager` tracks products, quantities, totals, and order history across views.
7. Checkout creates a local `Order`, stores it in order history, and clears the cart.

## Current Scope

HUCart is a prototype rather than a production shopping service. The current version does not connect to retailer APIs or databases, process real payments, persist accounts or orders between sessions, or use production-grade authentication.

## Future Improvements

- Add backend and database integration
- Add persistent user accounts and secure authentication
- Connect to real product or retailer APIs
- Add payment processing
- Persist order history between sessions
- Improve cart quantity editing directly from the cart screen
- Expand error handling and validation
- Continue refining UI and accessibility

## Running the Project

1. Clone the repository:

```bash
git clone https://github.com/SilentRequiem/HUCart.git
```

2. Open the Xcode project.
3. Build and run HUCart on an iOS simulator or compatible device.

## Project Highlight

Built a multi-view iOS shopping prototype that demonstrates SwiftUI navigation, shared application state, reusable data models, cart management, simulated checkout, and local order tracking.

## License

This project is open source and available for learning and personal use.
