# AgilisiumProduct
Test Project for Agilisum getPoductDetails and getConfigDetails


End Point Urls:
domain = http://localhost:8080
API1: {domain}/api/getproductdetails?id=1  -- credentials (username/password)user/user   -- role (USER)
API2: {domain}/api/getconfigdetails   -- credentials (username/password)admin/admin -- role (ADMIN)

Basic Authentication is provided by using InMemoryAuthentication
=================================================================================
Product Model Class Properties:
productId
productName
productCost
productMFD
=================================================================================
Config Model Class Properties:
name
url
=================================================================================
ProductController.java
ProductRepo.java (data get from mysqlDB)
ProductStaticRepo(Static data added)
ProductService.java
ProductResponseModel.java
=================================================================================
ConfigController.java
ConfigService.java
========================================================
I have commented this code //return productRepo.findById(id).get();// where you can get product details from Mysql DB
If you want to try this please uncomment this line and give username and password(your corresponding username and password)
in appilacation.properties file.

or you can try with static data.
================================================
http://localhost:8080/api/getproductdetails?id=1
Result in JSON:
{"statusCode":200,
"date":"2020-05-10T11:46:56.751",
"message":"Product details successfully fetched.",
"payload":{
"productId":1,
"productName":"Laptop",
"productCost":50000,
"productMFD":"2019-03-15"}
}

http://localhost:8080/logout
http://localhost:8080/login?logout

http://localhost:8080/api/getconfigdetails
Result in JSON:
{"statusCode":200,
"date":"2020-05-10T12:01:02.41",
"message":"fetched successful",
"payload":{
"name":"Agilisium Product",
"url":"http://localhost:8080/api"}
}
