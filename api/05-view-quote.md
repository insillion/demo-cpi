### API Endpoint: View Quote

This endpoint retrieves the details of a specific insurance policy based on the provided `policy_id`.

### Request

- **Method**: GET
    
- **URL**: `{{host}}/v1/policy?policy_id={{policy_id}}`
    

#### Query Parameters

- `policy_id` (string): The unique identifier of the policy you wish to retrieve. This parameter is required.
    

### Response

The response will return a JSON object containing the status of the request and the details of the requested policy.

#### Response Structure

- **status** (integer): Indicates the success or failure of the request. A value of `0` typically indicates success.
    
- **txt** (string): A text field that may contain additional information about the request status (usually empty).
    
- **data** (array): An array containing the policy details, where each policy object may include the following fields:
    
    - `policy_id` (string): The unique identifier of the policy.
        
    - `product_id` (string): The identifier of the product associated with the policy.
        
    - `wf_id` (integer): Workflow ID related to the policy.
        
    - `customer_id` (string): The ID of the customer associated with the policy.
        
    - `policy_no` (string|null): The policy number, which may be null if not assigned.
        
    - `issue_date` (string|null): The date the policy was issued.
        
    - `policy_start_date` (string): The start date of the policy coverage.
        
    - `policy_end_date` (string): The end date of the policy coverage.
        
    - Additional fields related to quotes, documents, payments, and other relevant details.
        

### Notes

- Ensure that the `policy_id` parameter is valid to receive the appropriate policy details.
    
- The response may contain nested objects with further details about quotes, payments, and documents associated with the policy.
    
- The structure of the response allows for extensibility, meaning additional fields may be included in future updates.