# Tcl Procedure Bug: Incorrect Variable Substitution

This repository demonstrates a subtle bug in a Tcl procedure related to variable substitution.  The procedure `badproc` is designed to compare two arguments and return 1 if they're equal, 0 otherwise. However, due to the way the comparison is written, it always returns 0.

The `bug.tcl` file contains the buggy code. The `bugSolution.tcl` file provides a corrected version.

## Bug Description

The original code uses double quotes around the variable names (`"$a"` and `"$b"`). This prevents variable substitution, so the comparison is always comparing the literal strings "$a" and "$b", resulting in an incorrect result.

## Bug Solution

The solution is to remove the double quotes around the variable names so that variable substitution is performed correctly.