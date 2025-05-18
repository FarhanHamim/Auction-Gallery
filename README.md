# Auction Gallery

Auction Gallery is a dynamic web application that allows users to view active auction items, bid on them (conceptually), and manage a list of their favorite items. The platform provides real-time information on current bid prices, time left for bidding, and the number of bids.

**Live Link:** [https://auction-gallery-bid.netlify.app/](https://auction-gallery-bid.netlify.app/)

**GitHub Repository:** [https://github.com/FarhanHamim/Auction-Gallery](https://github.com/FarhanHamim/Auction-Gallery)

## Features

### Main Requirements

* **Navbar:**
    * Designed precisely according to the Figma specifications.
* **Banner:**
    * Created to exactly match the Figma design.
* **JSON Data for Bid Items:**
    * Includes a JSON file (`public/auctionItems.json`) with at least 6 bid items. Each item contains:
        * `id`
        * `title`
        * `description`
        * `currentBidPrice`
        * `timeLeft`
        * `bidsCount`
        * `image`
* **Active Auctions Section:**
    * Section title and subtitle match the Figma design.
    * Displays 6 auction items, each showing:
        * Item Image (🖼️)
        * Item Name (🏷️)
        * Current Bid Price (💰)
        * Time Left (⏳)
        * A "Bid Now" button (❤️ - icon seems to be used for favorites, actual button text may vary or be a generic bid button)
* **Favorite Items Section:**
    * **Initial State:**
        * Displays a title.
        * Shows a "No items" message.
        * Total amount displayed as 0.
    * **Adding to Favorites:**
        * Clicking the ❤️ icon on an auction item adds it to the favorites list.
        * The favorites list displays:
            * Item Name
            * Current Bid Price
            * Bids Count
            * A Remove Icon (❌)
        * The favorite total price updates dynamically based on the `currentBidPrice` of the added items.
* **React-Toastify Integration:**
    * Uses `react-toastify` to show toast notifications when:
        * An item is added to favorites.
* **Footer:**
    * Built to exactly match the Figma design.

### Challenge Requirements

* **Show Data Using Table:**
    * Bid items are displayed in a table format in a dedicated "All Bids" or similar section.
* **Disable ❤️ Button After Click (Favorite Button Behavior):**
    * When the ❤️ (favorite) icon is clicked for an item:
        * The cursor changes to `not-allowed`.
        * The button becomes disabled.
        * The button/icon color might change (e.g., to red) to indicate it has been favorited.
* **Remove from Favorites:**
    * Clicking the ❌ icon next to an item in the favorites list:
        * Removes the item from the favorites list.
        * Deducts its price from the total favorite items price.

## Technologies Used

Based on an inspection of the repository (`package.json`) and common practices:

* **Frontend:**
    * **React (Vite + React template):** For building the dynamic user interface.
    * **JavaScript (ES6+):** Core programming language.
    * **HTML5 & CSS3:** For structure and styling.
    * **Tailwind CSS:** A utility-first CSS framework for rapid UI development.
    * **DaisyUI:** A plugin for Tailwind CSS providing pre-styled components.
* **Routing:**
    * **React Router DOM:** For handling client-side navigation between different views/pages.
* **Notifications:**
    * **React Toastify:** For displaying toast notifications.
* **Icons:**
    * **React Icons:** For incorporating a wide variety of icons.
* **Development Tools:**
    * **Vite:** Fast frontend build tool.
    * **ESLint:** For code linting and maintaining code quality.
* **Deployment:**
    * **Netlify:** The live version is hosted on Netlify.

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

* Node.js (v18.x or later recommended) and npm (or yarn) installed on your machine. You can download them from [nodejs.org](https://nodejs.org/).

### Installation

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/FarhanHamim/Auction-Gallery.git](https://github.com/FarhanHamim/Auction-Gallery.git)
    ```
2.  **Navigate to the project directory:**
    ```sh
    cd Auction-Gallery
    ```
3.  **Install NPM packages:**
    ```sh
    npm install
    ```
    *(If you prefer yarn, you can use `yarn install`)*

4.  **Run the development server:**
    ```sh
    npm run dev
    ```
    *(If you prefer yarn, use `yarn dev`)*

    This will typically open the application in your default web browser at `http://localhost:5173` (the port might vary if 5173 is in use).

## Project Structure (Anticipated)

The project likely follows a structure typical for Vite + React applications:

Auction-Gallery/
├── public/
│   └── auctionItems.json  # Static JSON data for auction items
├── src/
│   ├── assets/            # Images, logos, etc.
│   ├── components/        # Reusable UI components (e.g., Navbar, Footer, AuctionCard, FavoriteItem)
│   ├── layouts/           # Main layout structure
│   ├── pages/             # Page components (e.g., Home, AllBids, FavoritesPage)
│   ├── routes/            # Route definitions
│   ├── App.jsx            # Main application component
│   ├── main.jsx           # Entry point for React
│   └── index.css          # Global styles / Tailwind imports
├── .eslintrc.cjs          # ESLint configuration
├── .gitignore             # Specifies intentionally untracked files
├── index.html             # Main HTML file served by Vite
├── package.json           # Project metadata, scripts, and dependencies
├── postcss.config.js      # PostCSS configuration (for Tailwind)
├── tailwind.config.js     # Tailwind CSS configuration
├── vite.config.js         # Vite configuration
└── README.md              # This file

## How to Use

1.  Navigate to the live link: [https://auction-gallery-bid.netlify.app/](https://auction-gallery-bid.netlify.app/) or run the project locally.
2.  Explore the **Homepage** which includes:
    * A navigation bar for easy access to different sections.
    * A prominent banner.
    * An "Active Auctions" section displaying various items up for bid.
3.  In the "Active Auctions" section, view details for each item like image, name, current bid, and time left.
4.  Click the ❤️ icon on an item card to add it to your "Favorite Items". A toast notification will confirm the addition. The icon will then appear disabled for that item in the active auctions list.
5.  Navigate to a "Favorites" section/page (if distinct) or view the "Favorite Items" component on the page. Here you will see:
    * A list of all items you've marked as favorite, showing their name, bid price, and bids count.
    * The total combined price of all your favorite items.
    * An ❌ icon next to each favorite item.
6.  Click the ❌ icon to remove an item from your favorites. The list and total price will update accordingly.
7.  There might be an "All Bids" or similar section where auction items are displayed in a table format for a comprehensive overview.

## Contributing

Contributions are welcome and greatly appreciated! If you have suggestions for improving the application:

1.  **Fork the Project**
2.  **Create your Feature Branch** (`git checkout -b feature/AmazingFeature`)
3.  **Commit your Changes** (`git commit -m 'Add some AmazingFeature'`)
4.  **Push to the Branch** (`git push origin feature/AmazingFeature`)
5.  **Open a Pull Request**

You can also simply open an issue with the tag "enhancement".

## Author

* **Farhan Hamim**
    * GitHub: [https://github.com/FarhanHamim](https://github.com/FarhanHamim)

## License

This project is open source. Please refer to the `LICENSE` file in the repository if one is added. For now, it is under the repository owner's copyright.

## Acknowledgements

* Project requirements and design inspiration (Figma).
* Creators of React, Vite, Tailwind CSS, DaisyUI, React Router, React Toastify, and React Icons.
