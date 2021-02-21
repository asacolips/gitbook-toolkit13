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
      <td style="text-align:left"><code>@str.mod</code>
      </td>
      <td style="text-align:left">
        <p>Ability score modifiers, such as +5 for a 20.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li><code>@str.mod</code> (strength)</li>
          <li><code>@dex.mod</code> (dexterity)</li>
          <li><code>@con.mod</code> (constitution)</li>
          <li><code>@int.mod</code> (intelligence)</li>
          <li><code>@wis.mod</code> (wisdom)</li>
          <li><code>@cha.mod</code> (charisma)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>@str.dmg</code>
      </td>
      <td style="text-align:left">
        <p>Ability score modifiers multipled by tier, such as +10 for a score of
          20 at 5th level.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li><code>@str.dmg</code> (strength)</li>
          <li><code>@dex.dmg</code> (dexterity)</li>
          <li><code>@con.dmg</code> (constitution)</li>
          <li><code>@int.dmg</code> (intelligence)</li>
          <li><code>@wis.dmg</code> (wisdom)</li>
          <li><code>@cha.dmg</code> (charisma)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>@lvl</code>
      </td>
      <td style="text-align:left">Your level</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>@ed</code>
      </td>
      <td style="text-align:left">The current escalation die value for the current combat/scene</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>@init</code>
      </td>
      <td style="text-align:left">Your initiative bonus</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>@std</code>
      </td>
      <td style="text-align:left">Standard bonuses for attack rolls. This is calculated as <code>@lvl+@ed+penalties</code> if
        any (such as having negative remaining recoveries).</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>@tier</code>
      </td>
      <td style="text-align:left">A number that can be used for cases where you need to multiply by tier. <code>1</code> at
        adventurer tier, <code>2</code> at champion tier, and <code>3</code> at epic
        tier.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>@wpn.m.die</code>
      </td>
      <td style="text-align:left">
        <p>The single die associated with your melee damage rolls, such as <code>d10</code>.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li><code>@wpn.m.die</code> (melee)</li>
          <li><code>@wpn.r.die</code> (ranged)</li>
          <li><code>@wpn.j.die</code> (JAB)</li>
          <li><code>@wpn.p.die</code> (PUNCH)</li>
          <li><code>@wpn.k.die</code> (KICK)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>@wpn.m.dice</code>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>The total dice per level associated with your melee damage rolls, such
          as <code>5d10</code> for a 5th level fighter with a heavy weapon.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li><code>@wpn.m.dice</code> (melee)</li>
          <li><code>@wpn.r.dice</code> (ranged)</li>
          <li><code>@wpn.j.dice</code> (JAB)</li>
          <li><code>@wpn.p.dice</code> (PUNCH)</li>
          <li><code>@wpn.k.dice</code> (KICK)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>@atk.m.bonus</code>
      </td>
      <td style="text-align:left">
        <p>The item bonus for your magic item&apos;s attack and damage rolls.</p>
        <p><b>Variants:</b>
        </p>
        <ul>
          <li><code>@atk.m.bonus</code> (melee weapons)</li>
          <li><code>@atk.r.bonus</code> (ranged weapons)</li>
          <li><code>@atk.a.bonus</code> (arcane implements)</li>
          <li><code>@atk.d.bonus</code> (divine implements)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

