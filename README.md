# code-web-fonts

Web fonts for programming, including [**Powerline** enabled fonts](https://github.com/powerline/fonts) working in [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo) and working also on **Chromebook** (or pretty much anything running Chrome).

[Preview the fonts](https://rawcdn.githack.com/cfal/code-web-fonts/7b73784ae5acd0d783f9f3629c845a9e51ec1dbf/preview.html) (courtesy of raw.githack.com)

## Available fonts

There are several `font-family` you can choose from.

Powerline enabled:

  * `Anonymous Pro` - [Anonymice Powerline](https://github.com/powerline/fonts/tree/master/AnonymousPro)
  * `DejaVu Sans Mono` - [DejaVu Sans Mono for Powerline](https://github.com/powerline/fonts/tree/master/DejaVuSansMono)
  * `Hack` - [Hack Webfont](https://github.com/chrissimpkins/Hack)
  * `Inconsolata` - [Inconsolata for Powerline](https://github.com/powerline/fonts/tree/master/Inconsolata)
  * `Inconsolata-g` - [Inconsolata-g for Powerline](https://github.com/powerline/fonts/tree/master/Inconsolata-g)
  * `Iosevka` - [Iosevka Webfont](https://github.com/be5invis/Iosevka)
  * `Liberation Mono` - [Literation Mono Powerline](https://github.com/powerline/fonts/tree/master/LiberationMono)
  * `Monofur for Powerline` - [Monofur for Powerline](https://github.com/powerline/fonts/tree/master/Monofur)
  * `Noto Mono for Powerline` - [Noto Mono for Powerline](https://github.com/powerline/fonts/tree/master/NotoMono)
  * `PT Mono` - PT Mono for Powerline
  * `Source Code Pro` - [Source Code for Powerline](https://github.com/powerline/fonts/tree/master/SourceCodePro)
  * `Ubuntu Mono` - [Ubuntu Mono derivative Powerline](https://github.com/powerline/fonts/tree/master/UbuntuMono)

Other fixed-width fonts:

  * `Fixedsys Excelsior` - [Fixedsys Excelsior](https://www.cufonfonts.com/font/fixedsys-excelsior-301)

See [Slant](http://www.slant.co/topics/67/~programming-fonts) if you don't know which to choose.

## Usage example

### Usage example for [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo)

  - Launch *Secure Shell* and click on **Options**
    (or go to `chrome-extension://pnhechapfaindjhompbnflcldabbghjo/html/nassh_preferences_editor.html`):
      - Set **font-family**: `"Source Code Pro", monospace`
      - Set **Custom CSS (URI)** to one of the following:
        - jsdelivr CDN at hash (longest cache expiry):
          ```
          https://cdn.jsdelivr.net/gh/cfal/code-web-fonts@7b73784ae5acd0d783f9f3629c845a9e51ec1dbf/CodeFonts.css
          ```
        - jsdelivr CDN (latest):
          ```
          https://cdn.jsdelivr.net/gh/cfal/code-web-fonts/CodeFonts.css
          ```
        - github (latest):
          ```
          https://raw.githubusercontent.com/cfal/code-web-fonts/master/CodeFonts.css
          ```

### Usage example for [Crosh Window](https://chrome.google.com/webstore/detail/crosh-window/nhbmpbdladcchdhkemlojfjdknjadhmh)

  - Start crosh window then press `Ctrl+Shift+J` and paste in the following:

```js
term_.prefs_.set('font-family', '"Source Code Pro", monospace');
term_.prefs_.set('user-css', 'https://cdn.jsdelivr.net/gh/cfal/code-web-fonts@7b73784ae5acd0d783f9f3629c845a9e51ec1dbf/CodeFonts.css');
```

If you have [Crouton](https://github.com/dnschneid/crouton) installed on a developer mode Chromebook,
or if you're on pretty much any other OS, you can install those fonts locally or copy them locally
and it'll work with little to no effort.

## Suggesting a new font

To add a new font, you can submit a GitHub pull request through a forked repository. Your pull request should:

  - Include a new font file in [WOFF2 format](https://gist.github.com/sergejmueller/cf6b4f2133bcb3e2f64a).
  - Add your font to `CodeFonts.css`, `preview.html` and `README.md` (might use [Transfonter](http://transfonter.org/) to help with the CSS).

### Converting to WOFF2

There are various methods, including:

  * [otf to woff2 | Everything Fonts](https://everythingfonts.com/otf-to-woff2)
  * [ttf to woff2 | Everything Fonts](https://everythingfonts.com/ttf-to-woff2)
  * [Webfont Generator | Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator)
  * Using [FontForge](https://fontforge.github.io/en-US/):

    ```bash
    #!/usr/bin/env fontforge
    Open($1)
    Generate($1:r + ".woff2")`
    ```
