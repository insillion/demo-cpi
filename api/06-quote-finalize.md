## API Endpoint : Quote Finalize

This endpoint allows users to create a new quote for a specified product within the system. The request must include various parameters that define the quote details, and upon successful execution, it returns a structured response containing information about the created quote and associated entities.

### Request Parameters

The request is sent as a JSON object with the following parameters:

- **wf_id** (string): The workflow ID associated with the quote.
    
- **product_id** (string): The unique identifier for the product being quoted.
    
- **quote_id** (string): The ID of the quote being created or referenced.
    
- **line_of_business_tag** (string): The tag indicating the line of business, e.g., "COMMERCIAL PROPERTY".
    
- **transaction_stage** (string): The current stage of the transaction, which should be "Quote".
    
- **application_date** (integer): The date of the application represented as a timestamp.
    
- **policy_start_date** (object): An object representing the start date of the policy (currently empty in the example).
    

### Expected Response

On a successful request, the API responds with a status code of `200` and a JSON object containing:

- **status** (integer): Indicates the success or failure of the request (0 for success).
    
- **data** (array): An array of objects containing detailed information about the quote and related entities, including:
    
    - **policy_id** (string): The ID of the policy created.
        
    - **product_id** (string): The ID of the product associated with the quote.
        
    - **quote_id** (string): The ID of the quote.
        
    - **premium_value** (number): The calculated premium value for the quote.
        
    - **quote** (object): Contains detailed information about the quote, including customer details, coverage options, and more.
        

### Notes

- Ensure that all required parameters are included in the request body to avoid errors.
    
- The response may contain additional nested objects and arrays that provide comprehensive details about the quote and its associated data.
    
- Users should handle the response appropriately, especially when processing the `data` array for further actions or displays.
    

This endpoint is essential for managing quotes in the system, particularly for commercial property insurance transactions.