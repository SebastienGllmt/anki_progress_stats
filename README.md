# Anki Progress Stats

This is a plugin for [Anki](http://ankisrs.net/) that adds the following graphs.  You can find it listed under Anki addons [here](https://ankiweb.net/shared/info/266436365).

## Graphs

### Learned Cards

This is the number of cards that were learned.  A card is considered "learned" if it leaves the learning phase.  This ignores cards that were relearned.  This also plots the cumulative total. When this is plotted over the deck lifetime, the final cumulative total roughly equals the number of young cards plus the number of matured cards plus the number of young and mature cards that are suspended.

![Learned Cards](screenshots/learned_cards.png)

### Net Matured Cards

This is the net change in the number of matured cards, equal to the number of matured cards minus the number of cards that were mature but were forgotten.  A card is considered "matured" when its interval increases above 21 days and forgotten when its interval drop below 21 days.  This also plots the cumulative total. When this is plotted over the deck lifetime, the final cumulative total roughly equals the number of matured cards plus the number of matured cards that are suspended.

![Net Matured Cards](screenshots/net_matured_cards.png)

## Motivation

Anki includes a Review Count graph that plots the total reviews for learning, relearning, young, and mature cards.  This graph is great if you want to know how many reviews occurred in each category, but it can be difficult to understand progress using it.  Since one of the goals is to learn cards and have them eventually mature, this plugin tracks statistics for that specifically.

## Version History

* 0.1: Initial Release
* 0.2: Fix for error when no reviews
* 0.3: Fix learned cards wrong for filtered deck
* 0.4: Fix Anki yaxis tick rounding issue
* 0.5: Fix issue including relearned cards in Learned Cards graph
* 0.6: Revert recent learned cards changes pending better solution for filtered decks
* 0.7: More robust detection of learned cards
* 0.8: Improve graph performance
* 0.9: Fix calculation of matured cards due to apparent lastIvl bug in revlog table
* 0.10: Fix bug with last_ivl leading to overcounting of mature cards
* 0.11: Merged all the mature card graphs into one

## License

Copyright 2016 Matthew Hayes
Copyright 2017 Sebastien Guillemot

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
