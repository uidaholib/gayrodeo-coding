---
title: 2 - Code
nav: true
---
{% assign filters = site.data.filters | sort: "shortfilter" %}
{% assign conversation = site.data.conversation-filters | sort: "tag" %}

# Code Your Transcript

At this point, you should have three documents:

1. A Google Doc version of the transcript

2. A Google Sheet named `lastnamefirstname_original`

3. A Google Sheet named `lastnamefirstname`. This is the file you'll be working on from now on. It should be a transcript that's set up like this...

{% include figure.html img="/code/codesample2.png" caption="Sample Transcript CSV" alt="a screenshot of a transcript coded in google sheets" width="100%" %}

...with four columns labeled `timestamp`, `speaker`, `words`, and `tags`

Now it's time to start coding! Follow these steps:

- [Tag Your Transcript](#trans)
- [Remove Unwanted Content](#remove)
- [Identify Conversations](#conv)
- [Finish Up](#finish)

{:.pt-4 .mt-4 #trans}
***

## Transcript Tagging

1. Read through your transcript and tag cells with the preapproved tags in the table below. These tags should be entered into the `tags` column, in the same row as the text they're describing.

    - If you think of a new tag you'd like to use, be sure to add it to this [filters spreadsheet](https://docs.google.com/spreadsheets/d/1RX6nVuVGtlN3icz6ffOQgPDcbCXq6Rag6SgQVd-bIJA/edit?usp=sharing) before you use it.

{:.card .card-body .card-text .mx-4}
**Note: you don't need to insert a tag in every single row, only when you come across text that you think needs to be tagged**

2. Keep tags lowercase (following the format in the table below).

3. If you put multiple tags in one cell, **separate them with a semicolon (`;`)**. 

{:.pt-4}
### Tags
<table class="table table-striped border">
    <thead>
        <tr>
            <th scope="col">Tag (for use when coding):</th>
            <th scope="col">Description:</th>
        </tr>
    </thead>
    <tbody>
    {% for f in filters %}
        <tr>
            <td>{{ f.shortfilter }}</td>
            <td>{{ f.text }}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>


{:.pt-4}
### Coded Spreadsheet

{:.pt-3}
Here's how your tagged spreadsheet should look:

{% include figure.html img="/code/codesample1.png" caption="Sample Coded Spreadsheet" alt="a screenshot of a transcript coded in google sheets" width="100%" %}

{:.pt-4 .mt-4 #remove}
***

## Remove Unwanted Content

- As you read through, you might find sections of the text that should be removed from the transcript

- When you remove an entire cell of text, enter an ellipsis in brackets (`[...]`) into the empty cell

- When you remove some text from a paragraph in the middle of a cell, also replace this removed text with an ellipsis in brackets (`[...]`)

{:.pt-4 .mt-4 #conv}
***

## Curate Some Conversations

Keep track of snippets of text that you think might fit into [existing conversations](https://www.voicesofgayrodeo.com/).

{:.alert .alert-danger .text-center .mx-5}
Important: **Don't** tag your transcript spreadsheets using the conversation tags. Follow these steps instead:

1. When you find some text you think might fit in a current conversation, copy it and paste it into this spreadsheet: [Master Conversations](https://docs.google.com/spreadsheets/d/1TZpHcIRAI9KzGUwtXteLvNrPm6QO5HiNzHyZ2S9gxmU/edit?usp=sharing). 

2. When you find some text that you think should fit into a new conversation, copy and paste it into this spreadsheet: [New Conversations](https://docs.google.com/spreadsheets/d/1F0CFz7At16GcllvFMJ6MaecURfgmYW0McCeVfxgJrDU/edit?usp=sharing).

3. Insert your snippet of text into the `comments` column in the spreadsheet, and add the speaker's first name and last name to the row. 

4. Text for conversations should be short and to the point. To skip over portions of the transcript in the conversation text, simply replace the unwanted text with an epllisis in brackets `[...]`.

5. Tag your snippet of text with an appropriate tag selected from *Conversation Tags* table below. **Only one conversation tag is allowed per text selection**.

{:.pt-4}

### Conversation Tags
<table class="table table-striped border">
    <thead>
        <tr>
            <th scope="col">Tag (for use when coding):</th>
            <th scope="col">Question:</th>
        </tr>
    </thead>
    <tbody>
    {% for c in conversation %}
        <tr>
            <td>{{ c.tag }}</td>
            <td>{{ c.question }}</td>
        </tr>
    {% endfor %}
    </tbody>
</table>

{:.pt-4 .mt-4 #finish}
***

## Finishing Up

When your transcript is finished, notify Becca and she will check it for you. 

Once she approves it, you'll need to download the transcript to your computer as a **comma-separated file (CSV)**. Follow the steps below:

1. Click on `File` > `Download` > `Comma-separated values (.csv, current sheet)`.

2. **Don't** open the CSV. Make sure you know where it's located on your computer, then move to the next page for instructions on what to do next.

{% include figure.html img="/code/download.png" caption="Download Your Transcript as a CSV" alt="a screenshot of steps to download a google sheet as a csv" width="100%" %}

