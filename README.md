# Physicians Business URL Status Check and 404 Link Identification

## Project Overview

This project involves building a scalable crawler to verify the status of Physicians' business URLs. The crawler sends requests to each unique business URL and captures the response status code, including all possible HTTP response codes such as:
- **200 (OK)**
- **301/302 (Redirect)**
- **400 (Bad Request)**
- **401 (Unauthorized)**
- **403 (Forbidden)**
- **404 (Not Found)**
- **500 (Internal Server Error)**
- And others.

Additionally, the script handles redirects and captures the redirected URL where applicable, allowing us to check the current availability, accessibility, and behavior of these URLs.

The project involved crawling approximately **2.6 million unique business URLs**, showcasing our ability to provide a **scalable solution** capable of handling large volumes of data efficiently.

## Data Fields
The following fields are included in the output:
- **npi**: Unique NPI number associated with each physician.
- **keyword**: Search keyword linked to the business URL.
- **business_url**: The actual business URL for each physician.
- **domain**: The domain extracted from the business URL.
- **status_code**: Response status code (e.g., 200, 301, 302, 400, 401, 403, 404, 500).
- **redirected_link**: URL to which the request is redirected, if applicable.

## Deliverables

1. **URL Status Code Report**
   - A detailed report capturing the status code for each unique business URL.
   - Columns included: **npi**, **keyword**, **business_url**, **domain**, **status_code**, and **redirected_link**.

2. **Summary Report**
   - A summary report that provides a breakdown of the status codes with counts and percentages.
   - Example format:
     - **status**: HTTP status code (e.g., 200, 401).
     - **count**: The number of occurrences of each status code.
     - **percentage**: The percentage of each status code relative to the total.

   **Example**:
   - 200, 79508, 40.0165%
   - 401, 33, 0.0166%

## Acceptance Criteria
- The script should request each unique business URL and capture the correct status code.
- The summary report must include status code, count, and percentage of each status.
- Both the detailed and summary reports should be formatted in a **CSV file** for easy client review.

## Additional Notes
- Implement retry logic in case of temporary connection issues with the URLs.
- Handle redirects to capture the **redirected_link** correctly.
- Coordinate with the client on any additional columns or requirements during the report generation.

## Usage
This solution can be used to:
- Scan all pages and internal links to ensure there are no 404 Not Found errors, **helping to prevent Google Search Console from flagging 404 and internal dead links** .
- Identify the availability and status of business URLs.
- Detect broken links (e.g., **404 Not Found**).
- Provide a summary analysis of the URL statuses to monitor website health and accessibility.

This project is ideal for businesses looking to maintain up-to-date information on large numbers of business URLs and ensure that their online presence is accessible and error-free.

