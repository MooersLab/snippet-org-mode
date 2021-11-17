# snippet-org-mode

A library of yasnippet snippets for org-mode. Install where you store your user generated snippets for the yasnippet package. This is usually in `~/.emacs.d/snippets/org-mode`.

## latex-env-

The snippets with the `latex-env` prefix are snippets for creating LaTeX environments insdie of org.
Org will send these to the LaTeX compiler upon export to PDF.

The `mintin*` snippets are preset with the corresponding language parameter for the `\mintinline{}{}` command.
This is not an environment, but I included this group of snippets to save space in the yasnippet pulldown menu.
Obviously, the pygments Python package has to be installed on your system to use these.

The `code*` snippets are a series alternate configurations for the custom-mode code env which encloses code in the minted env.
The code env enables adding a caption to the minted code block. 
It also adda an index key and label.
You have to define the code env by adding `\newenvironment{code}{\captionsetup{type=listing}}{}` to the preamble of your LaTeX file.

The `eqcaptioned` snippet encloses an equation and adds a caption as wells as index key and label.
