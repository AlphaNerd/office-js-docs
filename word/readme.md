
# Word JavaScript APIs

Welcome to the Word JavaScript API open specification documentation. The Word JavaScript API provides Word-specific functionality related to documents, paragraphs, content controls, and other common Word objects. This API complements the functionality of our existing Office.js library. This branch documents the new APIs that our team is working on and plans to ship in the next few months.

In order to try the Preview APIs in Word Desktop, please make sure to: 

1. Get on the First Release so you can get the latest Word! Follow the instructions here: https://github.com/OfficeDev/office-js-docs/blob/215f5d35490c943cc06c29b98357ba8cb034ec81/docs/develop/install-latest-office-version.md
2. Use the PREVEW CDN for OFfice.js:https://appsforoffice.microsoft.com/lib/beta/hosted/office.js
3. Code and provide feedback!!!

To try the Preview APIs in Word Online, you can skip the first step above, and use the Preview CDN for Office.


## Introduction to Word JavaScript API 1.3 

This section describes the new set of Word JavaScript APIs that are planned for the next release (requirement set 1.3). To provide feedback on the new APIs, use the links in the following table to open issues in GitHub. 

_**Note**: The features listed are still in the design and review phase and are not yet available as part of the product. The final design is subject to change. When the feature is made available, the final specification will be published as part of the master repository._

### FEATURES
|Object                   | What is new        | Description                                         |Req. Set|
|:------------------------|:-------------------|:----------------------------------------------------|:-------|
|[body](../reference/word/body.md)|_Property_ > styleBuiltIn|Gets or sets the built-in style name for the body. Use this property for built-in styles that are portable between locales. To use custom styles or localized style names, see the "style" property. Possible values are: Other, Normal, Heading1, Heading2, Heading3, Heading4, Heading5, Heading6, Heading7, Heading8, Heading9, Toc1, more...|1.3|
|[body](../reference/word/body.md)|_Property_ > type|Gets the type of the body. The type can be 'MainDoc', 'Section', 'Header', 'Footer', or 'TableCell'. Read-only. Possible values are: Unknown, MainDoc, Section, Header, Footer, TableCell.|1.3|
|[body](../reference/word/body.md)|_Property_ > lists|Gets the collection of list objects in the body. Read-only.|1.3|
|[body](../reference/word/body.md)|_Property_ > parentBody|Gets the parent body of the body. For example, a table cell body's parent body could be a header. Throws if there isn't a parent body. Read-only.|1.3|
|[body](../reference/word/body.md)|_Property_ > parentBodyOrNullObject|Gets the parent body of the body. For example, a table cell body's parent body could be a header. Returns a null object if there isn't a parent body. Read-only.|1.3|
|[body](../reference/word/body.md)|_Property_ > parentContentControlOrNullObject|Gets the content control that contains the body. Returns a null object if there isn't a parent content control. Read-only.|1.3|
|[body](../reference/word/body.md)|_Property_ > parentSection|Gets the parent section of the body. Throws if there isn't a parent section. Read-only.|1.3|
|[body](../reference/word/body.md)|_Property_ > parentSectionOrNullObject|Gets the parent section of the body. Returns a null object if there isn't a parent section. Read-only.|1.3|
|[body](../reference/word/body.md)|_Property_ > tables|Gets the collection of table objects in the body. Read-only.|1.3|
|[body](../reference/word/body.md)|_Method_ > [getRange(rangeLocation: string)](../reference/word/body.md#getrangerangelocation-string)|Gets the whole body, or the starting or ending point of the body, as a range.|1.3|
|[body](../reference/word/body.md)|_Method_ > [insertTable(rowCount: number, columnCount: number, insertLocation: string, values: string[][])](../reference/word/body.md#inserttablerowcount-number-columncount-number-insertlocation-string-values-string)|Inserts a table with the specified number of rows and columns. The insertLocation value can be 'Start' or 'End'.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > styleBuiltIn|Gets or sets the built-in style name for the content control. Use this property for built-in styles that are portable between locales. To use custom styles or localized style names, see the "style" property. Possible values are: Other, Normal, Heading1, Heading2, Heading3, Heading4, Heading5, Heading6, Heading7, Heading8, Heading9, Toc1, more...|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > subtype|Gets the content control subtype. The subtype can be 'RichTextInline', 'RichTextParagraphs', 'RichTextTableCell', 'RichTextTableRow' and 'RichTextTable' for rich text content controls. Read-only. Possible values are: `RichText` Identifies a rich text content control.,`Unknown` ,`RichTextInline` ,`RichTextParagraphs` ,`RichTextTableCell` contains whole cell,`RichTextTableRow` contains whole row,`RichTextTable` contains whole table,`PlainTextInline` ,`PlainTextParagraph` ,`Picture` ,`BuildingBlockGallery` ,`CheckBox` ,`ComboBox` ,`DropDownList` ,`DatePicker` ,`RepeatingSection` ,`PlainText` |1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > lists|Gets the collection of list objects in the content control. Read-only.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > parentBody|Gets the parent body of the content control. Read-only.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > parentContentControlOrNullObject|Gets the content control that contains the content control. Returns a null object if there isn't a parent content control. Read-only.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > parentTable|Gets the table that contains the content control. Throws if it is not contained in a table. Read-only.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > parentTableCell|Gets the table cell that contains the content control. Throws if it is not contained in a table cell. Read-only.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > parentTableCellOrNullObject|Gets the table cell that contains the content control. Returns a null object if it is not contained in a table cell. Read-only.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > parentTableOrNullObject|Gets the table that contains the content control. Returns a null object if it is not contained in a table. Read-only.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Property_ > tables|Gets the collection of table objects in the content control. Read-only.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Method_ > [getRange(rangeLocation: string)](../reference/word/contentcontrol.md#getrangerangelocation-string)|Gets the whole content control, or the starting or ending point of the content control, as a range.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Method_ > [getTextRanges(endingMarks: string[], trimSpacing: bool)](../reference/word/contentcontrol.md#gettextrangesendingmarks-string-trimspacing-bool)|Gets the text ranges in the content control by using punctuation marks andor other ending marks.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Method_ > [insertTable(rowCount: number, columnCount: number, insertLocation: string, values: string[][])](../reference/word/contentcontrol.md#inserttablerowcount-number-columncount-number-insertlocation-string-values-string)|Inserts a table with the specified number of rows and columns into, or next to, a content control. The insertLocation value can be 'Start', 'End', 'Before' or 'After'.|1.3|
|[contentControl](../reference/word/contentcontrol.md)|_Method_ > [split(delimiters: string[], multiParagraphs: bool, trimDelimiters: bool, trimSpacing: bool)](../reference/word/contentcontrol.md#splitdelimiters-string-multiparagraphs-bool-trimdelimiters-bool-trimspacing-bool)|Splits the content control into child ranges by using delimiters.|1.3|
|[contentControlCollection](../reference/word/contentcontrolcollection.md)|_Method_ > [getByIdOrNullObject(id: number)](../reference/word/contentcontrolcollection.md#getbyidornullobjectid-number)|Gets a content control by its identifier. Returns a null object if there isn't a content control with the identifier in this collection.|1.3|
|[contentControlCollection](../reference/word/contentcontrolcollection.md)|_Method_ > [getByTypes(types: ContentControlType[])](../reference/word/contentcontrolcollection.md#getbytypestypes-contentcontroltype)|Gets the content controls that have the specified types andor subtypes.|1.3|
|[contentControlCollection](../reference/word/contentcontrolcollection.md)|_Method_ > [getFirst()](../reference/word/contentcontrolcollection.md#getfirst)|Gets the first content control in this collection. Throws if this collection is empty.|1.3|
|[contentControlCollection](../reference/word/contentcontrolcollection.md)|_Method_ > [getFirstOrNullObject()](../reference/word/contentcontrolcollection.md#getfirstornullobject)|Gets the first content control in this collection. Returns a null object if this collection is empty.|1.3|
|[customProperty](../reference/word/customproperty.md)|_Property_ > key|Gets the key of the custom property. Read only. Read-only.|1.3|
|[customProperty](../reference/word/customproperty.md)|_Property_ > type|Gets the value type of the custom property. Read only. Read-only. Possible values are: String, Number, Date, Boolean.|1.3|
|[customProperty](../reference/word/customproperty.md)|_Property_ > value|Gets or sets the value of the custom property.|1.3|
|[customProperty](../reference/word/customproperty.md)|_Method_ > [delete()](../reference/word/customproperty.md#delete)|Deletes the custom property.|1.3|
|[customPropertyCollection](../reference/word/custompropertycollection.md)|_Property_ > items|A collection of customProperty objects. Read-only.|1.3|
|[customPropertyCollection](../reference/word/custompropertycollection.md)|_Method_ > [deleteAll()](../reference/word/custompropertycollection.md#deleteall)|Deletes all custom properties in this collection.|1.3|
|[customPropertyCollection](../reference/word/custompropertycollection.md)|_Method_ > [getCount()](../reference/word/custompropertycollection.md#getcount)|Gets the count of custom properties.|1.3|
|[customPropertyCollection](../reference/word/custompropertycollection.md)|_Method_ > [getItem(key: string)](../reference/word/custompropertycollection.md#getitemkey-string)|Gets a custom property object by its key, which is case-insensitive. Throws if the custom property does not exist.|1.3|
|[customPropertyCollection](../reference/word/custompropertycollection.md)|_Method_ > [getItemOrNullObject(key: string)](../reference/word/custompropertycollection.md#getitemornullobjectkey-string)|Gets a custom property object by its key, which is case-insensitive. Returns a null object if the custom property does not exist.|1.3|
|[customPropertyCollection](../reference/word/custompropertycollection.md)|_Method_ > [set(key: string, value: object)](../reference/word/custompropertycollection.md#setkey-string-value-object)|Creates or sets a custom property.|1.3|
|[document](../reference/word/document.md)|_Property_ > properties|Gets the properties of the current document. Read-only.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > applicationName|Gets the application name of the document. Read only. Read-only.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > author|Gets or sets the author of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > category|Gets or sets the category of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > comments|Gets or sets the comments of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > company|Gets or sets the company of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > format|Gets or sets the format of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > keywords|Gets or sets the keywords of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > lastAuthor|Gets or sets the last author of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > manager|Gets or sets the manager of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > revisionNumber|Gets the revision number of the document. Read only. Read-only.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > security|Gets the security of the document. Read only. Read-only.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > subject|Gets or sets the subject of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > template|Gets the template of the document. Read only. Read-only.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > title|Gets or sets the title of the document.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > creationDate|Gets the creation date of the document. Read only. Read-only.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > customProperties|Gets the collection of custom properties of the document. Read only. Read-only.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > lastPrintDate|Gets the last print date of the document. Read only. Read-only.|1.3|
|[documentProperties](../reference/word/documentproperties.md)|_Property_ > lastSaveTime|Gets the last save time of the document. Read only. Read-only.|1.3|
|[inlinePicture](../reference/word/inlinepicture.md)|_Property_ > parentContentControlOrNullObject|Gets the content control that contains the inline image. Returns a null object if there isn't a parent content control. Read-only.|1.3|
|[inlinePicture](../reference/word/inlinepicture.md)|_Property_ > parentTable|Gets the table that contains the inline image. Throws if it is not contained in a table. Read-only.|1.3|
|[inlinePicture](../reference/word/inlinepicture.md)|_Property_ > parentTableCell|Gets the table cell that contains the inline image. Throws if it is not contained in a table cell. Read-only.|1.3|
|[inlinePicture](../reference/word/inlinepicture.md)|_Property_ > parentTableCellOrNullObject|Gets the table cell that contains the inline image. Returns a null object if it is not contained in a table cell. Read-only.|1.3|
|[inlinePicture](../reference/word/inlinepicture.md)|_Property_ > parentTableOrNullObject|Gets the table that contains the inline image. Returns a null object if it is not contained in a table. Read-only.|1.3|
|[inlinePicture](../reference/word/inlinepicture.md)|_Method_ > [getNext()](../reference/word/inlinepicture.md#getnext)|Gets the next inline image. Throws if this inline image is the last one.|1.3|
|[inlinePicture](../reference/word/inlinepicture.md)|_Method_ > [getNextOrNullObject()](../reference/word/inlinepicture.md#getnextornullobject)|Gets the next inline image. Returns a null object if this inline image is the last one.|1.3|
|[inlinePicture](../reference/word/inlinepicture.md)|_Method_ > [getRange(rangeLocation: string)](../reference/word/inlinepicture.md#getrangerangelocation-string)|Gets the picture, or the starting or ending point of the picture, as a range.|1.3|
|[inlinePictureCollection](../reference/word/inlinepicturecollection.md)|_Method_ > [getFirst()](../reference/word/inlinepicturecollection.md#getfirst)|Gets the first inline image in this collection. Throws if this collection is empty.|1.3|
|[inlinePictureCollection](../reference/word/inlinepicturecollection.md)|_Method_ > [getFirstOrNullObject()](../reference/word/inlinepicturecollection.md#getfirstornullobject)|Gets the first inline image in this collection. Returns a null object if this collection is empty.|1.3|
|[list](../reference/word/list.md)|_Property_ > id|Gets the list's id. Read-only.|1.3|
|[list](../reference/word/list.md)|_Property_ > levelExistences|Checks whether each of the 9 levels exists in the list. A true value indicates the level exists, which means there is at least one list item at that level. Read-only.|1.3|
|[list](../reference/word/list.md)|_Property_ > levelTypes|Gets all 9 level types in the list. Each type can be 'Bullet', 'Number' or 'Picture'. Read-only. Possible values are: Bullet, Number, Picture.|1.3|
|[list](../reference/word/list.md)|_Property_ > paragraphs|Gets paragraphs in the list. Read-only.|1.3|
|[list](../reference/word/list.md)|_Method_ > [getLevelParagraphs(level: number)](../reference/word/list.md#getlevelparagraphslevel-number)|Gets the paragraphs that occur at the specified level in the list.|1.3|
|[list](../reference/word/list.md)|_Method_ > [getLevelString(level: number)](../reference/word/list.md#getlevelstringlevel-number)|Gets the bullet, number or picture at the specified level as a string.|1.3|
|[list](../reference/word/list.md)|_Method_ > [insertParagraph(paragraphText: string, insertLocation: string)](../reference/word/list.md#insertparagraphparagraphtext-string-insertlocation-string)|Inserts a paragraph at the specified location. The insertLocation value can be 'Start', 'End', 'Before' or 'After'.|1.3|
|[list](../reference/word/list.md)|_Method_ > [setLevelAlignment(level: number, alignment: string)](../reference/word/list.md#setlevelalignmentlevel-number-alignment-string)|Sets the alignment of the bullet, number or picture at the specified level in the list.|1.3|
|[list](../reference/word/list.md)|_Method_ > [setLevelBullet(level: number, listBullet: string, charCode: number, fontName: string)](../reference/word/list.md#setlevelbulletlevel-number-listbullet-string-charcode-number-fontname-string)|Sets the bullet format at the specified level in the list. If the bullet is 'Custom', the charCode is required.|1.3|
|[list](../reference/word/list.md)|_Method_ > [setLevelIndents(level: number, textIndent: float, textIndent: float)](../reference/word/list.md#setlevelindentslevel-number-textindent-float-textindent-float)|Sets the two indents of the specified level in the list.|1.3|
|[list](../reference/word/list.md)|_Method_ > [setLevelNumbering(level: number, listNumbering: string, formatString: object[])](../reference/word/list.md#setlevelnumberinglevel-number-listnumbering-string-formatstring-object)|Sets the numbering format at the specified level in the list.|1.3|
|[list](../reference/word/list.md)|_Method_ > [setLevelStartingNumber(level: number, startingNumber: number)](../reference/word/list.md#setlevelstartingnumberlevel-number-startingnumber-number)|Sets the starting number at the specified level in the list. Default value is 1.|1.3|
|[listCollection](../reference/word/listcollection.md)|_Property_ > items|A collection of list objects. Read-only.|1.3|
|[listCollection](../reference/word/listcollection.md)|_Method_ > [getById(id: number)](../reference/word/listcollection.md#getbyidid-number)|Gets a list by its identifier. Throws if there isn't a list with the identifier in this collection.|1.3|
|[listCollection](../reference/word/listcollection.md)|_Method_ > [getByIdOrNullObject(id: number)](../reference/word/listcollection.md#getbyidornullobjectid-number)|Gets a list by its identifier. Returns a null object if there isn't a list with the identifier in this collection.|1.3|
|[listCollection](../reference/word/listcollection.md)|_Method_ > [getFirst()](../reference/word/listcollection.md#getfirst)|Gets the first list in this collection. Throws if this collection is empty.|1.3|
|[listCollection](../reference/word/listcollection.md)|_Method_ > [getFirstOrNullObject()](../reference/word/listcollection.md#getfirstornullobject)|Gets the first list in this collection. Returns a null object if this collection is empty.|1.3|
|[listCollection](../reference/word/listcollection.md)|_Method_ > [getItem(index: number)](../reference/word/listcollection.md#getitemindex-number)|Gets a list object by its index in the collection.|1.3|
|[listItem](../reference/word/listitem.md)|_Property_ > level|Gets or sets the level of the item in the list.|1.3|
|[listItem](../reference/word/listitem.md)|_Property_ > listString|Gets the list item bullet, number or picture as a string. Read-only.|1.3|
|[listItem](../reference/word/listitem.md)|_Property_ > siblingIndex|Gets the list item order number in relation to its siblings. Read-only.|1.3|
|[listItem](../reference/word/listitem.md)|_Method_ > [getAncestor(parentOnly: bool)](../reference/word/listitem.md#getancestorparentonly-bool)|Gets the list item parent, or the closest ancestor if the parent does not exist. Throws if the list item has no ancester.|1.3|
|[listItem](../reference/word/listitem.md)|_Method_ > [getAncestorOrNullObject(parentOnly: bool)](../reference/word/listitem.md#getancestorornullobjectparentonly-bool)|Gets the list item parent, or the closest ancestor if the parent does not exist. Returns a null object if the list item has no ancester.|1.3|
|[listItem](../reference/word/listitem.md)|_Method_ > [getDescendants(directChildrenOnly: bool)](../reference/word/listitem.md#getdescendantsdirectchildrenonly-bool)|Gets all descendant list items of the list item.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > isLastParagraph|Indicates the paragraph is the last one inside its parent body. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > isListItem|Checks whether the paragraph is a list item. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > styleBuiltIn|Gets or sets the built-in style name for the paragraph. Use this property for built-in styles that are portable between locales. To use custom styles or localized style names, see the "style" property. Possible values are: Other, Normal, Heading1, Heading2, Heading3, Heading4, Heading5, Heading6, Heading7, Heading8, Heading9, Toc1, more...|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > tableNestingLevel|Gets the level of the paragraph's table. It returns 0 if the paragraph is not in a table. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > list|Gets the List to which this paragraph belongs. Throws if the paragraph is not in a list. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > listItem|Gets the ListItem for the paragraph. Throws if the paragraph is not part of a list. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > listItemOrNullObject|Gets the ListItem for the paragraph. Returns a null object if the paragraph is not part of a list. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > listOrNullObject|Gets the List to which this paragraph belongs. Returns a null object if the paragraph is not in a list. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > parentBody|Gets the parent body of the paragraph. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > parentContentControlOrNullObject|Gets the content control that contains the paragraph. Returns a null object if there isn't a parent content control. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > parentTable|Gets the table that contains the paragraph. Throws if it is not contained in a table. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > parentTableCell|Gets the table cell that contains the paragraph. Throws if it is not contained in a table cell. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > parentTableCellOrNullObject|Gets the table cell that contains the paragraph. Returns a null object if it is not contained in a table cell. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Property_ > parentTableOrNullObject|Gets the table that contains the paragraph. Returns a null object if it is not contained in a table. Read-only.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [attachToList(listId: number, level: number)](../reference/word/paragraph.md#attachtolistlistid-number-level-number)|Lets the paragraph join an existing list at the specified level. Fails if the paragraph cannot join the list or if the paragraph is already a list item.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [detachFromList()](../reference/word/paragraph.md#detachfromlist)|Moves this paragraph out of its list, if the paragraph is a list item.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [getNext()](../reference/word/paragraph.md#getnext)|Gets the next paragraph. Throws if the paragraph is the last one.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [getNextOrNullObject()](../reference/word/paragraph.md#getnextornullobject)|Gets the next paragraph. Returns a null object if the paragraph is the last one.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [getPrevious()](../reference/word/paragraph.md#getprevious)|Gets the previous paragraph. Throws if the paragraph is the first one.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [getPreviousOrNullObject()](../reference/word/paragraph.md#getpreviousornullobject)|Gets the previous paragraph. Returns a null object if the paragraph is the first one.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [getRange(rangeLocation: string)](../reference/word/paragraph.md#getrangerangelocation-string)|Gets the whole paragraph, or the starting or ending point of the paragraph, as a range.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [getTextRanges(endingMarks: string[], trimSpacing: bool)](../reference/word/paragraph.md#gettextrangesendingmarks-string-trimspacing-bool)|Gets the text ranges in the paragraph by using punctuation marks andor other ending marks.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [insertTable(rowCount: number, columnCount: number, insertLocation: string, values: string[][])](../reference/word/paragraph.md#inserttablerowcount-number-columncount-number-insertlocation-string-values-string)|Inserts a table with the specified number of rows and columns. The insertLocation value can be 'Before' or 'After'.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [split(delimiters: string[], trimDelimiters: bool, trimSpacing: bool)](../reference/word/paragraph.md#splitdelimiters-string-trimdelimiters-bool-trimspacing-bool)|Splits the paragraph into child ranges by using delimiters.|1.3|
|[paragraph](../reference/word/paragraph.md)|_Method_ > [startNewList()](../reference/word/paragraph.md#startnewlist)|Starts a new list with this paragraph. Fails if the paragraph is already a list item.|1.3|
|[paragraphCollection](../reference/word/paragraphcollection.md)|_Method_ > [getFirst()](../reference/word/paragraphcollection.md#getfirst)|Gets the first paragraph in this collection. Throws if the collection is empty.|1.3|
|[paragraphCollection](../reference/word/paragraphcollection.md)|_Method_ > [getFirstOrNullObject()](../reference/word/paragraphcollection.md#getfirstornullobject)|Gets the first paragraph in this collection. Returns a null object if the collection is empty.|1.3|
|[paragraphCollection](../reference/word/paragraphcollection.md)|_Method_ > [getLast()](../reference/word/paragraphcollection.md#getlast)|Gets the last paragraph in this collection. Throws if the collection is empty.|1.3|
|[paragraphCollection](../reference/word/paragraphcollection.md)|_Method_ > [getLastOrNullObject()](../reference/word/paragraphcollection.md#getlastornullobject)|Gets the last paragraph in this collection. Returns a null object if the collection is empty.|1.3|
|[range](../reference/word/range.md)|_Property_ > hyperlink|Gets the first hyperlink in the range, or sets a hyperlink on the range. All hyperlinks in the range are deleted when you set a new hyperlink on the range. Use a '#' to separate the address part from the optional location part.|1.3|
|[range](../reference/word/range.md)|_Property_ > isEmpty|Checks whether the range length is zero. Read-only.|1.3|
|[range](../reference/word/range.md)|_Property_ > styleBuiltIn|Gets or sets the built-in style name for the range. Use this property for built-in styles that are portable between locales. To use custom styles or localized style names, see the "style" property. Possible values are: Other, Normal, Heading1, Heading2, Heading3, Heading4, Heading5, Heading6, Heading7, Heading8, Heading9, Toc1, more...|1.3|
|[range](../reference/word/range.md)|_Property_ > lists|Gets the collection of list objects in the range. Read-only.|1.3|
|[range](../reference/word/range.md)|_Property_ > parentBody|Gets the parent body of the range. Read-only.|1.3|
|[range](../reference/word/range.md)|_Property_ > parentContentControlOrNullObject|Gets the content control that contains the range. Returns a null object if there isn't a parent content control. Read-only.|1.3|
|[range](../reference/word/range.md)|_Property_ > parentTable|Gets the table that contains the range. Throws if it is not contained in a table. Read-only.|1.3|
|[range](../reference/word/range.md)|_Property_ > parentTableCell|Gets the table cell that contains the range. Throws if it is not contained in a table cell. Read-only.|1.3|
|[range](../reference/word/range.md)|_Property_ > parentTableCellOrNullObject|Gets the table cell that contains the range. Returns a null object if it is not contained in a table cell. Read-only.|1.3|
|[range](../reference/word/range.md)|_Property_ > parentTableOrNullObject|Gets the table that contains the range. Returns a null object if it is not contained in a table. Read-only.|1.3|
|[range](../reference/word/range.md)|_Property_ > tables|Gets the collection of table objects in the range. Read-only.|1.3|
|[range](../reference/word/range.md)|_Method_ > [compareLocationWith(range: Range)](../reference/word/range.md#comparelocationwithrange-range)|Compares this range's location with another range's location.|1.3|
|[range](../reference/word/range.md)|_Method_ > [expandTo(range: Range)](../reference/word/range.md#expandtorange-range)|Returns a new range that extends from this range in either direction to cover another range. This range is not changed. Throws if the two ranges do not have a union.|1.3|
|[range](../reference/word/range.md)|_Method_ > [expandToOrNullObject(range: Range)](../reference/word/range.md#expandtoornullobjectrange-range)|Returns a new range that extends from this range in either direction to cover another range. This range is not changed. Returns a null object if the two ranges do not have a union.|1.3|
|[range](../reference/word/range.md)|_Method_ > [getHyperlinkRanges()](../reference/word/range.md#gethyperlinkranges)|Gets hyperlink child ranges within the range.|1.3|
|[range](../reference/word/range.md)|_Method_ > [getNextTextRange(endingMarks: string[], trimSpacing: bool)](../reference/word/range.md#getnexttextrangeendingmarks-string-trimspacing-bool)|Gets the next text range by using punctuation marks andor other ending marks. Throws if this text range is the last one.|1.3|
|[range](../reference/word/range.md)|_Method_ > [getNextTextRangeOrNullObject(endingMarks: string[], trimSpacing: bool)](../reference/word/range.md#getnexttextrangeornullobjectendingmarks-string-trimspacing-bool)|Gets the next text range by using punctuation marks andor other ending marks. Returns a null object if this text range is the last one.|1.3|
|[range](../reference/word/range.md)|_Method_ > [getRange(rangeLocation: string)](../reference/word/range.md#getrangerangelocation-string)|Clones the range, or gets the starting or ending point of the range as a new range.|1.3|
|[range](../reference/word/range.md)|_Method_ > [getTextRanges(endingMarks: string[], trimSpacing: bool)](../reference/word/range.md#gettextrangesendingmarks-string-trimspacing-bool)|Gets the text child ranges in the range by using punctuation marks andor other ending marks.|1.3|
|[range](../reference/word/range.md)|_Method_ > [insertTable(rowCount: number, columnCount: number, insertLocation: string, values: string[][])](../reference/word/range.md#inserttablerowcount-number-columncount-number-insertlocation-string-values-string)|Inserts a table with the specified number of rows and columns. The insertLocation value can be 'Before' or 'After'.|1.3|
|[range](../reference/word/range.md)|_Method_ > [intersectWith(range: Range)](../reference/word/range.md#intersectwithrange-range)|Returns a new range as the intersection of this range with another range. This range is not changed. Throws if the two ranges are not overlapped or adjacent.|1.3|
|[range](../reference/word/range.md)|_Method_ > [intersectWithOrNullObject(range: Range)](../reference/word/range.md#intersectwithornullobjectrange-range)|Returns a new range as the intersection of this range with another range. This range is not changed. Returns a null object if the two ranges are not overlapped or adjacent.|1.3|
|[range](../reference/word/range.md)|_Method_ > [split(delimiters: string[], multiParagraphs: bool, trimDelimiters: bool, trimSpacing: bool)](../reference/word/range.md#splitdelimiters-string-multiparagraphs-bool-trimdelimiters-bool-trimspacing-bool)|Splits the range into child ranges by using delimiters.|1.3|
|[rangeCollection](../reference/word/rangecollection.md)|_Property_ > items|A collection of range objects. Read-only.|1.3|
|[rangeCollection](../reference/word/rangecollection.md)|_Method_ > [getFirst()](../reference/word/rangecollection.md#getfirst)|Gets the first range in this collection. Throws if this collection is empty.|1.3|
|[rangeCollection](../reference/word/rangecollection.md)|_Method_ > [getFirstOrNullObject()](../reference/word/rangecollection.md#getfirstornullobject)|Gets the first range in this collection. Returns a null object if this collection is empty.|1.3|
|[rangeCollection](../reference/word/rangecollection.md)|_Method_ > [getItem(index: number)](../reference/word/rangecollection.md#getitemindex-number)|Gets a range object by its index in the collection.|1.3|
|[section](../reference/word/section.md)|_Method_ > [getNext()](../reference/word/section.md#getnext)|Gets the next section. Throws if this section is the last one.|1.3|
|[section](../reference/word/section.md)|_Method_ > [getNextOrNullObject()](../reference/word/section.md#getnextornullobject)|Gets the next section. Returns a null object if this section is the last one.|1.3|
|[sectionCollection](../reference/word/sectioncollection.md)|_Method_ > [getFirst()](../reference/word/sectioncollection.md#getfirst)|Gets the first section in this collection. Throws if this collection is empty.|1.3|
|[sectionCollection](../reference/word/sectioncollection.md)|_Method_ > [getFirstOrNullObject()](../reference/word/sectioncollection.md#getfirstornullobject)|Gets the first section in this collection. Returns a null object if this collection is empty.|1.3|
|[table](../reference/word/table.md)|_Property_ > alignment|Gets or sets the alignment of the table against the page column. The value can be 'left', 'centered' or 'right'. Possible values are: `Unknown` Unknown alignment.,`Left` Alignment to the left.,`Centered` Alignment to the center.,`Right` Alignment to the right.,`Justified` Fully justified alignment.|1.3|
|[table](../reference/word/table.md)|_Property_ > headerRowCount|Gets and sets the number of header rows.|1.3|
|[table](../reference/word/table.md)|_Property_ > horizontalAlignment|Gets and sets the horizontal alignment of every cell in the table. The value can be 'left', 'centered', 'right', or 'justified'. Possible values are: `Unknown` Unknown alignment.,`Left` Alignment to the left.,`Centered` Alignment to the center.,`Right` Alignment to the right.,`Justified` Fully justified alignment.|1.3|
|[table](../reference/word/table.md)|_Property_ > isUniform|Indicates whether all of the table rows are uniform. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > nestingLevel|Gets the nesting level of the table. Top-level tables have level 1. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > rowCount|Gets the number of rows in the table. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > shadingColor|Gets and sets the shading color.|1.3|
|[table](../reference/word/table.md)|_Property_ > style|Gets or sets the style name for the table. Use this property for custom styles and localized style names. To use the built-in styles that are portable between locales, see the "styleBuiltIn" property.|1.3|
|[table](../reference/word/table.md)|_Property_ > styleBandedColumns|Gets and sets whether the table has banded columns.|1.3|
|[table](../reference/word/table.md)|_Property_ > styleBandedRows|Gets and sets whether the table has banded rows.|1.3|
|[table](../reference/word/table.md)|_Property_ > styleBuiltIn|Gets or sets the built-in style name for the table. Use this property for built-in styles that are portable between locales. To use custom styles or localized style names, see the "style" property. Possible values are: Other, Normal, Heading1, Heading2, Heading3, Heading4, Heading5, Heading6, Heading7, Heading8, Heading9, Toc1, more...|1.3|
|[table](../reference/word/table.md)|_Property_ > styleFirstColumn|Gets and sets whether the table has a first column with a special style.|1.3|
|[table](../reference/word/table.md)|_Property_ > styleLastColumn|Gets and sets whether the table has a last column with a special style.|1.3|
|[table](../reference/word/table.md)|_Property_ > styleTotalRow|Gets and sets whether the table has a total (last) row with a special style.|1.3|
|[table](../reference/word/table.md)|_Property_ > values|Gets and sets the text values in the table, as a 2D Javascript array.|1.3|
|[table](../reference/word/table.md)|_Property_ > verticalAlignment|Gets and sets the vertical alignment of every cell in the table. The value can be 'top', 'center' or 'bottom'. Possible values are: Mixed, Top, Center, Bottom.|1.3|
|[table](../reference/word/table.md)|_Property_ > width|Gets and sets the width of the table in points.|1.3|
|[table](../reference/word/table.md)|_Property_ > font|Gets the font. Use this to get and set font name, size, color, and other properties. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > parentBody|Gets the parent body of the table. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > parentContentControl|Gets the content control that contains the table. Throws if there isn't a parent content control. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > parentContentControlOrNullObject|Gets the content control that contains the table. Returns a null object if there isn't a parent content control. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > parentTable|Gets the table that contains this table. Throws if it is not contained in a table. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > parentTableCell|Gets the table cell that contains this table. Throws if it is not contained in a table cell. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > parentTableCellOrNullObject|Gets the table cell that contains this table. Returns a null object if it is not contained in a table cell. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > parentTableOrNullObject|Gets the table that contains this table. Returns a null object if it is not contained in a table. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > rows|Gets all of the table rows. Read-only.|1.3|
|[table](../reference/word/table.md)|_Property_ > tables|Gets the child tables nested one level deeper. Read-only.|1.3|
|[table](../reference/word/table.md)|_Method_ > [addColumns(insertLocation: string, columnCount: number, values: string[][])](../reference/word/table.md#addcolumnsinsertlocation-string-columncount-number-values-string)|Adds columns to the start or end of the table, using the first or last existing column as a template. This is applicable to uniform tables. The string values, if specified, are set in the newly inserted rows.|1.3|
|[table](../reference/word/table.md)|_Method_ > [addRows(insertLocation: string, rowCount: number, values: string[][])](../reference/word/table.md#addrowsinsertlocation-string-rowcount-number-values-string)|Adds rows to the start or end of the table, using the first or last existing row as a template. The string values, if specified, are set in the newly inserted rows.|1.3|
|[table](../reference/word/table.md)|_Method_ > [autoFitWindow()](../reference/word/table.md#autofitwindow)|Autofits the table columns to the width of the window.|1.3|
|[table](../reference/word/table.md)|_Method_ > [clear()](../reference/word/table.md#clear)|Clears the contents of the table.|1.3|
|[table](../reference/word/table.md)|_Method_ > [delete()](../reference/word/table.md#delete)|Deletes the entire table.|1.3|
|[table](../reference/word/table.md)|_Method_ > [deleteColumns(columnIndex: number, columnCount: number)](../reference/word/table.md#deletecolumnscolumnindex-number-columncount-number)|Deletes specific columns. This is applicable to uniform tables.|1.3|
|[table](../reference/word/table.md)|_Method_ > [deleteRows(rowIndex: number, rowCount: number)](../reference/word/table.md#deleterowsrowindex-number-rowcount-number)|Deletes specific rows.|1.3|
|[table](../reference/word/table.md)|_Method_ > [distributeColumns()](../reference/word/table.md#distributecolumns)|Distributes the column widths evenly. This is applicable to uniform tables.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getBorder(borderLocation: string)](../reference/word/table.md#getborderborderlocation-string)|Gets the border style for the specified border.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getCell(rowIndex: number, cellIndex: number)](../reference/word/table.md#getcellrowindex-number-cellindex-number)|Gets the table cell at a specified row and column. Throws if the specified table cell does not exist.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getCellOrNullObject(rowIndex: number, cellIndex: number)](../reference/word/table.md#getcellornullobjectrowindex-number-cellindex-number)|Gets the table cell at a specified row and column. Returns a null object if the specified table cell does not exist.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getCellPadding(cellPaddingLocation: CellPaddingLocation)](../reference/word/table.md#getcellpaddingcellpaddinglocation-cellpaddinglocation)|Gets cell padding in points.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getNext()](../reference/word/table.md#getnext)|Gets the next table. Throws if this table is the last one.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getNextOrNullObject()](../reference/word/table.md#getnextornullobject)|Gets the next table. Returns a null object if this table is the last one.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getParagraphAfter()](../reference/word/table.md#getparagraphafter)|Gets the paragraph after the table. Throws if there isn't a paragraph after the table.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getParagraphAfterOrNullObject()](../reference/word/table.md#getparagraphafterornullobject)|Gets the paragraph after the table. Returns a null object if there isn't a paragraph after the table.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getParagraphBefore()](../reference/word/table.md#getparagraphbefore)|Gets the paragraph before the table. Throws if there isn't a paragraph before the table.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getParagraphBeforeOrNullObject()](../reference/word/table.md#getparagraphbeforeornullobject)|Gets the paragraph before the table. Returns a null object if there isn't a paragraph before the table.|1.3|
|[table](../reference/word/table.md)|_Method_ > [getRange(rangeLocation: string)](../reference/word/table.md#getrangerangelocation-string)|Gets the range that contains this table, or the range at the start or end of the table.|1.3|
|[table](../reference/word/table.md)|_Method_ > [insertContentControl()](../reference/word/table.md#insertcontentcontrol)|Inserts a content control on the table.|1.3|
|[table](../reference/word/table.md)|_Method_ > [insertParagraph(paragraphText: string, insertLocation: string)](../reference/word/table.md#insertparagraphparagraphtext-string-insertlocation-string)|Inserts a paragraph at the specified location. The insertLocation value can be 'Before' or 'After'.|1.3|
|[table](../reference/word/table.md)|_Method_ > [insertTable(rowCount: number, columnCount: number, insertLocation: string, values: string[][])](../reference/word/table.md#inserttablerowcount-number-columncount-number-insertlocation-string-values-string)|Inserts a table with the specified number of rows and columns. The insertLocation value can be 'Before' or 'After'.|1.3|
|[table](../reference/word/table.md)|_Method_ > [search(searchText: string, searchOptions: ParamTypeStrings.SearchOptions)](../reference/word/table.md#searchsearchtext-string-searchoptions-paramtypestrings.searchoptions)|Performs a search with the specified searchOptions on the scope of the table object. The search results are a collection of range objects.|1.3|
|[table](../reference/word/table.md)|_Method_ > [select(selectionMode: string)](../reference/word/table.md#selectselectionmode-string)|Selects the table, or the position at the start or end of the table, and navigates the Word UI to it.|1.3|
|[table](../reference/word/table.md)|_Method_ > [setCellPadding(cellPaddingLocation: CellPaddingLocation, cellPadding: float)](../reference/word/table.md#setcellpaddingcellpaddinglocation-cellpaddinglocation-cellpadding-float)|Sets cell padding in points.|1.3|
|[tableBorder](../reference/word/tableborder.md)|_Property_ > color|Gets or sets the table border color, as a hex value or name.|1.3|
|[tableBorder](../reference/word/tableborder.md)|_Property_ > type|Gets or sets the type of the table border. Possible values are: Mixed, None, Single, Thick, Double, Hairline, Dotted, Dashed, DotDashed, Dot2Dashed, Triple, ThinThickSmall, ThickThinSmall, ThinThickThinSmall, ThinThickMed, ThickThinMed, ThinThickThinMed, ThinThickLarge, ThickThinLarge, ThinThickThinLarge, Wave, DoubleWave, DashedSmall, DashDotStroked, ThreeDEmboss, ThreeDEngrave.|1.3|
|[tableBorder](../reference/word/tableborder.md)|_Property_ > width|Gets or sets the width, in points, of the table border. Not applicable to table border types that have fixed widths.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > cellIndex|Gets the index of the cell in its row. Read-only.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > columnWidth|Gets and sets the width of the cell's column in points. This is applicable to uniform tables.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > horizontalAlignment|Gets and sets the horizontal alignment of the cell. The value can be 'left', 'centered', 'right', or 'justified'. Possible values are: `Unknown` Unknown alignment.,`Left` Alignment to the left.,`Centered` Alignment to the center.,`Right` Alignment to the right.,`Justified` Fully justified alignment.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > rowIndex|Gets the index of the cell's row in the table. Read-only.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > shadingColor|Gets or sets the shading color of the cell. Color is specified in "#RRGGBB" format or by using the color name.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > value|Gets and sets the text of the cell.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > verticalAlignment|Gets and sets the vertical alignment of the cell. The value can be 'top', 'center' or 'bottom'. Possible values are: Mixed, Top, Center, Bottom.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > width|Gets the width of the cell in points. Read-only.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > body|Gets the body object of the cell. Read-only.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > parentRow|Gets the parent row of the cell. Read-only.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Property_ > parentTable|Gets the parent table of the cell. Read-only.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Method_ > [deleteColumn()](../reference/word/tablecell.md#deletecolumn)|Deletes the column containing this cell. This is applicable to uniform tables.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Method_ > [deleteRow()](../reference/word/tablecell.md#deleterow)|Deletes the row containing this cell.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Method_ > [getBorder(borderLocation: string)](../reference/word/tablecell.md#getborderborderlocation-string)|Gets the border style for the specified border.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Method_ > [getCellPadding(cellPaddingLocation: CellPaddingLocation)](../reference/word/tablecell.md#getcellpaddingcellpaddinglocation-cellpaddinglocation)|Gets cell padding in points.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Method_ > [getNext()](../reference/word/tablecell.md#getnext)|Gets the next cell. Throws if this cell is the last one.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Method_ > [getNextOrNullObject()](../reference/word/tablecell.md#getnextornullobject)|Gets the next cell. Returns a null object if this cell is the last one.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Method_ > [insertColumns(insertLocation: string, columnCount: number, values: string[][])](../reference/word/tablecell.md#insertcolumnsinsertlocation-string-columncount-number-values-string)|Adds columns to the left or right of the cell, using the cell's column as a template. This is applicable to uniform tables. The string values, if specified, are set in the newly inserted rows.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Method_ > [insertRows(insertLocation: string, rowCount: number, values: string[][])](../reference/word/tablecell.md#insertrowsinsertlocation-string-rowcount-number-values-string)|Inserts rows above or below the cell, using the cell's row as a template. The string values, if specified, are set in the newly inserted rows.|1.3|
|[tableCell](../reference/word/tablecell.md)|_Method_ > [setCellPadding(cellPaddingLocation: CellPaddingLocation, cellPadding: float)](../reference/word/tablecell.md#setcellpaddingcellpaddinglocation-cellpaddinglocation-cellpadding-float)|Sets cell padding in points.|1.3|
|[tableCellCollection](../reference/word/tablecellcollection.md)|_Property_ > items|A collection of tableCell objects. Read-only.|1.3|
|[tableCellCollection](../reference/word/tablecellcollection.md)|_Method_ > [getFirst()](../reference/word/tablecellcollection.md#getfirst)|Gets the first table cell in this collection. Throws if this collection is empty.|1.3|
|[tableCellCollection](../reference/word/tablecellcollection.md)|_Method_ > [getFirstOrNullObject()](../reference/word/tablecellcollection.md#getfirstornullobject)|Gets the first table cell in this collection. Returns a null object if this collection is empty.|1.3|
|[tableCellCollection](../reference/word/tablecellcollection.md)|_Method_ > [getItem(index: number)](../reference/word/tablecellcollection.md#getitemindex-number)|Gets a table cell object by its index in the collection.|1.3|
|[tableCollection](../reference/word/tablecollection.md)|_Property_ > items|A collection of table objects. Read-only.|1.3|
|[tableCollection](../reference/word/tablecollection.md)|_Method_ > [getFirst()](../reference/word/tablecollection.md#getfirst)|Gets the first table in this collection. Throws if this collection is empty.|1.3|
|[tableCollection](../reference/word/tablecollection.md)|_Method_ > [getFirstOrNullObject()](../reference/word/tablecollection.md#getfirstornullobject)|Gets the first table in this collection. Returns a null object if this collection is empty.|1.3|
|[tableCollection](../reference/word/tablecollection.md)|_Method_ > [getItem(index: number)](../reference/word/tablecollection.md#getitemindex-number)|Gets a table object by its index in the collection.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > cellCount|Gets the number of cells in the row. Read-only.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > horizontalAlignment|Gets and sets the horizontal alignment of every cell in the row. The value can be 'left', 'centered', 'right', or 'justified'. Possible values are: `Unknown` Unknown alignment.,`Left` Alignment to the left.,`Centered` Alignment to the center.,`Right` Alignment to the right.,`Justified` Fully justified alignment.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > isHeader|Checks whether the row is a header row. Read-only. To set the number of header rows, use HeaderRowCount on the Table object. Read-only.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > preferredHeight|Gets and sets the preferred height of the row in points.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > rowIndex|Gets the index of the row in its parent table. Read-only.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > shadingColor|Gets and sets the shading color.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > values|Gets and sets the text values in the row, as a 2D Javascript array.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > verticalAlignment|Gets and sets the vertical alignment of the cells in the row. The value can be 'top', 'center' or 'bottom'. Possible values are: Mixed, Top, Center, Bottom.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > cells|Gets cells. Read-only.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > font|Gets the font. Use this to get and set font name, size, color, and other properties. Read-only.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Property_ > parentTable|Gets parent table. Read-only.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [clear()](../reference/word/tablerow.md#clear)|Clears the contents of the row.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [delete()](../reference/word/tablerow.md#delete)|Deletes the entire row.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [getBorder(borderLocation: string)](../reference/word/tablerow.md#getborderborderlocation-string)|Gets the border style of the cells in the row.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [getCellPadding(cellPaddingLocation: CellPaddingLocation)](../reference/word/tablerow.md#getcellpaddingcellpaddinglocation-cellpaddinglocation)|Gets cell padding in points.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [getNext()](../reference/word/tablerow.md#getnext)|Gets the next row. Throws if this row is the last one.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [getNextOrNullObject()](../reference/word/tablerow.md#getnextornullobject)|Gets the next row. Returns a null object if this row is the last one.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [insertRows(insertLocation: string, rowCount: number, values: string[][])](../reference/word/tablerow.md#insertrowsinsertlocation-string-rowcount-number-values-string)|Inserts rows using this row as a template. If values are specified, inserts the values into the new rows.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [search(searchText: string, searchOptions: ParamTypeStrings.SearchOptions)](../reference/word/tablerow.md#searchsearchtext-string-searchoptions-paramtypestrings.searchoptions)|Performs a search with the specified searchOptions on the scope of the row. The search results are a collection of range objects.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [select(selectionMode: string)](../reference/word/tablerow.md#selectselectionmode-string)|Selects the row and navigates the Word UI to it.|1.3|
|[tableRow](../reference/word/tablerow.md)|_Method_ > [setCellPadding(cellPaddingLocation: CellPaddingLocation, cellPadding: float)](../reference/word/tablerow.md#setcellpaddingcellpaddinglocation-cellpaddinglocation-cellpadding-float)|Sets cell padding in points.|1.3|
|[tableRowCollection](../reference/word/tablerowcollection.md)|_Property_ > items|A collection of tableRow objects. Read-only.|1.3|
|[tableRowCollection](../reference/word/tablerowcollection.md)|_Method_ > [getFirst()](../reference/word/tablerowcollection.md#getfirst)|Gets the first row in this collection. Throws if this collection is empty.|1.3|
|[tableRowCollection](../reference/word/tablerowcollection.md)|_Method_ > [getFirstOrNullObject()](../reference/word/tablerowcollection.md#getfirstornullobject)|Gets the first row in this collection. Returns a null object if this collection is empty.|1.3|
|[tableRowCollection](../reference/word/tablerowcollection.md)|_Method_ > [getItem(index: number)](../reference/word/tablerowcollection.md#getitemindex-number)|Gets a table row object by its index in the collection.|1.3|


## Try it out 

_**Note**: This feature is not currently available for new features._


We've been working on a Snippet Explorer that you can use to browse through common code snippets and learn how the new APIs work. Give it a try. You can find the code snippets referenced by the Snippet Explorer at [Office 2016 JavaScript API Snippet Explorer (Preview)](../reference/word/https://officesnippetexplorer.azurewebsites.net/#/snippets/word). 

## Give feedback

We need it, you want to give it. Feedback is much easier to give now that we're on GitHub. Check out the docs and let us know your feedback by submitting [issues](../reference/word/https://github.com/OfficeDev/office-js-docs/issues) directly in this repository. 

For API support, you can post questions to the community on [StackOverflow](../reference/word/http://stackoverflow.com/questions/tagged/office-js) and tag them with [office-js] and [word].
