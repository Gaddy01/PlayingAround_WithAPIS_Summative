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
- Python 3.x installed on your system
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
