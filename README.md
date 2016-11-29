# DataFire - News Headlines
> This is a reference project for [DataFire](https://github.com/DataFire/DataFire)

Send yourself an e-mail with the latest items from a few RSS feeds.

To use this flow, first create a GMail client in the
[Google Dev Console](https://console.developers.google.com)
To register a Google Sheets client, visit
[console.developers.google.com](https://console.developers.google.com/apis/)
* search for and select "Gmail"
* click "Enable API"
* click "Credentials"
* click "Create Credentials" -> "OAuth Client ID"
* Choose "web application"
* add `http://localhost:3000` as an "Authorized redirect URI"

```
git clone https://github.com/DataFire/headlines
cd headlines
npm install

datafire integrate gmail cnn npr nytimes
datafire authenticate gmail --generate_token
# Follow the command-line prompts

datafire run headlines
```

## Serverless
Runs every day by default. You can change this in `serverless.yml`

```
serverless deploy -v
```
