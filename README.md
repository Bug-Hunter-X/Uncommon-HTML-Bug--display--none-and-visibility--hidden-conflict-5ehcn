# Uncommon HTML Bug: display: none and visibility: hidden conflict

This repository demonstrates an uncommon bug in HTML related to the use of `display: none` and `visibility: hidden` on the same element.

While both properties control the visibility of an element, they do so in different ways.  Using them together can lead to unexpected and inconsistent results across browsers.

**Bug Description:**
The bug involves setting both `display: none` and `visibility: hidden` on an element. While `display: none` removes the element from the layout flow completely, `visibility: hidden` keeps the element in the flow but makes it invisible.

The combination of both can produce unexpected behavior because the order of operations might lead to one property overriding the other, potentially causing elements to display unexpectedly or not at all. It's generally better to use only one of these styles for clearer and more consistent results.

**Solution:**
Use only one of `display: none` or `visibility: hidden`, depending on the desired effect.  If you want to completely remove the element from the flow (and any space it occupies), use `display: none`. If you want to keep the element in the flow but hide its contents, use `visibility: hidden`.