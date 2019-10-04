# Markdown Syntax

Markdown is an easy to use markup language to format text which offers multiple ways to achieve the same result. Markdown was designed to be easy to learn as well as be easy to read and write. Markdown allows the author to keep their hands on the keyboard and focus on writing content. Markdown supports HTML, and HTML syntax can be used in combination with Markdown.

### Markdown supports the following types of formatting

Headings  
Text formatting  
Link formatting  
Page formatting  
Embedded content  
Task and List formatting  
Table formatting  
Special formatting

### Headings

Markdown allows for text to be resized by typing 1-6 \# \(hash or pound\) symbols in front of the text that is to be resized, followed by a space. One \# renders the largest text size, while six \# symbols renders the smallest text size. Typically, this is used at the beginning of a paragraph or section in a document, to make the title stand out from the rest of the text.

> * `# Heading 1`
> * `## Heading 2`
> * `### Heading 3`
> * `#### Heading 4`
> * `##### Heading 5`
> *  `###### Heading 6`

### Text Formatting

* **Indent size**: pressing the tab key will indent 4 spaces.
* **Single space**: pressing the tab key at the end of a line will single space the next line. Alternatively, pressing the space bar four times will single space the next line.
* **Double space:** leaving no spaces at the end of the line will double space the next line.
* **Bold**: used to show emphasis. Type two \* \(asterisk\) symbols on each side of the text that is to be bolded.

  > \*\*_Bold text\*_\*

* **Italic**: used to show emphasis or distinction. Type two \_ \(underline\) on each side of text that is to be emphasized.

  > \_Italic text\_

* ~~**Strikethrough**~~: used to mark text that should not be included, but should not be removed from the document. Type two ~ \(tilde\) symbols on each side of text that should show a strikethrough.

  > ~~Strikethrough text~~

* **Escape character**: used to prevent text from being formatted into Markdown. Type a \ \(backslash\) at the beginning of the text that is to be escaped.  

  > \escaped text

* **Bullet**: used to separate and order items in a list without using numbers. You should also indent these to ensure the numbering of tasks continues.

  > `-`

* **Inline code block**: used to provide a snippet of code that can be copied and pasted. Type a \` \(backtick\) on each side of the text that is to be displayed in the code block. The backtick is located above the tab key, to the left of the 1 key on the keyboard.

  > ```code block```

![Code Block displayed in Lab Guide](../.gitbook/assets/image%20%28105%29.png)

* **Fenced code block**: used to provide a programming language-specific code snippet. Type three \` \(backticks\) on each side of the text that should be displayed in the fenced code block. This should consume at least 3 lines in the text editor; the first line should display three backticks followed by the programming language name, the second line should display the code snippet, and the last line should only display three backticks. Markdown allows for more than one line to be used to display the code snippet.  In order for numbering to continue you should indent the fenced code block with a tab.  You may use any of the following language-specific codes:

  * powershell
  * cli
  * bash
  * json
  * xml
  * sql
  * csharp
  * fsharp
  * visual-basic

  > ```text
  > ```PowerShell
  > get-service | stop-service -whatif
  > ```
  > ```

![PowerShell displayed in Lab Guide](../.gitbook/assets/image%20%2899%29.png)

### Alert Boxes

Alert boxes allow you to highlight specific text.  See the example in the screenshot below:

![Alert Box examples](../.gitbook/assets/image%20%28106%29.png)

There are 7 different alert box options

* primary 
* secondary \(Used generally for scenarios\)
* success \(Used at the end of labs\)
* danger \(Used to inform users not to do something\)
* warning \(Used to warn or inform users of something\) 
* info \(Used for informational purposes\)
* light \(Used as answer area for questions\)

![Examples if different Alert Boxes](../.gitbook/assets/image%20%28101%29.png)

To insert an Alert Box simply add the following markdown code with the relevant alert box type

```text
@@@warning
**Note**: This may take upto 15 minutes to complete.
@@@
```

{% hint style="info" %}
Add the Alert Box directly under the text without a space to maintain formatting.
{% endhint %}

### Page formatting

* **Page break**: Used to separate content into pages. Separating into pages creates a next button that the student must click to navigate to the next page. This is useful for displaying small sections of instruction to the student at a time, rather than all instructions on the same page within the lab. Type three = \(equals\) symbols on the line where the current page should end. The new page will begin on the line following the three = symbols.

  > ===

* **Horizontal Line**: Used to separate content on the same page. Type three --- \(dash or hyphen\) on the line where the horizontal line should appear.

  > ---

### **Media content**

Images and videos can be inserted into lab guides.  

* **Embedded Images**: You can copy and paste image directly into the markdown.  This will then be uploaded to our storage and converted into a thumbnail and larger image.   You should ensure you tab a space prior to pasting the image in order to maintain lab step numbering.
* **Linked Images:** Linked images are external images \(ie images that are locates externally\).  To link a new image use the following code:
* > !\[ \]\(url\)
* **Image Dimensions**: You can specify image dimensions in your lab. Dimension values are in pixels and are placed inside curly braces, immediately after the end of the link URL syntax. Height and width are separated by a "x" in this format:{widthxheight} It's also possible to simply supply the width: {width}. In this case, the height is automatically calculated for you to be proportional to the provided width.

  > `![](image url){heightXwidth}` or `{height}`

* **Video:** Used to embed an image inline with other content use a tab then paste the embedded code for the video.

  \*\*\*\*

### Task and List formatting

* **Unordered list:** Used to list items in no particular order, separated by bullets rather than numbers. Type a - \(dash or hyphen\) followed by a space and then the text to be listed. Pressing enter at the end of the text will start the next line with a bullet.
* **Ordered list:** Used to list items in a particular order, separated by numbers rather than bullets. Type the number 1, followed by a space and then the text to be listed. Pressing enter at the end of the text will start the next line with number 2.
* Both Unordered and Ordered lists can contain Task Checkboxes for the student to check off steps as completed. Both list types can be combined in the same list. Task Checkboxes are used track and report lab progress to LOD and TMS, as well as a visual marker for students. Lab progress is calculated by the percentage of Task Checkboxes that are checked in the lab instructions.

```text
- [] Item 1
- [] Item 2
- [] Item 3
- [] Item 4
- [] Item 5
```

```text
1. [] Item 1
1. [] Item 2
1. [] Item 3
1. [] Item 4
1. [] Item 5
```

### Table formatting

* Tables can be aligned left, right or center by placing a : \(colon\) on the head row of the table. Placing a colon on the left side, right side or both sides of the dashes in the header row, will align the text in the table accordingly.  They should also be indented to align correctly.

**Left-aligned text**

```text
| column 1 | column 2 |
|:---------|:---------|
| data 1   | data 2   |
| data 3   | data 4   |
```

**Right-aligned text**

```text
| column 1 | column 2 |
|---------:|---------:|
| data 1   | data 2   |
| data 3   | data 4   |
```

**Center-aligned text**

```text
| column 1 | column 2 |
|:--------:|:--------:|
| data 1   | data 2   |
| data 3   | data 4   |
```

### Dynamic Lab Guides

**Replacement Tokens:** used to replace text in lab instructions with a variable that is unknown at the time of authoring the lab instructions. These variables may not be generated or created until the lab is launched by the student. These can include usernames, passwords, URLs etc.  
  
They can be added by using the options in the lab guide editor:  


![Dynamic Lab Guides - Replacement Tokens](../.gitbook/assets/image%20%28110%29.png)

* **Virtual Machines:** This section allows you to add a Replacement Token for the VM names. When multiple VMs are added to a lab image using this feature allows the student to switch VMs without having to use the commands in the home tab of the lab environment. Username and Passwords can also be inserted which allow pasting directly from the lab guide.

![Example of Vitual Machine and Password links inside a lab guide](../.gitbook/assets/image%20%28103%29.png)

* **Key Combinations**: This section allows you to embed virtual machine commands such as Ctrl + Alt + Del commands.

![](../.gitbook/assets/image%20%2896%29.png)

* **Lab Domain**: When labs have a lab domain added to the lab template, the dynamically assigned lab domain in the format labXXXXXX.godeploylabs.com is inserted.
* **M365 Actions**: This section allows you to add different elements and credentials of an assigned M365 tenant which can be added to a lab template.  These include:
  * Paste Admin Email:  example: admin@M365XXXXXXX.onmicrosoft.com
  * Paste Admin Email:  This is the password for the allocated tenant
  * Domain Name:  This is the Microsoft 365 domain.  example: M365XXXXXXX.onmicrosoft.com
  * Tenant Name:  This is the unique tenant name.  example M365XXXXXXX
  * M365 email address.  Here you can reference a user.  example: amal@M365XXXXXXX.onmicrosoft.com
* **Cloud Share Actions**: When you add a Cloud Share template \(either Azure, AWS or GCP\) to your lab template you can paste the credentials allocated when the resources are deployed to the cloud platform.

{% hint style="info" %}
Make Replacement Tokens bold to stand out.
{% endhint %}

