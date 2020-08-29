# FileMarks

This script will store a link inside a file which, upon execution, will open the link in your $BROWSER.\
It makes handling bookmarks as easy as handling any other files.\
Uses dmenu and notify-send.

## How to use

Call the script with an URL as the first argument. You will be asked to type a name and navigate to destination folder.\
Default location is `~/Bookmarks`. You can type an absolute path as well.\
Remember that not all characters are supported in file names (e.g. slashes).

## Binding to keys
- Qutebrowser

	Add following lines to `~/.config/qutebrowser/config.py`
	```
	# bind filemarks to ctrl-shift-b
	config.bind('<Ctrl-Shift-b>', 'spawn filemarks {url}')
	```

- Vimb

	Add following lines to `$XDG_CONFIG_HOME/vimb/config`
	```
	" bind filemarks to ctrl-b
	:nmap <C-B> :shellcmd filemarks "$VIMB_URI"<CR>
	```

- surf

	*todo*



## Possible future improvements

Use page name as default name.\
Add option to create directories?\
Open and store multiple URL's with one file (collection)?
