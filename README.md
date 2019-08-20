# ProductBasket
It is a simple basket developed on Node JS platform with loopback framework. (Ex : Clone of Flipkart Add cart and product basket and pay logic). <br />
#Required Tool and Steps to Run The Project
1 : oracle DB
2 : Node Envoiroment
3 : Clone the folder into your System
4 : Go inside folder and run into CMD.
5 : npm install
6 : nodemon .
Product will start listening on the port number 3000.
Web server listening at: http://localhost:3000
Browse your REST API at http://localhost:3000/explorer
# PFB API's with Request and Response
1 : Basic API for Admin to register A,B,C,D Products

Api : https://localhost:3000/api/getList/product
Method : POST
Request :

{
  "prodCategory": "B",
  "prodName": "Apple",
  "prodPrice": "20",
  "prodDiscount": "1"
}
Response :
{
    "message": "Product added Successfully."
}

2 : Add Items :

API : https://localhost:3000/api/user/addItems

Method : POST

Request :

{
  "prodId": 262,
  "prodName": "Mango",
  "prodPrice": 30,
  "prodDiscount" : 15
}

Response :
{
   message : 'Product added successfully'.
}
3: Updating Quantity of Items :

Method  : POST
API : https://localhost:3000/api/user/updating_Items

Request :

{
  "prodId": 262,
  "prodName": "Potato",
  "prodPrice": 20,
  "prodDiscount" : 5,
  "totalNumber" : 2
}

Response :

{
    "message": "Quantity added successfully."
}

4 : Returning list of data basket/cart(with individual price and discount data),the total price and total discounts applied.
Method : GET ( NOTE : Pass ProdId as a unique guest user and basketCheckout_Price is a total amount and discount calculation object).
API : https://localhost:3000/api/user/calcItems?prodId=262

Response :

[
    {
        "prodA_Price": 30,
        "prodA_Discount": 15,
        "total_Price": 135,
        "discount_Applied": 15
    },
    {
        "prodB_Price": 20,
        "prodB_Discount": 5,
        "total_Price": 35,
        "discount_Applied": 5
    },
    {
        "prodC_Price": 50,
        "prodC_Discount": 0,
        "total_Price": 50,
        "discount_Applied": 0
    },
    {
        "prodD_Price": 15,
        "prodD_Discount": 0,
        "total_Price": 45,
        "discount_Applied": 0
    },
    {
        "basketCheckout_Price": {
            "Total_Price": 265,
            "Total_Discount": 20
        }
    }
]

# Please go threw Test Cases attached with project for more clarity.
