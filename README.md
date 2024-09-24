# Reddit Recommendation System

This repository contains the implementation of a **Reddit Recommendation System** that suggests relevant subreddits to users based on their interests and activity. The project focuses on creating a content-based or collaborative filtering recommendation engine using Reddit data to improve the user experience by suggesting subreddits tailored to user preferences.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Overview

The Reddit Recommendation System aims to recommend subreddits to users based on their interaction history or interests. The system uses a combination of **NLP** (Natural Language Processing), **content-based filtering**, and **collaborative filtering** techniques to deliver personalized subreddit suggestions.

This project processes data from Reddit to create a recommendation engine that learns from user behavior and subreddit content. It leverages text data and user activity patterns to generate meaningful recommendations.

## Features

- **User-based Recommendations**: Recommends subreddits based on the user's interaction history.
- **Content-based Recommendations**: Analyzes the textual content of posts to recommend subreddits with similar content.
- **Collaborative Filtering**: Utilizes user behavior patterns to suggest subreddits that similar users engage with.
- **NLP for Subreddit Analysis**: Processes post content to extract key themes and match users with relevant subreddits.

## Installation

### Prerequisites

- Python 3.x
- Numpy (`numpy`)
- Pandas (`pandas`)
- Scikit-learn (`scikit-learn`)
- Natural Language Toolkit (`nltk`)
- Reddit API (via PRAW)

### Steps

1. Clone the repository:

    ```bash
    git clone https://github.com/simarmehta/RedditRecSys.git
    cd RedditRecSys
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

    *(Note: If `requirements.txt` is missing, manually install the dependencies: `pip install numpy pandas scikit-learn nltk praw`)*

3. Set up the Reddit API credentials by registering your application on [Reddit's API page](https://www.reddit.com/prefs/apps). Add your credentials to the configuration file.

## Usage

1. Run the script to collect Reddit data and generate recommendations:

    ```bash
    python reddit_rec_sys.py
    ```

2. Input a user's Reddit interaction history or specify keywords/interests to get subreddit recommendations.

3. The system will output a list of recommended subreddits based on the specified preferences.

## How It Works

1. **Data Collection**: The system fetches data from Reddit's API using the **PRAW (Python Reddit API Wrapper)** library. This data includes subreddit posts, user activity, and subreddit metadata.
   
2. **Text Processing & NLP**: The textual content of posts is processed using NLP techniques, including tokenization, stop-word removal, and TF-IDF vectorization. This helps in identifying the key themes and topics of each subreddit.

3. **Recommendation Engine**:
    - **Content-based Filtering**: Recommends subreddits based on the similarity of post content to the user's interests.
    - **Collaborative Filtering**: Leverages the behavior of similar users to recommend subreddits that they are active in.
   
4. **Model Training**: The recommendation models are trained using either user-based collaborative filtering or content-based methods to predict relevant subreddits for a given user or set of interests.

### Key Techniques and Libraries:
- **TF-IDF Vectorization**: Converts textual data into feature vectors.
- **Cosine Similarity**: Measures similarity between different subreddit content.
- **Collaborative Filtering**: Suggests subreddits based on user behavior patterns.
- **PRAW**: A Python wrapper for the Reddit API, used for fetching data.

## Project Structure

```bash
RedditRecSys/
├── data/                 # Raw and processed Reddit data
├── reddit_rec_sys.py     # Main script for running the recommendation system
├── utils/                # Helper functions (data processing, NLP)
├── models/               # Pre-trained models or trained recommendation models
├── requirements.txt      # Required Python libraries
└── README.md             # Documentation
