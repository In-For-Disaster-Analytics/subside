---
Title: Mkdocs Reference Examples
---
## Admonitions

### Standard
!!! note "Custom name text"

    Look in [documentation](https://squidfunk.github.io/mkdocs-material/reference/admonitions/) for alternative icon options. 

    Standard type qualifiers (for the icon): note; abstract; info; tip; success; question; warning; failure; danger; bug; example; quote

### Collapsible
???+ note "Custom name text"

    This is defined with ??? rather than !!! to start the admonition.  ???+ defaults to open while ??? defaults closed.

## Annotations

Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
{ .annotate }

1.  :man_raising_hand: I'm an annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be expressed in Markdown.

### Nested
!!! note annotate "Phasellus posuere in sem ut cursus (1)"

    Lorem ipsum dolor sit amet, (2) consectetur adipiscing elit. Nulla et
    euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
    purus auctor massa, nec semper lorem quam in massa.

1.  :man_raising_hand: I'm an annotation!
2.  :woman_raising_hand: I'm an annotation as well!

## Buttons

[Test Button](#){ .md-button }

## Code Blocks
Include Code Blocks with copy feature

``` py 
import pandas as pd
```

``` py title="bubble_sort_example.py" linenums="1"
def bubble_sort(items): 
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

``` yaml
theme:
  features:
    - content.code.annotate # (1) (2)
```

1.  :man_raising_hand: I'm a code annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be written in Markdown.
2. This is another

## Content Tabs

=== "TAB 1"

    Add content here
=== "TAB 2"
    tab 2 content here.
