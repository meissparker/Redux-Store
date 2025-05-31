ManageProducts.tsx


This component allows the user to create, edit, and delete products using a form and displays the list of existing
products as cards. It uses Firebase-based service functions for database operations and provides feedback 
and editing options through state and Bootstrap UI.


OrderDetails.tsx


This component shos the details of a certain order when the user clicks on View Details. It shows the order
in a Card with the date, price and list of purchased items with their quantities and prices.


NavBar.tsx


This responsive navbar contains links based on whether or not the user is logged in and where they are at in the website.
It has navigation to different pages in the website.


Orders.tsx


The Orders component fetches and displays the users past orders showing each order's items date and total price.
It provides a "View Details" button that links the user to a detailed page for each order.


PageLayout.tsx


This page provides a consistent structure since the return statements in the other pages are wrapped in it.
It ensures there is a navigation bar at the top and that everything is wrapped in a bootstrap container. It has children passed to it.


PrivateRoute.tsx
This component restricts access to its child content using Firebase authentication. It redirects unauthenticated users 
to the login page and shows a loading message during verification.


ProductDetails.tsx


This component fetches and displays detailed info about a single product using the product ID. Users can 
also add items to their cart from this page.


Products.tsx


This component displays a list of products fetched by category. Users can choose the category using the category
dropdown.


Profile.tsx


This component allows users to view and update their account info, such as email, password, name, and address.
It also gives them the option to delete their account.


Register.tsx


This component provides users with a registration form to create an account on the website. They are asked to enter an 
email and a password. Then they are redirected to the login page where they can enter their new credentials and login to the website.


ShoppingCart.tsx


This component shows the items in the user's cart and calculates the total of the items in the cart.
It also gives users the option to remove individual items. It also enables checking out by placing an order with FireStore.



asyncActions.ts


This function is a Redux Tookit createAsyncThunk which fetches a counter value from an external API.


cartSelectors.tx


This file defines three Redux selectors for accessing cart data from the global state. 
selectCartTotal which calculates the total price of all cart items, selectCartQuantity, which sums up
the total quantity of items in the cart, and selectCartItems which returns the raw array of cart items from the 
state.


CartSlice.ts


This redux slice defines aand manages the shopping cart state. It has three reducers, addToCart which adds
an item to the cart, decrementFromCart which removes an item from the cart, and clearCart which empties the cart.


store.ts


This codes sets up a Redux store with a cart reducer and custom middleware to save cart items in sessionStorage
after each action.


OrderService.ts


This code defines Firestore-based functions to place an order, fetch a specific order by ID, and retrieve
all orders for a user, including their items, total price, and creation timestamp.


ProductService.ts

This module provides Firestore functions to fetch products retrieve unique categories, and perform create,
update, and delete operations on product documents.


App.tsx

The app component provides routing and uses PrivateRoute to enforce authentication, which allows only users 
that are logged in to access the store.


main.tsx


This file renders the app by wrapping the App component with BrowserRouter for routing, QueryClientProvider for React Query,
and Provider for Redux state management.
















