BeatNik Application
Overview
BeatNik is a web-based music library application designed to provide users with a seamless experience for managing and enjoying their favorite songs. The application features user authentication, audio playback, and a dynamic interface that displays available tracks. Users can easily navigate through their music collection, play songs, and manage their playlists.

Table of Contents
         Features
         Technologies Used
         File Structure
         Usage
         Contributing
         License
         Acknowledgments
         
Features

User Authentication
Users can create an account and log in securely. Passwords are hashed for security using PHP's password_hash() function.
The login form provides feedback for successful or failed login attempts.

Music Playback
Users can play, pause, and skip tracks in their music library. The application uses the HTML5 Audio API for audio playback.
The current song's playback time is displayed, along with the total duration.

Dynamic Song Listing
The application fetches a list of songs from a server, displaying them in an organized manner. Users can click on a song to play it.
Songs are displayed with their titles and artist names, making it easy for users to browse their library.

Playlist Management
Users can create, edit, and delete playlists to organize their favorite songs. This feature allows users to group songs by mood, genre, or any other criteria.
Each playlist can contain multiple songs, and users can easily switch between playlists.

Search Functionality
Users can search for specific songs or artists within the music library, making it easy to find their favorite tracks quickly.
The search bar filters the displayed songs in real-time based on user input.

Audio Progress Indicator
The application provides a visual progress bar that indicates the current playback time of the song and allows users to seek to different parts of the track.
Users can click on the progress bar to jump to a specific point in the song.

Volume Control
Users can adjust the volume of the audio playback directly from the application interface using a volume slider.
The volume level is visually represented, allowing users to see their current volume setting.

Previous and Next Track Navigation
Users can easily navigate to the previous or next song in their playlist using dedicated buttons.
This feature enhances the music listening experience by allowing users to quickly switch tracks.

User Profiles
Each user has a profile that displays their username and allows them to manage their playlists and preferences.
Users can view their recently played songs and favorite tracks.

Error Handling and User Feedback
The application includes error messages and alerts to inform users of successful actions or issues, improving usability.
Users receive feedback when actions are completed, such as successfully adding a song to a playlist.

Technologies Used
Frontend:
HTML: For structuring the web pages.
CSS: For styling the application and ensuring a responsive design.
JavaScript: For implementing interactivity and dynamic content loading.
Backend:

PHP: For handling server-side logic, user authentication, and database interactions.
Database:

MySQL: For storing user data, song information, and playlists.
Audio Playback:

HTML5 Audio API: For playing audio files and managing playback controls.
Icons:

Font Awesome: For providing icons used throughout the application.




File Structure

/beatnik
│
├── LOGIN_BEATNIK.php        # PHP script for user login
├── SIGNUP_BEATNIK.php       # PHP script for user signup
├── login.php                 # PHP script to handle login requests
├── signup.php                # PHP script to handle signup requests
├── playlists.php             # PHP script for managing playlists
├── LOGIN_BEATNIK.css        # CSS styles for the login page
├── LOGIN_BEATNIK.js         # JavaScript for handling login functionality
├── SIGNUP_BEATNIK.js        # JavaScript for handling signup functionality
├── PLAYLISTS.js             # JavaScript for managing playlists
├── BEATNIK.js               # JavaScript for handling main application functionality
├── script.js                 # Additional JavaScript for music player controls
├── assects/                  # Directory for assets (images, videos)
│   ├── background beatnik.mp4 │   └── Assets/
│
└── index.html               # Main HTML file to load the application


Created a MySQL database named beatnik.
Run the following SQL commands to create the necessary tables:
sql

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    password VARCHAR(255) NOT NULL
);

CREATE TABLE songs (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(100) NOT NULL,
    artist VARCHAR(100) NOT NULL,
    file_path VARCHAR(255) NOT NULL
);

CREATE TABLE playlists (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT NOT NULL,
    name VARCHAR(100) NOT NULL,
    FOREIGN KEY (user_id) REFERENCES users(id)
);

CREATE TABLE playlist_songs (
    playlist_id INT NOT NULL,
    song_id INT NOT NULL,
    FOREIGN KEY (playlist_id) REFERENCES playlists(id),
    FOREIGN KEY (song_id) REFERENCES songs(id)
);


Configure Database Connection:

Update the database connection settings in your PHP files to match your local database configuration.
Run the Application:

Open index.html in your web browser to start using the BeatNik application.
Usage
Creating an Account:

Navigate to the signup page and fill in the required fields to create a new account.
Logging In:

Use your credentials to log in to the application.
Managing Playlists:

After logging in, you can create new playlists, add songs to them, and manage existing playlists.
Playing Music:

Browse the music library, select a song to play, and use the playback controls to manage your listening experience.
Searching for Songs:

Use the search bar to quickly find specific songs or artists in your library.
Contributing
Contributions are welcome! If you would like to contribute to the BeatNik application, please follow these steps:


Acknowledgments
Special thanks to the contributors and the open-source community for their support and resources that made this project possible.





# beatnik-music-player
![Screenshot 2024-11-29 160145](https://github.com/user-attachments/assets/aae01160-08b8-4f06-8e2f-4197c57b90cf)
![Screenshot 2024-11-29 161642](https://github.com/user-attachments/assets/4b3c588e-a431-464f-b4c1-67b3fa3d3ef4)
![Screenshot 2024-11-29 161656](https://github.com/user-attachments/assets/2dc579ff-439a-49e7-b023-4998ae58a764)
![Screenshot 2024-11-29 161707](https://github.com/user-attachments/assets/edf69154-86a5-4cb3-a8e0-fdc50aa3938f)
![Screenshot 2024-11-29 161724](https://github.com/user-attachments/assets/1527d8c2-24e2-435c-b9f3-2be7b09d2270)
![Screenshot 2024-11-29 161741](https://github.com/user-attachments/assets/627244f6-ecba-4c46-a06f-c859b3a08672)
![Screenshot 2024-11-29 161756](https://github.com/user-attachments/assets/3cfeabd9-1371-4f3b-9f86-b19adf4d3604)
![Screenshot 2024-11-29 161809](https://github.com/user-attachments/assets/765c4d3d-2e13-4b32-9c8f-278c823c7d16)
![Screenshot 2024-11-29 184330](https://github.com/user-attachments/assets/dfd5d8e1-c587-4aa8-9e0e-6eb2c58f0326)
![Screenshot 2024-11-29 155841](https://github.com/user-attachments/assets/9db92648-be5d-4e53-8734-43431d1f7d17)
![Screenshot 2024-11-29 160034](https://github.com/user-attachments/assets/dead4a49-b754-4561-83a0-692530c8aed0)
![Screenshot 2024-11-29 160104](https://github.com/user-attachments/assets/d02aa622-8024-49d4-b78d-cccd1f2412da)
![Screenshot 2024-11-29 160127](https://github.com/user-attachments/assets/9cbe3c71-6883-471d-8536-2447ac28c7e1)


![Screenshot 2024-11-29 160204](https://github.com/user-attachments/assets/991dffc8-5ab8-4e04-83a8-5c482f4ecf80)
![Screenshot 2024-11-29 160238](https://github.com/user-attachments/assets/1cc54e4f-b696-4014-8f58-739275ceffa1)
![Screenshot 2024-11-29 160311](https://github.com/user-attachments/assets/dc2e0dea-2627-4c0e-ae61-2d597d7bb31b)
![Screenshot 2024-11-29 160342](https://github.com/user-attachments/assets/4eefb0aa-26c1-443c-88b9-e3f2728d42d3)
![Screenshot 2024-11-29 160402](https://github.com/user-attachments/assets/d28f6e49-bc13-49d4-b1c0-378d7f6b7326)
![Screenshot 2024-11-29 160418](https://github.com/user-attachments/assets/867db2c1-8362-4740-94d9-9a79f44c54c2)











