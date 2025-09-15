---
id: quote
---

# !quote

Displays a random quote from the channel's quote collection, or allows moderators to manage quotes.

## !quote

Returns a random quote from the channel's quote collection.

#### Parameters

This command takes **one** *optional* parameter that is a **quote number** to display a specific quote.

#### Example Output

* `!quote`

    ```
    #42: Welcome to my stream!
    ```

* `!quote 5`

    ```
    #5: That was an amazing play!
    ```

#### Error Output

* In case no quotes exist in the channel, returns the following:

    ```
    Error: No quotes found.
    ```

* In case an invalid quote number is provided, returns the following:

    ```
    Error: Quote not found.
    ```

## !quote add

Adds a new quote to the channel's quote collection.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **one** *required* parameter that is the **quote content** to add.

#### Example Output

* `!quote add Welcome to my stream!`

    ```
    Fossabot: @User, added quote #43
    ```

#### Error Output

* In case no quote content is provided, returns the following:

    ```
    Usage: !quote add <quote>
    ```

## !quote edit

Edits an existing quote in the channel's quote collection.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **two** *required* parameters:

1. **Quote number** - The number of the quote to edit
2. **New quote content** - The updated quote content

#### Example Output

* `!quote edit 5 This was an incredible play!`

    ```
    Fossabot: @User, updated quote #5
    ```

#### Error Output

* In case insufficient parameters are provided, returns the following:

    ```
    Usage: !quote edit <number> <message>
    ```

* In case the quote number is invalid, returns the following:

    ```
    Error: Quote not found.
    ```

## !quote delete

Deletes a quote from the channel's quote collection.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **one** *required* parameter that is the **quote number** to delete.

#### Example Output

* `!quote delete 5`

    ```
    Fossabot: @User, deleted quote #5
    ```

#### Error Output

* In case no quote number is provided, returns the following:

    ```
    Usage: !quote delete <number>
    ```

* In case the quote number is invalid, returns the following:

    ```
    Error: Quote not found.
    ```
