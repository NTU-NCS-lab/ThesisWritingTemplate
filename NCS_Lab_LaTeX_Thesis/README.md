<!-- Badge for License -->
<div align="right">

  [![](https://img.shields.io/badge/docs-Wiki-F7D360.svg?logo=&style=flat-square)](https://hsins.me/NTU-Thesis/)
  [![](https://img.shields.io/github/license/Hsins/NTU-Thesis.svg?style=flat-square)](./LICENSE)

</div>

<!-- Logo -->
<p align="center">
  <img src="https://i.imgur.com/x2M158J.png" alt="NTU Thesis" height="150px">
</p>

</div>

<!-- Title and Description -->
<div align="center">

# NTU Thesis

đ _Unofficial LaTeX and Word templates for your master/doctor thesis at National Taiwan University._

![](https://img.shields.io/badge/LaTeX%202%CE%B5-3.14159265-blueviolet?logo=latex&style=flat-square)
![](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey.svg?style=flat-square)
<br>
[![](https://img.shields.io/badge/GitHub%20Actions%20-Open%20as%20Template-2088ff?logo=github-actions&style=flat-square)](https://github.com/NTU-NCS-lab/ThesisWritingTemplate)
[![](https://img.shields.io/badge/Overleaf%20-Open%20as%20Template-46a247?logo=overleaf&style=flat-square)](https://www.overleaf.com/read/cjhmcnpxjbgp)

</div>

## NTU NCS Lab Latex Thesis Template
This is a modification from [this](https://github.com/Hsins/NTU-Thesis-LaTeX-Template) work, the original author is [Hsins](https://github.com/Hsins).

## Structures

```
âââ back
âÂ Â  âââ appendix-*.tex              // éé
âÂ Â  âââ references.bib              // ĺčćçť
âÂ Â  âââ ...
âââ contents
âÂ Â  âââ chapter-*.tex               // čŤćĺ§ĺŽš
âÂ Â  âââ ...
âââ figures
âÂ Â  âââ ...
âââ fonts
âÂ Â  âââ chinese
âÂ Â  âÂ Â  âââ BiauKai.ttf             // ć¨ćĽˇéŤ
âÂ Â  âÂ Â  âââ Arphic-*.ttf            // ćéźĺ­éŤ
âÂ Â  âÂ Â  âââ MOE-*.ttf               // ćč˛é¨ĺ­éŤ
âÂ Â  âÂ Â  âââ WHZ-*.ttf               // çćź˘ĺŽĺ­éŤ
âÂ Â  âÂ Â  âââ cwTeX-*.ttf             // cwTeX ĺ­éŤ
âÂ Â  â   âââ ...
âÂ Â  âââ english
âÂ Â   Â Â  âââ Times New Roman-*.ttf   // Times New Roman ĺ­éŤ
âÂ Â      âââ ...
âââ front
âÂ Â  âââ abstract.tex                // ćčŚ
âÂ Â  âââ acknowledgement.tex         // č´čŹ
âÂ Â  âââ denotation.tex              // çŹŚčĺčĄ¨
âââ main.tex                        // ä¸ťćäťś
âââ ntusetup.tex                    // ć¨Ąćżč¨­ĺŽ
âââ ntuthesis.cls                   // ć¨Ąćżćäťś
âââ ...
```

## Quick start
Please use `xelatex` to compile this project.

### Overleaf
The easiest method is to edit on Overleaf, please follow this [link](https://www.overleaf.com/read/cjhmcnpxjbgp) and make a copy from it.

### Build at local
Please follow the [instructions](https://github.com/NTU-NCS-lab/ThesisWritingTemplate#quick-start) to setup the environments.

#### Method 1
Please run `biber main` to generate `main.bbl` first and then run `xelatex main` to generate pdf file.

#### Method 2
1. Open your VScode, press `ctrl+shift+P`.
2. Type `settings`, and select `Open User Settings`.
3. Go to the last json object, add a comma to the last object, and add following lines:
    ```json=
    "latex-workshop.latex.recipes": [
      {
        "name": "xelatex+biber",
        "tools": [
          "xelatex",
          "biber",
          "xelatex"
        ]
      },
      {
        "name": "xelatex",
        "tools": [
          "xelatex"
        ]
      },
      {
        "name": "pdflatex+biber",
        "tools": [
          "pdflatex",
          "biber",
          "pdflatex"
        ]
      },
      {
        "name": "pdflatex",
        "tools": [
          "pdflatex"
        ]
      },
      {
        "name": "biber only",
        "tools": [
          "biber"
        ]
      }
    ],
    "latex-workshop.latex.tools": [
      {
        "name": "biber",
        "command": "biber",
        "args": [
          "%DOCFILE%"
        ]
      },
      {
        "name": "pdflatex",
        "command": "pdflatex",
        "args": [
          "-synctex=1",
          "-interaction=nonstopmode",
          "-file-line-error",
          "%DOC%"
        ],
        "env": {}
      },
      {
        "name": "bibtex",
        "command": "bibtex",
        "args": [
          "%DOCFILE%"
        ],
        "env": {}
      },
      {
        "name": "xelatex",
        "command": "xelatex",
        "args": [
          "%DOC%"
        ],
        "env": {}
      },
    ],
    ```
4. This will add commands to your Latex button, and then you should be able to compile the project by clicking `build` button. You can aslo find the buttons at ` TEX(extension column) > commands > Build LaTex project`

## License

Licensed under the MIT License, Copyright ÂŠ 2017-present Hsins.
