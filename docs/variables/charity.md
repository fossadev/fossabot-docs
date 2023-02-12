---
id: charity
---

# $(charity)

Returns a range of metadata around the currently running [Twitch Charity](https://dashboard.twitch.tv/charity) campaign in the channel.

## $(charity)

An alias for combining many charity variables together in the following format: `$(charity.name): $(charity.description) - $(charity.website)`.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(charity)`

    ```
    St Jude ChildCare Centres UK: St Jude India ChildCare Centres UK provides cost-free accommodation and holistic care to help disadvantaged children survive cancer. - https://www.stjudechild.org
    ```

#### Error Output

* In case there is no active Charity campaign in the channel, returns the following:

    ```
    [Error: No campaign active.]
    ```

## $(charity.amount_raised)

Returns the name of the total raised for the Charity in the current campaign that the channel is running.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(charity.amount_raised)`

    ```
    $58.00
    ```

#### Error Output

* In case there is no active Charity campaign in the channel, returns the following:

    ```
    [Error: No campaign active.]
    ```

## $(charity.description)

Returns the description of the Charity the channel is fundraising for.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(charity.description)`

    ```
    St Jude India ChildCare Centres UK provides cost-free accommodation and holistic care to help disadvantaged children survive cancer.
    ```

#### Error Output

* In case there is no active Charity campaign in the channel, returns the following:

    ```
    [Error: No campaign active.]
    ```

## $(charity.name)

Returns the name of the Charity the channel is fundraising for.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(charity.name)`

    ```
    St Jude ChildCare Centres UK
    ```

#### Error Output

* In case there is no active Charity campaign in the channel, returns the following:

    ```
    [Error: No campaign active.]
    ```

## $(charity.progress)

Returns the progress towards the current fundraising goal for the Charity campaign in the channel, as a percentage.

**This value may exceed `100%`, allowing Fossabot to highlight the achievement of a channel exceeding their fundraising goal.**

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(charity.progress)`

    ```
    58%
    ````

#### Error Output

* In case there is no active Charity campaign in the channel, returns the following:

    ```
    [Error: No campaign active.]
    ```

* In case there is no fundraising goal set for this campaign, returns the following:

    ```
    [Error: No fundraising goal set.]
    ```

* In case Twitch returns the current amount raised and the fundraising goal in different currencies, returns the following:

    ```
    [Error: Cannot calculate progress: Current and target currencies mismatch.]
    ```

## $(charity.remaining)

Returns the amount left to raise for the current fundraising goal set for the Charity campaign running in the channel.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(charity.remaining)`

    ```
    $42.00
    ```

* In case the goal has already been reached, returns the following:

    ```
    $0.00
    ```

#### Error Output

* In case there is no active Charity campaign in the channel, returns the following:

    ```
    [Error: No campaign active.]
    ```

* In case there is no fundraising goal set for this campaign, returns the following:

    ```
    [Error: No fundraising goal set.]
    ```

* In case Twitch returns the current amount raised and the fundraising goal in different currencies, returns the following:

    ```
    [Error: Cannot calculate progress: Current and target currencies mismatch.]
    ```

## $(charity.target)

Returns the fundraising goal set for the Charity campaign that the channel is fundraising for.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(charity.target)`

    ```
    $100.00
    ```

#### Error Output

* In case there is no active Charity campaign in the channel, returns the following:

    ```
    [Error: No campaign active.]
    ```

* In case there is no fundraising goal set for this campaign, returns the following:

    ```
    [Error: No fundraising goal set.]
    ```

## $(charity.website)

Returns the website of the Charity the channel is fundraising for.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(charity.website)`

    ```
    https://www.stjudechild.org
    ```

#### Error Output

* In case there is no active Charity campaign in the channel, returns the following:

    ```
    [Error: No campaign active.]
    ```
