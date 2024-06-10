Initial Flow of the project:
![[flow.jpg]]

I initially worked on this project where i used a command line tool called yt-dlp (a fork of youtube-dlp) to download the best video+audio then extract the audio. The extracted audio is then uploaded to an automatic speech recognition model called whisper which transcribes the text and then detect the language where if it is other than English then it is translated to English. The transcribed text is the divided into chunks of text which is sent to Google's Gemini pro 1.5 model through developer API. The model transforms the chunks of text into beautiful markdown notes one by one and then the whole markdown notes is again divided and overlapping notes are corrected. 


The three problems were hitting Gemini API rate limit, Whisper audio limit and Fixing the overlapping or Unnecessarily directed context of the notes.

