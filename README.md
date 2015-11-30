# Dashing Shoutbox widget

A widget to send a message/announcement/quote etc to a Shoutbox widget.

## About

The given scenario is that you want to share a message with the the dashboard viewers using a simple curl request.

## Installation

From your Dashing Dashboard's directory, use the command:

```
dashing install 3401cd33d5375bbac81d
```

## Using the widget

Just include a widget with a `data-view` of `Shoutbox` and you're done!
```
<li data-row="1" data-col="1" data-sizex="1" data-sizey="1">
  <div data-id="shoutbox" data-view="Shoutbox" data-title="Shoutbox"></div>
</li>
```

Now you just have to send the curl that contains the `message` and optionally a `type`.
```
curl -d '{ "auth_token": "[AUTH_TOKEN]", "message": "Hey, Look what I can do!", "type": "alarm"}' http://localhost:3030/widgets/shoutbox
```

## Types

 - alarm
 - alert
 - angry
 - bithday
 - black
 - celebrating
 - funny
 - happy
 - love


## Sound support

As a bonus, this widget can also play a sound when status is modified. Just add one or more `data-*type*sound` attributes with the value set to an absolute or relative url pointing to an audio file.

Each time the stattypeus will change, the widget will play the audio file associated to the new status.

Example:

```
<div data-id="shoutbox" data-view="Shoutbox" data-title="Shoutbox" data-funnysound="/mp3/funny.mp3"></div>
```

## Thanks 

Special thanks to the Dashing HotStatus Widget author as this widget is nearly forked from the HotStatus widget.
    
