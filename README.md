# FilmFlix

A Flask-based movie recommendation system that suggests films matching the user's taste — either by selecting a preferred genre and release year, or by entering a previously watched movie to receive content-similar recommendations.

## Overview

- Genre + year-based filtering for casual discovery.
- Content-based filtering (cosine similarity on movie features) for personalised recommendations from a watched title.
- Clean web UI served by Flask + Bootstrap.

## Features

- Genre-and-year movie discovery
- Content-based "similar to" recommendations
- Bootstrap-styled responsive UI
- Pre-trained similarity model bundled in `Model/`

## Tech Stack

- **Backend:** Python, Flask
- **ML:** scikit-learn, pandas (content-based filtering — see `Content Based Filtering.ipynb`)
- **Frontend:** HTML, CSS, Bootstrap

## Project Structure

```
FilmFlix/
├── app.py                          # Flask app entry point
├── Content Based Filtering.ipynb   # Model training notebook
├── Model/                          # Serialized similarity matrix + movie data
├── dataset/                        # Source movie dataset
├── templates/                      # Jinja2 HTML templates
└── Images/                         # Screenshots
```

## Setup

```bash
git clone https://github.com/WorkRabdeepSinghKharbanda/FilmFlix.git
cd FilmFlix
pip install flask pandas scikit-learn numpy
python app.py
```

Open `http://127.0.0.1:5000/`.

## Screenshots

| Home |
|------|
| ![](Images/img1.png) |

### Recommend by Genre + Year
| Form | Result |
|------|--------|
| ![](Images/im1.png) | ![](Images/img3.png) |

### Recommend by Previously Watched Movie
| Form | Result |
|------|--------|
| ![](Images/im2.png) | ![](Images/img5.png) |

## License

MIT
