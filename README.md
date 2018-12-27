# sentry-discord webhooks

This is a basic `micro` server that accepts an incoming [Sentry](https://sentry.io) webhook and transforms it to the format expected by [Discord](https://discordapp.com/).

## Usage
First create a Discord Webhook URL

This repository is configured to run with [Zeit Now](https://zeit.co/now).

Create an account on Ziet & install now CLI. There should be some verifications.
Open cmd prompt in the cloned repository and type now help, just to make sure it is installed. 
Once that's done make sure you have now installed by typing now -version.
Then go back to the folder and open now.json remove the
```
"alias": "sentry-discord",
```
Go back to the console make sure you're in the same directory. Type 
```
$ now
```
Now will prompt you for the Webhook URL - paste the Discord Webhook URL you created FIRST. After that, Now should give you the URL to your new deployment keep the new url now gave you.

Finally, add a new Webhook alert to Sentry by pasting in the Now deployment URL. When you click `Test Plugin` on Sentry, you should receieve an alert on Discord.
