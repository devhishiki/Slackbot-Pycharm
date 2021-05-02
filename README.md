## run local
command
```
pip install -r requirements.txt
export FLASK_RUN_PORT=8080
export SLACKBOT_TOKEN=[SLACKBOT_TOKEN]
export SLACK_EVENTS_TOKEN=[SLACK_EVENTS_TOKEN]
python -m flask run
```
##### SLACKBOT_TOKEN
OAuth & Permissions -> OAuth Tokens for Your Workspace -> Bot User OAuth Token
##### SLACK_EVENTS_TOKEN
Basic Information -> App Credentials -> Signing Secret

result
```
* Serving Flask app "app.py"
* Environment: FLASK_RUN_PORT=8080
* Debug mode: off
* Running on http://127.0.0.1:8080/ (Press CTRL+C to quit)
```

## allow external access
command
```
ngrok http 8080
```
result
```
Forwarding  https://dd9f5a1c4f65.ngrok.io -> http://localhost:8080
```

## setup url in slack app
Event Subscriptions -> Request URL
https://dd9f5a1c4f65.ngrok.io/slack/events

### webinar
[Building Your first Python Slackbot](https://www.youtube.com/watch?v=2X8SrKL7E9A)
