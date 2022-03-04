# shopoth-ra-api

Authentication

* **Auth URL**: `http://shopoth-ra.com/v1/api/login`

* **Method:** `POST`

*  **Params:** `email`,`password`

params do
 requires :email, type: String
 requires :password, type: String
end


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