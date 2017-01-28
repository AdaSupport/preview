# Previewer
Our link previewer! It returns JSON describing a given `url`. To use it, navigate to https://previews.ada.support/

We built this for ourselves, but you can use it too if you like.

## Arguments
The only argument we need is a `url` pass it in as a url argument like this:

```sh
https://previews.ada.support/?url=slack.com
```

## Response
We return JSON with utf-8 characters encoded using `\u`. Here's what a good response might look like:

```js
{
    "desc": "Slack brings all your communication together in one place. It\u2019s real-time messaging, archiving and search for modern teams.",
    "title": "Slack: Where work happens",
    "icon": "https://a.slack-edge.com/66f9/img/icons/favicon-32.png"
}
```

## Errors
Errors will return a 400 status code and a `message` parameter describing the issue.
