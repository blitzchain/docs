---
layout: page
title: Data Lake
permalink: /data-lake/
---

# JavaScript quick start

After following this guide you will have published an event to your web app using Channels. If you have any questions [get in touch](https://support.pusher.com/hc/en-us/requests/new).

## Get your free API keys

[Create an account](https://dashboard.pusher.com/accounts/sign_up), then create a Channels app. Go to the "Keys" page for that app, and make a note of your `app_id`, `key`, `secret` and `cluster`.

## Include the Channels Client

Include the [pusher-js](https://github.com/pusher/pusher-js) script tag on your page.

```html
<script src="https://js.pusher.com/{{ env.pusherJSVersion }}/pusher.min.js"></script>
```

## Open a connection to Channels

Open a connection to Channels using the `key` and `cluster` you noted down earlier.

```js
var pusher = new Pusher("APP_KEY", {
  cluster: "APP_CLUSTER",
});
```

## Subscribe to a channel

You will soon publish an event to a channel called `my-channel`, and your web app will receive this event. But to receive this event, your web app first needs to subscribe to the `my-channel` channel. Do this with `pusher.subscribe`:

```js
var channel = pusher.subscribe("my-channel");
```

## Listen for events on your channel

Every published event has an "event name". The event you will publish will have the event name `my-event`. For your web app to do something when it receives an event called `my-event`, your web app must first "bind" a function to this event name. Do this using the channel’s `bind` method:

```js
channel.bind("my-event", (data) => {
  // Method to be dispatched on trigger.
});
```

## Trigger events from your server

In the examples below we trigger an event named `my-event` to Channels on a channel called `my-channel`. For each example below a server library deals with the server communication.



If there isn’t an example in a language that you are familiar with then have a look on our server libraries page to see if anyone has created one in your language.

## Where next?

If you published an event and it triggered your `alert(...)` call, well done! If you had any trouble, [get in touch](https://support.pusher.com/hc/en-us/requests/new). Otherwise, you could look at the more advanced features of the JavaScript client library.