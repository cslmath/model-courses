# Notes for Template_201-SN1

`Template_201-SN1/README.md`

This is currently a subdirectory of the `templates` directory in `model201-SN1`.

Files saved here will eventually be moved into `CPL/Course-Templates/model201-SN1/` keeping the same directory structure.  
A softlink named `Template_201-SN1` pointing at `Course-Templates/model201-SN1/` will replace this subdirectory.
This way no renaming of paths should be needed in any saved set definitions
when we transition from edited files save here to edited files saved in `CPL/Course-Templates/model201-SN1/`.

To this end it will save work to use the directory structure detailed in [CPL issue #41](https://github.com/cslmath/Champlain-Saint-Lambert-webwork-repo/issues/41).

```bash
model201-901/ or Template_201-901/
│   set01.def
│   set02.def
│   setLab01.def
│   setLab02.def
│ ...
├───library-bugs
│   └───Library
│       ├───school3
│       │       fixed1.pg
│       │       ...
│       └───school4
│               fixed1.pg
                ...
├───library-edits
│   └───Library
│       ├───school1
│       │       changed1.pg
│       │       changed2.pg
│       │       ...
│       └───school2
│               changed1.pg
│               changed2.pg
│               ...
└───MHAuthor
    ├───Labs
    │       MHLab01q01.pg
    │       MHLab01q02.pg
    │       setHeaderPaperLab.pg
    │       setHeaderScreenLab.pg
    │       ...
    └───Statistics
        └───Chapter1
            ├───Section1
            │       MH21problem.pg
            │       MH21problem2.pg
            │       ...
            └───Section2
                    MH21problem3.pg
                    MH21problem4.pg
                    ...
```
