# nicebread theme - based on Quarto clean theme

A minimal and elegant presentation theme for Quarto Reveal.js.

The theme is heavily based on the **[clean](https://github.com/grantmcdermott/quarto-revealjs-clean)** theme by Grant McDermott, which itself is based inspired by Kyle Butts' [LaTex template](https://raw.githack.com/kylebutts/templates/master/latex-slides/auxiliary/slides.pdf).


## Use

Depending on your use case, here are some [Quarto CLI](https://quarto.org/)
commands to get started.

If you would like to add the **nicetheme** theme to an existing directory:

```bash
quarto install extension nicebread/quarto-FS
```

Alternatively, you can use a
[Quarto template](https://quarto.org/docs/extensions/starter-templates.html)
that bundles the **nicetheme** theme plus a .qmd starter document. This is a better
option if you are starting a new project from scratch, since it will automatically
create a new directory with all of the necessary scaffolding in one go. We provide
two template options.

```bash
quarto use template nicebread/quarto-FS
```

# Resources

https://stackoverflow.com/questions/76505317/custom-footer-on-the-title-slide-for-quarto-revealjs-slides


# TODO:

Store Google fonts locally in template:
https://github.com/quarto-dev/quarto-cli/issues/4387

# Style guide

## Changing the font size and color

If a bullet point list is too large, wrap it in a `{.smaller}` section. Sections are marked by a leading and a trailing `:::`:

```
::: {.smaller}
- long list 1
- long list 2
...
- long list 13
:::
```

It even gets smaller with the `{.smallest}` class:

```
::: {.smallest}
- long list 1
- long list 2
...
- long list 23
:::
```

But if you need the `{.smallest}` class as a "last resort" to squeeze everything onto one slide, you should consider to split it over multiple slides.

---
For changing the text to a specific font size, use this:

```
<div style=" font-size: 24px;"> 
Text
</div>
```
---

For changing the text color, use this:

```
<div style="color: gray;"> 
Text
</div>
```
---

For changing both the font size and the text color, use this:

```
<div style="font-size: 24px; color: gray;"> 
Text
</div>
```
---

For **highlighting** words or short sentences with a yellow background, use `{.hl}`:
`This is a [highlighted]{.hl} word.`

---


## Changing the position of the text

To center the text, use this:

```
<div style="text-align: center;">
Text
</div>
```

If the only text on the slide is the title, and it needs to be centered, use this:

```
<div style="display: flex; align-items: center; justify-content: center; height: 600px;">
  <h1>Title</h1>
</div>
```
You can adjust the position of the text by changing the height values in the code.


To reduce the space above or under the text, you have to change the margins:

```
<div style="margin-bottom: -40px;">
Text
</div>
```
To change the margin above the text, use 'margin-top'.
To change the margin on the left side of the text, use 'margin-left'.
To change the margin on the right side of the text, use 'margin-right'.

You can also add some space above or below the text, or on its sides, by using:

```
<div style="margin-bottom: 40px;">
Text
</div>
```

To split the text, use the `<br>` command:

```
This text is too long <br> and it needs to be split.
```
---

## Changing the style of the text

Italic text:

```
*Text*
```

Bold text:

```
**Text**
```

Bold and italic text:

```
***Text***
```

Underlining text:

```
<u>underlined</u>
```

Underlining text with a specific color:

```
<span style="border-bottom: 2px solid #89CFF0; display: inline;">Text</span>
```

'#89CFF0' is a code for a baby blue underline. You can change it to any color you wish, but you need to look up the specific color code on the internet.

If you want to change the thickness of the underline, you can do it by changing this part of the code '2px'.

---

More finegrained control over the style can be achieved by adding CSS attributes to a div:

```
::: {#test .hl style="text-size: 80%; color: red;"}
CONTENT
:::
```

- `#test` is the id of the div
- `.hl` is the class of the div (defined in the CSS file)
- in the `style` string, you can add any CSS attribute you like (on top of the attributes already defined in your separate CSS file). Don't forget to separate attributes with a semicolon.


### References

Put links and references into the **footer**. Whenever possible, provide an html link to the source. Try to find an Open Access version of papers and add this as additional link (if the original source is not already OA).

**Example reference**:

```
::: footer
See Schönbrodt, F. D., & Perugini, M. (2013). At what sample size do correlations stabilize? *Journal of Research in Personality, 47*, 609-612. doi:[10.1016/j.jrp.2013.05.009](http://www.sciencedirect.com/science/article/pii/S0092656613000858). [OA version](https://osf.io/5u6hv/).
:::
```

If the text in the footer is too long, shorten it.

Before:

```
::: {.footer}

                                                    
Benjamin, D. J., Berger, J. O., Johannesson, M., Nosek, B. A., Wagenmakers, E. J., Berk, R., ... & Cesarini, D. (2018). Redefine statistical significance. Nature Human Behaviour, 2(1), 6. doi:10.1038/s41562-017-0189-z


Bondareva, D. (2013). Introduction to Power Analysis. Presentation for EPSE 482 Introduction to Statistics for Research in Education. Slides available [slideshare.net/dbondareva/introduction-to-power-analysis](slideshare.net/dbondareva/introduction-to-power-analysis)
                                                    
                                                    
Lakens, D., Adolfi, F. G., Albers, C. J., Anvari, F., Apps, M. A., Argamon, S. E., ... & Buchanan, E. M. (2018). Justify your alpha. Nature Human Behaviour, 2, 168-171. doi: 10.1038/s41562-018-0311-x

                                                    
:::

```
After (without line break, shorter; set the link to the doi):

```
::: {.footer}
                                                    
::: {.smaller}
                                                    
Benjamin et al. (2018). Redefine statistical significance. doi:[10.1038/s41562-017-0189-z]([10.1038/s41562-017-0189-z]()); Lakens et al. (2018). Justify your alpha.
 doi:[10.1038/s41562-018-0311-x](https://pure.tue.nl/ws/portalfiles/portal/119109470/Lakens_et_al._2018_Justify_your_alpha.pdf)
                                                    
:::
                                                    
:::

```

**Example for image source**:

When you use an external image, always give a link to the original location and state the license. From the Creative Commons licenses, only CC-BY, CC-BY-SA, or CC0 can be included in Open Educational Materials.

```
::: footer
Photography from [Ferdinand Schmutzer](https://de.wikipedia.org/wiki/Albert_Einstein#/media/Datei:Albert_Einstein_1921_by_F_Schmutzer.jpg), CC0.
:::
```

Alternatively, you can put a reference into a *vertical text* field on the right side using the `{.attribution}` class:

```
::: {.attribution}
Slide by [Karolin Salmen](https://www.psycharchives.org/en/item/cde1ef17-611c-42d0-8835-95592cab521a), CC-BY
:::
```
If many references are on one slide, you can "distribute" them across the footer and the attribution text field.

---

### Images

When shrinking images, only use *either* `height=???px` *or* `width=???px` (otherwise the aspect ratio of the image is changed).

```
![](img/Observation-Intervention-Modells-Graph.jpg){height=300px}
![](img/reportedeffectsize.png){fig-align="center" height=420px}
```

Add a drop-shadow to images with the `.ds` class:

```
![](img/forestplot.png){.ds}
```

# Troubleshooting: How to resolve merge conflicts after pulling

1. Locally resolve the merge conflict:

Look for:

```
<<<<<<<< HEAD

Version 1 Text

=========

Version 2 Text

>>>>>>>> Revision abcd12345567
```

Decide which version is the correct one (or merge them manually).
Delete the other version, including the tags (`<<<<<<<< HEAD`, `=========` and `>>>>>>>> Revision abcd12345567`)

2. Commit locally.
3. Push.
