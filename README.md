# Youtube-Data-collection-using-API

YouTube Video Data Fetcher
This script allows you to search for YouTube videos based on a specific query, retrieve their comments, download and traslate the transcripts in English (if available), and save the data into an Excel file. The script is useful for analyzing YouTube content, comments, and video metadata.

Prerequisites
To use this script, you'll need to install the following Python libraries:

google-api-python-client – to interact with the YouTube Data API.
youtube-transcript-api – to fetch and download video transcripts.
pandas – to organize data and export it to an Excel file.
openpyxl – to handle Excel files.
re and os – for sanitizing filenames and handling directories.
datetime and timedelta – for managing date ranges.
You can install the required packages using:


How to Get a YouTube Data API Key

1. Go to Google Cloud Console.
2. Create a new project:
3. Click the project drop-down at the top, then select “New Project.”
4. Enter a project name and click “Create.”
4. Enable the YouTube Data API v3:
     In the left-hand menu, go to “APIs & Services” > “Library.”
     Search for “YouTube Data API v3” and click on it.
5. Click the “Enable” button.
6. Create API credentials:
7. Navigate to “APIs & Services” > “Credentials.”
8. Click “+ CREATE CREDENTIALS” and select “API key.”
9. Copy the generated API key to use in the script.

   
How the Script Works
YouTube Video Search:

The script allows you to search for videos on YouTube by a specific keyword. You can specify the number of results you want to retrieve and set a date filter to limit the videos based on when they were published.

Fetching Comments:

After retrieving the video details, the script fetches the latest comments for each video (up to a specified limit).
Downloading Transcripts:

For each video, the script attempts to download the transcript. If a transcript is not available, it returns an appropriate message. Transcripts in non-English languages are translated to English if possible.

Saving Data to Excel:

The script compiles the video metadata, comments, and transcript information into a pandas DataFrame. It then saves the data in an Excel file, which is named based on the search query.
Inputs

Search Term: The keyword for YouTube video search.
Number of Videos: The number of videos to retrieve.
Number of Comments: The number of comments to fetch for each video.
Years Back: The time frame for when videos should have been published.
Save Directory: The directory where the Excel file will be saved.


Output
The script generates an Excel file containing:

1. Video Title and Link.
2. Publication Date.
3. Comments (up to a specified number).
4. Transcript (if available).
