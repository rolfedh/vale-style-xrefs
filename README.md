# vale-style-xrefs

This [is a vale style](https://docs.errata.ai/vale/styles) to help technical writers produce good asciidoc cross references.

## Installation

These installation instructions show you how to install this vale style in a Linux environment.

If you're running vale on a different operating system, such as macOS or Windows, adapt these instructions so they work in that operating system.

*Prerequisites*
* [Install vale](https://docs.errata.ai/vale/install)
* Recommended: [Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git/)

*Procedure*

1. Determine your vale styles' path by examining the value of `StylesPath` in `.vale.ini`. For example:
```
$ cat ~/vale-boilerplate/.vale.ini
```
Example output:
```
...
StylesPath = styles
...
```

1. `cd` to your `styles` directory and clone the repo of this style. For example:
```
$ cd ~/vale-boilerplate/styles
$ git clone git@github.com:rolfedh/vale-style-xrefs.git
```

1. Open `.vale.ini` in a text editor. For example:
```
$ nano  ~/vale-boilerplate/.vale.ini
```

1. Add `localization-friendly` to the `BasedOnStyles` attribute. For example:
```
...
BasedOnStyles = write-good,xrefs
```

1. Change `MinAlertLevel` in `.vale.ini` to `suggestion`:
```
MinAlertLevel = suggestion
```

1. Optional: If you are authoring in asciidoc, add `adoc` to the list of file types vale inspects. For example:
```
[*.{md,txt,adoc]
```

1. Save your changes and close `.vale.ini`.

*Verification steps*

1. Verify that you correctly installed and configured the `xrefs` style. Enter:
```
$ vale ~/vale-boilerplate/style/xrefs/verify-installation-example.adoc
```

*Troubleshooting steps*

* TBD
