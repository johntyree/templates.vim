This fork is just to get around the problem of the original repo being packaged as a vim archive that gets exploded on first run and ruins Vundle. I have done nothing here but unpacked the plugin and stuck a few useful default templates in. Ping me if it's out of date, but the script hasn't been updated since 2005...

This is a mirror of http://www.vim.org/scripts/script.php?script_id=1172

templates.vim lets you use filetype-dependent templates for new files, using a simple but effective mechanism.

It is, in various ways, a more sophisticated approach to the same problem that vimscript #1160 addresses, but doesn't try to do quite as much.

Usage is simple: when you start with a fresh buffer, setting a filetype on it will load the corresponding template. To test it, open Vim and issue

    :set ft=html

One new command has been added for convenience: it is called :New and takes exactly one argument. It will open a new empty window and set the filetype for it to the argument given.

Templates are kept in .vim/templates. The template filename must be equal to the filetype. So when you set the filetype of an empty buffer to html, .vim/templates/html will be loaded. It's that simple.

In the templates, you can use a cursorline to specify a position for the cursor after loading the template. Such a cursorline works much like a modeline: the word cursor: must appear, followed by one or two numbers and opionally the word del, all separated by whitespace. The first number specifies the line the cursor will be placed in. The second, if present, specifies a column. The optional word del directs the script to remove the cursorline at load time. Take a look at the templates supplied in the package, it should be fairly self-explanatory.
