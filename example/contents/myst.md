# MyST Markdown

MyST (Markedly Structured Text) markdown is a superset of CommonMark Markdown which extend the flavor of Markdown with rich features. It's inspired by RMarkdown.

```{note}
For those who are familiar with Sphinx, MyST is CommonMark + Markdown extensions + Sphinx roles andirectives.
```


## Directives and roles

Directives and roles are maybe the most used features in Jupyter Book, especially in MyST. They behaves like a function that transforms your content into beautiful styled section.


### Directives

The syntax for creating a content using directives is:

````
```{note}
This is a note
```
````

The above syntax will result in:

```{note}
This is a note
```

Some directives require us to provide argument(s), called directive arguments. For example, when we use `admonition`, `figure`, etc. The syntax is pretty straightforward.

Directive Arguments
: a list of words that come after the `{directivename}`.

````
```{directivename} arg1 arg2
Directive content
```
````

We can also provide some configuration to the directive by using directive keywords.

Directive Keywords
: a collection of flags in key/value paris that come underneath `{directivename}`.

````
```{directivename}
:key1: metadata1
:key2: metadata2
```
directive content.
````

or,


````
```{directivename}
---
key1: metadata1
key2: metadata2
---
directive content.
```
````


### Roles

To use roles, we use below syntax.

```
A content {rolename}`of roles`.
```

For example, we can use roles to refer and provide a link to go to certain file. For example, the syntax {doc}`../references` will result in: {doc}`../references`.

```{admonition} Directives and Roles Availability
* Any directive/role that is available in Sphinx
* reStructuredText directives
```
