# W-11078543 Error - Illegal Constructor
Repro steps:
- Deploy code with LWC, with LWS disabled
- Place the LWC on a record page (like Account)
- Create a Record (Account) and view it
- Notice that the LWC renders fine on the record page, where it was placed
- Enable LWS in Setup -> Session Settings
- Logout
- Login
- Load the same record (Account)
- Observe that the entire record page fails to load, and you get a message saying "Looks like there is a problem"
- If you break on errors, you will see the illegal constructor error, but nothing is logged in the console

Note that the LWC is extending **LightningElement()** with parens on the end.  This is causing the problem.
