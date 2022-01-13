# snippet-org-mode

This is a library of yasnippet snippets for Org-mode. Install the library where you store your user-generated snippets for the yasnippet package. This is usually in `~/.emacs.d/snippets/org-mode`. Use the `File/Save copy in Drive` pulldown menu item. 

## latex-env- snippets

The snippets with the `latex-env' prefix are snippets for creating LaTeX environments inside of Org. Org will send these to the LaTeX compiler upon export to PDF.

The `mintin*` snippets are preset with the corresponding language parameter for the `\mintinline{}{}` command. This is not an environment, but I included this group of snippets to save space in the yasnippet pulldown menu. Obviously, the pygments Python package has to be installed on your system to use these.

The `code*' snippets are a series of alternate configurations for the custom-mode code env, which encloses code in the minted env. The code env enables adding a caption to the minted code block.  It also adds an index key and label. You have to define the code env by adding `\newenvironment{code}{\captionsetup{type=listing}}{}` to the preamble of your LaTeX file. The `eqcaptioned` snippet encloses an equation and adds a caption as wells as index key and label.

## pymolpy- snippets

See this [repo](https://github.com/MooersLab/orgpymolpysnips) for PyMOL snippets written in Python for use in org-mode.
These snippets are also stored in `~/.emacs.d/snippets/org-mode`.
