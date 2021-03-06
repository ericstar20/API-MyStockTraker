# API-MyStockTraker

__Motivation__:\
As an enthusiast of programming, I used APIs to acquire data in several projects. However, my knowledge of API is still on the basic level, only use GET to grab the data.
To reveal the mask of the mystery box, I built my first REST API during the thanksgiving holiday.

__Project Objective__:\
The main purpose of this project is to store my stock purchase records by custom API. Then, build a python program to calculate the difference between total investment and current market values of my stocks.\
Below is the workflow of this project:
<img src = "/images/WorkFlow-MyRestAPI.jpg" width='900' heigh='600'>

__The API introduction__:\
The purpose of this API is to store my stock purchasing records.\
The storing table includes 5 columns
* 1. __Transaction id__: The incremental id (Primary key).
* 2. __Transaction Datetime__: The combination of data and time. The value is generated by python DateTime.now().
* 3. __Transaction Symbol__: The symbol of the transaction. The value sent by URL request.
* 4. __Transaction Volumns__: How many shares I bought in the transaction.
* 5. __Transaction Price__: Acquire the real-time price by connecting to twelvedata API.

Below is the view of the table's structure:
<img src = "/images/MyStockAPI - GetAll.png" width='900' heigh='600'>

The API requests include __GET__ (both all shares or by specific symbol ticker), __POST__ (insert a new transaction), __PUT__ (modify exist transaction), __Delete__ (delete a transaction).\
* __GET__
<img src = "/images/MyStockAPI - GET symbol.png" width='700' heigh='600'>

* __POST__
<img src = "/images/MyStockAPI - Post New Share.png" width='700' heigh='600'>

* __PUT__
<img src = "/images/MyStockAPI - Modify Share.png" width='700' heigh='600'>

* __DELETE__
<img src = "/images/MyStockAPI - Delete Share.png" width='700' heigh='600'>

After constructed the API, I built a python code - StockTracker.py to calculate the difference between total investment and current market values of my stocks.\
Then, use Tkinter to generate a simple GUI result.

The result is as below\
<img src = "/images/Stock Tracker Dash.png" width='700' heigh='600'>

## Conclusion
Through this project, I understand how to build a REST API by flask and also gain hands-on experience. Moreover, by taking the flask tutorial, I brush up on my python basic knowledge such as Class, List comprehension, etc.\
Even though I did not enroll in the stock market right now, I believe this project can help me better understand my future investment. The code is just a prototype, after I officially access the stock market, I will definitely modify it to align my requirement!

## Important Resourses

### The Reference and Tutorial I used
1. [Flask Tutorial](https://www.udemy.com/course/rest-api-flask-and-python/)
2. [Twelvedata's API document](https://twelvedata.com/docs#getting-started)
