# Third party module integrations

The following Modules have explicit integration or support with the System

### 🌑Dungeon Moon: Encounter Builder

![](https://raw.githubusercontent.com/cswendrowski/FoundryVTT-Encounter-Builder/master/dungeonmoon_cover.png)

🌑Dungeon Moon has built-in support for loading the included SRD monsters, as well as any Actors you have defined in your world. It uses the SRD rules for building a fair encounter, enabling GM's to guickly and easily build up ambushes, chance encounters, or the next session's foes.

See it in action here: https://www.patreon.com/posts/dungeon-moon-45469551

https://github.com/cswendrowski/FoundryVTT-Encounter-Builder


### Arbron's Improved HP Bar

![](https://raw.githubusercontent.com/arbron/fvtt-hp-bar/main/images/temp.webp)

Temporary health will be rendered in the Token's bars

https://github.com/arbron/fvtt-hp-bar


### Iconic Relationship Point Card Support

As of 1.7.0, Iconic Relationship points can automatically give out Cards that represent them using this module: 

[https://github.com/spacemandev-git/fvtt-card-support](https://github.com/spacemandev-git/fvtt-card-support)

![](https://cdn.discordapp.com/attachments/718595753852797012/746472772162814082/mageflame_icon_cards.gif)

Card support works with any SDF \(Standard Deck Format\) deck. You can use your own custom Icons and Cards so long as the Icon Relationship name in your Actor field matches the name in the metadata on the deck

Example from the included Mageflame Tarot Card SDF deck

[https://github.com/Mageflame/Toolkit13/raw/alpha/Mageflame%20Tarot%20Cards.zip](https://github.com/Mageflame/Toolkit13/raw/alpha/Mageflame%20Tarot%20Cards.zip)

```yaml
name: The Gatekeeper 5
img: The Gatekeeper 5.jpg
back: The Gatekeeper 6.jpg
data:
    value: 5
    icon: The Gatekeeper
---
name: The Gatekeeper 6
img: The Gatekeeper 6.jpg
back: The Gatekeeper 5.jpg
data:
    value: 6
    icon: The Gatekeeper
```

For instructions on how to load the SDF deck, please see the Card Support documentation.

Once loaded, if a match is found on Iconic Relationship rolls, the correct cards will be dealt to players.

{% hint style="warning" %}
As of time of writing, Card Support **requires** a GM to be logged in to work.
{% endhint %}

