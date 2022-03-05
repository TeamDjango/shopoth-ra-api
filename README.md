# shopoth-ra-api

Authentication

* **Auth URL**: `http://shopoth-ra.com/v1/api/login`

* **Method:** `POST`

*  **Params:** `email`,`password`

params do
 requires :email, type: String
 requires :password, type: String



* **Success Response:**
* **Code:** `200`
  	* **Content:**

```json
{
    "success": true,
    "data": {
        "token": "1|DocZetbYVl3WVqYpSo4aENOKkLL9blTvRPRUbxfb",
        "name": "Shopoth"
    },
    "message": "User signed in"
}
 

```

* ** Error Response:**
* **Code:** `403`
  	* **If username or password not matched then:**
  	* **Content:**
```json
{
    "success": false,
    "message": "Unauthorised.",
    "data": {
        "error": "Unauthorised"
    }
}

```

View All Retailer_Assistants

* **URL**: `http://shopoth-ra.com/v1/api/ra-list`

* **Method:** `GET`

*  **Headers:**
	 `Authorization: token’`


```json
{
    "success": true,
    "data": [
        {
            "id": 1,
            "fname": "Noor Mohammad",
            "lname": "BABU",
            "contact": "01715619984",
            "email": "babubph007@gmail.com",
            "territory_id": 2,
            "distribution_point_id": "6"
        },
        {
            "id": 10,
            "fname": "Asker",
            "lname": "Firoz",
            "contact": "01711574170",
            "email": "rusho127@gmail.com",
            "territory_id": 2,
            "distribution_point_id": "6"
        },
        {
            "id": 12,
            "fname": "Md. Sarower",
            "lname": "Azam",
            "contact": "01551577577",
            "email": "mdsarowerazam_87@yahoo.com",
            "territory_id": 2,
            "distribution_point_id": "6"
        }
		    ],
    "message": "Successfully fetched all Retail Assistant data.",
    "status": 200
}

```


Find Retailer_Assistants by contact no

* **URL**: `http://shopoth-ra.com/v1/api/ra/{ra:contact}`

* **Method:** `GET`

*  **Headers:**
	 `Authorization: token’`


```json
{
    "success": true,
    "data": {
        "id": 1,
        "fname": "Noor Mohammad",
        "lname": "BABU",
        "contact": "01715619984",
        "email": "babubph007@gmail.com",
        "territory_id": 2,
        "distribution_point_id": "6"
    },
    "message": "Individual Retail Assistant data.",
    "status": 200
}

```

* ** Error Response:**
* **Code:** `403`
  	* **If Retail Assistan contact not found then:**
  	* **Content:**
```json
{
    "success": false,
    "message": "Retail Assistant does not exist.",
    "status": 404
}

```

