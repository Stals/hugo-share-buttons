# Hugo Share Buttons
hugo-share-buttons is a [partial template](https://gohugo.io/templates/partials/) that allows you to show social share buttons on your Hugo website, without any JavaScript or http requests.
It is based on sharingbuttons.io and can look something like this:
<br>
<img src="https://letsmakeagame.net/github/hugo-share-buttons/hugo-share-buttons-all.png" height="60">

or like this:
<br>
<img src="https://letsmakeagame.net/github/hugo-share-buttons/hugo-share-buttons-medium.png" height="60">


## How To Use
Copy the share-buttons.html and place it inside layouts/partials,
then place this inside one of your template files:
``` {{ partial "share-buttons" . }} ```

Create a shareButtons section under 'params' in your root config file (i.e. config.yaml)
As a jumping of point you can use these

<table>
<tr>
<th>for YAML</th>
<th>for TOML</th>
<th>for JSON</th>
</tr>
<tbody>
<tr>
<td>
    
```
shareButtons:
  size: small
  networks:
    - facebook
    - twitter
```

</td>
<td>
    
```
[params.shareButtons]
  size = "small"
  networks = ["facebook", "twitter"]
```

</td>
<td>
    
```
  "shareButtons" : {
    "networks" : [
      "facebook",
      "twitter"
    ],
    "size" : "small"
  }
```

</td>
</tr>
</tbody>
</table>
For TOML - put it at the end of you [params], or everything else will be a part of [params.shareButtons] and not [params]
Also note that if your runing hugo locally with ```hugo server```, then you may need to stop it and re-run for changes to take effect.

## Settings

### - networks (required)
'networks' supported: facebook, twitter, tumblr, email, pinterest, linkedin, reddit, xing, whatsapp, hackernews, vk, telegram

### - size (required)
'size' can be one of
- small
- medium
- large
<img src="https://letsmakeagame.net/github/hugo-share-buttons/hugo-share-buttons-sizes.png" height="70">

### - icon (optional)
You can specify icon as one of the following:
- normal (default)
- solid
- circle
- solidcircle

<img src="https://letsmakeagame.net/github/hugo-share-buttons/hugo-share-buttons-icon-options.png" height="70">

### - buttonMargin (optional)
You can specify margins to change the spacing between buttons. 
Default is 0.5em.

### - fontsize (optional)
The button size is changed by specifying a font size, because everything else is dependatnt on 'em' numbers, which is the sharingbuttons.io recommended way.

## Examples
Let's do a bigger example of how shareButtons would look in your config file, and the result it produces

<table>
<tr>
<th>config.yaml</th>
<th>config.toml</th>
<th>config.json</th>
</tr>
<tbody>
<tr>
<td>
    
```
baseURL: 'https://yoursite.example.com/'
params:
  author: Nikola Tesla
  shareButtons:
    networks:
      - facebook
      - twitter
      - email
      - reddit
    size: small
    icon: solid
    buttonMargin: 0.2em
```

</td>
<td>
    
```
baseURL = "https://yoursite.example.com/"

[params]
author = "Nikola Tesla"

  [params.shareButtons]
  networks = [ "facebook", "twitter", "email", "reddit" ]
  size = "small"
  icon = "solid"
  buttonMargin = "0.2em"
```

</td>
<td>
    
```
{
   "baseURL" : "https://yoursite.example.com/",
   "params" : {
      "author" : "Nikola Tesla",
      "shareButtons" : {
         "networks" : [
            "facebook",
            "twitter",
            "email",
            "reddit"
         ],
         "size" : "small",
         "icon" : "solid",
         "buttonMargin" : "0.2em"
      }
   }
}

```

</td>
</tr>
</tbody>
</table>

<img src="https://letsmakeagame.net/github/hugo-share-buttons/hugo-share-buttons-small.png" height="60">

Currently in development by https://letsmakeagame.net/
