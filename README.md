# Description

This is another GPT3-based chatbot project.

It's inspired by a few things:
- GPT3 few-shot abilities make me able to solve a few required task (dialogue generation itself, character wiki page summarization, search result summarization, etc) just by telling it what to do with minimal example
- There was a few works showing GPT can use hints from external search engine (so at first it generate search request in specified format and after second pass having hints from seach system - make an answer). So it can retrieve fictional setting-specific information by search through external systems - wikis in my case
- During with it I found that chain reasoning can help too. Like - a character from Fallout universe probably shouldn't know about Warhammer Fantasy warpstone, should it? Well, without chain reasoning it were generating texts like "It's a mineral found in the Big MT, it's magical properties is ...", which is absurd. But with it...

```
[DIALOGUE]
Coorier: Did you ever heard about the warpstone
(machine generation here)
[REASONING]
[UNIVERSE] Probably warpstone comes from Warhammer universe
[KNOWLEDGE] As a Fallout character it's almost impossible Ulysses know about Warhammer or it's warpstone
[SEARCH] fallout warpsone
[ANSWER] Ulysses: Let me think
```
```
[HINTS]
fallout warpstone: nothing found
[DIALOGUE]
Coorier: Did you ever heard about the warpstone
(machine generation here)
[REASONING]
[UNIVERSE] Probably warpstone comes from Warhammer universe
[KNOWLEDGE] As a Fallout character it's almost impossible Ulysses know about Warhammer or it's warpstone
[SEARCH] fallout warpsone
[ANSWER] Ulysses: No, never heard about it. Another mineral found by that Old World remnants in the Big MT?
```

# Running

To run this thing you'll need 2 things
- OpenAI api key
- Google Custom Search search system configured to search through required sites (I used *.fandom.com wiki sites)

![Dialogue with chatbot on Fallout New Vegas Ulysses's preset](/screenshot.png)
