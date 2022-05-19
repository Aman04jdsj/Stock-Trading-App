# Stock-Trading-App
A native SwiftUI application that allows users to search different stock symbols/tickers and obtain detailed insights about them. In addition the users can trade with virtual money and create a portfolio. Users can also favorite certain stocks to track them.

# Demo video
https://user-images.githubusercontent.com/58076457/169390747-6a8284ad-55df-4a5a-91c2-2c7c8d61d44b.mp4

# Technologies used
SwiftUI, NodeJS, express, SFSymbols, Finnhub APIs

# Walkthrough
## Home Screen
<img width="269" alt="Screen Shot 2022-05-12 at 5 11 01 PM" src="https://user-images.githubusercontent.com/58076457/168186935-50b518e2-ceac-4b7c-9b3b-471dcc916e31.png">
The home screen will have a Navigation Bar toolbar at the top with title “Stocks”. A search bar is attached to the navigation bar and will be revealed if you scroll up. The first row displays the current date. This is followed by 2 sections:

### *Portfolio:
This section will show:
#### *Cash Balance:
The money in the wallet currently for the user, which is uninvested cash
#### *Net Worth:
Cash Balance + total values of stocks owned

This is followed by the list of stocks in the user portfolio with that stock’s:
#### 1. Stock Symbol
#### 2. Market Value - latest stock quote * number of shares owned
#### 3. Change In Price From Total Cost – (latest stock quote – stock avg cost) * number of shares owned
#### 4. Change In Price From Total Cost Percentage - (change in price from total cost / total cost of stock (stock avg cost * number of shares owned)) * 100
#### 5. Total Shares Owned:
If the user starts the app for the first time, they will not have any stocks/shares in the portfolio and an initial pre-loaded amount of $25,000 to trade on the app. This amount can change based on the trading done by the user. (For example, if the market fluctuates after buying and selling stocks, it can become more, or less than $25,000)

### *Favorites:
This section will show all the stocks that have been favorited by the user to
allow the user to easily check the prices of stocks in their watchlist. For each favorited stock the following information is displayed:
#### 1. Stock Symbol
#### 2. Current price - Latest Stock Quote
#### 3. Change In Price (Since Last Close)
#### 4. Change In Price Percentage (Since Last Close)

#### Delete functionality:
Allows the user to remove/delete the stock from the Favorites section.
#### Move functionality:
Allows the user to reorder the stocks in either section. The user can long press on the right of the stock listing and drag it to a new position. The list will be updated accordingly to ensure the new order going forward.

<img width="293" alt="Screen Shot 2022-05-12 at 5 18 39 PM" src="https://user-images.githubusercontent.com/58076457/168187525-a70f9e05-c103-404d-aa35-896175eb5dcf.png">

#### Search functionality:
When pulled down from the home screen, a search bar will appear. When the search bar is clicked, the users will be able to enter a keyword to search for stock symbols. The users will get provided with suggestions of tickers. When the user taps on a suggestion, the user goes to the stock detail screen.

<img width="254" alt="Screen Shot 2022-05-12 at 5 23 17 PM" src="https://user-images.githubusercontent.com/58076457/168187870-75207a33-4d98-42c1-84d4-cf79f259c265.png">

## Detailed Stock Information Screen
On clicking any stock on the home screen or in the search result list, the user is navigated to the stock detail screen. The NavigationBar has a Stocks back button which when clicked will go back to the home screen. The Navigation title will be set to the ticker of the stock currently being viewed. The Navigation bar also contains a favorite icon on the right to add or remove the stock from favorites. Adding/removing stocks from favorites will display a toast message.
    Below the NavigationBar, there are 5 fields: company name, company logo, current price with ‘$’ sign, the change price with ‘$’ sign (the text color will be green, red, or grey based on the change price value being positive, negative or zero respectively) and the change percentage with ‘%’ sign.

### *Portfolio Section:
The Portfolio section allows the user to trade the shares of the stock. It contains a left section which shows the number of stocks the user owns, the avg cost per share, total cost of shares owned, change in price from total cost and the market value of the shares owned (2 decimals, same for all money related fields) of the stock in the user portfolio. The right section contains a trade button.

<img width="524" alt="Screen Shot 2022-05-12 at 5 32 19 PM" src="https://user-images.githubusercontent.com/58076457/168188534-cc10bd00-1e58-4312-b780-dd258b2b8de4.png">

### *Stats Section:
The Stats section shows various stats of the given stock symbol. These are:
1. High Price
2. Low Price
3. Open Price
4. Previous Close Price

### *About Section:
The About section shows various details about the given stock symbol. These are:
1. IPO Start Date
2. Industry
3. Webpage link
4. Company Peers

### *Insights Section:
The insights section contains the social sentiments table that shows information organized in three lists:
1. First List
o Stock Name Header
o Total Mentions Header
o Positive Mentions Header 
o Negative Mentions Header

2. Second List
o Reddit Header
o Reddit Total Mentions Value
o Reddit Positive Mentions Value 
o Reddit Negative Mentions Value

3. Third List
o Twitter Header
o Twitter Total Mentions Value
o Twitter Positive Mentions Value
o Twitter Negative Mentions Value

<img width="367" alt="Screen Shot 2022-05-12 at 5 42 27 PM" src="https://user-images.githubusercontent.com/58076457/168189566-89f886eb-00d3-40cc-947b-cadd3b607b5c.png">

### *News Section:
The News section displays the news articles related to the given stock symbol. For each article, the information displayed is article source, article published ago (time since article was published relative to now), article image and article title. Clicking on a news article opens a sheet for more detail.
The sheet shows a close button on the top right corner. The following information is shown below it:
1. Article Source
2. Article Published Date
3. Article Title
4. Article Description
5. Article Link
6. Twitter Button (clicking it opens Twitter into safari with title and url being shared)
7. Facebook Button (clicking it opens Facebook into safari with url being shared)

<img width="365" alt="Screen Shot 2022-05-12 at 5 42 54 PM" src="https://user-images.githubusercontent.com/58076457/168189623-24bef9ef-8045-4762-98e1-7b1b3c7508bf.png">

<img width="365" alt="Screen Shot 2022-05-12 at 5 43 12 PM" src="https://user-images.githubusercontent.com/58076457/168189640-3849df2b-9a09-48aa-a715-aedb2a23b8c9.png">

<img width="365" alt="Screen Shot 2022-05-12 at 5 44 02 PM" src="https://user-images.githubusercontent.com/58076457/168189655-2f2e96e3-e6b3-4db9-b272-0d911262c8b1.png">

<img width="365" alt="Screen Shot 2022-05-12 at 5 44 11 PM" src="https://user-images.githubusercontent.com/58076457/168189664-56703f92-96db-4382-9db4-8b3777d02f85.png">

<img width="365" alt="Screen Shot 2022-05-12 at 5 44 32 PM" src="https://user-images.githubusercontent.com/58076457/168189684-d4a38fdf-fc73-4df0-ba21-fffcfb3ef291.png">

### *Trade Sheet:
The Trade button in the Portfolio section opens a sheet for trading. In the middle is a TextField. There is also a numeric keyboard that pops up on clicking the TextField. Below the TextField, there is a calculation result which updates based on the numeric input to display the final price of the trade. At the bottom, the trade sheet displays the current amount of uninvested money available to trade for the user and two buttons for the user to either buy or sell the number of shares they have entered. After the user presses Buy or Sell, and a trade is successful the user is shown the trade success message. 

<img width="304" alt="Screen Shot 2022-05-12 at 5 50 54 PM" src="https://user-images.githubusercontent.com/58076457/168190004-2fc1726f-eced-4928-b064-6f816aef4a77.png">

<img width="321" alt="Screen Shot 2022-05-12 at 5 52 01 PM" src="https://user-images.githubusercontent.com/58076457/168190095-0af7585c-501d-43d3-a000-20bfdecee201.png">

