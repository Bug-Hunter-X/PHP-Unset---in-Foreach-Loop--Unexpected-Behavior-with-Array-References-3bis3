# PHP Unset() in Foreach Loop Bug

This repository demonstrates an uncommon bug in PHP related to the use of `unset()` within a `foreach` loop iterating over an array's references. The problem arises from the way `foreach` handles references, causing unexpected behavior when elements are removed during iteration.

## Bug Description
The primary issue is that removing elements using `unset()` inside a `foreach` loop, while simultaneously using references (`&`), disrupts the iteration process. The loop might skip elements or produce incorrect results.

## Reproduction
Clone the repository and run `bug.php`. The output will demonstrate the unexpected behavior. The solution (`bugSolution.php`) provides a corrected version of the code.

## Solution
The solution avoids the problematic `unset()` operation during the loop and handles removal separately using `array_filter()` or by creating a new array.