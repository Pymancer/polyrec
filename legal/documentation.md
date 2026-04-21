# Documentation — Polyrec Meeting Bot

Scribe automatically joins Zoom meetings, transcribes speech using a self-hosted AI model, and stores structured transcripts in a private knowledge base.

## Adding the App
Polyrec is an internal app and is not available for public installation. Access is granted by the Polyanalitika administrator.

## Starting a Recording

Send a POST request to the Attendee  
API to dispatch the bot to a meeting:

```
POST https://[attendee-url]/api/v1/bots
Authorization: Token [your-api-key]
Content-Type: application/json

{
  "meeting_url": "https://zoom.us/j/[meeting-id]?pwd=[password]",
  "bot_name": "Polyrec",
  "transcription_settings": {"custom_async": {}}
}
```

The bot will appear in the participants list within ~10 seconds.

## Monitoring Status

```
GET https://[attendee-url]/api/v1/bots/[bot-id]
Authorization: Token [your-api-key]
```

States: `joining` → `joined_recording` → `post_processing` → `ended`

## Viewing Transcripts
Once the bot status is `ended`, the transcript is automatically uploaded to the Open WebUI knowledge base at the configured URL under the **meetings** collection.

## Removing the App
To remove Scribe from your Zoom account, contact the administrator. No Zoom user data is retained after removal.

## Contact
pymancer@gmail.com
