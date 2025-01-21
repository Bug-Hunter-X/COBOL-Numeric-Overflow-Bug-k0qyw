# COBOL Numeric Overflow Bug

This repository demonstrates a common, yet easily overlooked, bug in COBOL programs involving numeric overflow. When adding two numbers, if the receiving field is not large enough to accommodate the sum, the result will silently overflow, leading to incorrect calculations. 

The `bug.cob` file contains the problematic code, while `bugSolution.cob` shows the corrected version.

**Bug:**
The `ADD` statement lacks proper size handling, and an overflow occurs silently when the sum of WS-DATA-1 and WS-DATA-2 exceeds the capacity of WS-SUM. 

**Solution:**
The solution involves using larger fields to ensure that they can store the potential maximum value of the sum.