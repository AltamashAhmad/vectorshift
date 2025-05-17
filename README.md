# VectorShift Technical Assessment

This repository contains my implementation of the VectorShift integrations technical assessment, focusing on HubSpot OAuth integration.

## Project Overview

This project implements a full-stack application that allows users to connect with third-party services (Notion, Airtable, and HubSpot) through OAuth. The implementation focuses specifically on:

1. **HubSpot OAuth Integration** - A complete OAuth2 flow for authenticating with HubSpot
2. **HubSpot Data Retrieval** - Fetching contact data from the HubSpot API

## Features Implemented

- Complete HubSpot OAuth flow including authorization, callback, and credential storage
- Secure management of OAuth state and tokens using Redis
- Frontend UI for initiating the OAuth connection
- Backend API for processing OAuth callbacks and retrieving data
- Data retrieval from HubSpot's Contacts API

## Tech Stack

### Frontend
- React.js
- Material UI for components
- Axios for API requests

### Backend
- Python FastAPI
- Redis for credential storage
- HTTPX for async HTTP requests

## How to Run

### Prerequisites
- Node.js and npm
- Python 3.8+
- Redis server

### Running the Backend
```bash
cd backend

# Install dependencies
pip install -r requirements.txt

# Start the FastAPI server
uvicorn main:app --reload
```

### Running the Frontend
```bash
cd frontend

# Install dependencies
npm i

# Start the React development server
npm run start
```

### Starting Redis
```bash
redis-server
```

## Implementation Details

### Part 1: HubSpot OAuth Integration

I've completed the HubSpot OAuth integration by implementing:

1. **Backend (Python/FastAPI)**:
   - `authorize_hubspot`: Generates authorization URL with proper scopes and state parameter
   - `oauth2callback_hubspot`: Handles OAuth callback and exchanges authorization code for access token
   - `get_hubspot_credentials`: Retrieves stored credentials from Redis

2. **Frontend (React/JavaScript)**:
   - Created HubSpot integration component with OAuth flow
   - Added UI for initiating the connection and displaying connection status
   - Integrated the component with the existing application

### Part 2: Loading HubSpot Items

I've implemented the `get_items_hubspot` function to:
- Take OAuth credentials and use them to authenticate with HubSpot's API
- Fetch contact data from HubSpot's CRM API
- Format the data as IntegrationItem objects
- Return the formatted data to be displayed in the UI

## Testing

The implementation can be tested by:
1. Entering user and organization details
2. Selecting "Hubspot" from the integration dropdown
3. Clicking "Connect to Hubspot" to initiate the OAuth flow
4. Once authenticated, clicking "Load Data" to retrieve contacts
