# Flipkart Product Review Scraper

This is a web application built using Flask, Python, and BeautifulSoup to scrape and display product reviews from Flipkart. It allows users to search for a product and retrieve customer reviews along with relevant details such as customer name, rating, heading, and comment.

## How to Use

1. Install the required dependencies by running the following command:

   ```
   pip install Flask flask_cors requests beautifulsoup4
   ```

2. Run the Flask application by executing the following command:

   ```
   python app.py
   ```

   This will start the Flask server.

3. Open a web browser and visit [http://localhost:5000](http://localhost:5000) to access the home page of the application.

4. On the home page, enter the product name in the search box and click the **Search** button.

5. The application will scrape the Flipkart website for reviews related to the entered product.

6. The results page will display the product reviews along with customer names, ratings, headings, and comments.

7. You can view multiple pages of reviews by clicking the **Next** button.

## Code Overview

The application consists of the following main components:

- **Flask**: Flask is a web framework for Python. It is used to handle HTTP requests and responses, render HTML templates, and serve the application.

- **BeautifulSoup**: BeautifulSoup is a library for parsing HTML and XML documents. It is used to extract data from the Flipkart website by searching for specific HTML elements and their attributes.

- **Requests**: The Requests library is used to send HTTP requests to the Flipkart website and retrieve the HTML content of the product pages.

- **index.html**: This is the home page template where users can enter the product name to search for reviews.

- **results.html**: This template is used to display the scraped reviews in a tabular format.

- **app.py**: This is the main Flask application file that defines the routes and implements the scraping logic.

The application follows the following workflow:

1. The user enters a product name on the home page and submits the search form.

2. The Flask route `/review` is triggered, and the entered product name is extracted from the form data.

3. The application constructs a URL for the Flipkart search page with the entered product name.

4. The application sends an HTTP request to the Flipkart search page, retrieves the HTML content, and parses it using BeautifulSoup.

5. The relevant review data is extracted from the HTML using BeautifulSoup, and a list of dictionaries containing the review details is created.

6. The application renders the `results.html` template, passing the list of review dictionaries as a parameter.

7. The `results.html` template displays the reviews in a table format, with each row representing a review and its associated details.

## Note

- This application scrapes data from the Flipkart website, which may be subjected to their terms and conditions. Make sure to use it responsibly and for personal use only.

- The application may require modifications if there are changes in the HTML structure or class names on the Flipkart website.

---

Feel free to explore and modify the code to suit your requirements or add additional features to the application.
