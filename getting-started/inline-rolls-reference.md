# Inline Rolls Reference

## Accessing the Inline Rolls Reference Dialog

The system includes a helpful dialog to show common attributes used in inline rolls. To access it, go to the **Settings** tab of Foundry's right sidebar and then click the **Attributes and Inline Rolls Reference** button to open the dialog. It shows the most common properties used by powers in the system's included compendiums, along with an example attack roll and damage roll for martial characters.

![](../.gitbook/assets/image%20%2814%29.png)

## Where Inline Rolls Can be Placed

Inline rolls can be placed inside _any_ text or text editor field in powers you add to your character or world, along with monster actions. The parsing for inline rolls happens in chat messages during render, so you can even put them directly in the chat box!

## An Example of an Inline Roll

Before we go into detail on the available attributes, here's a few examples:

### Attack Rolls

* **Attack:** `[[d20+@str.mod+@std+@atk.m.bonus]] vs. AC` 

What that's saying is `d20` + Strength modifier + standard bonuses \(level, escalation die, attack penalties\) + melee magic item bonuses.

### Damage Rolls

* **Hit:** `[[@wpn.m.dice+@str.dmg+@atk.m.bonus]] damage` ****
* **Miss:** `[[@lvl]] damage`

Your character sheet has a setting where you can define the weapon dice associated with it, such as a d10, an the `@wpn.m.dice` attribute will be your damage dice per level, such as 5d10 for a 5th level fighter with a heavy greatsword. Similarly, `@str.dmg` will be your strength bonus multiplied per tier, such as `+8` for a strength of 18 at 5th level.

### Special Damage Rolls

But what if you have something like the cleric's Hammer of Faith ability and need to use a different damage die? There's also a `@wpn.m.die` attribute that will give you a single die, so you could do this to do your level in a different damage die:

* **Hit:** `[[(@lvl)@wpn.m.die+@str.dmg+@atk.m.bonus]] damage` 
* **Hit:** `[[(@lvl)d12+@str.dmg+@atk.m.bonus]] damage`

### Basic Math

You can also perform basic math in your rolls, such as `[[2d10*10]]` or `[[floor(d12/2)]]` 

If you need to select between two ability scores, you can use `min()` to select the lower, or `max()` to select the higher. For example:

`[[d20+max(@str.mod,@dex.mod)+@std+@atk.m.bonus]]` for a ranger's melee attack roll.

## Attributes Reference

<table>
  <thead>
    <tr>
      <th style="text-align:left">Attribute</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">@str.mod</td>
      <td style="text-align:left">
        <p>Ability score modifiers, such as +5 for a 20.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li>@str.mod (strength)</li>
          <li>@dex.mod (dexterity)</li>
          <li>@con.mod (constitution)</li>
          <li>@int.mod (intelligence)</li>
          <li>@wis.mod (wisdom)</li>
          <li>@cha.mod (charisma)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">@str.dmg</td>
      <td style="text-align:left">
        <p>Ability score modifiers multipled by tier, such as +10 for a score of
          20 at 5th level.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li>@str.dmg (strength)</li>
          <li>@dex.dmg (dexterity)</li>
          <li>@con.dmg (constitution)</li>
          <li>@int.dmg (intelligence)</li>
          <li>@wis.dmg (wisdom)</li>
          <li>@cha.dmg (charisma)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">@lvl</td>
      <td style="text-align:left">Your level</td>
    </tr>
    <tr>
      <td style="text-align:left">@ed</td>
      <td style="text-align:left">The current escalation die value for the current combat/scene</td>
    </tr>
    <tr>
      <td style="text-align:left">@init</td>
      <td style="text-align:left">Your initiative bonus</td>
    </tr>
    <tr>
      <td style="text-align:left">@std</td>
      <td style="text-align:left">Standard bonuses for attack rolls. This is calculated as <code>@lvl+@ed+penalties</code> if
        any (such as having negative remaining recoveries).</td>
    </tr>
    <tr>
      <td style="text-align:left">@tier</td>
      <td style="text-align:left">A number that can be used for cases where you need to multiply by tier. <code>1</code> at
        adventurer tier, <code>2</code> at champion tier, and <code>3</code> at epic
        tier.</td>
    </tr>
    <tr>
      <td style="text-align:left">@wpn.m.die</td>
      <td style="text-align:left">
        <p>The single die associated with your melee damage rolls, such as <code>d10</code>.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li>@wpn.m.die (melee)</li>
          <li>@wpn.r.die (ranged)</li>
          <li>@wpn.j.die (JAB)</li>
          <li>@wpn.p.die (PUNCH)</li>
          <li>@wpn.k.die (KICK)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">@wpn.m.dice</td>
      <td style="text-align:left">
        <p></p>
        <p>The total dice per level associated with your melee damage rolls, such
          as <code>5d10</code> for a 5th level fighter with a heavy weapon.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li>@wpn.m.dice (melee)</li>
          <li>@wpn.r.dice (ranged)</li>
          <li>@wpn.j.dice (JAB)</li>
          <li>@wpn.p.dice (PUNCH)</li>
          <li>@wpn.k.dice (KICK)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">@atk.m.bonus</td>
      <td style="text-align:left">
        <p>The item bonus for your magic item&apos;s attack and damage rolls.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li>@atk.m.bonus (melee weapons)</li>
          <li>@atk.r.bonus (ranged weapons)</li>
          <li>@atk.a.bonus (arcane implements)</li>
          <li>@atk.d.bonus (divine implements)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

