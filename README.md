# snippet-org-mode

This is a library of yasnippet snippets for Org-mode. 
Install the library where you store your user-generated snippets for the yasnippet package. 
This is usually in `~/.emacs.d/snippets/org-mode`. 
Use the `File/Save copy in Drive` pulldown menu item option. 

The snippets are grouped via their filename.
The snippet tab trigger is often not the same as the filename.


## latex-env-* snippets

The snippets with the `latex-env' prefix are snippets for creating LaTeX environments inside of Org. 
Org will send these to the LaTeX compiler upon export to PDF.

The `mintin*` snippets are preset with the corresponding language parameter for the `\mintinline{}{}` command. 
This command is not an environment, but I included this group of snippets to save space in the yasnippet pulldown menu. 
Obviously, the pygments Python package has to be installed on your system to use these.

### latex-env-code-* snippets

The `latex-envcode*` snippets are a series of alternate configurations for the custom-mode code env, which encloses code in the minted env. 
The code env enables adding a caption to the minted code block.  
It also adds an index key and label. 
You have to define the code env by adding `\newenvironment{code}{\captionsetup{type=listing}}{}` to the preamble of your LaTeX file. 
The numbers in the snippet name correpsond to alternate configurations of the minted environment.

### latex-env-eqcaptioned gives equations with captions

The `eqcaptioned` snippet encloses an equation in a `eqc` environment to enable the addition of a caption.
The eqc environment is a float whereas an equation is not.
Only floats can have captions.
The snippet also adds an index key and a label.

## org-* snippets

These snippets are written in org markdown.

### org-codeblock-* snippets

These snippets provide templates for org-mode code blocks.
This header parameters required to obtain in-line output can vary with programming language.
Configuring the header can be time-consuming becuase the information can take time to dig up and to test.
For example, it took me two hours to figure out how to get Emacs lisp to send output to the `:RESULTs:` drawer. 


### org-property-* snippets

These snippets are property block snippets.
For example, the `org-property-category` snippet is useful for labeling sections so that they show up in customized agenda views.
I use these to label the TODO items of a specific project. 
A customized agenda view can then include these TODO items.

The `org-property-habit` snippet is useful for repeating TODO items.

## protocol-* snippets

These snippets print out the steps for doing multi-step tasks.

## pymolpy-* snippets

See this [repo](https://github.com/MooersLab/orgpymolpysnips) for PyMOL snippets written in Python for use in org-mode.
These snippets are also stored in `~/.emacs.d/snippets/org-mode` so that they are accessible for literate programmming with PyMOL in org documents.
