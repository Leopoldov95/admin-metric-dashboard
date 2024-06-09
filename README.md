# Employee Metrics Dashboard

## Project Overview

The Employee Metrics Dashboard is a web application designed to simplify the process of analyzing and visualizing employee performance data stored in Google Sheets. This application provides team leads with interactive tools to filter and display metrics such as time to complete work, accuracy, on-time completion vs. late tasks, and the number of tickets handled.

## Features

- **Interactive Data Visualization**: Use of D3.js to render charts and graphs for better data interpretation.
- **Date Range and Employee Selectors**: Filter data based on specific employees and date ranges.
- **Data Caching**: Improved performance by caching Google Sheets data in IndexedDB.
- **User Authentication**: Secure access through Google OAuth for whitelisted users only.

## Technology Stack

### Frontend

- **React**: Used for building the user interface and breaking down the application into reusable components.
- **Tailwind CSS**: Utilized for streamlined and responsive styling.
- **D3.js**: Implemented for creating dynamic and interactive data visualizations.

### Backend

- **Node.js**: Handles server-side logic and API endpoints.
- **Google Sheets API**: Fetches data from Google Sheets and converts it into JSON format.
- **Google OAuth**: Manages user authentication to ensure secure access to the application.

## Architecture

1. **Data Retrieval**: The backend fetches employee data from Google Sheets using the Google Sheets API.
2. **Data Conversion**: The retrieved data is converted into JSON format.
3. **Data Caching**: JSON data is cached in the browser using IndexedDB to improve performance.
4. **Frontend Display**: The frontend retrieves cached data, processes it, and uses D3.js to display charts and graphs.
5. **User Authentication**: Only whitelisted users can access the application via Google OAuth.

## Technical Challenges and Solutions

- **Slow API Calls**: To address the slow response times when querying Google Sheets, data is cached in the browser using IndexedDB. The cache is refreshed once a week to ensure data is up-to-date.
- **Non-Technical User Requirements**: Google Sheets was retained as the data source to allow non-technical team leads to easily edit and correct data without needing to migrate to a more complex database system.

## Impact

The implementation of this dashboard has significantly streamlined the process of analyzing employee performance metrics. Team leads are now able to:

- Save time during one-on-one meetings with their direct reports.
- Make more informed decisions regarding employee performance.
