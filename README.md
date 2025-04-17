# Social Media Trend Analyzer

## Description

The Social Media Trend Analyzer is a web application that analyzes the sentiment and trend score of social media posts. It utilizes an API (which can be powered by OpenAI or a dummy analyzer) to analyze multiple posts and display the results in real-time. Users can input a list of social media posts, and the app will return the sentiment (Positive, Negative, Neutral) and a trend score (a value between 0 and 1).

## Features

- **Sentiment Analysis**: The application analyzes the sentiment of the posts and categorizes them as Positive, Negative, or Neutral.
- **Trend Score**: Each post is assigned a trend score that represents its popularity or impact.
- **Multiple Posts**: Users can input multiple posts and analyze them in one go.
- **Responsive UI**: The web interface is simple and easy to use.

## Prerequisites

- Python 3.x
- Flask
- Flask-CORS
- OpenAI API key (if you plan to use OpenAI for analysis)

## Installation

### Backend Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/aman-205/assignment.git
   ```

2. Install dependencies: Make sure you have `pip` installed and then run:
```bash
pip install -r requirements.txt
```

3. Set up your OpenAI API key (if using OpenAI for analysis):

* OpenAI API key is required for deeper analysis. You can get an API key from OpenAI.

* Replace the placeholder YOUR_OPENAI_API_KEY in the backend code with your actual key:

```bash
openai.api_key = "YOUR_OPENAI_API_KEY"
```

4. Run the Flask app:

```bash
python server.py
```

## Frontend Setup

1. Open the HTML file in your browser:

* Open index.html in any web browser (Chrome, Firefox, etc.).

* You should see the input box where you can type or paste your social media posts.

2. Frontend Dependencies:

* The HTML uses script.js for client-side logic and styles.css for styling. Ensure these files are in the same directory as the HTML file.

## How It Works
1. Enter Posts: In the web interface, input your social media posts into the textarea, with each post on a new line.

2. Analyze: Click on the Analyze button to send the posts to the backend for analysis. The backend processes the posts and returns the sentiment and trend score for each post.

3. View Results: The results will be displayed on the same page, showing the sentiment (Positive, Negative, or Neutral) and the trend score (a float value between 0 and 1) for each post.

## Example Request
Here’s an example of how a request might look when sending a list of posts to the backend API:
```typescript
{
    "posts": [
        "I love this product! It's amazing.",
        "Worst purchase I've ever made. Waste of money.",
        "This is a decent product. Could be better."
    ]
}
```
* The response will look like:

```typescript
[
    {
        "text": "I love this product! It's amazing.",
        "sentiment": "Positive",
        "trend_score": 0.92
    },
    {
        "text": "Worst purchase I've ever made. Waste of money.",
        "sentiment": "Negative",
        "trend_score": 0.45
    },
    {
        "text": "This is a decent product. Could be better.",
        "sentiment": "Neutral",
        "trend_score": 0.68
    }
]
```

## Contributing
Feel free to fork this project, submit issues, or send pull requests. Contributions are welcome!

# License
This project is licensed under the MIT License.
