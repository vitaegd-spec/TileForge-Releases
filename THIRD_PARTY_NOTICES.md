# TileForge Third-Party Notices

This file identifies third-party software used by the current TileForge 1.12 source/build configuration and summarizes the relevant licence notices that must travel with a commercial distribution.

**Important build note:** the current `requirements.txt` uses minimum-version constraints rather than exact pins (`PySide6>=6.8`, `Pillow>=10.0`, `numpy>=1.26`, `scipy>=1.14`). Therefore this document records the dependency families known from the current TileForge source, but it cannot truthfully identify the exact wheel/runtime versions that will be embedded in the final `TileForge.exe` until the release environment is frozen. Before shipping, record the output of `python -m pip freeze` from the exact environment used for the PyInstaller build and verify the licences shipped inside those exact wheels.

TileForge's proprietary `LICENSE.md` applies only to TileForge-owned code and assets. The third-party components below remain governed by their own licences.

---

## 1. Python

**Component:** Python runtime (when bundled in a PyInstaller distribution)  
**Project:** Python  
**Licence:** Python Software Foundation License Version 2, plus the historical Python licence stack and licences for incorporated software included in the Python distribution  
**Copyright / rights holders:** Python Software Foundation and earlier Python contributors/rightsholders as described in the official Python licence documentation.

Python may be bundled with a non-open-source application. If Python is redistributed with TileForge, retain the applicable Python copyright notices and include the PSF licence and other licences in Python's licence stack applicable to the redistributed Python version.

Official licence: https://docs.python.org/3/license.html

---

## 2. Qt for Python / PySide6

**Component:** PySide6 / Qt for Python  
**Current TileForge requirement:** `PySide6>=6.8`  
**Licensing model:** Qt for Python follows the Qt licensing model. The Community Edition is available under LGPLv3/GPLv3 licensing, while a separate Commercial Edition is available from The Qt Company.

TileForge does not relicense PySide6 or Qt. Their applicable licence terms remain in force.

### If distributing the Community/LGPL build

A closed-source TileForge distribution must preserve all rights users receive under the applicable LGPL and other Qt/PySide licences. The release package must include the licence texts/notices required by the exact PySide6/Qt components that are shipped and satisfy the requirements applicable to the way those libraries are packaged and linked.

In particular, do not apply TileForge's anti-reverse-engineering restriction to the extent doing so would take away a user's non-waivable rights to debug modifications to an LGPL-covered library. Do not prevent lawful replacement/relinking of LGPL-covered components where the licence requires that capability.

Qt for Python also contains or may include third-party code under additional licences. The official Qt for Python licence page specifically recommends that applications acknowledge the third-party components actually used and reproduce their required licence statements. The exact set must be taken from the exact PySide6/Qt build shipped with TileForge.

**Official licensing information:**  
https://doc.qt.io/qtforpython-6/commercial/index.html  
https://doc.qt.io/qtforpython-6/licenses.html

### Commercial Qt alternative

If TileForge is built and distributed using a commercial Qt for Python package obtained under an applicable Qt commercial licence, follow the commercial agreement and notices applicable to that distribution instead of assuming the Community Edition terms.

---

## 3. Shiboken6

**Component:** shiboken6  
**Relationship:** Runtime helper installed as part of the Qt for Python / PySide6 stack  
**PyPI licence expression:** LGPL-3.0-only OR GPL-2.0-only OR GPL-3.0-only for the community package.

The exact shiboken6 version is normally coupled to the chosen PySide6 release. Include the corresponding licence notice/text from the exact shipped package and comply with the selected licence terms.

Project information: https://pypi.org/project/shiboken6/

---

## 4. Pillow

**Component:** Pillow (Python Imaging Library fork)  
**Current TileForge requirement:** `Pillow>=10.0`  
**Licence:** MIT-CMU

Copyright (c) 1997-2011 by Secret Labs AB  
Copyright (c) 1995-2011 by Fredrik Lundh and contributors  
Pillow is Copyright (c) 2010 by Jeffrey 'Alex' Clark and contributors.

Permission to use, copy, modify and distribute Pillow and its documentation for any purpose and without fee is granted provided the required copyright and permission notices are retained. The name of Secret Labs AB or the author may not be used in advertising or publicity pertaining to distribution without specific prior written permission. Pillow is provided without warranty as described in its licence.

**Action for the release package:** include Pillow's complete `LICENSE` file from the exact Pillow wheel/source distribution shipped with TileForge.

Official licence source: https://github.com/python-pillow/Pillow/blob/main/LICENSE

---

## 5. NumPy

**Component:** NumPy  
**Current TileForge requirement:** `numpy>=1.26`  
**Licence:** BSD 3-Clause

Copyright (c) 2005-2025, NumPy Developers. All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted subject to the BSD 3-Clause conditions. Binary redistribution must reproduce the copyright notice, conditions and disclaimer in the documentation and/or other materials provided with the distribution, and contributor names may not be used to endorse derived products without specific prior written permission.

NumPy wheels can include compiled third-party runtime libraries that have their own licences. The exact bundled libraries depend on the NumPy version/platform. Current NumPy documentation notes examples such as OpenBLAS and the GNU Fortran runtime in published binary wheels. TileForge's final notice bundle must therefore include the licence files installed with the **exact Windows NumPy wheel used for the release build**, not only NumPy's top-level BSD licence.

**Action for the release package:** preserve NumPy's `LICENSE.txt` and the licence files for vendored/bundled components from the exact installed wheel.

Official licence: https://numpy.org/doc/stable/license.html

---

## 6. SciPy

**Component:** SciPy  
**Current TileForge requirement:** `scipy>=1.14`  
**TileForge usage:** Optional enhanced black-background removal when slicing sheets  
**Licence:** BSD 3-Clause

Copyright (c) 2001-2002 Enthought, Inc.  
Copyright (c) 2003, SciPy Developers. All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted subject to the BSD 3-Clause conditions. Binary redistribution must reproduce the copyright notice, conditions and disclaimer in the documentation and/or other materials provided with the distribution. The names of the copyright holders/contributors may not be used to endorse or promote derived products without written permission.

SciPy's binary wheels may also include compiled libraries with their own notices. Preserve all licence files installed with the exact SciPy wheel used for the TileForge release.

Official licence: https://scipy.org/ and https://github.com/scipy/scipy/blob/main/LICENSE.txt

---

## 7. PyInstaller (build tool; not required to be credited in the generated app)

**Component:** PyInstaller  
**TileForge usage:** Builds the Windows `TileForge.exe` distribution using `--windowed --name TileForge --icon assets\\tileforge.ico`  
**Licence:** GPL 2.0 with a special exception for building and distributing commercial applications; certain PyInstaller files are Apache License 2.0.

PyInstaller's official licence documentation states that PyInstaller may be used to bundle commercial applications and that generated executable bundles may be shipped under the application's chosen licence, subject to the licences of the application's dependencies. It also states that a generated application does **not** need to include the PyInstaller licence or a PyInstaller acknowledgement merely because PyInstaller was used to build it.

Accordingly, this notice is retained for TileForge's internal release record. PyInstaller itself does not need to be credited in the customer-facing executable distribution unless the release actually redistributes PyInstaller source/files outside the normal generated bundle or other circumstances require it.

Official licence: https://pyinstaller.org/en/stable/license.html

---