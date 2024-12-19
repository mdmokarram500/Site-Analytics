# Site Analytics - README

## Overview
Site Analytics is a robust platform designed to provide insights into website performance, user interactions, and tracking capabilities. With the ability to monitor multiple websites, administrators can generate custom JavaScript tracking codes to embed in external sites, collecting data to analyze user activity and performance metrics. This functionality mirrors features offered by Google Analytics.

---

## Features
1. **Website Management:**
   - Add, update, and remove websites for tracking.
   - Maintain a record of website details such as name and URL.

2. **Custom Tracking Code:**
   - Generate unique JavaScript tracking scripts for each website.
   - Embed scripts into external sites to monitor user interactions and activities.

3. **Data Insights:**
   - Collect data on user visits, page views, and interactions.
   - View analytics and insights for decision-making.

4. **Secure Authentication:**
   - User sessions are secured to ensure only authorized access.

---

## Technology Stack
- **Backend:** PHP (MVC Architecture)
- **Frontend:** HTML, CSS, JavaScript
- **Database:** MySQL
- **Tracking Script:** JavaScript

---

## Installation Guide

### Prerequisites
- PHP 7.4+
- MySQL Database
- Web Server (e.g., Apache, Nginx)

### Steps
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-repository/site-analytics.git
   ```

2. **Set Up the Database:**
   - Import the SQL schema provided in `database/schema.sql` into your MySQL server.
   - Update `config/database.php` with your database credentials.

3. **Configure the Application:**
   - Set up the `BASE_URL` in `config/config.php` to match your server environment.

4. **Run the Application:**
   - Start your web server and navigate to the application URL.

5. **Embed Tracking Script:**
   - Generate a tracking script from the admin panel and embed it into the `<head>` section of the target website.

---

## Database Schema
### Table: `websites`
| Column         | Type         | Description                          |
|----------------|--------------|--------------------------------------|
| `website_id`   | INT (Primary)| Unique identifier for each website. |
| `user_id`      | INT          | ID of the admin user.               |
| `website_name` | VARCHAR(255) | Name of the website.                |
| `website_url`  | VARCHAR(255) | URL of the website.                 |
| `created_at`   | TIMESTAMP    | Timestamp when the record was created. |
| `updated_at`   | TIMESTAMP    | Timestamp when the record was last updated. |

---

## Usage
1. **Log In:**
   - Use your administrator credentials to log in.
2. **Add Website:**
   - Navigate to the "Add Website" section and provide the website details.
3. **Generate Tracking Code:**
   - After adding a website, generate a unique JavaScript code.
4. **Embed Code:**
   - Copy the generated code and embed it into the `<head>` section of the target website.
5. **View Analytics:**
   - Access the dashboard to monitor performance and insights.

---

## Custom JavaScript Tracking Script
```javascript
(function() {
    var siteAnalytics = siteAnalytics || [];
    siteAnalytics.push({
        websiteId: 'your_website_id',
        timestamp: new Date().toISOString()
    });

    var script = document.createElement('script');
    script.src = 'https://your-domain.com/tracking.js';
    script.async = true;
    document.head.appendChild(script);
})();
```

---

## Contribution
Contributions are welcome! Please follow the steps below:
1. Fork the repository.
2. Create a new branch (`feature/your-feature`).
3. Commit your changes and push them to your fork.
4. Open a pull request.

---

## License
This project is licensed under the [MIT License](LICENSE).

---

## Contact
For any queries or support, reach out to:
- Email: support@siteanalytics.com
- Website: [www.siteanalytics.com](https://www.siteanalytics.com)

