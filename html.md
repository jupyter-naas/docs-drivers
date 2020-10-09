# Html

## Address

## link

## Header

## Footer

## Info

## Space

## Table

## Logo

## Cover

## Title

## Subtitle

## Button

## Text

## Template\_basic

## Generate

```text
title = "All new: Accessibility"
sub_title = "Accessibility baked-in for better user experiences"
content = "Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae laborum, eveniet asperiores atque repellendus quo nostrum eos enim eum illum non ad quidem ipsa dolore esse, reprehenderit obcaecati! Vel, quas."
logo = Html().logo("https://i.ibb.co/PchQTbY/Screenshot-2020-10-08-at-21-20-39.png")
address = Html().address("Your Friends:", "1234 Main Street, Anywhere, US 56789")

content = Html().table([content, sub_title, logo, address, sub_title, logo], column=3, border=True)

cover = Html().cover("https://i.ibb.co/pr7vbMC/Screenshot-2020-10-08-at-21-20-30.png")
link = Html().link("https://litmus.com/community/templates/31-accessible-product-announcement-email", "you can unsubscribe here")
footer = Html().footer("You received this email because you care about creating more accessible experiences for people. Don't worry,", link, address)
button = Html().button("Get Accessible Now", "https://google.com")
table = Html().table(["😁 Happier subscribers!", "👌 Touchable interface!", "❤️ No more frustration!", "💌 Semantic email markup!", "🦻 Screenreader friendly!", "💬 Commented for easy use!"])
main = Html().template_basic(
        title,
        sub_title,
        content,
        logo,
        cover,
        table,
        button,
        footer
)
res = Html().generate(title, sub_title, main)
```

