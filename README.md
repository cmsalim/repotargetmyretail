# repotargetmyretail

myRetailApplication RESTful service

Technologies
Java 11 , Spring Boot 2.4.3 ,Maven ,H2 Database ,STS (IDE)
 Get Product details By Product id
HTTP Method	URL	Action	Description
GET	http://localhost:8080/myRetail/v1/product/{id}	Get Product details By Product id	This service is used to get product details of a product(price and name of the product,currency) by passing product ID{id}

•	RestTemplate is used to consume GetProductName Service(Separate service used  to retrieve only Product name)

Sample Response : 
http://localhost:8080/myRetail/v1/getProductDetails/1231
{
    "id": 1231,
    "name": "Men's 9\" Lined Run Shorts",
    "current_price": {
        "value": 28.33,
        "currency_code": "USD"
    }
}
GetProductName Service: (Separate service used to retrieve only Product name)
Total 5 products are available in this service, product ids mentioned below
1231,1232,1233,1234,1235
HTTP Method	URL	Action	Description
GET	http://localhost:8080/myRetail/v1/getProductName/{id}	Get Product Name By Product id	This service is used to retrieve Product Name by passing product ID{id}

Sample response:
http://localhost:8080/myRetail/v1/getProductName/1234
Men's Knit to Woven Jogger Pants

 Update Product Price by Product Id
This service will accept JSON request similar to the response of  Get Product details By Product id service



HTTP Method	URL	Action	Description
PUT	http://localhost:8080/myRetail/v1/product/{id}	Update Product Price by Product Id 	This service is used to update Product Price by passing product ID{id}

Request and Response:
http://localhost:8080/myRetail/v1/product/1231
Request:
{
    "id": 1231,
    "name": "Men's 9\" Lined Run Shorts",
    "current_price": {
        "value": 55.33,
        "currency_code": "USD"
    }
}





Response:

{
    "id": 1231,
    "name": "Men's 9\" Lined Run Shorts",
    "current_price": {
        "value": 55.33,
        "currency_code": "USD"
    }
}

Databse  -- H2 in memory database
For H2 –console, please use below link after running the application
http://localhost:8080/h2-console/
 
 
