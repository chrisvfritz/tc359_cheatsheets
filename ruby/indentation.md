# Indentation

The standard indentation for Ruby (`.rb`) files is with two-space soft-tabs (as opposed to hard-tabs). If most of your programming is web development, I recommend making this the standard for every file you work in, as it's convention not only in [Ruby](https://github.com/styleguide/ruby), but also [HTML](https://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml#Indentation), [CSS](https://github.com/styleguide/css), and [JavaScript](http://seravo.fi/2013/javascript-the-winning-style).

You may sometimes work in Python though - or another language with different tab conventions. So below are instructions for updating a variety of text editors to use two-space soft-tabs, either globally or just for specific file types.

## Sublime Text 3

### Global

Edit your `Preferences: Settings - User` with:

``` json
{
  "tab_size": 2,
  "translate_tabs_to_spaces": true
}
```

I also recommend the following setting, so that you can better see when spaces and tabs mixed up together:

``` json
{
  "draw_white_space": "all"
}
```

### File-specific

[EditorConfig](http://stackoverflow.com/questions/9474090/how-do-i-force-sublime-text-2-to-indent-two-spaces-per-tab#answer-24619474) is a plugin you can use to set project-specific and file-specific indentation settings.

## Vim

Vim has a built-in way of controlling the type of indentation you use for every kind of file. [Documentation here](http://vim.wikia.com/wiki/Indenting_source_code#Different_settings_for_different_file_types) explains how.