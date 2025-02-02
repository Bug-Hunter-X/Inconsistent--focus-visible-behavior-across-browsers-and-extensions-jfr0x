# Inconsistent :focus-visible Behavior

This repository demonstrates an uncommon issue with the CSS `:focus-visible` pseudo-class.  The problem stems from inconsistencies in how different browsers and browser extensions handle this pseudo-class, particularly when accessibility settings or extensions that modify focus behavior are enabled.

The `focus-issue.css` file contains the problematic code.  The `focus-solution.css` file offers a potential workaround to ensure more consistent styling across various environments.

## Problem

The primary problem is that `:focus-visible` may not reliably trigger the intended styling in all situations. This is primarily due to the fact that `:focus-visible`'s purpose is to avoid styling elements focused via mouse clicks, only styling those focused via keyboard navigation.  However, extensions and accessibility settings can introduce unexpected behavior, leading to inconsistent visual feedback across platforms.

## Solution

The solution attempts to provide a fallback mechanism using the standard `:focus` pseudo-class, ensuring the styling is applied consistently regardless of whether `:focus-visible` is correctly functioning.  However, this might impact the accessibility of the application if the goal is to only style keyboard-focused elements.