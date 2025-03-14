---
layout: entry
title:  "Textarea"
description: "How to code and test an accessible textarea for Web"
categories: form

keyboard:
  tab: |
    Focus moves visibly to the textarea unless it's disabled
      
mobile:
  swipe: |
    Focus moves to the textarea
  keyboard: |
    Keyboard appears

screenreader:
  name:  |
    Its purpose is clear
  role:  |
    It identifies itself as a textarea
  group: |
    Hints or errors (ex: chars remaining) are read after the label, related inputs include a group name (ex: Contact us)
  state: |
    If applicable, it expresses its state (required, disabled / dimmed / unavailable)

gherkin-keyboard: 
  - when:  |
      the tab key to move focus to a textarea
    result: |
      focus is strongly visually indicated

gherkin-mobile:
  - when:  |
      swipe to focus on a textarea

design:
  - name: Perceivable
    list:
      - criteria: Is easy to identify as interactive
      - criteria: Type size is optically no smaller than 16px Helvetica
      - criteria: The text has a 4.5:1 minimum contrast ratio
      - criteria: Label is always visible (placeholder cannot be used as a label)
      - criteria: Color is not used as the only means of conveying information or state (error, success, focus, disabled etc)
  - name: Operable
    list:
      - criteria: The click/tap target area is no smaller than 44x44px
      - criteria: The disabled and focus states have a 3:1 minimum contrast ratio against default
      - criteria: The focus indication has a 3:1 minimum contrast ratio against adjacent elements
      - criteria: The focus indication has a minimum area equal to the width of the element and 2px in height
  - name: Understandable
    list:
      - criteria: The input purpose should be clear in the context of the whole page
      - criteria: The width of the input accommodates/affords the intended input, reinforcing its purpose
  - name: Robust
    list:
      - criteria: Meets criteria across platforms, devices and viewports
---

## Code examples

### Use semantic HTML
This semantic HTML contains all accessibility features by default. 

{% highlight html %}
{% include /examples/textarea.html %}
{% endhighlight %}

{::nomarkdown}
<example>
{% include /examples/textarea.html %}
</example>
{:/}
