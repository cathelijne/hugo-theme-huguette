# Hugette - a theme for Hugo

Install the theme like any other theme:

```
git submodule add https://github.com/cathelijne/hugo-theme-huguette.git themes/huguette
cp themes/huguette/static .
echo "theme = 'huguette'" >> config.toml
```

If you want to enable the included Classless CSS:

```
echo '[params]
  css = true' >> config.toml
  ```

To enable Netlify CMS, please follow the instructions on the [example site](https://github.com/cathelijne/hugo-huguette-example)
