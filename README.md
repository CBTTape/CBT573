# CBT573
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 573 is from Shane Ginnane, and contains an IEFUJV exit    *   FILE 573
//*           which allows for substitution of system symbols into  *   FILE 573
//*           execution JCL.  There's a bit more, too.              *   FILE 573
//*                                                                 *   FILE 573
//*           email:  Shane.Ginnane@qr.com.au                       *   FILE 573
//*                                                                 *   FILE 573
//*       - - - - - - - - - - - - - - - - - - - - - - - - - - -     *   FILE 573
//*                                                                 *   FILE 573
//*        IEFUJV    SMF JOB VALIDATION - ALLOW JCL VARIABLES       *   FILE 573
//*                                                                 *   FILE 573
//*        MODULE NAME = IEFUJV                                     *   FILE 573
//*                                                                 *   FILE 573
//*        FUNCTION =                                               *   FILE 573
//*                                                                 *   FILE 573
//*           Provide access to system symbols in JCL               *   FILE 573
//*           use a "// SET " statement to assign system symbols    *   FILE 573
//*           to variables local to the job;                        *   FILE 573
//*                                                                 *   FILE 573
//*           e.g. "// SET LPAR=&SYSNAME  " resolves to             *   FILE 573
//*                "// SET LPAR=PROD      "                         *   FILE 573
//*                                                                 *   FILE 573
//*           This may then be used in a DSNAME, such as ...        *   FILE 573
//*                                                                 *   FILE 573
//*           //DD1   DD  DSN=SYS1.&LPAR..MYLIB                     *   FILE 573
//*                                                                 *   FILE 573
//*         Warning:  Symbols are resolved at pre-conversion.       *   FILE 573
//*                                                                 *   FILE 573
//*            This is particularly relevant for date and time      *   FILE 573
//*            where a job is placed on hold or crosses a day       *   FILE 573
//*            boundary.                                            *   FILE 573
//*                                                                 *   FILE 573
//*            Likewise there are JES, MAS, and NJE issues.         *   FILE 573
//*                                                                 *   FILE 573
//*            Caveat emptor....                                    *   FILE 573
//*                                                                 *   FILE 573
//*         Notes =                                                 *   FILE 573
//*                                                                 *   FILE 573
//*            Trailing period on symbol may or may not be          *   FILE 573
//*            included - has no effect on functionality.           *   FILE 573
//*                                                                 *   FILE 573
//*            Multiple symbols per card image is supported.        *   FILE 573
//*                                                                 *   FILE 573
//*            Continuation of "SET" card image is *not*            *   FILE 573
//*            supported.  (Use multiple "SET" cards.)              *   FILE 573
//*                                                                 *   FILE 573
//*            Be aware of symbol substitution extending the        *   FILE 573
//*            card beyond column 72 - this will be returned,       *   FILE 573
//*            and will generally cause a JCL error.                *   FILE 573
//*                                                                 *   FILE 573
//*            Exit will clear the input area to accommodate the    *   FILE 573
//*            situation where the resolved text is shorter.        *   FILE 573
//*                                                                 *   FILE 573
//*            Exit will copy an extra byte from the target to      *   FILE 573
//*            ensure a blank at end.  This handles the scenario    *   FILE 573
//*            where the resolved is longer, and comments           *   FILE 573
//*            follow.                                              *   FILE 573
//*                                                                 *   FILE 573
```
