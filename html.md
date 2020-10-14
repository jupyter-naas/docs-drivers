---
description: Buil html easily for emails or webpages
---

# Html

## Title

### Solo

```text
naas_drivers.html().title("My title")
```

### Subtitle

```text
naas_drivers.html().title("My title", "My subtitle")
```

## Heading



```text
naas_drivers.html().heading("My heading")
```

## Subheading

```text
naas_drivers.html().subheading("My subheading")
```

## Text

### Simple

```text
naas_drivers.html().text("My text")
```

### Font Size

```text
naas_drivers.html().text("My text", font_size="42px")
```

## Info

Create info box

```text
text = naas_drivers.html().text("My text")
naas_drivers.html().info(text)
```

## Space

Add a empty line 

```text
naas_drivers.html().space()
```

## Separator

Add a line separator

```text
naas_drivers.html().separator()
```

## Button

### Link

```text
naas_drivers.html().button("https://www.google.com")
```

### Title

```text
url = "https://www.google.com"
naas_drivers.html().button(url, title="Open me")
```

### Size

```text
url = "https://www.google.com"
naas_drivers.html().button(url, width="300px")
```

### Colors

```text
url = "https://www.google.com"
naas_drivers.html().button(url, color="blue", background_color="white")
```

## Address

```text
naas_drivers.html().address("My title", "My content")
```

## Link

### Simple

```text
link = "https://google.com"
naas_drivers.html().link(link)
```

### Title

```text
link = "https://google.com"
naas_drivers.html().link(link, title="My title")
```

### Color

```text
link = "https://google.com"
naas_drivers.html().link(link, color="#F2F2F2")
```



## Table

```text
naas_drivers.html().table("My title")
```

## Image

### Simple

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
naas_drivers.html().image(url)
```

### Link

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
link = "https://google.com"
naas_drivers.html().image(url, link=link)
```

### Name

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
name = "Image name"
naas_drivers.html().image(url, name=name)
```

### Align

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
align = "right" # can be right left or center
naas_drivers.html().image(url, align=align)
```

### Size

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
width="90%"
height="80%"
naas_drivers.html().image(url, width=width, height=height)
```

## Logo

### Simple

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
naas_drivers.html().image(url)
```

### Link

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
link = "https://google.com"
naas_drivers.html().image(url, link=link)
```

### Name

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
name = "Image name"
naas_drivers.html().image(url, name=name)
```

### Align

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
align = "right" # can be right left or center
naas_drivers.html().image(url, align=align)
```

### Size

```text
url = "https://raw.githubusercontent.com/jupyter-naas/naas/main/images/naas_logo.svg"
size="90px"
naas_drivers.html().image(url, size=size)
```

## Header

```text
elems = [naas_drivers.html().text("My text")]
naas_drivers.html().header(elems)
```

## Footer

```text
elem = naas_drivers.html().title("My title")
elems = [naas_drivers.html().text("My text")]
naas_drivers.html().footer("My title", elem, elems)
```

## Generate

```text
action="TSLA"
title=f'Evolution of {action} stock'
email_content = naas_drivers.html().generate(
        title=f'Evolution of {action} stock',
        display='iframe',
        heading="👉 Analyze daily performance over time.",
        image=url_img,
        table=news_table,
        content="""
        🚀 Explore the data, zoom, and get deeply insights over the 100 last days Below. 
        Picture are nice but dynamic chart below are way more fun  :",
        """,
        button_Explore_white_300px=url_html
)
```

