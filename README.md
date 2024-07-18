# Print Ticket PDF documentation

The application uses its own editor to create the template. This article will help you in creating/modifying a template

## How to use HTML content option

The "HTML content" field contains the content of the selected block. You can use any HTML tags. You can also set the <style> tag with your own settings. You can also use specified variables, which will be replaced with real values when generating a PDF file. The list of available variables is listed at the bottom of this document.
Example HTML block:

```
<style>
.inline {
  display: inline-block;
  vertical-align: top;
}
.message-container {padding: 0 16px;}
.created-at {
  font-style: italic;
  color: #475867;
  font-weight: 400;
}
</style>
<div style="display:flex">
<div class="inline message-container">
<div><b>{{name}} added private note</b></div>
<div class="created-at">{{created_at}}</div>
<br>
<div>{{message}}</div>
</div>
</div>
```

## How to use Custom CSS option

The CSS custom field displays the specified styles of the selected block. You can also add your own styles or change existing ones. The specified styles are applied to the entire block.

## How to create/update Message block

When you select a block with "Messages Block" type, the application creates block, which contain several message blocks. You can change each type of message. Message can contain avatar block. Use **img** tag with **"avatar-image"** class and **image/url** to add avatar. In this case, if requester/agent has avatar it will be displayed in PDF. Otherwise the app will display image/url from img tag.

## Variables list

**Global variables**:
{{ticket_id}}
{{requester_email}}
{{requester_name}}
{{requester_mobile}}
{{requester_phone}}
{{tags}}
{{created_at}}
{{group}}
{{company}}
{{priority}}
{{product}}
{{source}}
{{status}}
{{subject}}
{{ticket_type}}
{{description}}
{{agent}}

**Message**:
{{name}}
{{created_at}}
{{message}}
{{to_email}}
{{cc_email}}

**Attachment**:
{{attachment_name}}
{{size}}
{{type}}
