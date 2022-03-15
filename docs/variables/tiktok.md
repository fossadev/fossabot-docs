---
id: tiktok
---

# $(tiktok)

Returns a range of metadata around a broadcaster's latest [**TikTok**](https://www.tiktok.com/en/) video that can be accessed via multiple different placeholders.

:::caution Authorization required!

This variable will only function if a broadcaster has authorized and connected a TikTok account within Fossabot's dashboard under the **Integrations** tab.

:::

## $(tiktok)

Returns the same as `$(tiktok.video)`, the metadata around a broadcaster's latest TikTok video.

#### Parameters

This variable takes **one** *optional* parameter that is a **custom format** in which to return the latest video information.

* **Supported Placeholders**
  * `{title}` - *The video's title.*
  * `{description}` - *The video's description.*
  * `{url}` - *The video's URL.*
  * `{created}` - *The video's creation date.*
  * `{duration}` - *The video's length.*
  * `{like_count}` - *How often the video was liked.*
  * `{comment_count}` - *How often the video was commented on.*
  * `{share_count}` - *How often the video was shared.*
  * `{view_count}` - *How often the video has been watched.*
  * `{id}` - *The video's unique identifier.*

#### Example Output

* `$(tiktok.video)`

    ```
    Test - https://www.tiktok.com/@wallisdev/video/7063753526857485574
    ```

* `$(tiktok.video "{title}" currently has {view_count} views, {share_count} shares and {like_count} likes.)`

    ```
    "Test" currently has 243 views, 11 shares and 62 likes.
    ```

#### Error Output

* In case no TikTok account is connected, returns the following:

    ```
    [Error: TikTok authorization invalid. Please authorize on fossabot.com -> integrations] 
    ```

## $(tiktok.video)

Returns the same as `$(tiktok)`, the metadata around a broadcaster's latest TikTok video.

#### Parameters

This variable takes **one** *optional* parameter that is a **custom format** in which to return the latest video information.

* **Supported Placeholders**
  * `{title}` - *The video's title.*
  * `{description}` - *The video's description.*
  * `{url}` - *The video's URL.*
  * `{created}` - *The video's creation date.*
  * `{duration}` - *The video's length.*
  * `{like_count}` - *How often the video was liked.*
  * `{comment_count}` - *How often the video was commented on.*
  * `{share_count}` - *How often the video was shared.*
  * `{view_count}` - *How often the video has been watched.*
  * `{id}` - *The video's unique identifier.*

#### Example Output

* `$(tiktok)` or `$(tiktok.video)`

    ```
    Test - https://www.tiktok.com/@wallisdev/video/7063753526857485574
    ```

* `$(tiktok '{title}' currently has {view_count} views, {share_count} shares and {like_count} likes.)`

    ```
    'Test' currently has 243 views, 11 shares and 62 likes.
    ```

#### Error Output

* In case no TikTok account is connected, returns the following:

    ```
    [Error: TikTok authorization invalid. Please authorize on fossabot.com -> integrations] 
    ```
