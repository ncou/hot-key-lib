# hot-key-lib
javascript hot key(shortcut key) library on web

## How to use

### 1. Create a HotKey Object
<pre>
var hotKey = new HotKey();
</pre>


### 2. Add HotKey
<pre>
hotKey.add("CTRL+A", function(e) {
  // do something when CTRL+A keydown
});
</pre>


### 3. Setup (if you want)
<pre>
hotKey.setup({
  "preventDefault": true
});
</pre>

* preventDefault: if true, prevent default behavior from browser (default: false)


### 4. Start HotKey
<pre>
hotKey.start();
</pre>


## Key Name Rule

### Default Rule

[CTRL+][SHIFT+][ALT+][META+]KEY

#### Example
<pre>
CTRL+A (A+CTRL is not available)
CTRL+SHIFT+A (SHIFT+CTRL+A is not available)
META+A (META is a Command key on Mac)
</pre>

#### Use `META` for Command Key on Mac
<pre>
META+C means Command+C on Mac
</pre>

### Reserved KEY
<pre>
Arrows => LEFT-ARROW, UP-ARROW, RIGHT-ARROW, DOWN-ARROW
Tab => TAB
Space Bar => SPACE
Back Space => DELETE
</pre>

#### Example
<pre>
CTRL+LEFT-ARROW
CTRL+RIGHT-ARROW
CTRL+UP-ARROW
</pre>
