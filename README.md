# Overview
ink is a texthandling library that takes care of all font & text related needs for modern applications.
It is supposed to provide a standardised interface for all major plattforms with an additional focus on i18n.
ink is part of a larger application development framework called [alloy](https://github.com/Folling/alloy).

This document is a WIP and will be expanded upon as the project progresses.

This library has existed in multiple forms before. Two C++ versions and one previous rust version. 
You can find these projects (in ascending order of the creation date):
- [Original C++ version](https://memleak.eu/Folling/graphite)
- [Original Rust version](https://memleak.eu/Folling/graphite-rs)
- [Second C++ iteration](https://memleak.eu/Folling/graphite-CPP-v2)

# Features
- [ ] Font loading
- [ ] CTL
- [ ] Text shaping (via [harfbuzz]())
- [ ] Property based font selection (bold, monospace, etc.)
- [ ] Linebreaking calculations
- [ ] Text segmentation identification
- [ ] Unicode normalisation
- [ ] UTF8, UTF16, and UTF32 & conversion between them
- [ ] Bidi support
- [ ] Vertical text layout
- [ ] Subpixel rendering support
- [ ] (M)SDF rendering support

---

# Used Libraries
alloy is a lot of work as it is, so some corners had to be cut in order to make the workload feasible.
hence ink uses a variety of C libraries to easen the burden:
- [FontConfig](https://www.freedesktop.org/wiki/Software/fontconfig/) for font discovery on linux
- [FreeType](https://freetype.org/) for font loading, font property analsys and (subpixel) rendering of bitmaps
- [HarfBuzz](https://harfbuzz.github.io/) for text shaping
- [WinAPI](https://docs.microsoft.com/en-us/windows/win32/apiindex/windows-api-list) for font discovery on windows
- [Cocoa](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/CocoaFundamentals/WhatIsCocoa/WhatIsCocoa.html) for font discovery on MacOS

Note that FontConfig is not used for font selection as it was deemed inadequate for that usage.

# Contributing
alloy is open source and is supposed to benefit from the inclusion of other people. 
However I do reserve the rights to deny any feature requests or pull requests but am always open to discussion and having my mind changed. 
If you're uncertain whether or not a certain pull request would be appreciated and don't want to waste effort without knowing whether it's worth it, feel free to open an issue and ask. 
All code should be formatted using the same guideline. For this please use rustfmt. In the future a customised rustfmt stylisation might be used.
File and directory names are are to be formatted using snake_case. Excluded from this rule are files that have a certain convention such as .gitignore, LICENCE.txt and markdown files.

# Support
I have a fulltime job and can only afford so much time for alloy (the root project of graphite). If you would like to change that in the future consider donating to the project (note: Donating link will follow, graphite isn't worth donating yet). I also appreciate feedback (next to constructive criticism) so feel free to email me at coding@folling.de. 
