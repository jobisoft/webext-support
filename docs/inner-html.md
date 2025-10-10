---
layout: default
title: Avoid using `innerHTML`
nav_order: 2
---

# Avoid using `innerHTML`

Directly assigning to `element.innerHTML` can introduce XSS vulnerabilities and break Thunderbird's content policies.

## Recommended Alternatives

Use the DOM API to create and append elements safely:

```js
const div = document.createElement("div");
div.textContent = "Safe text here";
parent.appendChild(div);
