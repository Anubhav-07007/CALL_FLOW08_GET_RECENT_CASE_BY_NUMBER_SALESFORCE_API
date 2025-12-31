# CALL_FLOW08_GET_RECENT_CASE_BY_NUMBER_SALESFORCE_API
# This project demonstrates the integration between Genesys Cloud CX and Salesforce to fetch the most recent open case of a customer using their phone number during an inbound call.
# The solution helps contact center agents quickly understand customer issues and provide faster resolution.

#  Use Case

  When a customer calls the contact center:
  
  System captures the caller's phone number (ANI)
  
  Genesys triggers a Salesforce API call
  
  Salesforce returns the most recent open case
  
  Case details are displayed to the agent
  
  Agent continues the call with full context

#  Features

   Real-time Salesforce integration
  
   Fetch latest open case by phone number
  
   Supports live inbound call flow

# Technologies Used

  Genesys Cloud CX
  
  Salesforce REST API
  
  Genesys Data Actions
  
  Architect Flow
  
  OAuth 2.0 Authentication
  
  JSON / API Integration

# Implementation Details

  Salesforce Configuration
  
  Enabled REST API access
  
  Used SOQL query to fetch cases
  
  Filtered by:
  
  Customer phone number
  
  Case status = Open
  
  Sorted by most recent case

#  Genesys Cloud – Data Action

  Created a Data Action with:
  
  Request URL: Salesforce Case API
  
  Authentication: OAuth 2.0
  
  Request Mapping: Phone number input
  
  Response Mapping:
  
  Case ID
  
  Case Number
  
  Subject
  
  Description

#  Architect Flow Logic

    Capture caller ANI
    
    Trigger Salesforce Data Action
    
    Retrieve latest case details
    
    Store values in flow variables
    
    Use data for:
    
    Screen pop
    
    Agent context
    
    Call routing logic

# Sample Response (Salesforce)

    {
  "id": "500dL00002bE25IQAS",
  "casenumber": "00036518",
  "subject": "google pay",
  "description": "google pay not working"
}
    
        ✅ Improves customer experience
        
        ✅ Reduces Average Handle Time (AHT)
