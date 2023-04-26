# REST API for Online Cab Booking Application

Our team has developed a REST API for an online cab booking application. This API enables customers to log in, modify their profile details, and book rides. Likewise, drivers can log in, update their information and vehicle details, and accept ride requests. An admin account is also available to oversee the entire process, including updating information and accessing the application's data. To ensure data and user security, we have implemented rigorous validation procedures at every stage for all users.


# Tech Stack

- Java
- Hibernate
- Spring Framework
- Spring Boot
- Spring Data JPA
- MySQL
- Swagger UI
- Maven

# Modules

- Login Module
- Cab Driver Module
- Customer Module
- Admin Module
- Trip Details Module

## Admin Features
- Admin can access all the information of customer, cab driver and cab.
- Admin can access all Trip Details along with specific trip details using a particular cab or a customer.


## Customer Features
- Customer can login in the application and update their information using their username and password.
- Customer can book trips using pickup location and destination.
- Customer can access the bill after the trip is completed.


## Cab Driver features
- Cab Driver can login in the application and update their information using their username and password.
- Cab driver can add and update their cab details.
- Cab Driver can mark their availability according to the trips status.
- Cab Driver can end the trip and application generates a bill for the trip.

# API Root Endpoint
```
https://localhost:8888/
```
```
http://localhost:8888/swagger-ui/
```
# API Reference

## Customer Requests

```http
  Customer Controller
```

| Request | METHOD     |  URI | Description                |
| :-------- | :------- | :----- | :------------------------- |
| `POST` | `Create` | `http://localhost:8888/customer/create` | Create Customer |
| `PUT` | `Update` | `http://localhost:8888/customer/update` | Update Customer |
| `DELETE` | `Delete` | `http://localhost:8888/customer/delete` | Delete Customer |
| `POST` | `Book Trip` | `http://localhost:8888/customer/booktrip` | Book Trip |
| `DELETE` | `Cancel Trip` | `http://localhost:8888/customer/canceltrip` | Cancel Trip |
| `POST` | `Trip List` | `http://localhost:8888/customer/triplist` | Trip List |
| `POST` | `Generate Bill` | `http://localhost:8888/customer/generatebill` | Generate Bill |


## Cab Driver Requests

```http
  Cab Driver Controller 
```

| Request | METHOD     |  URI | Description                |
| :-------- | :------- | :----- | :------------------------- |
| `POST` | `Create` | `http://localhost:8888/cabdriver/create` | Create Cab Driver |
| `PUT` | `Update` | `http://localhost:8888/cabdriver/update` | Update Cab Driver |
| `DELETE` | `Delete` | `http://localhost:8888/cabdriver/delete` | Delete Cab Driver |
| `POST` | `Book Trip` | `http://localhost:8888/cabdriver/tripcompleted` | Trip Completed |


## Admin Requests

```http
  Admin Controller
```

| Request | METHOD     |  URI | Description                |
| :-------- | :------- | :----- | :------------------------- |
| `POST` | `Create` | `http://localhost:8888/admin/create` | Create Admin |
| `PUT` | `Update` | `http://localhost:8888/admin/update` | Update Admin |
| `DELETE` | `Delete` | `http://localhost:8888/admin/delete` | Delete Admin |
| `POST` | `Get All Trip` | `http://localhost:8888/admin/getalltrips` | Show All Trip |
| `DELETE` | `Get Trip By Cab` | `http://localhost:8888/admin/getalltripsbycab/{cabId}` | Get All Trip By Cab ID |
| `POST` | `Get Trip By Customer` | `http://localhost:8888/admin/triplist` | Get All Trip By Customer |


# Sample API Response for Customer Account Creation
### Request Type
```
POST
```

### Request URI
```
http://localhost:8888/customer/create
```

### Request Body
```
{
    "username":"pablo",
    "password":"escobar",
    "mobile":"9874568721"
}
```
### Response Body

```
{
  "adminId": 1,
  "username": "pablo",
  "password": "escobar",
  "address": null,
  "mobile": "9874568721",
  "email": null
}
```