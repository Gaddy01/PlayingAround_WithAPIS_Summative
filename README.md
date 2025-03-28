## Web-infrastructure Summative: Playing around with APIs

# BOOKSTORE - Online Book Browser

## Introduction
BOOKSTORE is an online platform that allows users to browse books from the Amazon library. It helps users retrieve books based on:
- ISBN number
- Author name
- Book title
- Publisher name

The platform provides the following details for each book:
- International Standard Book Number (ISBN)
- Title
- Author
- Publication year
- Cover page image link

## Features
- Search books by ISBN, author name, title, or publisher.
- Display detailed information for each book.
- Fast and efficient book data retrieval from Amazon's book database.

## APIs Used
This project leverages the **Amazon Books Data API** to fetch book information. You can find the official documentation here: [Amazon Books Data API](https://rapidapi.com/AssadAzeem/api/amazon-books-data-api1).

### API Endpoints
- Retrieve book by ISBN: `/api/book_isbn`
- Retrieve books by author name: `/api/book_author`
- Retrieve books by title: `/api/book_title`
- Retrieve books by publisher: `/api/book_publisher`

## Prerequisites
- Internet browser
- An API key from [RapidAPI](https://rapidapi.com/AssadAzeem/api/amazon-books-data-api1)
- Internet connection

## Project Structure
```
.
├── index.html                  # Main html script to run the application
├── style.css                   # The file file contain css styles
├── Images                      # The folder contaings images
      └── bookstore_logo.jpg 
├── .gitignore                  # Excludes sensitive data and unnecessary files
└── README.md                   # Project documentation
```

## Video demo link (google drive)
https://drive.google.com/file/d/1P8XNwk172BWMBTgpuAeJBSCFPJC6wKM9/view

## Setup Instructions
### Step 1: Clone the Repository
```
git clone https://github.com/Gaddy01/PlayingAround_WithAPIS_Summative.git
```

### Step 2: Install Dependencies
No external libraries are required, as the project runs in the browser.

### Step 3: Run the Application: run in the browser the index.html file

## Deployment
#### 1. The application was deployed on my Ubuntu web server (web01, web02) as follows:  
1.1. Connect to the server via SSH:
   ```
   ssh ubuntu@100.27.27.252
   ssh ubuntu@18.208.133.92
   ```
1.2. In each server navigate to /var/www/html
   ```
   cd /var/www/html
   ```
1.3. Clone the repository on the server:
   ```
   git clone https://github.com/Gaddy01/PlayingAround_WithAPIS_Summative.git
   ```
1.4. Copy the content of the index file in index.nginx-debian.html:
   ```
   sudo cat PlayingAround_WithAPIS_Summative/index.html > index.nginx-debian.html
   ```
1.5. Adjust the index.nginx-debian.html file content to meet the actual folder/files locations

## Run the deployed app
### To run the app on my servers (web01 and we02) search in your browser: 
   ```
   www.gaddiel.tech
   ```
## Challenges and Solutions
### 1. API Response Delays and Timeouts
- **Challenge:** Sometimes, when making requests to the API, the response times were slower than expected, or there were occasional timeouts. This delay caused issues in maintaining a smooth user experience, especially if the user had to wait for a long time before seeing the results.
- **Solution:** To tackle API response delays, we implemented timeout handling mechanisms, ensuring the app didn’t hang indefinitely. Additionally, using asynchronous JavaScript (async/await), we improved the overall responsiveness of the app and allowed users to continue interacting with the page while waiting for the data.

### 2. Pagination Handling
- **Challenge:** The API returns a large number of results that need to be split across multiple pages. Implementing pagination to allow users to view books on subsequent pages was tricky, especially when dealing with dynamic page numbers.
- **Solution:** To handle the pagination feature, we implemented dynamic pagination buttons. These buttons would automatically adjust based on the totalPages value returned by the API. If there were more than one page of books, users could easily navigate to the next set of books without refreshing the page.

## Credits
- API developed and provided by [RapidAPI](https://rapidapi.com/)
- Special thanks to the developers of the **Amazon Books Data API**

## Author
Developed by Gaddiel Irakoze
