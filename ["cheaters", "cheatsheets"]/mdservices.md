
[Source](https://raw.githubusercontent.com/nhatthanh310895/cheaters/master/cheaters/cheatsheets/towergit.html "Permalink to ")

[Source][1]

### Markdown Service Tool

**The following Services are included:**

* md - Code - Make Code Block
* md - Convert - HTML to Clipboard
* md - Convert - HTML to Markdown
* md - Convert - MultiMarkdown to HTML
* md - Convert - MultiMarkdown to RTF
* md - Emphasis - Bold
* md - Emphasis - Italics
* md - Footnotes - Convert Inline Format
* md - Footnotes - Make IDs Unique
* md - Indentation - Indent
* md - Indentation - Outdent
* <del>md - Links - Auto-link web search</del>
* md - Links - Auto-link Wikipedia
* md - Links - Chrome Tabs
* md - Links - Clipboard
* md - Links - Flip Link Style
* md - Links - New Link
* md - Links - Safari Tabs
* md - Links - Self-Link URLs
* md - Links - To References
* md - Lists - Bullet List
* md - Lists - Fix Numbered List
* md - Lists - Numbered List
* md - Paragraphs - Blockquote
* md - Paragraphs - Compress Empty Lines
* md - Paragraphs - Preserve Line Breaks
* md - Paragraphs - Unwrap
* md - Tables - Cleanup
* md - Wrap - Angle Brackets
* md - Wrap - Parenthesis
* md - Wrap - Square Brackets

Note: _some Services are only available when text is selected, and some only when no text is selected but a text field is focused._

### Descriptions

_The suggested key bindings in each description are just what work for me, personally; there's no consequence for using something completely different. Just be aware that an application's default keyboard commands will override any in the Services menu, so a command's shortcut may become unavailable if it's already in use by the current application._

#### Conversion/Rendering

Convert - HTML to Clipboard
: This service does the same thing as "MultiMarkdown to HTML," but leaves the selection alone and copies the resulting HTML directly to the clipboard.

:

**Suggested key bindings:** Command-Shift-Option-C

Convert - HTML to Markdown
: This Service "Markdownifies" HTML source, creating readable Markdown from it. It does not work directly on Rich Text, but if you use it on the source of a web page it will do its best to recreate the document in clean Markdown.

Convert - MultiMarkdown to HTML
: Processes the selected text through Markdown and SmartyPants to generate clean, typographically correct HTML. The selected text is replaced with the final HTML, but if you want both you can select it again, copy it (Command-C) and then Undo (Command-Z) to get the original text back. Markdown and SmartyPants are bundled in this Service, so no external installation is required.

Convert - MultiMarkdown to RTF
: This Service does an in-place conversion to styled text in any field that handles Rich Text. It's ideal for writing an email in Markdown and converting it directly in the field before sending.

:

See [this post][2] for more information and requirements. _Full credit to [Tobias O'Leary][3] for figuring out this magic._

Footnotes - Convert Inline Format
: Allows you to write footnotes inline using `(*This is a footnote*)` syntax and converts them to standard MultiMarkdown footnotes when run on the full text of the document. Works with multi-paragraph footnotes, keeps markers unique and recognizes existing footnote ids.

:

You can also use `([*marker] This is a footnote*)` to define a custom name for the footnote.

Footnotes - Make IDs Unique
: When working on short documents — such as blog posts — that will be combined with other documents on a page, footnotes can end up with conflicting names or ids. This service, when run on the full text of a single document, will update all existing footnote pairs with a unique, time-based string to avoid any conflicts with other documents.

#### Linking

Links - Auto-link web search (deprecated)
: This Service has been superceded by [SearchLink][4].

Links - Auto-link Wikipedia
: This Service takes the selected text and runs an immediate Wikipedia search for it. The first returned link is inserted with inline link syntax. It works well for unique words (application names, famous people, unusual words).

Links - Chrome Tabs/Safari Tabs
: These Services will collect all of the tabs in the foreground Safari or Chrome window (respectively), and generate a reference list in the same fashion as Link List From Clipboard. **These Services are only available when no text is selected.**

Links - Clipboard
: Copy text containing links to the clipboard (in any format, even embedded within other text) and this Service will find all of the links and generate a "reference-style" list of the urls, with titles you can then refer to in your document using [`link text][title]` syntax. It creates short titles based on the domain of the url, and adds incrementing numbers to duplicate titles to differentiate. **This Service is only available when no text is selected.**

:

**Suggested key bindings:** Control-Option-V, or run it from the Services menu

Links - Flip Link Style
: This Service uses [formd][5] to guess what the primary format of links (inline or reference) in the document currently is and reverse it. If your document is mostly inline links, this will turn them into numbered reference links, and vice versa. _It can be messy if you use footnotes._

Links - New Link
: This will surround the selected text with inline link syntax, and if there's a single url in the clipboard, will link it automatically. Otherwise, it will create a shell ([`link text]()`) with an empty parenthesis pair for you to paste a url into.

:

**Suggested key bindings:** Command-Shift-L

Links - Self-Link URLs
: This will search your selection for urls that aren't currently part of an HTML or Markdown link and surround them with angle brackets (`&lt;&gt;`). This makes the URL itself a hyperlink when converting to HTML or other formats.

Links - To References
: Select the entire text of a Markdown document with inline links (or a mix of inline and reference links) and run this service to have your links replaced with the reference title format ([`link text][title]`) and the references placed at the end of the document. Existing references will be preserved, and titles for new references will be automatically generated based on the domain name.

#### Lists

Lists - Bullet List/Numbered List
: These two commands create and clean up bulleted and ordered lists. They will remove any current list characters at the beginning of each line, compress blank lines in the selection, fix minor indentation mistakes while maintaining the original structure of the list, and properly increment the leading characters of ordered lists. Just select multiple lines and run one of the Services.

:

**Suggested key bindings:** Command-Shift–1 (ordered list) and Command-Shift–8 (unordered list)

Lists - Fix Numbered List
: Fixes numerical order and indentation in MultiMarkdown lists.

#### Paragraphs

Paragraphs - Blockquote
: This service will look for tab indents at the beginning of each line and assume they define the depth of a quote. Tabs at the beginning of each line will be replaced with "&gt;" characters.

Paragraphs - Compress Empty Lines
: Compresses consecutive newlines into a single blank line, good for cleaning up documents after formatting.

Paragraphs - Preserve Line Breaks
: In Markdown, text without blank lines between it is concatenated into one continuous paragraph, removing line breaks. This is prevented by three spaces at the end of each line, and this Service just adds the spaces to the end of each selected line of text.

Paragraphs - Unwrap
: Removes single line breaks within the selection to remove the effects of "hard wrapping." It doesn't change the way the final document renders, but it makes the original Markdown document much more readable on variable-width screens.

#### Tables

Tables - Cleanup
: Based on the Perl script by Fletcher Penney, this Service will take MultiMarkdown-format tables and clean them up to be readable in plain text.

#### Misc.

Code - Make Code Block
: Indents the selection by 5 spaces, creating a code (or poetry) block that preserves line breaks and indentations. This format is recognized by all Markdown processors.

Emphasis - Bold/Italics
: These simply wrap selected text in Markdown emphasis syntax. `*` for italics, `**` for bold.

:

**Suggested key bindings:** Command-Shift-B (bold) and Command-Shift-I (italics)

Indentation - Indent/Outdent
: These Services shift the beginning of all selected lines to the left or right by 4 spaces. Useful for manipulating sections of lists to create nested portions.

:

**Suggested key bindings:** Command-Shift-] (indent) and Command-Shift-[ (outdent)

Wrap - Angle Brackets/Parenthesis/Square Brackets
: These services wrap the selected text in angle brackets (`&lt;&gt;`), parenthesis (`()`) or square brackets (`[]`). To be useful, they need intuitive shortcuts assigned for quick triggering. You may also consider using [keybindings][6] for this.

### Installation

For more information, see [Stephen Margheim's post at Hackademic][7].

Simply drag the Services you want to use into `~/Library/Services` (where ~ represents your user's home folder). You will have to enable the Services manually in the Keyboard Shortcuts preference pane of System Preferences. Locate them in the list and check the box to the left. You may have to restart running applications to get them to show up. They will become available in the **Application Menu-&gt;Services** menu, as well as from the right/Control-click contextual menu, under the Services submenu (Snow Leopard).

For more information, see my article on [installing System Services][8].

#### Customizing key bindings

To add keyboard shortcuts to your Services, open System Preferences and choose the Keyboard Shortcuts tab at the top. Sometimes there's a delay when loading this tab as OS X indexes all of the available applications and services. Click on the Services item in the left side of the panel, and then locate your new Service on the right. Note that you can use the checkboxes you see there to enable and disable Services without having to remove them from the Services folder.

![System Preferences - Keyboard Screenshot}][9]System Preferences - Keyboard Screenshot}

Double click in the blank, white area to the right of your Service, as shown with the arrow in the image. When the blank area turns into a text field, press the key combination you want to use to activate the Service. Use a combination of modifier keys (Command, Shift, Control, Option) and a letter or number. If the combination is available (not used by another Service or existing system shortcut), the input field will disappear and be replaced by your new shortcut. If it doesn't do anything, you'll need to try a different combination of keys.

If you see a yellow "warning" triangle next to your Service, it means that there is another Service or Application Shortcut using that key combination, but it let you add it anyway. This can cause odd results, but mostly just results in neither shortcut doing anything if both associated actions are available at any given time. Sometimes, if one action is only available in one place, and the other in another place, it can be useful to have the same shortcut on related actions. If you're not sure what's conflicting, it's safest just to change your shortcut and avoid the warning.

### End note

The original Markdown Service Tools were created in Perl, Bash and Ruby and made into Services using [ThisService][10]. I found the Services [created by Automator][11] in Snow Leopard to be a bit slow, but have switched to using Automator for newer Services created in Lion and later. All Services sometimes lag on the first run, but are quite fast for me after first use.

For more Markdown goodness, check out [nvALT][12] and, if you're a TextMate user, have a look at the [Blogsmith Bundle][13] ([docs][14]). There are a lot of timesaving tricks in there!

[1]: http://brettterpstra.com/projects/markdown-service-tools/ "Permalink to Markdown Service Tools - BrettTerpstra.com"
[2]: /2013/03/08/new-in-the-markdown-service-tools-in-place-markdown-to-rtf/
[3]: http://twitter.com/tobiasoleary
[4]: /projects/searchlink/
[5]: https://github.com/drbunsen/formd
[6]: http://brettterpstra.com/2011/11/15/keybindings-new-improved-surround-commands/
[7]: http://hackademic.postach.io/post/download-and-install-the-markdown-service-tools
[8]: /howtos/install-an-os-x-system-service/
[9]: http://cdn3.brettterpstra.com/images/grey.gif
[10]: http://wafflesoftware.net/thisservice/
[11]: http://macosxautomation.com/services/index.html
[12]: /projects/nvalt/
[13]: http://github.com/ttscoff/blogsmith-tmbundle/
[14]: http://bundle.weblogzinc.com/
  