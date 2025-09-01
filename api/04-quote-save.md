### API Endpoint: Create Quote

This endpoint allows users to create a new insurance quote based on the provided parameters. It is primarily used for generating quotes in the context of commercial property insurance.

#### Request Format

- **Method**: POST
    
- **URL**: `{{host}}v1/quote`
    
- **Content-Type**: application/json
    

#### Request Body

The request body must be in JSON format and should include the following fields:

- `wf_id` (string): The workflow identifier.
    
- `product_id` (string): The identifier for the product.
    
- `quote_id` (string): The identifier for the quote (can be empty for new quotes).
    
- `line_of_business_tag` (string): The tag indicating the line of business (e.g., "COMMERCIAL PROPERTY").
    
- `transaction_stage` (string): The current stage of the transaction (e.g., "Quote").
    
- `policy_start_date` (object): The start date of the policy (should be formatted accordingly).
    

**Example Request Body**:

``` json
{
  "wf_id": "6",
  "product_id": "M000000000002",
  "quote_id": "",
  "line_of_business_tag": "COMMERCIAL PROPERTY",
  "transaction_stage": "Quote",
  "policy_start_date": {}
}

 ```

#### Response Format

On a successful request, the API will return a JSON response with the following structure:

- `status` (integer): The status of the request (0 indicates success).
    
- `txt` (string): A message related to the status.
    
- `data` (array): An array containing details about the created quote and associated entities, including:
    
    - `policy_id`: Identifier for the policy.
        
    - `product_id`: Identifier for the product.
        
    - `quote_id`: Identifier for the quote.
        
    - `premium_value`: The calculated premium value.
        
    - `quote`: An object containing detailed information about the quote, including customer information, coverage details, and more.
        

**Example Response**:

``` json
{
  "status": 0,
  "txt": "",
  "data": [
    {
      "policy_id": "",
      "product_id": "",
      "quote_id": "",
      "premium_value": 0,
      "quote": {
        // quote details here
      }
    }
  ]
}

 ```

This endpoint is essential for initiating the insurance quoting process and will return all relevant details needed for further processing or user interaction.