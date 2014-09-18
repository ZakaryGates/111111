# Introduction

In order to translate the Blockly language, we need to add descriptions for every piece of text currently displayed in English.  There are 343 such messages, which are too many for the core Blockly team to mark up themselves.  We are looking for volunteers who are experienced with Blockly to help add descriptions to these messages.

# Background

Please read [The Blockly Language](https://translatewiki.net/wiki/Translating:Blockly#The_Blockly_Language) within [the Blockly translation instructions](https://translatewiki.net/wiki/Translating:Blockly#The_Blockly_Language) on Translatewiki.  This describes each of the types of text that appear in the language file:
  * block text
  * block input text
  * tooltip
  * context menu
  * url
  * dropdown choice
  * prompt
  * button
It is possible that there are other types I have not yet categorized.

# Examples

I have written descriptions for 43 messages.  See https://code.google.com/p/blockly/source/browse/branches/i18n/language/en/messages.js.

The general format is:
```
/** @desc <TYPE OF TEXT> - <DESCRIPTION OF TEXT FOR TRANSLATOR> */
Blockly.<MESSAGE NAME> = goog.getMsg("<ENGLISH TEXT OF MESSAGE>");
```

For example, the following definition of MSG\_DUPLICATE\_BLOCK indicates that the English-language text "Duplicate" appears on a "context menu" and that the user selects it in order to "make a duplicate of the selected block".

```
/** @desc context menu - make a duplicate of the selected block */
Blockly.MSG_DUPLICATE_BLOCK = goog.getMsg("Duplicate");
```

Descriptions can contain [wikitext](https://www.mediawiki.org/wiki/Help:Formatting), which will be properly displayed to the translator.  Specifically, you can include links to further information, as in this example:

```
/** @desc tooltip - how if statements work (see [https://code.google.com/p/blockly/wiki/If_Then]) */
Blockly.LANG_CONTROLS_IF_TOOLTIP_1 = goog.getMsg("If a value is true, then do some blocks");
```

Descriptions may also contain bold text, indicated by pairs of 3 single quotes, to show how a word might be used in a sentence:

```
/** @desc block text - if (as in: '''if''' there is a path to the right, turn right). */
Blockly.LANG_CONTROLS_IF_MSG_IF = goog.getMsg("if");
```

Descriptions may not include double quotes(").

# Sections

| **Name** | **# messages** | **corresponding source code** | **author** | **status** |
|:---------|:---------------|:------------------------------|:-----------|:-----------|
| context menus | 12             | [block.js](https://code.google.com/p/blockly/source/browse/trunk/core/block.js) | Ellen      | done       |
| variable renaming| 5              | [variables.js](https://code.google.com/p/blockly/source/browse/trunk/core/variables.js) | Ellen      | done       |
| colour   | 16             | [colours.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/colour.js) | Ellen      | done       |
| controls: if | 15             | [control.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/control.js) | Ellen      | done       |
| controls: repeat, while | 11             | [control.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/control.js) | --         | --         |
| controls: for, foreach, control flow | 19             | [control.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/control.js) | --         | --         |
| logic    | 27             | [logic.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/logic.js) | --         | --         |
| math     | 77             | [math.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/math.js) | --         | --         |
| text     | 56             | [text.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/text.js) | --         | --         |
| lists    | 70             | [lists.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/lists.js) | --         | --         |
| variables | 10             | [variables.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/variables.js) | Alexandros | in progress |
| procedures | 24             | [procedures.js](https://code.google.com/p/blockly/source/browse/trunk/language/common/procedures.js) | --         | --         |

# Steps

To volunteer:
  1. Visit and read through the file [messages.js](https://code.google.com/p/blockly/source/browse/branches/i18n/language/en/messages.js) to see how descriptions are written.
  1. Decide on a section you would like to volunteer for.
  1. Write descriptions for a few of the messages.
  1. Post a message to the [Blockly discussion group](https://groups.google.com/forum/?fromgroups#!forum/blockly) (or send it directly to me) with the above information and how long the work would take you.

Tips for translating messages:
  * If you're not sure how the message is used, play around with the [code application](https://blockly-demo.appspot.com/static/apps/code/index.html) and/or view the source code.
  * If a message consists of two (or more) strings joined by a plus sign, please combine them into a single string.
  * You can make additions to [the Blockly translation instructions](https://translatewiki.net/wiki/Translating:Blockly#The_Blockly_Language).
  * If you run into trouble, ask for help.

Also feel free to suggest improvements to the descriptions I wrote.