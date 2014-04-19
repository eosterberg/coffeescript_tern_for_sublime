# Tern for Sublime Text

This is a tweak of the sublime plugin ['tern_for_sublime'][tern], adding code-completion for CoffeeScript.

[tern]: https://github.com/marijnh/tern_for_sublime

It is based on [this][othree] fork of the official Tern.js library. I just upgraded it to the latest version of CoffeeScript (1.7.1).

[othree]: https://github.com/othree/tern


## Installation

Check out the code in this repository into a subdirectory of your
Sublime Text's `Packages` directory.

    cd /path/to/sublime-text-N/Packages
    git clone https://github.com/eosterberg/coffeescript_tern_for_sublime.git

The dependencies are included in this repo.

This plugin is just a ugly hack and wont work together with the original plugin. If you want to enjoy Tern for JavaScript, you can use [sublime-tern][ternjs], which is another Tern plugin for Sublime. It works really well.

[ternjs]: https://github.com/emmetio/sublime-tern


## Configuration

Tern uses `.tern-project` files to configure loading libraries and
plugins for a project. See the [Tern docs][docs] for details.

[docs]: http://ternjs.net/doc/manual.html#configuration

To get this plugin to work, add all your JAVASCRIPT files to the "loadEagerly" list in your .tern-project

    "loadEagerly": [
        "*.js"
    ]

This is a bit limited and wont work as well as the original plugin, but its still useful.

### Automatically Showing Completions

Add `{"selector": "source.coffee", "characters": "."}` to your `auto_complete_triggers` preference array to automatically show completions after a dot is typed following an object name.

Example:
```javascript
"auto_complete_triggers": [ {"selector": "text.html", "characters": "<"}, {"selector": "source.coffee", "characters": "."} ]
```

Ensure that your `auto_complete` preference is set to `true`. It's enabled by default.

Enjoy!