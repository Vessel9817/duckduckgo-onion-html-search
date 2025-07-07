# duckduckgo-onion-html-search

A browser web extension that adds DuckDuckGo's onion site as a search engine.
This can be useful when users have disabled JavaScript with NoScript, for example.
Prevents a needless redirect from the default script-enabled search URL
and uses POST requests instead of GET requests for added privacy and security.

## Installation

### Tor Browser (Desktop)

**From release**:

Install the extension from the [Firefox Add-ons page][download]

**From source**:

- Add the contents of [`web-extension`](./web-extension) to a ZIP file
- Go to `about:addons`
- Click the settings icon
- Click `Install Add-on from File...`
- Select the ZIP file

### Tor Browser (Android)

As search providers are currently [unsupported][android-support] in Firefox for
Android and its derivatives, this extension cannot be installed. However, it's
possible to manually add the search engine, but it'll need to use GET
instead of POST requests.

- In Tor Browser, go to `Settings > Search > Default search engine`
- Tap `Add search engine`
- In the `Name` text field, type `DuckDuckGo HTML (.onion)`,
  or whatever you prefer to call this search engine
- In the `Search string URL` text field, copy and paste the following:
  
  ```txt
  https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html?q=%s
  ```

- Tap `Save`
- Optionally, you can also make this search engine the default

## See also

- [duckduckgo-html-post-search](https://github.com/KiaraGrouwstra/duckduckgo-html-post-search)
- [duckduckgo-lite-search](https://github.com/andis-sprinkis/duckduckgo-lite-search)
- [firefox-duckduckgo-onion-extension](https://github.com/zompimalakae/firefox-duckduckgo-onion-extension)

[download]: https://addons.mozilla.org/en-US/firefox/addon/duckduckgo-onion-html-search/

[android-support]: https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/chrome_settings_overrides#browser_compatibility
