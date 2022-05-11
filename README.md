# W-11078543 Error - Illegal Constructor
Repro steps:
- Deploy code with LWC
- Attempt to place the LWC on a record page (like Account)
- Notice the error about an illegal Constructor.

Note that the LWC is extending **LightningElement()** with parens on the end.  This is causing the problem.
