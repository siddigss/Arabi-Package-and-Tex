In this page, we will explain how to get Arabi working with MiKTeX in Windows (to be generalied later).

### Preperations
* We suspect that Arabi does not work with the compiler XeLateX. Change your compiler to PDFLaTeX.
* Insall Babel.
* Download `ae_almohanad_bold.pfb` from this [link](https://ctan.org/tex-archive/language/arabic/arabi/arabi/texmf/fonts/type1/arabi/arabeyes?lang=en).
* Open MiKTeX Console (Admin may be needed) in your device and go to settings then press the tab Directories. In the list of pathes you will see a path with purpose `install`.
Go to this directory in you computer. Once in the directory go to `fonts` then `type1`. Create a folder and name it `arabeyes` and in this folder put the file 
`ae_almohanad_bold.pfb` which you downloaded in the previous step.
* In MiKTeX Console click Task in the upper bar and click `Refresh file name database`. After doing this click on Task again and choose `Refresh font map files`.
* Now we are ready to type and compile.

### Example
Try to compile this simple 
```
\documentclass{article}
\usepackage[LAE]{fontenc}
\usepackage[arabic,english]{babel}


\begin{document}
	\selectlanguage{arabic}
بسم الله الرحمن الرحيم
\end{document}
```
Now you may want to try writing Englsih with Arabic. You have to use the `\textLR{ }` and put the English part between the parentheses.


### Fonts
Certainly one will very soon be tempted to try other fonts, Arabic fonts are beautiful after all.
Arabi Package allows for the usage of several fonts, but seemingly all of them are of the format PostScript type 1 fonts. In page 50 of the user manual [1] you can
find fonts are supported by Arabi package and the commands to use them. Just like we did in the pereparation section above you have to download the fonts from
[here](https://ctan.org/tex-archive/language/arabic/arabi/arabi/texmf/fonts/type1/arabi/arabeyes?lang=en) first and then use the corresponding command.
An example is `\textnice{السلام عليكم}`.


## Templates to learn from.
Nothing yet, but soon Insha'allah.

## Notes
* You may encounter the warning `Font shape `LAE/lmr/m/n' undefined(Font) using `LAE/cmr/m/n' instead`. It seems innocuous. No need to worry.

## TO DO
* Generalize this guide to other LaTeX distributions and other operating systems.

## References
[1] [Arabi package user guide](https://ctan.mirrors.hoobly.com/language/arabic/arabi/arabi/texmf/doc/latex/arabi/user_guide.pdf)
