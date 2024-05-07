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

For **highlighting** words or short sentences with a yellow background, use `{.hl}`:
`This is a [highlighted]{.hl} word.`

---

### References

Put links and references into the **footer**. Whenever possible, provide an html link to the source. Try to find an Open Access version of papers and add this as additional link (if the original source is not already OA).

**Example reference**:

```
::: footer
See Schönbrodt, F. D., & Perugini, M. (2013). At what sample size do correlations stabilize? *Journal of Research in Personality, 47*, 609-612. doi:[10.1016/j.jrp.2013.05.009](http://www.sciencedirect.com/science/article/pii/S0092656613000858). [OA version](https://osf.io/5u6hv/).
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
![](img/Observation-Intervention-Modells-Graph.jpg){ height=300px }
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