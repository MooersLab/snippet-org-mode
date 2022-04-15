# snippet-org-mode

This is a library of yasnippet snippets for Org-mode.
It is designed to be used in Emacs.
Org-mode is a feature rich markup language that supports easy polyglot literate programming and that can incorporate blocks written in LaTeX.
This latter feature vastly extends the universe of possible typesetting compared to various markdown variants.
The long-term goal of this snippet library is to facilitate literate programming in Org-mode.

Install the library where you store your user-generated snippets for the yasnippet package. 
This is usually in `~/.emacs.d/snippets/org-mode`. 
Use the `File/Save copy in Drive` pulldown menu item option. 

The snippet tab trigger (or key in yasnippet parlance) is often not the same as the filename.
I mapped `C-o` to the function `yas-expand` to insert the snippet after entering the key.
Add the following line to your Emacs initialization file.

```elisp
(global-set-key "\C-o" 'yas-expand)
```

For my yasnippet configuration see the yasnippet section of my Emacs [config file](https://github.com/MooersLab/configorg/blob/main/config.org).

These snippets can be used in conjunciton with those in the *yasnippets-snippets* package, which you can install via MELPA even though they are stored in the elpa subfolder.
Both sets of snippets will appear in the table that is displayed in a separeate buffer when you enter `M-x yas-describe-tables`.
There is a separate table for each active mode and separate subtables for each group.

Below, the snippets are grouped via their filename.
Some prominant groups and subgroups are explained below.

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

## newsnip

This is a replacement template snippet for writing new snippets.
The template invoked in the yasnippet pulldown menu is not a complete and thereby not as useful to me.

## org-* snippets

These snippets are written in org markdown.

### org-codeblock-* snippets

These snippets provide templates for org-mode code blocks.
This header parameters required to obtain in-line output can vary with programming language.
Configuring the header can be time-consuming becuase the information can take time to dig up and to test.
For example, it took me two hours to figure out how to get Emacs lisp to send output to the `:RESULTS:` drawer. 


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
