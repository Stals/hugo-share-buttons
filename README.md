# Hugo Share Buttons
hugo-share-buttons is a [partial template](https://gohugo.io/templates/partials/) to show social share buttons on your Hugo website, without any JavaScript or http requests.
It is based on sharingbuttons.io and can look something like this:
<br>
<img src="https://letsmakeagame.net/github/hugo-share-buttons/hugo-share-buttons-small.png" height="60">

or like this:
<img src="https://letsmakeagame.net/github/hugo-share-buttons/hugo-share-buttons-medium.png" height="60">


## How To Use
Copy the share-buttons.html and place it inside layouts/partials,
then place this inside one of your template files:
``` {{ partial "share-buttons" . }} ```

## Settings
Create a shareButtons section in your root config file (i.e. config.yaml)

### networks (required)
'networks' supported: facebook, twitter, tumblr, email, pinterest, linkedin, reddit, xing, whatsapp, hackernews, vk, telegram

### size (required)
'size' can be one of
- small
- medium
- large
<img src="https://letsmakeagame.net/github/hugo-share-buttons/hugo-share-buttons-sizes.png" height="70">

### icon (optional)
You can specify icon as one of the following:
- normal (default)
- solid
- circle
- solidcircle

<img src="https://letsmakeagame.net/github/hugo-share-buttons/hugo-share-buttons-icon-options.png" height="70">

### fontsize (optional)


Currently in development by https://letsmakeagame.net/