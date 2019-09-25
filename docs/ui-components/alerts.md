---
layout: default
title: Alerts
parent: UI Components
nav_order: 4
---

# Alerts
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

Alerts are info, warning, tip or other messages you can call out in a special formating.

Alerts are added through special include statements you can add in your markdown pages. Here is a simple example:

```html
{% raw %}{% include alert.html content="This is my alert" %}{% endraw %}
```

Will give this result:

{% include alert.html content="This is my alert" %}

## Alert types

There are 4 types of alerts:

- Information alert
- Tip alerts
- Danger/warning alerts
- Important notice alerts

They all function the same except they have a different color and icon. You choose the type by calling it out in the `alert-type` parameter. Here are samples of each alert:

### Information alert 
{: .no_toc }

This is also the default type if `alert-type` isn't called out:

```html
{% raw %}{% include alert.html alert-type="info" content="This is my information alert" %}{% endraw %}
```

{% include alert.html alert-type="info" content="This is my information alert" %}

### Tip alert
{: .no_toc }

```html
{% raw %}{% include alert.html alert-type="tip" content="This is my tip alert" %}{% endraw %}
```

{% include alert.html alert-type="tip" content="This is my tip alert" %}

### Danger/warning alert
{: .no_toc }

```html
{% raw %}{% include alert.html alert-type="danger" content="This is my danger alert" %}{% endraw %}
```

{% include alert.html alert-type="danger" content="This is my danger alert" %}

### Important alert
{: .no_toc }

```html
{% raw %}{% include alert.html alert-type="important" content="This is my important alert" %}{% endraw %}
```

{% include alert.html alert-type="important" content="This is my important alert" %}

## Alert title

You can optionally add an alert title that will appear in bold after the alert icon and before the alert content. You can do that by adding the `title` parameter, like that:

```html
{% raw %}{% include alert.html alert-type="info" title="Note" content="this is my information alert" %}{% endraw %}
```

{% include alert.html alert-type="info" title="Note" content="this is my information alert" %}

## Using block level tags inside the alerts

If you need multiple paragraphs, enter `<br/><br/>` tags. This is because block level tags aren’t allowed here, as Kramdown is processing the content as Markdown despite the fact that the content is surrounded by HTML tags. Here’s an example with a break:

```html
{% raw %}{% include alert.html alert-type="important" title="Important" content="this is my important alert<br/><br/>Here is another paragraph" %}{% endraw %}
```

{% include alert.html alert-type="important" title="Important" content="this is my important alert<br/><br/>Here is another paragraph" %}

## Parameter summary

| Parameter    | Description       | Possible values                     | Must/Optional                |
|:-------------|:------------------|:------------------------------------|:-----------------------------|
| `content`    | alert content     | any string                          | must                         |
| `alert-type` | alert type        | `info`, `tip`, `danger`, `important`| optional (default: `info`)   |
| `title`      | alert title       | any string (supposed to be short)   | optional (default: no title) |