---
id: requesting-songs
slug: /mediarequest/requesting-songs
---

# Requesting songs

:::tip

You must manually enable this command in your `Default Commands` settings.

:::

Viewers request songs through the use of the [**!sr**](../commands/default/sr.md), depending on your settings, they can request with:

* A [**YouTube**](https://youtube.com) search query.
* Link a [**YouTube**](https://youtube.com) video directly.
* Link a [**SoundCloud**](https://soundcloud.com) song directly.

![Example of a user requesting a song](/img/mediarequest/sr-example.png)

## Restrictions

Fossabot enforces the following restrictions by default, these cannot be controlled by you:

* Fossabot will not play YouTube live streams, but it will play YouTube Live VODs.
* Fossabot will not allow requests that cannot be embedded into the media request page.
* Fossabot will apply [**YouTube's SafeSearch filters**](https://support.google.com/youtube/answer/174084) when using search queries in `!sr`. You can link a song directly to bypass these filters.
* If a playback location has been set, Fossabot will not accept requests that cannot be played in that country.

### Setting a playback location

Setting a playback location allows Fossabot to only accept content that can be played in your country. It works by checking the geo-blocking restrictions defined by the SoundCloud or YouTube API against your country.

![Example of playback location settings](/img/mediarequest/playback-location-settings-example.png)
