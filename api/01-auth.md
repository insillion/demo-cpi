# POST /api/v1/auth

This `auth` endpoint allows users to authenticate and obtain access to Carma's Insurance policy issuance system.

By default, the auth token remains valid for 15 minutes (idle period). To extend this duration for each user, kindly reach out to the admin/Carma.

We recommend making the auth request prior to each transaction.

#### Request Body Parameters

- `email` (string, required): The email address of the user.
    
- `pwd` (string, required): The password of the user.
    

The token from this request's response is used for subsequent API calls.

Please reach out to [sales@carma365.com](https://mailto:sales@carma365.com) to obtain Testing and/or Production credentials.

**Response**:

| Key | Description |
| --- | --- |
| status | The status of the response. 0 indicates success. |
| txt | Error message, if any. |
| token | System generated token to access other APIs. |
| email | The email of the logged-in user. |

_**By default – Tokens are configured to be valid for 15 minute sessions. To extend this duration, kindly reach out to**_ [<i><b>sales@carma365.com</b></i>](https://mailto:sales@carma365.com)_**.**_