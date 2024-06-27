Here's a detailed README for your HTML reader of JSON news:

---

# JSON News Reader

This project is an HTML-based news reader that fetches and displays news articles from a JSON file. It includes features for filtering news by country and language, and the ability to mark articles as favorites or bookmarks. Additionally, there is navigation to a separate page for viewing favorite articles.

## Features

- Fetch and display news articles from a JSON file.
- Filter news articles by country and language.
- Mark news articles as favorites or bookmarks.
- View a separate page for favorite articles.
- Persistent storage of favorites and bookmarks using local storage.

## Files

1. **index.html**: The main page that displays news articles and provides filtering options.
2. **favorites.html**: A separate page that displays only the favorite news articles.
3. **news.json**: The JSON file containing the news articles.

## Usage

### Step 1: Prepare the JSON File

Create a `news.json` file with the following structure:

```json
[
    {
        "_id": "1",
        "title": "News Title 1",
        "author": "Author 1",
        "published_date": "2024-06-27T00:00:00Z",
        "excerpt": "This is a brief excerpt of the news article 1.",
        "link": "http://example.com/news1",
        "country": "USA",
        "language": "English"
    },
    {
        "_id": "2",
        "title": "News Title 2",
        "author": "Author 2",
        "published_date": "2024-06-26T00:00:00Z",
        "excerpt": "This is a brief excerpt of the news article 2.",
        "link": "http://example.com/news2",
        "country": "Canada",
        "language": "French"
    }
]
```

### Step 2: Open the Main Page

Open `index.html` in a web browser. The page will automatically fetch and display the news articles from `news.json`.

### Step 3: Filter News Articles

Use the dropdown filters at the top of the page to filter news articles by country and language.

### Step 4: Mark Favorites and Bookmarks

Click the star icon (⭐) to mark an article as a favorite. Click the bookmark icon (🔖) to bookmark an article. These actions will be stored in the browser's local storage.

### Step 5: View Favorites

Click the "View Favorites" button to navigate to `favorites.html`, which displays only the articles marked as favorites.

## Code Overview

### index.html

This file contains the main page structure, including:

- Filters for country and language.
- News container to display articles.
- JavaScript functions to fetch data, populate filters, display news, and handle favorites and bookmarks.

### favorites.html

This file contains the structure for displaying favorite articles, including:

- A button to navigate back to the main page.
- JavaScript functions to fetch and display only the favorite articles.

### JavaScript Functions

- **fetchNews()**: Fetches news data from `news.json`.
- **populateFilters(newsData)**: Populates the country and language filters based on the news data.
- **filterNews(newsData)**: Filters news articles based on selected country and language.
- **displayNews(newsData)**: Displays news articles in the news container.
- **toggleFavorite(id, button)**: Toggles the favorite status of a news article.
- **toggleBookmark(id, button)**: Toggles the bookmark status of a news article.
- **isFavorite(id)**: Checks if a news article is marked as favorite.
- **isBookmarked(id)**: Checks if a news article is bookmarked.

## Local Storage

Favorites and bookmarks are stored in the browser's local storage, ensuring persistence across sessions. The keys used in local storage are:

- **favorites**: An array of favorite article IDs.
- **bookmarks**: An array of bookmarked article IDs.

## Styling

The project uses basic CSS for styling, including classes for news items, titles, filters, buttons, and more.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

Feel free to customize this README further based on your specific needs or additional features you may add.
