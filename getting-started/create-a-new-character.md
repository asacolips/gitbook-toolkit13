# How to create a new Character

To make a new character go to the Actors tab and click the **Create actor** button. Choose **Character** at the prompt that appears, and then confirm. You should then see a blank sheet similar to the following. Each of the magic sections of the sheet have been annotated, and we'll go into more detail on each of them below.

![](../.gitbook/assets/image%20%284%29.png)

## Name, Level, Race, and Class

Each of these fields are at the top of your character sheet and are freeform text fields where you can enter any values you want. For races and classes, the system includes special logic to recognize the races and classes available in the SRD. For example, if you enter "Fighter" as your class, you'll have the base stats of a Fighter and will be able to import powers from the Fighter compendium. Similarly, if you enter "Paladin / Commander" or "Rogue Wizard", you'll receive base stats based on the multiclass rules, and you'll be able to import powers for either class. The system will strip out all special characters, so you can use any convention you want to separate your class names when multiclassing, such as commas, slashes, or just empty spaces. 

## Character Statistics and Settings

Several of the statistics for your character can be controlled either automatically by the system, or semi-automatically via a default value that you can change later. When making a character, your first step to assign these values is to first set your **Race**, **Class**, and **Level**. Once you pick your class, your base HP, defenses, and damage die will be set for you, but you can adjust them if needed.

{% hint style="info" %}
Calculating out stats based on class is a setting in the system under **Settings &gt; System settings &gt; Automatically compute base stats**. If you would prefer to control this manually, the GM can disable this setting.
{% endhint %}

If you would like to tweak these values, such as disabling automatic HP calculation for your character, you can go to the **Settings** tab of your character sheet to see the current values and make adjustments. This is also where you can find a number of **Special Traits** such _Quick to Fight_ for humans or _Strong Recovery_ for barbarians.

![](../.gitbook/assets/image%20%285%29.png)

### Changing Hit Points, Defenses, Recoveries, and Initiative

In the screenshot above, the **Settings** tab of the character sheet's left sidebar can be seen, along with all of the various tweaks to the sheet that you can make. Let's review the first several of those which all relate to your HP, defenses, recoveries, and initiative.

{% hint style="info" %}
Any time you change your character class to one recognized by the system \(any class from the SRD\), the stats in this section will be replaced with the value associated with that class or multiclass combination. 
{% endhint %}

* **Special Traits** - As seen in the screenshot, the "Special Traits" text next to the gear icon is a link that will open a dialog with additional tweaks that you can make. These tweaks are all special "flags" that let your character behave one way or the other, such as rolling twice for initiative with the Quick to Fight flag enabled.
* **Group by Power Type** - We'll discuss this dropdown more in the power section, but it lets you choose the order in which your class powers are grouped together.
* **Base AC** - Your base armor class before applying ability score modifiers or magic item bonuses. If you're wielding a shield, it should be included in this number.
* **Base PD** - Your base physical defense before applying ability score modifiers or magic item bonuses.
* **Base MD** - Your base mental defense before applying ability score modifiers or magic item bonuses.
* **Base HP** - Your base hit points before adding your Constitution modifier or multiplying based on your level multiplier. This field is only used if the **Calculate Max HP?** box directly below it is enabled.
* **Base Recoveries** - Your base number of recoveries per full heal up. This field is only used if the **Calculate Max Recoveries?** box immediately below it is enabled.
* **Initiative** - Additional modifiers to increase your initiative modifier by. Initiative is always calculated as Dexterity modifier + Level, but it can be adjusted further by using the _Quick to Fight_ or _Improved Initiative_ flags, along with this field to adjust the final number.

Once all of those settings are in place, you can view your stats at the top of your character sheet:

![](../.gitbook/assets/image%20%2810%29.png)

### Changing Weapon and Basic Attack Settings

In addition to the settings related to base HP and defenses, the settings tab includes options to change the following values related to your basic attacks. These values aren't directly visible on your character sheet, but they are often factored into powers related to your class in the compendiums included with the system. As with the previous section, these values will be updated if you change your class.

* **Melee Weapon Dice** - The die size that your melee attacks should use without your level included, such as a `d8` or `d10`. This will later be available in your powers in versions that automatically give you the correct number per level.
* **Ranged Weapon Dice** - The die size that your ranged attacks should use without your level included, such as a `d6` or `d8`. As with melee attacks, this will be available in your powers as versions both with and without your level.
* The following four settings are all legacy settings that are not actively in use, but some characters from older versions of the system may still have powers that reference them.
  * **Melee Ability** - The ability score associated with your basic melee attacks.
  * **Ranged Ability** - The ability score associated with your basic ranged attacks.
  * **Melee Miss Dmg.** - Whether or not your basic melee attacks should apply miss damage.
  * **Ranged Miss Dmg.** - Whether or not your basic ranged attacks should apply miss damage.

### Background, Icon, and Resource Settings

Finally, there three sections towards the bottom of your sheet settings where you can toggle the number of backgrounds and icon relationships that you have, along with enabling custom resources that your character may need to track.

* **bg1 - bg8** - These checkboxes will enable additional rows on the **Backgrounds** section of your character sheet. By default, the first three are enabled, but you can enable up to 8 separate backgrounds.
* **i1 - i5** - These checkboxes will enable additional rows on the **Icon Relationships** section of your character sheet. By default, the first three are enabled, but you can enable up to 5 separate icon relationships.
* **Custom Resource 1 - 3**: These checkboxes will enable additional custom resources, which have a current value, a maximum value, and a customizable label. They will appear directly below the saving throws and disengage section of your character sheet.

## Ability Scores

The ability scores for your character are in the first section of the character sheet's left sidebar, under the **Abilities** tab.

* **Ability Name** - Each score has a clickable name that can be used to make ability check rolls, including an option to select a relevant background and apply modifiers.
* **Ability Score** - Your ability scores are the center column of numbers, which are editable. These default to 10 until you change them.
* **Ability Modifier** - Your raw ability modifier, such as +4 on a score of 18, is in the left column of numbers. This number is calculated.
* **Ability Modifier + Level** - Your ability modifier plus your current level, such as +6 on a score of 18  for a level 2 character, is in the right column of numbers. This number is calculated.

![](../.gitbook/assets/image%20%286%29.png)

## Backgrounds

You can choose how many backgrounds your character has in the **Settings** tab of the character sheet, up to a total of 8 backgrounds. Each background has two parts:

* **Bonus** - The number of points in the background that will apply as a bonus to relevant ability checks.
* **Name** - The name of the background, which can be any text that you want.

 

![](../.gitbook/assets/image%20%289%29.png)

## Icon Relationships

You can choose how many icon relationships your character has in the **Settings** tab of the character sheet, up to a total of 5 icon relationships. Each icon relationship has 4 parts.

* **Dice Icon** - The dice icon for each relationship can be clicked to roll the relationship.
* **Relationship Type** - The relationship type dropdown lets you choose between positive, conflicted, and negative relationships.
* **Relationship Points** - The total number of points you have in an icon relationship.
* **Icon Name** - The icon this relationship applies to.

![](../.gitbook/assets/image%20%288%29.png)

## One Unique Thing

Your character's One Unique Thing is in the bottom left corner of the sheet, and is a freeform text area where you can place any content you need to describe it.

![](../.gitbook/assets/image%20%287%29.png)

## Saves, Disengage, Initiative

TODO

## Momentum, Ki, Command Points, and Custom Resources

TODO

## Powers

TODO

## Biography

TODO

## Equipment and Magic ITems

TODO



