# Support — Polyrec Meeting Bot

Polyrec is an internal tool maintained by Polyanalitika.

## Getting Help
For issues or questions, contact the administrator:

**Email**: pymancer@gmail.com  
**Response time**: Within 2 business days

## Common Issues

**Bot does not join the meeting**  
Ensure the meeting URL includes the password parameter and that the meeting is hosted on the app owner's Zoom account.

**Transcript is missing or incomplete**  
Transcription runs after the meeting ends. Allow up to 5 minutes for processing. Check that the WhisperX service is running.

**Transcript not appearing in knowledge base**  
The pipeline polls every 60 seconds after the bot session ends. If the document does not appear after 5 minutes, check pipeline service logs.
