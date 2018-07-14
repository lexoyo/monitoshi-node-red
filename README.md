# Monitoshi, website uptime monitoring

## About

Ping URLs and send email alerts when it is down or goes up again.

I have [an instance online here](https://monitoshi.lexoyo.me/), feel free to use it - I use it myself to monitor my websites.

### How does it work?

You submit an URL to Monitoshi, along with your email adress, to receive a confirmation link by email. Then Monitoshi will send emails when the URL goes down or up again. In the emails you also have a link to remove your URL and email from Monitoshi's list.

### Links

[Roadmap is here](https://github.com/lexoyo/Monitoshi/issues/1) and [feature requests can be done here](https://github.com/lexoyo/Monitoshi/issues/).

### Badges

In the email your will receive upon creation of a new monitor, there will be the URL of a badge like this one:

![silexlabs.org status by monitoshi](http://monitoshi.lexoyo.me/badge/1477987707192-1847)

Use it with markdown to display if your service is up or down, on a status page or in the README of your project.

## Install locally

Requirements

* [Node.js](http://nodejs.org/)
* [MongoDB](https://www.mongodb.org/) installed and running (`npm run serve`)


```
    $ npm install
```

4- Then start the server with this command (mongodb needs to be running)

```
    $ npm start:local
```

## Notes for developers

### Env vars

* MONGODB_HOST
* MONGODB_PORT
* MONGODB_USER
* MONGODB_PASS
* MONGODB_NAME
* APP_URL
* EMAIL_SERVER
* EMAIL_USER
* EMAIL_PASS
* ENCRYPTION_KEY
* ENABLE_EDITOR

### Routes

You can use monitoshi as is, reaching the routes listed bellow with a web browser or use it as an API with `&format=json` at the end of the URLs in order to have JSON responses instead of HTML messages.

Here are the app routes

* POST /monitors => add a monitor
* DELETE /monitors => remove a monitor
* GET /monitors => displays all monitors

## License

license: GPL v2

