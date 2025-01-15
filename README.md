# Shell Script Bug: Whitespace Trimming

This repository demonstrates a common but subtle bug in shell scripting related to whitespace trimming.  The script attempts to remove leading and trailing whitespace from each line of a file, but it doesn't handle the situation correctly due to the use of `xargs`.  The solution provides a more robust approach to trimming whitespace.

## Bug Description
The original script uses `xargs` to trim whitespace from each line. While this might seem simple, it can cause issues with lines containing multiple spaces and tabs.  `xargs` often interprets multiple spaces as a single space, and it might handle tabs unpredictably.  This leads to incorrect or unexpected output.

## Solution
The solution uses parameter expansion to accurately remove leading and trailing whitespace. This approach is more robust and handles multiple spaces, tabs, and various whitespace combinations effectively.
