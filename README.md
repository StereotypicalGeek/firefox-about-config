
# Introduction

Here is my list of settings to change in the about:config menu of Firefox.
I originally created this list to remember what to change when I need to reinstall Firefox.
Some people have been interested and I've distributed it afterwards as a text file.
This way of diffusion being absolutely not practical I decided to put this list on GitHub.
The aim is also to receive contributions and discuss these parameters.

# Settings 

## Privacy and security

To access these setting type about:config in the Firefox url bar. This do not work for Chromium based browsers such as Google Chrome, Brave, Vivaldi, Opera or Edge

### Deactivate Safe Browsing

| Attribute | Value | Description |
| :-: | :-: | --- |
| `browser.safebrowsing.malware.enabled`          | **false** | Disables safebrowsing, provided by Google.   |
| `browser.safebrowsing.phishing.enabled`         | **false** | Disables safebrowsing.                      |
| `browser.safebrowsing.blockedURIs.enabled`         | **false** | Disables safebrowsing.                      |
| `browser.safebrowsing.downloads.remote.enabled` | **false** | Disables the updating of block lists. |
| `browser.safebrowsing.provider.google.updateURL` | **empty** | Disables the updating of block lists. |
| `browser.safebrowsing.provider.google4.updateURL` | **empty** | Disables the updating of block lists. |
| `browser.safebrowsing.provider.google4.dataSharingURL` | **empty** | Disables data sharing. |
| `browser.safebrowsing.provider.google4.gethashURL` | **empty** | Disables data sharing. |

### Referer management

| Attribut | value | Description |
| :-: | :-: | --- |
| `network.http.referer.spoofSource`           | **true** | Send as referer the site you are visiting, if you visit mozilla.org, Firefox will send as referer mozilla.org. |

### Deactivate preloading

| Attribute | Value | Description |
| :-: | :-: | --- |
| `network.dns.disablePrefetch`               | **true**  | Disable DNS preloading of links, if you trust your DNS server do not disable this useful option to improve performance. |
| `network.prefetch-next`                     | **false** | Disables page preloading. |
| `browser.urlbar.speculativeConnect.enabled` | **false** | Disables preloading in the Firefox "smart" bar. |
| `network.http.speculative-parallel-limit`   | **0**     | Disables preloading. |

### Deactivate telemetry

Type `telemetry` in the search bar, remove all links and switch everything to `false`.

| Attribute | Value | Description |
| :-: | :-: | --- |
| `toolkit.telemetry.enabled` | **false** | Deactivate telemetry. |
| `toolkit.telemetry.server` | **Empty** | Deactivate telemetry. |
| `dom.ipc.plugins.flash.subprocess.crashreporter.enabled` | **false** | Deactivate telemetry. |
| `app.normandy.enabled`                                   | **false** | Deactivate telemetry. |
| `app.normandy.first_run`                                 | **false** | Deactivate telemetry. |
| `app.normandy.api_url`                                   | **empty** | Deactivate telemetry. |
| `beacon.enabled`                                         | **false** | Deactivate telemetry. |

### Deactivate geolocation


| Attribut | value | Description |
| :-: | :-: | --- |
| `geo.enabled`              | **false** | Deactivate geolocation. |
| `geo.wifi.uri`             | **empty** | Deactivates the geolocation through Wi-Fi point enumeration. |
| `geo.provider.network.url` | **empty** | Deactivate geolocation. |

### Disable push notifications


Push notifications allow sites to send you notifications even when they are not open, if you allow them to do so. Mozilla uses its servers to do this. This can raise privacy concerns.


| Attribute | Value |
| :-: | :-: |
| `dom.push.connection.enabled` | **false** |
| `dom.push.enabled`            | **false** |
| `dom.push.serverURL`          | **empty**  |
   
### Other 

| Attribute | Value | Description |
| :-: | :-: | --- |
| `security.OCSP.enabled` | **0** | Disable [OCSP](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). |
| `browser.cache.offline.enable` | **false** | Disable the offline cache, it's not a good idea to allow sites to save anything on your computer. |
| `browser.cache.offline.capacity` | **0** | Deactivates the offline cache. |
| `extensions.pocket.enabled` | **false** | Deactivates pocket. If you don't use it, deactivate it. |
| `extensions.pocket.api` | **empty** | Deactivates pocket.
| `extensions.pocket.site` | **empty** | Deactivates pocket. |
| `browser.send_pings` | **false** | Disables click tracking. |
| `browser.send_pings.max_per_link` | **0** | Deactivate notification when you click |
| `dom.battery.enabled` | **false** | Prevents sites from seeing the status of your battery. |
| `dom.event.clipboardevents.enabled` | **false** | Prevents sites from knowing when you copy an item to the clipboard. |
| `media.navigator.enabled`| **false** | Prevents sites from tracking the state of the microphone and camera. |
| `webgl.disabled` | **true** | WebGL could be a source of security problems. May break some sites. |
| `network.captive-portal-service.enabled` | **false** | Deactivates the captive portal search. This is used, for example, to connect to public Wi-Fi networks. |
| `captivedetect.canonicalURL` | **empty** | Disables the search for captive portals. |
| `layout.css.visited_links_enabled` | **false** |[Too long to explain](https://hacks.mozilla.org/2010/03/privacy-related-changes-coming-to-css-vistited/).|
| `device.sensors.enabled` | **false** | Deactivates sensors |
| `browser.newtabpage.activity-stream.feeds.snippets` | **false** | Disables the display of Mozilla snippets. Firefox contacts Mozilla's servers to display them. |
| `privacy.firstparty.isolate` | **true** | Isolates each of your tabs. |
| `network.IDN_show_punycode` | **true** | Some links contain unicode characters. This gives greater possibilities for phishing. These unicode characters are encoded with the "punycode" code. Enabling this setting forces Firefox to display the punycode rather than the unicode character. |
| `media.peerconnection.enabled` | **false** | Disables WebRTC which may pose security and privacy concerns, such as revealing your IP address. |
| `signon.autofillForms` | **false** | Deactivates the automatic filling in of identifiers. |
| `network.security.esni.enabled` | **true** | Activates ESNI support, the article is in french, I haven't found such a detailed one in english. You can use Deepl.com to translate it.(https://lafibre.info/cryptographie/encrypted-sni/). |

## Performances

**I need to investigate further the real impact of changing these parameters; I leave it in this guide for your information, but if you don't know what you are doing, don't change them. **

| Attribute | Value | Description |
| :-: | :-: | --- |
| `browser.cache.memory.enable` | **true** | Activates the memory cache (RAM). For all cache settings, remember to enable automatic cache cleaning at the end of the session for privacy reasons. The best way to do this is to use an extension such as "autodelete cookie" and to activate the automatic cleaning when the tab is closed and after an interval of about ten seconds. |
| `browser.cache.memory.capacity` | **512000** | Memory cache size (in bytes, 512000 = 512 MB). Set -1 so that Firefox automatically manages this value according to your memory size. |
| `browser.cache.memory.max_entry_size` | **-1** | Set -1 to remove any size limit. |
| `browser.cache.disk.enable` | **true** | Allows the use of the disk cache. For confidentiality reasons, disabling the disk cache in favour of the memory cache may be a good thing; it ensures that no data is saved on your computer when you close Firefox. |
| `browser.cache.disk.capacity` | **512000** | Disk cache size. |
| `network.dnsCacheEntries` | **4000** | Number of entries in the DNS cache. For privacy reasons, if someone can access your computer leave the default setting. |
| `network.dnsCacheExpiration` | **43200** | Time before expiration, cleaning, of an entry in the DNS cache (in seconds). For confidentiality reasons, if someone can access your computer leave the default number. |
| `network.dnsCacheExpirationGracePeriod` | **43200** | Set the same value as for `network.dnsCacheExpiration`. |
| `browser.sessionstore.interval` | **60000** | Firefox backs up your tabs and their data every 15 seconds. This allows it to restore your session in the event of a crash. It changes from 15 seconds to a backup every 60 seconds (60 000 ms). One backup per minute is more than enough and it allows to reduce the accesses to the disk made by Firefox. |

## Utility

| Attribute | Value | Description |
| :-: | :-: | --- |
| `browser.tabs.closeWindowWithLastTab` | **false** | Disables the closing of Firefox when you close the last tab. |
| `browser.backspace_action` | **1** | The backspace key on your keyboard will no longer take you back to the previous link. |
| `security.secure_connection_icon_color_gray` | **false** | Switch the padlock on the address bar back to green instead of grey. Because it's prettier :-) |
| `accessibility.blockautorefresh` | **true** | Blocks the automatic page refresh. |
| `dom.event.contextmenu.enabled` | **false** | Prevents sites from blocking right-click use. |
| `browser.tabs.allowTabDetach` | **false** | Disables the ability to move a tab to a new window by dragging it. |
| `ui.SpellCheckerUnderlineStyle` | **3** | Create this entry in about:config and put the number 3 so that Firefox underlines misspelled words instead of drawing a small red wave. Another number will give a different shape](http://kb.mozillazine.org/Ui.SpellCheckerUnderlineStyle). |
| `full-screen-api.warning.timeout` | **0** | Firefox displays a popup when you switch to full screen. Changing this setting to 0 will cause this setting to no longer be displayed. |
| `browser.preferences.experimental` | **true** | Activates the "Experimental" tab in the Firefox settings. |

# Sources

https://github.com/kaliangel/firefox-about-config

https://www.dsfc.net/logiciel-libre/firefox-logiciel-libre/firefox-plus-rapide-respectueux-vie-privee/#Utiliser_la_memoire

https://www.privacytools.io/browsers/#about_config

https://support.mozilla.org/fr/kb/comment-empecher-firefox-etablir-automatiquement-connexions#w_mises-aa-jour-automatiques-et-saecuritae

https://sebsauvage.net/wiki/doku.php?id=firefox

https://wiki.mozilla.org/Privacy/Privacy_Task_Force/firefox_about_config_privacy_tweeks

https://www.kali-linux.fr/configuration/configurer-firefox-optimiser-securite-performances

https://lehollandaisvolant.net/?d=2020/01/02/11/28/39-ma-liste-des-tweaks-aboutconfig-dans-firefox

https://theprivacyguide1.github.io/about_config.html

https://www.ghacks.net/overview-firefox-aboutconfig-security-privacy-preferences/

https://librewolf-community.gitlab.io/

https://lehollandaisvolant.net/?d=2020/01/02/11/28/39-ma-liste-des-tweaks-aboutconfig-dans-firefox

http://kb.mozillazine.org/

https://www.malekal.com/mozilla-firefox-les-reglages-ultimes-anti-tracking-et-contre-le-pistage/

***Merci à eux !***
