---
layout: post
title:  "Listen to Pandora with Emacs"
date:   2014-06-03 17:04:35
categories: emacs
---

It is almost no surprise that you can listen to music with Emacs! You can listen
to [Pandora](http://pandora.com) and

- change the station
- love/ban the playing song
- skip the current song

without leaving the comfort of your favorite editor.

It is awesome and very convenient to use Emacs for many things
(e.g. [Dired](http://www.emacswiki.org/emacs/DiredMode) as file browser,
[shell](http://www.gnu.org/software/emacs/manual/html_node/emacs/Shell.html) to
run commands interactively, [magit](https://github.com/magit/magit) as git
interface). Although I don't think that listening to music with Emacs will make
me more effective, I started using it, because it is fun!

## Setting it up

The Emacs package that provides interface to Pandora is called
[Pianobar mode](http://www.emacswiki.org/emacs/PianobarMode) which actually uses
the command-line Pandora client [pianobar](http://6xq.net/projects/pianobar/).

First you need to install pianobar. It can be available to install via your
package manager. Otherwise, download pianobar
[here](http://6xq.net/projects/pianobar/). If you use Ubuntu, you can install it
using apt-get.

{% highlight sh %}
$ sudo apt-get install pianobar
{% endhighlight %}

The next step is to install `pianobar-mode`. The easiest way is to [install using
the package manager](http://ergoemacs.org/emacs/emacs_package_system.html).

```
M-x package-install <RET> pianobar-mode <RET>
```

If your Emacs is older than version 24, download `pianobar.el`
[here](http://www.emacswiki.org/emacs/pianobar.el).

Finally, autoload the package by adding the following to your init file.

{% highlight lisp %}
(autoload 'pianobar "pianobar" nil t)
{% endhighlight %}

And you are ready to listen to some music!

```
M-x pianobar
```

## Some optional configuration

You can set your username/password and define key bindings for some pianobar
functions.

{% gist sefakilic/3731a4112828793706fe %}


