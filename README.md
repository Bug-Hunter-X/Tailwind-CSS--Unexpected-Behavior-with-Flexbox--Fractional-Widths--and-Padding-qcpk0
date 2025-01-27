# Tailwind CSS Bug: Unexpected Behavior with Flexbox, Fractional Widths, and Padding

This repository demonstrates an uncommon bug encountered when using Tailwind CSS with flexbox, fractional widths (e.g., `w-1/2`), and padding on the parent container.  The issue leads to unexpected layout behavior, where the child elements don't perfectly fill the available space.

## Bug Description
The `w-1/2` class on flex items doesn't consider the padding added to the parent. The child divs do not split the container evenly. 

## Reproduction Steps
1. Clone this repository.
2. Run the project using any react framework (NextJS, Vite, CRA...).
3. Observe that the two divs inside the flex container are not of equal width.  

## Solution
The solution involves using the `flex-shrink-0` utility class on the child elements to prevent them from shrinking below their minimum size, resolving the uneven width distribution issue.  Additionally, using `box-sizing: border-box` can help manage unexpected layout behavior associated with padding.
