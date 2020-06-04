---
title: Theme

createdAt: 2020-06-01T00:00:00-0300
updatedAt: 2020-06-01T00:00:00-0300
noToc: true
---

Headings
--------

Heading 1
=========
Heading 2
---------
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6


Paragraphs
----------

In ornare dapibus nulla. Proin rhoncus consectetur ligula, eget porta enim laoreet nec. Vivamus pharetra vulputate felis in cursus. Integer quam quam, laoreet sed placerat facilisis, efficitur sit amet ligula. In quis diam ornare justo tincidunt cursus sit amet tincidunt risus. Donec bibendum auctor efficitur. Aenean sed libero magna. Phasellus porttitor placerat ipsum, iaculis porttitor ante tincidunt et. Nam ullamcorper ex eu leo pellentesque commodo. In egestas mi elementum turpis tincidunt, nec commodo nisi semper. Fusce tempus pharetra vestibulum. Proin eget lorem ex. Nulla auctor posuere tortor sed vestibulum. Fusce non leo mattis, sodales purus ac, tincidunt nulla. Maecenas dignissim, mi eget tempor vestibulum, odio ex scelerisque libero, ac sollicitudin arcu erat ut neque.

Vivamus aliquet a tortor non pretium. Integer ac molestie odio. Maecenas hendrerit feugiat nibh sit amet sollicitudin. Mauris vitae placerat orci. Donec ultricies venenatis convallis. Cras elementum velit nisl, posuere rhoncus orci consequat id. Vestibulum sit amet est varius, bibendum neque at, molestie sem. Nam ex dui, bibendum id blandit sed, imperdiet id ex. Cras consequat augue sit amet sapien rutrum luctus. In aliquam interdum diam faucibus sollicitudin. Etiam tortor lacus, scelerisque eu fringilla at, sodales ac enim. Duis convallis lectus dui, sit amet malesuada purus cursus a. Quisque et ultrices nisl. Sed eu mi vel eros convallis condimentum eget sed felis.


Text formatting
---------------

*Emphasized text*. **strong emphasis**. `code`.


Blockquote
----------

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.


Unordered List
--------------

  * Item 1
  * Item 2
  * Item 3
    * Item 3.1
    * Item 3.2
      * Item 3.2.1
  * Item 4


Ordered List
------------

1. Item
    1. First Subitem
    2. Second Subitem
1. Item
    - First Subitem
    - Second Subitem
1. Item


Links
-----

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.

This is [an example][id] reference-style link.


Horizontal Ruler
----------------

---


Code
----

```js
import fs from 'fs';
import path from 'path';

export default () => ({
  afterExport: state => {
    const {
      config: {
        paths: { DIST },
      },
      routes,
    } = state;
    routes.filter(({ data }) => data.dir && data.dir === 'gpg')
    .forEach(route => {
      fs.writeFileSync(path.join(DIST, 'gpg', route.data.filename), route.data.content);
    });
    return state;
  },
});
```


Admonitions
-----------

:::note Note
Future versions of this feature may not be backward compatible.
Consider implementing the revised interface now.
:::

:::important Important
No user-servicable parts inside. Breaking this seal voids all warranties.
:::

:::tip Tip
If you tie your shoelaces, you're less likely to trip and fall down.
:::

:::caution Caution
Breaking this seal voids all warranties.
:::

:::warning Warning
Striking your thumb with a hammer may cause severe pain and discomfort.
:::


[id]: http://example.com/  "Optional Title Here"
