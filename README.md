# NOTES FELIX

https://stackoverflow.com/questions/76505317/custom-footer-on-the-title-slide-for-quarto-revealjs-slides

# TODO:

Store Google fonts locally in template:
https://github.com/quarto-dev/quarto-cli/issues/4387


# Quarto clean theme - FOMO

A minimal and elegant presentation theme for Quarto Reveal.js, inspired by Kyle's
[LaTex template](https://raw.githack.com/kylebutts/templates/master/latex-slides/auxiliary/slides.pdf).

Click the screenshot below to be taken to a
[live demo](https://grantmcdermott.com/quarto-revealjs-clean-demo/template.html).

[![](clean-title.png "live demo")](https://grantmcdermott.com/quarto-revealjs-clean-demo/template.html)

## Use

Depending on your use case, here are some [Quarto CLI](https://quarto.org/)
commands to get started.

If you would like to add the **clean** theme to an existing directory:

```bash
quarto install extension nicebread/quarto-revealjs-clean-FS
```

Alternatively, you can use a
[Quarto template](https://quarto.org/docs/extensions/starter-templates.html)
that bundles the **clean** theme plus a .qmd starter document. This is a better
option if you are starting a new project from scratch, since it will automatically
create a new directory with all of the necessary scaffolding in one go. We provide
two template options.

- Bare bones template

```bash
quarto use template grantmcdermott/quarto-revealjs-clean
```

- Full demo template

```bash
quarto use template grantmcdermott/quarto-revealjs-clean-demo
```
