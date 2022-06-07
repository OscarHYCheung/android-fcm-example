# Example of Firebase Cloud Messaging Android App

- Assumed all notifications will be sent with data
- Add your own google-service.json, use package ID 'com.example.notificationtest', or change it to
  match

## Testing

Go to https://developers.google.com/oauthplayground/, authorise and POST to
endpoint `https://fcm.googleapis.com/v1/projects/<project_id>/messages:send` with below body:

```json
{
  "message": {
    "token": "<device_token>",
    "data": {
      "title": "<title>",
      "content": "<message_content>",
      "notificationId": "<unique_notification_id>"
    }
  }
}
```
