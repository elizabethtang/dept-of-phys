
# Video/Audio Transcriber

OpenAI Whisper-based project to transcribe audio and video files using React & Django

## Installation

You need the latest versions of pipenv and node to setup this project.

- First clone the repository `git clone https://github.com/elizabethtang/dept-of-phys` and navigate to the project's folder
`cd transcribe-video-audio`
- Install the dependencies of both the client and server.
- Run both the client and server separately
- Go to http//localhost:3000 to upload and transcribe your media files.


1- To install the server's dependencies, in the terminal run the following:

```bash
  cd api
  pipenv install
  pipenv shell 
  pipenv run python manage.py makemigrations
  pipenv run python manage.py migrate
  pipenv run server
```
- Navigate to navigate to http://localhost:8000 to check if the server was setup successfully.

2- To run the client, execute the following commands:

```bash
  cd client
  yarn install
  touch .env.local
  yarn dev
```


Adjust these if your going to deploy to any remote server.

- Navigate to http://localhost:3000/ to see if the client is working and the file upload section is visible.
- Since this project uses websockets to send realtime-messages between the client and server, you need to see if the console of the client is showing connected, which means both client and server can exchange messages.


3- Select a video or audio file to upload The transcripts will be extracted and displayed on the page.

4- You can also view all your uploaded video and audio files and see their transcriptions. 
- Note that this project only allows MP4, and MP3 format files. 
- Additional Notes Make sure ffmpeg is installed on your machine and available on your system's PATH
