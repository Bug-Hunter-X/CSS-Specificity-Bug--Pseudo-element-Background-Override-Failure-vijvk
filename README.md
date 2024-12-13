# CSS Specificity Bug: Pseudo-element Background Override Failure

This repository demonstrates a subtle CSS specificity issue where the background color of a parent element is unexpectedly not overridden by a pseudo-element with seemingly higher specificity.  The `::before` pseudo-element's background color should override the `.container`'s background, but it doesn't in some cases. This occurs due to the way the browser handles stacking contexts and background painting, especially when absolute positioning is involved.  The solution involves carefully considering the order of styles and ensuring the pseudo-element's background is correctly rendered within its own context. 