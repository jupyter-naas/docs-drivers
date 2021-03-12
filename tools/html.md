---
description: Build HTML easily for emails or webpages
---

# Email builder

## Title

### Solo

```python
email_content = naas_drivers.emailbuilder.title("My title")
```

### Subtitle

```python
email_content = naas_drivers.emailbuilder.title("My title", "My subtitle")
```

## Heading

```python
email_content = naas_drivers.emailbuilder.heading("My heading")
```

## Subheading

```python
email_content = naas_drivers.emailbuilder.subheading("My subheading")
```

## Text

### Simple

```python
email_content = naas_drivers.emailbuilder.text("My text")
```

### Font Size

```python
email_content = naas_drivers.emailbuilder.text("My text", font_size="42px")
```

## Info

Create infobox

```python
text = naas_drivers.emailbuilder.text("My text")
email_content = naas_drivers.emailbuilder.info(text)
```

## Space

Add a empty line 

```text
email_content = naas_drivers.emailbuilder.space()
```

## Separator

Add a line separator

```text
email_content = naas_drivers.emailbuilder.separator()
```

## Button

### Link

```python
email_content = naas_drivers.emailbuilder.button("https://www.google.com")
```

### Title

```python
url = "https://www.google.com"
email_content = naas_drivers.emailbuilder.button(url, title="Open me")
```

### Size

```python
url = "https://www.google.com"
email_content = naas_drivers.emailbuilder.button(url, width="300px")
```

### Colors

```python
url = "https://www.google.com"
email_content = naas_drivers.emailbuilder.button(url, color="blue", background_color="white")
```

## Address

```python
email_content = naas_drivers.emailbuilder.address("My title", "My content")
```

## Link

### Simple

```python
link = "https://google.com"
email_content = naas_drivers.emailbuilder.link(link)
```

### Title

```python
link = "https://google.com"
email_content = naas_drivers.emailbuilder.link(link, title="My title")
```

### Color

```python
link = "https://google.com"
email_content = naas_drivers.emailbuilder.link(link, color="#F2F2F2")
```



## Table

### Simple

```python
data = [["😁 Happier subscribers!", "👌 Touchable interface!", "❤️ No more frustration!"],["💌 Semantic email markup!", "🦻 Screenreader friendly!", "💬 Commented for easy use!"]]
email_content = naas_drivers.emailbuilder.table(data)
```

### Dataframe

{% hint style="info" %}
The drivers will try to transform all your column with they column title
{% endhint %}

{% hint style="success" %}
you can pass parameters with`_ exemple: text_14px link_Read`
{% endhint %}



\`\`

```python
data = pandas.DataFrame()
# each column title will be tranform in any html type
email_content = naas_drivers.emailbuilder.table(data)
```

## Image

### Simple

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
email_content = naas_drivers.emailbuilder.image(url)
```

### Link

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
link = "https://google.com"
email_content = naas_drivers.emailbuilder.image(url, link=link)
```

### Name

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
name = "Image name"
email_content = naas_drivers.emailbuilder.image(url, name=name)
```

### Align

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
align = "right" # can be right left or center
email_content = naas_drivers.emailbuilder.image(url, align=align)
```

### Size

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
width="90%"
height="80%"
email_content = naas_drivers.emailbuilder.image(url, width=width, height=height)
```

## Logo

### Simple

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
email_content = naas_drivers.emailbuilder.image(url)
```

### Link

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
link = "https://google.com"
email_content = naas_drivers.emailbuilder.image(url, link=link)
```

### Name

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
name = "Image name"
email_content = naas_drivers.emailbuilder.image(url, name=name)
```

### Align

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
align = "right" # can be right left or center
email_content = naas_drivers.emailbuilder.image(url, align=align)
```

### Size

```python
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
size="90px"
email_content = naas_drivers.emailbuilder.image(url, size=size)
```

## Header

```python
elems = [naas_drivers.html().text("My text")]
email_content = naas_drivers.emailbuilder.header(elems)
```

## Footer

```python
elem = naas_drivers.html().title("My title")
elems = [naas_drivers.html().text("My text")]
email_content = naas_drivers.emailbuilder.footer("My title", elem, elems)
```

## Generate

```python
stock="TSLA"

title=f'Evolution of {stock} stock'
heading="👉 Analyze daily performance over time."
content:"""
        🚀 Explore the data, zoom, and get deeply insights over the 100 last days Below. 
        Picture are nice but dynamic chart below are way more fun  :
"""
display = 'iframe' # can be iframe, embed or False ( for display in notebook)
email_content = naas_drivers.emailbuilder.generate(
        title=title,
        heading=heading,
        content=content,
        button_Explore_300px=url_html,
        display=display
)
```

## Export

```python
email_content = ""
filenames = "myfile.html" # can be .html .png .pdf or .jpeg file
# can be a list too
filenames = ["myfile.html", "myfile.pdf"]
css = ".class{ color: white;}" # allow css injection
naas_drivers.emailbuilder.export(email_content, filenames, css)
```

## Convert

{% hint style="info" %}
only support markdown to html for now
{% endhint %}

```python
data = """
# Welcome Title

text here
"""
naas_drivers.emailbuilder.convert(data, input_type="markdown")
```

