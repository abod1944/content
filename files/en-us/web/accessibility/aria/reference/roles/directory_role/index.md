---
title: "ARIA: directory role"
short-title: directory
slug: Web/Accessibility/ARIA/Reference/Roles/directory_role
page-type: aria-role
status:
  - deprecated
spec-urls: https://w3c.github.io/aria/#directory
sidebar: accessibilitysidebar
---

The `directory` role was for a list of references to members of a group, such as a static table of contents.

> [!WARNING]
> The `directory` role was deprecated in ARIA 1.2

## Description

A directory is a static table of contents, whether linked or unlinked. This includes tables of contents built with lists, including nested lists. Dynamic tables of contents, however, might use a tree role instead.

The deprecated `directory` role was used for lists of references to members of a group, such as a static table of contents.
Use the [`list`](/en-US/docs/Web/Accessibility/ARIA/Reference/Roles/list_role) role instead. Or, better yet, use the {{HTMLElement('ul')}} or {{HTMLElement('ol')}} elements, as using `directory` does not provide any additional benefits to assistive technology users.

## Specifications

{{Specifications}}

## See also

- [The `list` role](/en-US/docs/Web/Accessibility/ARIA/Reference/Roles/list_role)
- The {{HTMLElement('ul')}} element
- The {{HTMLElement('ol')}} element
