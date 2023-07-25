# Top Languages Card

The top languages card shows a GitHub user's most frequently used languages.


### Usage

Copy-paste this code into your readme and change the links.

Endpoint: `api/top-langs?username=anuraghazra`

```md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=anuraghazra)](https://github.com/anuraghazra/github-readme-stats)
```

### Language stats algorithm

We use the following algorithm to calculate the languages percentages on the language card:

```js
ranking_index = (byte_count ^ size_weight) * (repo_count ^ count_weight)
```

By default, only the byte count is used for determining the languages percentages shown on the language card (i.e. `size_weight=1` and `count_weight=0`). You can, however, use the `&size_weight=` and `&count_weight=` options to weight the language usage calculation. The values must be positive real numbers. [More details about the algorithm can be found here](https://github.com/anuraghazra/github-readme-stats/issues/1600#issuecomment-1046056305).

*   `&size_weight=1&count_weight=0` - *(default)* Orders by byte count.
*   `&size_weight=0.5&count_weight=0.5` - *(recommended)* Uses both byte and repo count for ranking
*   `&size_weight=0&count_weight=1` - Orders by repo count

```md
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=anuraghazra&size_weight=0.5&count_weight=0.5)
```
!!! warning
    By default, the language card shows language results only from public repositories. To include languages used in private repositories, you should [deploy your own instance](#deploy-on-your-own) using your own GitHub API token.

!!! note
    Top Languages does not indicate the user's skill level or anything like that; it's a GitHub metric to determine which languages have the most code on GitHub. It is a new feature of github-readme-stats.

!!! warning
    This card shows languages usage only inside your own non-forked repositories, not depending from who is the author of the commits. It does not include your contributions into another users/organizations repositories. Currently there are no way to get this data from GitHub API. If you want this behavior to be improved you can support [this feature request](https://github.com/orgs/community/discussions/18230) created by [@rickstaa](https://github.com/rickstaa) inside GitHub Community.

    #### Language Card Exclusive Options

*   `hide` - Hides the languages specified from the card *(Comma-separated values)*. Default: `[] (blank array)`.
*   `hide_title` - *(boolean)*. Default: `false`.
*   `layout` - Switches between five available layouts `normal` & `compact` & `donut` & `donut-vertical` & `pie`. Default: `normal`.
*   `card_width` - Sets the card's width manually *(number)*. Default `300`.
*   `langs_count` - Shows more languages on the card, between 1-20 *(number)*. Default: `5` for `normal` and `donut`, `6` for other layouts.
*   `exclude_repo` - Excludes specified repositories *(Comma-separated values)*. Default: `[] (blank array)`.
*   `custom_title` - Sets a custom title for the card *(string)*. Default `Most Used Languages`.
*   `disable_animations` - Disables all animations in the card *(boolean)*. Default: `false`.
*   `hide_progress` - Uses the compact layout option, hides percentages, and removes the bars. Default: `false`.
*   `size_weight` - Configures language stats algorithm *(number)* (see [Language stats algorithm](#Language-stats-algorithm)), defaults to 1.
*   `count_weight` - Configures language stats algorithm *(number)* (see [Language stats algorithm](#Language-stats-algorithm)), defaults to 0.

> [!WARNING]\
> Language names should be URI-escaped, as specified in [Percent Encoding](https://en.wikipedia.org/wiki/Percent-encoding)
> (i.e: `c++` should become `c%2B%2B`, `jupyter notebook` should become `jupyter%20notebook`, etc.) You can use
> [urlencoder.org](https://www.urlencoder.org/) to help you do this automatically.