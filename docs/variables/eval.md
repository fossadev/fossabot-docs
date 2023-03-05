---
id: eval
---

# $(eval)

Returns the output of custom [**JavaScript**](https://wikipedia.org/wiki/JavaScript) code using Fossabot's own JavaScript engine.

:::caution This variable is heavily limited to prevent abuse!

The **maximum** execution time of your code may not exceed **50ms**, and there is a limit of **one** evaluation **per action** *(command, keyword, or timer)*.

:::

#### Parameters

This variable takes **one** *required* parameter that is **JavaScript code** to be executed.

* **Please be aware of the following:**
  * All code has to be wrapped in **double quotes**, example: `$(eval "123 + 456")`
  * Only **single quotes** can be used to indicate a string, example: `$(eval "var test='hello world';test")`
  * Both `"` and `\` have to be escaped **thrice** when used within a string, example: `$(eval "'Félix \\\"xQc\\\" Lengyel'")`
  * Special characters have to be escaped **twice**, example: `$(eval "'1 (blabla) 3'.replace(/\\(.*\\)/, '2')")`

## Example Usage

* A simple command with the name `!sum` and a response of the following:

    ```
    $(eval "$(index1) + $(index2)")
    ```

    If triggered by `!sum 123 456`, would return the following response:

    ```
    579
    ```

* A more advanced command, a recreation of `!uptime`, with a response of the following:

    ```
    $(eval "var cname='$(channel.login)';var sname='$(sender.login)';var utime=`$(uptime)`; `${utime}` !== '[Error: Stream is offline.]' ? `${(sname === cname ? 'You have been' : cname + ' has been')} live for ${utime}.` : `${(sname === cname ? 'Your' : 'The')} stream is currently offline.`")
    ```

    If triggered in your *own channel* while you are *offline*, would return the following response:

    ```
    Your stream is currently offline.
    ```

    If triggered in your *own channel* while you are *online*, would return the following response:

    ```
    You have been live for 1 hour and 21 minutes.
    ```

    If triggered in *Aiden's channel* while he is *offline*, would return the following response:

    ```
    The stream is currently offline.
    ```

    If triggered in *Aiden's channel* while he is *online*, would return the following response:

    ```
    aiden has been live for 2 hours and 5 minutes.
    ```

#### Error Output

* In case of a [**standard JavaScript error**](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Errors#list_of_errors), returns the specific JavaScript error.

* In case an evaluation times out, returns the following:

    ```
    [Error: JavaScript evaluation timed out on remote server.]
    ```

* In case an evaluation fails to execute, returns the following:

    ```
    [Error: Failed to execute JavaScript on remote server.]
    ```
