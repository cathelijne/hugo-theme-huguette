# Huguette - a theme for Hugo

## TLDR;
```
git submodule add https://github.com/cathelijne/hugo-theme-huguette.git themes/huguette
echo "theme = 'huguette'" >> config.toml
```
![Huguette theme thumbnail](https://github.com/cathelijne/hugo-theme-huguette/blob/main/images/screenshot.png?raw=true)

## See it in action
Here's an [example site](https://huguette.netlify.app/) to see what Huguette looks like.

## About this theme
I am a cloud engineer by day, and a hobbyist website builder whenever I have the time. I like to try lots of different technologies, just for the fun of it. 
Often, I miss a very simple boilerplate theme that just demonstrates what a CMS or site builder can do. Either you have to take your pick from the many (and often excellent!) beautiful themes with lots of bells and whistles that obscure a bit how everything works, or you have to start from scratch.

When I ran into Hugo, I decided to actually make such a simple theme. Without bells an whistles, no javascript, no npm or yarn needed to make changes to the theme. Just plain HTML. And to make it look better, I included classless.css. But using that is entirely optional (it does look good though!). I included a few, just enough, _Hugo partials_ in the theme to give you an idea of what they can do, nothing more. I really had to sit on my hands there :)

## One-click install with NetlifyCMS
This repository holds the theme only so you can install it to any existing site. But if you're just starting with Hugo and want a one-click site install with the theme, the css and Netlify CMS enabled and hosted on Netlify, you can use the button below.
Jou can also have a look at the the [example site repository](https://github.com/cathelijne/hugo-huguette-example) or the [example site itself](https://huguette.netlify.app/) (you will find the one click install there too).

[![Deploy with Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/cathelijne/hugo-huguette-example&stack=cms)

If you want just the theme, read on.

## Theme Installation
Install the theme like any other theme:
```
git submodule add https://github.com/cathelijne/hugo-theme-huguette.git themes/huguette
echo "theme = 'huguette'" >> config.toml
```

## Enable the included Classless CSS:
```
echo '[params]
  css = true' >> config.toml
```
And copy the static/css folder included in this theme to the static folder in the root of your site:
```
mkdir static
cp -r themes/huguette/static/css static
```
## Enable Netlify CMS
To enable Netlify CMS, enable the inclusion of the CMS JavaScript by adding `netlifycms = true` to the params section of your config.toml so it looks like this:
```
[params]
  css = true
  netlifycms = true
```
Copy the static/admin folder to the static folder in the root of your site:
```
cp -r themes/huguette/static/admin static
```
You will need to edit config.yml in admin/static to match your site. Explaining how is outside of the scope if this installation doc, but you can use Netlify CMS's documentation: [instructions for adding NetlifyCMS](https://www.netlifycms.org/docs/hugo/) to Hugo.

## Thanks to
- [Hugo](https://gohugo.io)
- [Netlify CMS](https://www.netlifycms.org/)
- [classless.css](https://classless.de/)

### See my other resources for Hugo
- A [gist](https://gist.github.com/cathelijne/cc7b3b00725f70605321b138dc16f2a8) with a few snippets to use in templates
- [Huguette](https://github.com/cathelijne/hugo-theme-huguette), a boilerplate theme to get you started and nothing more <-- That's this repo!
- An [All-in-one](https://github.com/cathelijne/hugo-huguette-example), one-click Netlify install of Hugo with Huguette as a theme
- [Dummy Content for Hugo](https://github.com/cathelijne/hugo-dummy-content) for Hugo: 100 pages in 5 sections with categories and tags
