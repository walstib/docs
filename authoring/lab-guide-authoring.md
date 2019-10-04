---
description: >-
  The go deploy platform integrates the lab instructions within the lab
  environment to guide the users in completing the lab.
---

# Lab Guide Authoring

### Overview of lab guides within the lab environment

The go deploy platform integrates the lab instructions within the lab environment to guide the users in completing the lab. The platform allows users to view lab instructions inline with a Cloud portal or Virtual Machines.

One significant advantage of this presentation format is that the lab steps take up only a relatively small amount of screen real estate. This removes the need to switch back and forth between a lab document and the lab -- these activities distract from performing the lab and can take focus away from the lab steps and goals.

#### Launching a lab

A lab launch may take anywhere from a few seconds to a couple of minutes to fully launch, depending on the Cloud platform chosen and/or the size and number of VMs \(if using VMs\). Once the required resources are provisioned your lab will display.

![Lab interface post launch](../.gitbook/assets/image%20%2897%29.png)

Lab guides are presented in the **Lab Guide** tab

![Lab guides](../.gitbook/assets/image%20%2898%29.png)

For users who have multiple monitors, the lab guides can be popped out in a separate window.  This mode automatically shows screenshots \(if included\) in a larger format.

![Separate lab instruction window](../.gitbook/assets/image%20%28104%29.png)

A successful lab that is well-received by users usually contains more than a simple set of basic lab steps or tasks. It will have significant explanatory content to provide context, background information, tips, cautions, and other useful and relevant information. Additionally, visual elements such as screenshots, diagrams, videos, Alert focus areas and warning blocks can add clarity and reduce the likelihood of error on the part of the user.  Lab guides are authored using Markdown. Markdown allows instructions to be written however the author chooses, and the go deploy platform includes an authoring experience that allows for real-time updating of lab content, enabling authors to see exactly what the instructions they are authoring will look like at all times.

![Lab guide editor](../.gitbook/assets/image%20%28109%29.png)

#### Lab Instructions Format

In labs configured to use lab guides the lab instructions are written in a flavour of Markdown customised for the go deploy platform.  What those instructions contain is completely up to the author. There is no predefined format that must be followed. You simply author lab instructions whichever way you prefer. The content you include in your instructions may be all on one page, or you may break up your content across multiple pages. You may include task lists, with or without numbering, with or without subtasks, and you can go as many levels deep as you like. How the lab instructions present to users of your lab is entirely up to you

Even though the instructions are free form, here are a few general tips that you may want to take in consideration:

1. Keeping any introductory content to your lab on separate pages in the instructions allows users to understand what aim of the exercise/lab is trying to achieve without being overburdened by the rest of the lab content or completely missing it and starting on the first lab step.
2. If your lab contains multiple exercises or challenges, these are often natural locations to start a new page, allowing users to transition from one learning activity to the next.
3. Using task lists \(numbered or not\) allows users to track their own progress in a lab, while also allowing the lab owners to monitor progress over all students in a lab. Note, however, that it is completely optional for users to check off tasks as they complete them.
4. When using numbered lists of any kind, always use "1." for the number. This may seem odd when you look at a series of consecutive items, each numbered with 1., but it's a best practice worth following in Markdown. Markdown natively supports auto-numbering when it is rendered into HTML. Using 1-dot numbering makes ongoing maintenance easier \(inserting items in a numbered list does not require renumbering the list, and if you use revision control, comparing differences becomes much easier when changes are made in the middle of a numbered list\).
5. When you are working within numbered or bulleted lists, and you want to include additional content \(more paragraphs, images, videos, knowledge blocks, code blocks, etc.\) in a particular item in your list, indent that item by 4 spaces \(in Markdown, indentation creates a parent-child relationship between items\).
6. When you transition from one item type to another \(e.g. from a paragraph to a numbered list, or from a knowledge block to an alert\), you should insert a blank line for those items to be recognized as distinct and rendered properly. This also makes your Markdown easier to read. Note that multiple, consecutive blank lines are treated the same as a single blank line.
7. You can include rich media content from internal or external sources at any point in your lab instructions, directly in the Markdown either embedded inline, in a pop-up dialog behind a hyperlink, or in a new window behind a hyperlink. You can also include URLs to external content in the lab Resources tab that can be accessed at any time by lab users. These provide additional context to the lab instructions and help users learn more easily.
8. Learning about all of the different supported Markdown features early on will make it easier for you to create the best instructions possible for your users. You can read more about Markdown features in the [Markdown Syntax](https://github.com/LearnOnDemandSystems/docs/blob/master/guides/idl2/idlv2-authoring-guide-and-best-practice.md#markdown-syntax) section below.

### Overview of the Lab Client

The **Lab Console** is initially displayed on the left side of the lab environment, with the home tab showing. This initial view allows users to get started with a lab immediately once it has launched. All instructions written markdown within the Lab Guide tab. Activities that the user is instructed to do can optionally be created in a task list, which will render with checkboxes before each task, allowing users to track their progress in the lab. When a user checks a checkbox, all preceding checkboxes that were unchecked will be checked. This allows users to perform multiple tasks quickly, and then mark them as complete with a single click. As users mark tasks as complete, this progress is tracked and reported to a database, while providing a visual marker to the end user indicating where they are in the lab. Overall lab progress is reported as the percentage of tasks that are marked as complete in the lab instructions

### Authoring Lab Instructions

See the [Markdown Syntax](markdown-syntax.md) section for a detailed guide how to author lab instructions.

### \`\`

