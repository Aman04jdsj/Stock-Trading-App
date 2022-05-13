# Stock-Trading-App
A native SwiftUI application that allows users to search different stock symbols/tickers and obtain detailed insights about them. In addition the users can trade with virtual money and create a portfolio. Users can also favorite certain stocks to track them.

# Technologies used
SwiftUI, NodeJS, express, SFSymbols

# Walkthrough
## Home Screen
<img width="269" alt="Screen Shot 2022-05-12 at 5 11 01 PM" src="https://user-images.githubusercontent.com/58076457/168186935-50b518e2-ceac-4b7c-9b3b-471dcc916e31.png">
The home screen will have a Navigation Bar toolbar at the top with title “Stocks”. A search bar is attached to the navigation bar and will be revealed if you scroll up. The first row displays the current date. This is followed by 2 sections:
### Portfolio
This section will show:
#### Cash Balance - the money in the wallet currently for the user, which is
uninvested cash
#### Net Worth – Cash Balance + total values of stocks owned

This is followed by the list of stocks in the user portfolio with that stock’s:
#### Stock Symbol
#### Market Value - latest stock quote * number of shares owned
#### Change In Price From Total Cost – (latest stock quote – stock avg cost) *
number of shares owned
#### Change In Price From Total Cost Percentage - (change in price from total
cost / total cost of stock (stock avg cost * number of shares owned)) *
100
#### Total Shares Owned
If the user starts the app for the first time, they will not have any stocks/shares in the portfolio and an initial pre-loaded amount of $25,000 to trade on the app. This amount can change based on the trading done by the user. (For example, if the market fluctuates after buying and selling stocks, it can become more, or less than $25,000)

### Favorites
This section will show all the stocks that have been favorited by the user to
allow the user to easily check the prices of stocks in their watchlist. For each favorited stock the following information is displayed:
#### Stock Symbol
#### Current price - Latest Stock Quote
#### Change In Price (Since Last Close)
#### Change In Price Percentage (Since Last Close)

#### Delete functionality allows the user to remove/delete the stock from the Favorites section.
#### Move functionality allows the user to reorder the stocks in either section. The user can long press on the right of the stock listing and drag it to a new position. The list will be updated accordingly to ensure the new order going forward.

<img width="293" alt="Screen Shot 2022-05-12 at 5 18 39 PM" src="https://user-images.githubusercontent.com/58076457/168187525-a70f9e05-c103-404d-aa35-896175eb5dcf.png">
