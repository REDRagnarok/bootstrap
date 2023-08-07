---
layout: docs
title: Aspect ratio
description: Use the `aspect-ratio` property to make an element maintain the aspect ratio of your choosing. Ideal for responsively handling video or slideshow embeds based on the width of the parent.
group: utilities
toc: true
---

Use the ratio utility to manage the aspect ratios of content like `<iframe>`s, `<embed>`s, `<video>`s, and `<object>`s. These helpers also can be used on any standard HTML child element (e.g., a `<div>` or `<img>`). Customize the available aspect ratios with the Sass variable or the utility API.

{{< callout info >}}
**Pro-Tip!** You don't need `frameborder="0"` on your `<iframe>`s as we override that for you in [Reboot]({{< docsref "/content/reboot" >}}).
{{< /callout >}}

## Example

Add your ratio utility to the element you want to modify, like an `<iframe>`. Ratio utilities also pair well with any width utilities, as shown below.

{{< example >}}
<iframe class="w-100 ratio-16x9" src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0" title="YouTube video" allowfullscreen></iframe>
{{< /example >}}

## Aspect ratios

A handful of aspect ratio classes are provided by default, generated via the utility API and the `$aspect-ratios` Sass variable.

{{< example class="bd-example-ratios d-flex flex-column align-start" >}}
<div class="ratio-auto">
  <div>Auto</div>
</div>
<div class="w-25 ratio-1x1">
  <div>1x1</div>
</div>
<div class="w-50 ratio-4x3">
  <div>4x3</div>
</div>
<div class="w-75 ratio-16x9">
  <div>16x9</div>
</div>
<div class="w-100 ratio-21x9">
  <div>21x9</div>
</div>
{{< /example >}}

## Sass maps

Within `_variables.scss`, you can change the aspect ratios you want to use. Here's our default `$aspect-ratios` map. Modify the map as you like and recompile your Sass to put them to use.

{{< scss-docs name="aspect-ratios" file="scss/_variables.scss" >}}