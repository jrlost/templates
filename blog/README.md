# Create new blog schema

## Create a new application that contains the `blog` using the Dashboard

1. Go to the Dashboard.
2. Click on `Start - New App with Blog`  
  <img src="https://raw.githubusercontent.com/jrlost/templates/main/blog/dashboard.png" width="650" alt="Dashboard with Start link" />
3. A modal will pop up. Enter a new app name.
4. Click `Create`.

## Import the blog schema into an existing app

1. Copy this schema  
    ```jsob
    {
        "properties": {},
        "fieldsInLists": [
            "title",
            "author",
            "displayDate",
            "meta.status",
            "meta.lastModified"
        ],
        "fieldsInReferences": [],
        "fields": [
            {
                "name": "title",
                "properties": {
                    "isRequired": true,
                    "fieldType": "String",
                    "editor": "Input",
                    "maxLength": 200,
                    "label": "Post Title",
                    "hints": "Post Title"
                },
                "partitioning": "invariant"
            },
            {
                "name": "htmlTitle",
                "properties": {
                    "isRequired": false,
                    "fieldType": "String",
                    "editor": "Input",
                    "maxLength": 200,
                    "label": "HTML Title",
                    "hints": "Custom html title for the post."
                },
                "partitioning": "invariant"
            },
            {
                "name": "slug",
                "properties": {
                    "isRequired": true,
                    "fieldType": "String",
                    "editor": "Slug",
                    "inlineEditable": true,
                    "isUnique": true,
                    "maxLength": 200,
                    "label": "Slug",
                    "hints": "A unique string that appends the primary blog URL, where this post will display."
                },
                "partitioning": "invariant"
            },
            {
                "name": "fullText",
                "properties": {
                    "fieldType": "String",
                    "editor": "RichText",
                    "label": "Full Text"
                },
                "partitioning": "invariant"
            },
            {
                "name": "shortText",
                "properties": {
                    "isRequired": true,
                    "fieldType": "String",
                    "editor": "TextArea",
                    "maxLength": 500,
                    "label": "Short Description",
                    "hints": "This is the blog post teaser that will display on the main list page."
                },
                "partitioning": "invariant"
            },
            {
                "name": "image",
                "properties": {
                    "fieldType": "Assets",
                    "maxItems": 1,
                    "label": "Featured Image",
                    "hints": "The primary image for the post."
                },
                "partitioning": "invariant"
            },
            {
                "name": "imageAltTag",
                "properties": {
                    "isRequired": false,
                    "fieldType": "String",
                    "editor": "Input",
                    "maxLength": 200,
                    "label": "Alternate tag",
                    "hints": "Enter an alt tag for the primary image."
                },
                "partitioning": "invariant"
            },
            {
                "name": "metaDescription",
                "properties": {
                    "isRequired": false,
                    "fieldType": "String",
                    "editor": "Input",
                    "maxLength": 250,
                    "label": "Meta Description",
                    "hints": "Enter meta description for the post."
                },
                "partitioning": "invariant"
            },
            {
                "name": "metaKeywords",
                "properties": {
                    "isRequired": false,
                    "fieldType": "String",
                    "editor": "Input",
                    "maxLength": 250,
                    "label": "Meta Keywords",
                    "hints": "Enter meta keywords for the post."
                },
                "partitioning": "invariant"
            },
            {
                "name": "category",
                "properties": {
                    "fieldType": "String",
                    "editor": "Input",
                    "maxLength": 100,
                    "label": "Category",
                    "hints": "Enter a category to organize blog posts."
                },
                "partitioning": "invariant"
            },
            {
                "name": "tags",
                "properties": {
                    "fieldType": "Tags",
                    "editor": "Tags",
                    "label": "Tags",
                    "hints": "Enter one to many tags per blog posts for categorization."
                },
                "partitioning": "invariant"
            },
            {
                "name": "author",
                "properties": {
                    "fieldType": "String",
                    "editor": "Input",
                    "maxLength": 100,
                    "label": "Author"
                },
                "partitioning": "invariant"
            },
            {
                "name": "displayDate",
                "properties": {
                    "isRequired": true,
                    "fieldType": "DateTime",
                    "editor": "Date",
                    "calculatedDefaultValue": "Today",
                    "label": "Date Display",
                    "hints": "The date (Central Standard Time) that will display on the blog post."
                },
                "partitioning": "invariant"
            }
        ],
        "isPublished": true
    }
    ```
2. Open the schema page.  
  <img src="https://raw.githubusercontent.com/jrlost/templates/main/blog/schema.png" width="650" alt="Schema Modal" />
3. Click on the `Add Schema Button`.
4. This will open a new modal. Enter `blog` as the schema name in this new modal.
5. Click on the `Import schema` link.
6. Paste the copied schema into the textbox.
7. Click on `Create`
