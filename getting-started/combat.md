# Running combat

### How to Start and Run a Combat

\(this section is WIP, needs revision\)

1. Select everyone, roll for initiative, add to combat
2. Process first player

    A. Choose power/attack

    B. Select targets on map

    C. Click on selected power/attack

    D. If hit/effect, right-click on effect to apply to targets

### **Attack and Targeting Automation**

Recommended Addons:

* [https://foundryvtt.com/packages/easy-target/](https://foundryvtt.com/packages/easy-target/)
* [https://foundryvtt.com/packages/target-enhancements/](https://foundryvtt.com/packages/target-enhancements/)

Both Player Powers and Monster Attacks often have "Triggers" - things like "Natural 15+", "Natural Even", "Natural Odd Hit".

For Triggers that rely only on the Natural roll such as "Natural 15+" or "Natural Even", they will always execute when rolled

// TODO: Image

For Triggers that rely on Hitting / Missing, the System will only evaluate the Trigger if 1+ Targets are selected. In the case of multiple Targets, each Target is evaluated separately for hits / misses, which is displayed in the final Chat message. For powers such as "1d3 in a group", you can select the max number \(3\) in the preference you want to hit them, and the System will pick them in that order in cases you roll less than max. If your target is random such as "1d3 random enemies in a group", the System will randomly pick instead.

// TODO: Image

Trigger evaluation is powered by Natural Language Processing \(regexes, not full NLP AI\) - all you need to do is type the power using the words we support.

### **Target Amount**

| Trigger | Example Text | Description |
| :--- | :--- | :--- |
| Default | "far away target", "far away targets", "nearby target" | Checks attack against all selected targets |
| Amount | "1 nearby target", "3 nearby targets" | If more than specified number of targets is selected, only up to X \(in the order of selection\) is checked |
| Variable Amount | "\[\[d2 + 2\]\] nearby targets", "\[\[d3\]\] nearby targets in a group" | Evaluates the roll, then executes as if \#2 |
| Random Selection | "3 random nearby targets", "\[\[d3\]\] random far away targets" | As \#3, except the targets are picked randomly instead of in-order |

### **Natural Roll Triggers**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Trigger</b>
      </th>
      <th style="text-align:left">Example Text</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Always</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>&quot;Always:&quot;</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>Always triggers</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Hit</td>
      <td style="text-align:left">
        <p></p>
        <p>&quot;Natural even hit:&quot;, &quot;Hit:&quot;, &quot;Natural Hit:&quot;</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>Triggers when the natural attack roll matches or beats the target&apos;s
          defense</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Miss</td>
      <td style="text-align:left">&quot;Natural even miss:&quot;, &quot;Miss:&quot;, &quot;Natural Miss:&quot;</td>
      <td
      style="text-align:left">Triggers when the natural attack roll is less than the target&apos;s defense</td>
    </tr>
    <tr>
      <td style="text-align:left">Even</td>
      <td style="text-align:left">&quot;Natural even:&quot;, &quot;Natural Even:&quot;</td>
      <td style="text-align:left">Triggers with the natural attack roll is even</td>
    </tr>
    <tr>
      <td style="text-align:left">Odd</td>
      <td style="text-align:left">&quot;Natural odd:&quot;, &quot;Natural Odd:&quot;</td>
      <td style="text-align:left">Triggers with the natural attack roll is odd</td>
    </tr>
    <tr>
      <td style="text-align:left">X+</td>
      <td style="text-align:left">&quot;Natural 6+:&quot;, &quot;Natural 11+:&quot;</td>
      <td style="text-align:left">Triggers when the natural attack roll matches or beats the target number
        such as 6</td>
    </tr>
    <tr>
      <td style="text-align:left">X</td>
      <td style="text-align:left">&quot;Natural 1:&quot;, &quot;Natural 20:&quot;, &quot;Natural 10:&quot;</td>
      <td
      style="text-align:left">Triggers when the natural attack roll exactly matches the target number
        such as 10</td>
    </tr>
    <tr>
      <td style="text-align:left">Crit</td>
      <td style="text-align:left">&quot;Crit:&quot;</td>
      <td style="text-align:left">Shorthand for &quot;Natural 20&quot;</td>
    </tr>
  </tbody>
</table>

### **Damage / Healing menu**

You can right click a non-Attack roll to open a Context menu. This menu allows you to apply the roll as straight damage, half damage, double damage, triple damage, healing, or temporary health.

// TODO: Image

Please note that this will apply to the **Selected** token\(s\), ensuring that players can only apply damage to Tokens they control. The GM, as always, can select everything.



