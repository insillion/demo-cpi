## API Endpoint: Add Cash Payment

This endpoint allows users to add a cash payment to their account.

### Request Method

`POST`

### Endpoint

`{{host}}v1/payment/cash`

### Request Body

The request body should be sent in JSON format and must include the following parameters:

- **key** (string): The unique identifier for the payment (e.g., payment ID).
    
- **amount** (object): The amount associated with the payment. This should be a valid object representing the payment amount.
    

### Expected Response

On a successful request, the API will return a response indicating the status of the cash payment addition. The response format will typically include a confirmation message and may also include additional details related to the transaction.

Ensure that the `key` and `amount` fields are correctly populated to avoid errors in processing the payment.