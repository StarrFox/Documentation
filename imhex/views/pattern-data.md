---
description: Visualize all patterns generated by the source code in the Pattern Editor View
---

# Pattern Data

<figure><img src="../.gitbook/assets/imhex_h4gXrsglWd.png" alt=""><figcaption><p>The Pattern Data View</p></figcaption></figure>

The Pattern Data View is a simple tree representation of the Patterns generated by the Pattern Language source code that has been executed in the Pattern Editor View. These two views work hand in hand. By default, the table in this view will be completely empty until any Pattern Language source code is executed and that code places any type into the loaded data throught the placement syntax.

### Structure of the patterns

The table in the Pattern Data view consists of six columns:

* `Name`: This column simply displays the name of this pattern. The name is either the name of the variable or a customized string set through the `[[name("value")]]` attribute.
* `Color`: This column shows the color of this pattern as it's highlighted in the Hex Editor View. This color is usually selected from a repeating color pallette but can also be manually assigned using the `[[color("RRGGBB")]]` attribute.
* `Offset`: This colum shows the start and end address of the pattern where it has been placed into the data.
* `Size`: This column shows the size of the pattern.
* `Type`: This column displays a formatted version of this pattern's Type name.
* `Value`: This column is the most important one as it displays the value that this pattern has decoded from the data it was placed on.

### Interacting with the patterns

Each line in the table correspons to one pattern that was generated. Simple patterns such as a `u32` will stand on their own and simply display their decoded value. Other more complicated patterns such as custom struct types might have children that can be displayed. If a pattern has any children, an arrow icon appears to the left of their name. Clicking on the name will expand the tree view of that pattern and display its children.

Clicking anywhere else on the pattern will cause the Hex Editor View to jump to the address of this pattern and select it.

When bytes are being selected in the Hex Editor View, some of the names of the patterns might turn blue. This color indicates that the current selection in the Hex Editor View overlaps with this pattern or one of its children.

### Modifying pattern values

Most built-in pattern types as well as custom types that have been attributed with the `[[format_write]]` attribute can be modifed by double clicking their `Value` field. Doing so will turn the `Value` field into a text box where the new value can be entered. Pressing the `Enter` key will cause the pattern to format the entered value and write the bytes back into the data where the pattern has been placed at.

### Visualizers

{% hint style="info" %}
TODO
{% endhint %}
