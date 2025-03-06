# Music Controller

A **Django-based music controller** that integrates with the **Spotify API** to enable shared music playback in a collaborative environment. Users can create and join rooms, control playback, and vote to skip tracks.

## Features
- **Spotify API Integration**: Control music playback directly via Spotify.
- **OAuth Authentication**: Secure user login and access control.
- **Room-based Music Control**: Users can create or join rooms to share music.
- **Play/Pause/Skip Functionality**: Hosts and authorized guests can manage playback.
- **Voting System for Track Skipping**: Users can vote to skip a song if enough votes are collected.
- **Real-time Song Synchronization**: Ensures all users in a room see the same currently playing song.

## Tech Stack
- **Backend**: Django, Django REST Framework
- **Authentication**: OAuth 2.0 (Spotify API)
- **Frontend**: React (if applicable)
- **Database**: SQLite/PostgreSQL (as needed)
- **API Requests**: Requests Library

## Setup Instructions

### Prerequisites
- Python 3.x
- Django
- Spotify Developer Account

### Installation
1. **Clone the repository:**
   ```sh
   git clone https://github.com/your-username/music_controller.git
   cd music_controller
   ```

2. **Create a virtual environment:**
   ```sh
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

4. **Set up environment variables:**
   Create a `.env` file and add the following:
   ```
   CLIENT_ID='your_spotify_client_id'
   CLIENT_SECRET='your_spotify_client_secret'
   REDIRECT_URI='your_redirect_uri'
   ```

5. **Run migrations:**
   ```sh
   python manage.py migrate
   ```

6. **Start the Django server:**
   ```sh
   python manage.py runserver
   ```

## Usage
- **Obtain Spotify authentication** by navigating to `/spotify/get-auth-url/`.
- **Create or join a room** via the frontend (if applicable) or API.
- **Control music playback** using play, pause, and skip options.
- **Vote to skip a song** when in a shared room.

## API Endpoints
| Endpoint | Method | Description |
|----------|--------|-------------|
| `/spotify/get-auth-url/` | GET | Get Spotify authentication URL |
| `/spotify/callback/` | GET | Handle Spotify OAuth callback |
| `/spotify/is-authenticated/` | GET | Check if user is authenticated |
| `/spotify/current-song/` | GET | Get currently playing song |
| `/spotify/pause/` | PUT | Pause playback |
| `/spotify/play/` | PUT | Resume playback |
| `/spotify/skip/` | POST | Vote to skip the current song |

## Contributing
Feel free to submit issues and pull requests to improve the project.

## License
This project is licensed under the MIT License.

## Author
Smriti Chapra
