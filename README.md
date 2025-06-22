# Recommender System

A content-based movie and TV show recommender system built with Python and Flask, using a real Netflix dataset. It allows users to get personalized recommendations based on selected titles and preferred languages.

## Features

- Content-based recommendations using genres, tags, actors, and ratings
- User can filter recommendations by languages
- IMDb ratings and images are displayed for recommendations
- Interactive web UI built using Flask and HTML templates

## Dataset

The system utilizes a Netflix dataset (`NetflixDataset.csv`) containing extensive metadata:
- Title
- Genre
- Tags
- Languages
- Country Availability
- Runtime
- Director
- Writer
- Actors
- Viewer Rating
- IMDb Score
- Awards, Box office, Release Dates, and more

## How it Works

1. **Data Preparation:**  
   - Reads and cleans Netflix metadata.
   - Handles missing values and duplicates.
   - Prepares textual features: genre, tags, actors, viewer rating.

2. **Feature Engineering:**  
   - Combines features into a "soup" for each title.
   - Uses `CountVectorizer` and cosine similarity to compute similarity scores.

3. **Recommendation:**  
   - Given a user's selected titles and language preferences, returns top recommendations sorted by IMDb score.
   - Recommendations can be explored in detail via a dedicated movie page.

## Project Structure

```
.
├── app.py                # Main Flask application
├── netflix.ipynb         # Data exploration and feature engineering notebook
├── NetflixDataset.csv    # Netflix dataset (required)
├── static/               # Static assets (CSS, images)
├── templates/            # HTML templates for Flask
├── README.md             # This file
```

## Install & Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/divyanshi116/Recommender-System.git
   cd Recommender-System
   ```

2. **Install dependencies:**
   ```bash
   pip install flask pandas scikit-learn matplotlib seaborn plotly
   ```

3. **Ensure the dataset file `NetflixDataset.csv` is in the root directory.**

4. **Run the Flask app:**
   ```bash
   python app.py
   ```
   The app will be available at `http://127.0.0.1:5000/`.

## Usage

- Open the homepage.
- Select titles and languages to get recommendations.
- Click on a recommended title for more details.

## Example Screenshots

_Add screenshots of the UI here if possible._

## Contributing

Contributions are welcome!  
- Fork the repo and submit a pull request.
- For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](LICENSE) © divyanshi116

---

_This project is for educational and demonstration purposes. Not affiliated with Netflix._
