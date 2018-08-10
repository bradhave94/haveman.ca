# Custom Module Fields

### Available Fields

* [Choice](#choice)
* [Text](#text)
* [Image](#Image)
* [Number](#Number)
* [Date](#date)
* [Date and Time](#date-and-time)
* [CTA](#cta)
* [Blog](#blog)
* [Tag](#tag)
* [Form](#form)
* [Color](#color)
* [Page](#page)
* [Workflow](#workflow)
* [Follow-up Email](#follow-up-email)
* [Email Address](#email-address)
* [File](#file)
* [HubDB Table](#hubdb-table)
* [Simple Menu](#simple-menu)
* [Menu](#menu)
* [Meetings](#meetings)
* [Logo](#logo)
* [Icon](#icon)

### Choice
A radio select/pick list option visible in the content editor that lets the marketer select and insert a predefined value into the content of the module.
* For dropdown select - `"display" : "select"`
* For radio buttons - `"display" : "radio"`

``` 
{
    "id" : "",
    "name" : "",
    "label" : "",
    "display" : "select",
    "choices" : [ 
        [ "valueOne", "Label One" ], 
        [ "valueTwo", "Label Two" ], 
        [ "valueThree", "Label Three" ]
    ],
    "placeholder" : "",
    "type" : "choice",
    "default" : ""
}
```

### Text
Use this for text sections of your custom module
* `"type" : "richtext"` - for a rich text field
* `"placeholder" : "Placeholder"` - to set placeholder text
* `"validation_regex" : "/.+\@.+\..+/"` - for regex
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "text",
    "default" : null
}
```

### Image
A single image container module that includes sizing options, default image, and alt text parameters
* `"resizable" : false` - will hide resizing options


```
{
    "id" : "",
    "name" : "",
    "label" : " ",
    "type" : "",
    "default" : {
        "src" : "",
        "alt" : "",
        "width" : "",
        "height" : ""
    }
}
```

### Number
A spinner style text field that only supports decimal or integer values.

```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "min" : 1,
    "max" : 3,
    "step" : 1,
    "type" : "number",
    "default" : 2
}
```

### Date
Selects a date. The value is stored as milliseconds since the epoch at midnight UTC on that date.

```
{
  "id" : "",
  "name" : "",
  "label" : "",
  "step" : 1,
  "type" : "date",
  "default" : 1533700800000
}
```

### Date and Time
Selects a date and optional time. The value is stored as millseconds since the epoch in UTC.

```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "step" : 45,
    "type" : "datetime",
    "default" : 1534910400000
}
```

### Image
Selects a CTA. Required for CTA module.

```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "cta",
    "default" : null
}
```

### Blog 
Selects a blog from the portal's list of blogs. Required for Blog Email Subscription, Post Listing and RSS Listing modules.

```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "blog",
    "default" : 6019357429
}
```

### Tag 
Selects a blog tag from the portal. Required for RSS Listing module.
* `"tag_value" : "SLUG",`
*  `"tag_value" : "ID",`
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "tag_value" : "SLUG",
    "type" : "tag",
    "default" : "insider"
}
```

### Form
Selects a HubSpot form. Required for Form module.
* `"response_type" : "redirect",`
* `"response_type" : "inline",`
```
{
    "id" : "",
    "name" : "form_page",
    "label" : "Form page",
    "type" : "form",
    "default" : {
        "form_id" : "",
        "response_type" : "redirect",
        "message" : "Thanks for submitting the form.",
        "redirect_id" : page-id,
        "redirect_url" : "",
        "gotowebinar_webinar_key" : null
    }
}
```

### Color 
Picks a color.
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "color",
    "default" : {
        "color" : "#ffffff",
        "opacity" : 100
    }
}
```

### Page 
Selects a published website or landing page. Required for form module.
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "page",
    "default" : "page-id"
}
```

### Workflow 
Selects a HubSpot workflow. Required for form module.
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "workflow",
    "default" : workflow-id
}
```

### Follow-up email
Selects a follow-up email.
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "followupemail",
    "default" : email-id
}
```

### Email address 
Autofills with email addresses from portal users, but also allows any other valid email address. The value is a list of strings.
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "email",
    "default" : [ "bradley@lean-labs.com" ]
}
```

### File 
Similar to the image selector, but allows selection of other file types from File Manager. Useful for picking a PDF or image to link to. The picker attribute allows selecting files of certain types.
* `"picker" : "file"`
* `"picker" : "image"`
* `"picker" : "document"`

```
{
    "picker" : "file",
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "file",
    "default" : "file-url"
}
```


### HubDB Table 
Selects a published HubDB table to associate with this module.	
```
{
  "id" : "",
  "name" : "",
  "label" : "",
  "type" : "hubdbtable",
  "default" : "table-id"
}
```

### Simple Menu
Allows creation of a local simple menu.	
```
{
	"id": "",
	"name": "",
	"label": "",

	"type": "simplemenu",
	"default": [
	{
		"isPublished": false,
		"pageLinkId": null,
		"pageLinkName": null,
		"isDeleted": null,
		"categoryId": null,
		"subCategory": null,
		"contentType": null,
		"state": null,
		"linkLabel": "Link Level 1",
		"linkUrl": null,
		"linkParams": null,
		"linkTarget": null,
		"type": "PAGE_LINK",
		"children": [{
			"isPublished": false,
			"pageLinkId": null,
			"pageLinkName": null,
			"isDeleted": null,
			"categoryId": null,
			"subCategory": null,
			"contentType": null,
			"state": null,
			"linkLabel": "Link Level 2",
			"linkUrl": null,
			"linkParams": null,
			"linkTarget": null,
			"type": "PAGE_LINK",
			"children": []
		}]
	}, {
		"isPublished": false,
		"pageLinkId": null,
		"pageLinkName": null,
		"isDeleted": null,
		"categoryId": null,
		"subCategory": null,
		"contentType": null,
		"state": null,
		"linkLabel": "Link Level 1",
		"linkUrl": null,
		"linkParams": null,
		"linkTarget": null,
		"type": "PAGE_LINK",
		"children": []
	}]
}
```

### Menu 
Selects a menu from the portal's menu.
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "menu",
    "default" : null
}
```

### Logo
Allows selection of a logo
* `"override_inherited_src" : false`
* `"override_inherited_src" : true`
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "resizable" : true,
    "type" : "logo",
    "default" : {
        "override_inherited_src" : false,
        "src" : null,
        "alt" : null
    }
}
```

### Icon 
Allows selection of an icon
```
{
    "id" : "",
    "name" : "",
    "label" : "",
    "type" : "icon",
    "default" : {
        "name" : "facebook",
        "unicode" : "f09a",
        "type" : "REGULAR"
    }
}
```

### Field options
Modules now include validation, editor options, and display conditions as well as repeating and grouping functionality.

#### Regex
**Use a regular expression to validate a field**
`"validation_regex" : "/.+\@.+\..+/"`

#### Editor Options
**Make this field required**
User will not be able to leave this field blank.
`"required" : false,`

**Prevent editing in content editors**
Allows you to have content that is hidden and uneditable by end users
`"locked" : false,`

**Help text**
Add helper text to give users context or instruction.
`"help_text": "Your help text",`

**Display conditions**
Display if another feild meets certain criteria. A set field ID is required
Operator Options: 
* Is equal to - `"operator" : "EQUAL"`
* Is empty - `"operator" : "EMPTY"`
* Is not empty - `"operator" : "NOT_EMPTY"`
* Is not equal to - `"operator" : "NOT_EQUAL"`
* Custom regex - `"operator" : "MATCHES_REGEX"`
```
"visibility" : {
    "controlling_field" : "field-id",
    "controlling_value_regex" : null,
    "operator" : "NOT_EMPTY"
  },
```

**Field grouping**
Group indiviual fields into one group, **Note:** groups must have a set `id` to fuction properly

```
{
    {
	"id": 1,
	"label": "",
	"name": "",
	"type": "group",
	"occurrence": {
        "min" : 1,
        "max" : 10,
        "sorting_label_field" : "field-id",
        "default" : 5
	},
	"children": [
	    {
			"default": "",
			"label": "Text",
			"name": "text",
			"type": "text"
		},
		{
			"default": "",
			"label": "Rich Text",
			"name": "richtext",
			"type": "richtext"
		}
	],
	"default": [
	    {
			"text": "",
			"link": ""
		},
		{
			"text": "",
			"link": ""
		}
	]
}
```

**Field repeating**
All feilds/groups can be repeaters, Groups that are repeaters can use a Sorting Label by adding `"sorting_label_field" : "field-id",`
```
"occurrence" : {
    "min" : 1,
    "max" : 10,
    "default" : 1
}
```

**Moduel Meta Fields**
```
{
	"custom_module": {
		"author": "YOUR_EMAIL",
		"name": "MODULE_NAME",
		"css_assets": [ ],
		"editable_contexts": [ ],
		"external_js": [ ],
		"host_template_types" : [ "PAGE", "BLOG_POST", "BLOG_LISTING" ],
		"js_assets": [ ],
		"other_assets": [ ],
		"fields": [{
                "default": "",
                "label": "",
                "name": "",
                "type": ""
            }
		],
		"source": "",
		"widgetLabel": "MODULE_VERSION"
	},
	"custom_module_template": "MODULE_TEMPLATE",
	"files": []
}
```

**Adding File**
```
"files": [{
    "file": "",
    "folder_paths": ""
}]
```

