# A Pip Package to Enwrap YouTube Data API and YouTube Transcript API

## A simple youtube api wrapper for getting video details and transcripts.

1. Introduction
The YouTube Wrapper package is a Python library that simplifies interactions with the YouTube Data API and the YouTube Transcript API. It allows developers to easily retrieve video details and transcripts using simple function calls.

2. Installation
You can install the package directly from PyPI:

bash
Copy code
pip install youtube-wrapper-nav
3. Getting Started
To start using the package, you need to have a YouTube Data API key. If you don't have one, you can create it by following these steps:

Go to the Google Cloud Console.
Create a new project or select an existing one.
Navigate to APIs & Services > Credentials.
Click on Create Credentials and select API key.
4. Usage
4.1 Initializing the Wrapper

To use the YouTubeWrapper, import it and create an instance with your API key:

python
Copy code
from youtube_wrapper import YouTubeWrapper

api_key = 'YOUR_API_KEY'
youtube = YouTubeWrapper(api_key)
4.2 Retrieving Video Details

You can retrieve details of a specific video using its video ID:

python
Copy code
video_id = 'pgTF5MFG7tk'
video_details = youtube.data_api.get_video_details(video_id)
print(video_details)
4.3 Fetching Video Transcripts

To fetch the transcript of a video:

python
Copy code
transcript = youtube.transcript_api.get_transcript(video_id)
print(transcript)
5. Examples
Here’s a complete example to fetch and display the title and transcript of a video:

python
Copy code
from youtube_wrapper import YouTubeWrapper

api_key = 'YOUR_API_KEY'
youtube = YouTubeWrapper(api_key)

video_id = 'pgTF5MFG7tk'

# Get video details
video_details = youtube.data_api.get_video_details(video_id)
print(f"Title: {video_details['title']}")

# Get transcript
transcript = youtube.transcript_api.get_transcript(video_id)
print(f"Transcript: {transcript}")
6. Contributing
Contributions are welcome! Please follow these steps to contribute:

Fork the repository on GitHub.
Create a new branch for your feature or bug fix.
Implement your changes and commit them with a descriptive message.
Push your branch to your forked repository.
Create a pull request to the main repository.
7. License
This project is licensed under the MIT License - see the LICENSE file for details.
