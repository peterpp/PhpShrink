# PhpShrink
Remove spaces and comments from PHP code.

Operations:
- remove unnecessary whitespace, change necessary whitespace to `\n`
- strip comments, preserve only the first doc-comment
- minify variables, e.g. in `function f($long) { return $long; }` (incompatible with https://php.net/functions.arguments#functions.named-arguments)
- remove extra `{}`, e.g. in `if (true) { oneCommand(); }`
- remove `?><?php` and empty `<?php ?>`
- change `?>HTML<?php` to `echo 'HTML'` if it saves space
- join consecutive echo, e.g. in `echo 'a'; echo 'b';`
- strip public visibility or change it to `var`

Demo: https://vrana.github.io/PhpShrink/

The main user is [Adminer](https://www.adminer.org/).
