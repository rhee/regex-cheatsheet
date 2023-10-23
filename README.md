# regex-cheatsheet

- [ see google docs version ](https://docs.google.com/spreadsheets/d/13SBG5RT96XueNl7UP6C-QMAo99RLxz2ms4yyGx_jSuo/pubhtml?gid=0&single=true)
- [ (glob) greg's wiki ](https://mywiki.wooledge.org/glob)
- [ (sed) Linux sed command ](https://www.computerhope.com/unix/used.htm)
- [ (regex) remram44 ](https://remram44.github.io/regex-cheatsheet/regex.html)


Note: for sed, tokens escaped by `\` could be a GNU extension, and may not work for non-linux (i.e.: mac os) sed


simple | grep | egrep | [sed](http://www.gnu.org/software/sed/manual/html_node/Regular-Expressions.html#Regular-Expressions)  | awk  | PCRE: perl java javascript | comment
-------|------|-------|------|------|----------------------------|------------- 
`^`    | `^`  |  `^`  | `^`  | `^`  | `^`  | &nbsp;
`.`    | `.`  | `.`  | `.`  | `.`  | `.` | &nbsp;
`$`    | `$`  | `$`  | `$`  | `$`  | `$` | &nbsp;
_a_&vert;_b_  |_a_\\&vert;_b_  |_a_&vert;_b_ | _a_\\&vert;_b_ | _a_&vert;_b_ | _a_&vert;_b_  | &nbsp;
`(` ... `)` | `\(` ... `\)` | `(` ... `)` | `\(` ... `\)` | `(` ... `)`  | `(` ... `)`  | &nbsp;
`[` ... `]` | `[` ... `]` | `[` ... `]` | `[` ... `]` | `[` ... `]` | `[` ... `]` | &nbsp;
`[^` ... `]` | `[^` ... `]` | `[^` ... `]` | `[^` ... `]` | `[^` ... `]` | `[^` ... `]` | &nbsp;
`*`    | `\*`  | `*`  | `*`  | `*`  | `*` | &nbsp;
`+`    | `\+` | `+`  | `\+` | `+`  | `+` | &nbsp;
`?`    | `\?` | `?`  | `\?` | `?`  | `?` | &nbsp;
`{`_i_`}`   | `\{`_i_`\}` | `{`_i_`}` | `\{`_i_`\}` | `{`_i_`}` | `{`_i_`}` | &nbsp;
`{`_i_`,}`  | `\{`_i_`,\}` | `{`_i_`,}` | `\{`_i_`,\}` | `{`_i_`,}` | `{`_i_`,}` | &nbsp;
`{`_i_`,`_j_`}` | `\{`_i_`,`_j_`\}` | `{`_i_`,`_j_`}` | `\{`_i_`,`_j_`\}` | `{`_i_`,`_j_`}` | `{`_i_`,`_j_`}` | &nbsp;
`[:alnum:]` ||  | | `[:alnum:]` | `[:alnum:]` or `\p{alnum}` | &nbsp;
`[:alpha:]` | | | | `[:alpha:]` | `[:alpha:]` or `\p{alpha}` | &nbsp;
`[:blank:]` | | | | `[:blank:]` | `[:blank:]` or `\p{blank}` | &nbsp;
`[:cntrl:]` | | | | `[:cntrl:]` | `[:cntrl:]` or `\p{cntrl}` | &nbsp;
`[:digit:]` | | | `[[:digit:]]` | `[:digit:]` | `[:digit:]` or `\p{digit}` | &nbsp;
`[:graph:]` | | | | `[:graph:]` | `[:graph:]` or `\p{graph}` | &nbsp;
`[:lower:]` | | | | `[:lower:]` | `[:lower:]` or `\p{lower}` | &nbsp;
`[:print:]` | | | | `[:print:]` | `[:print:]` or `\p{print}` | &nbsp;
`[:punct:]` | | | | `[:punct:]` | `[:punct:]` or `\p{punct}` | &nbsp;
`[:space:]` | | | | `[:space:]` | `[:space:]` or `\p{space}` | &nbsp;
`[:upper:]` | | | | `[:upper:]` | `[:upper:]` or `\p{upper}` | &nbsp;
`[:xdigit:]` || | | `[:xdigit:]`| `[:xdigit:]` or `\p{xdigit}` | &nbsp;
`\w` |        | |     | `\w`   | `\w` | &nbsp;
`\W` |        | |     | `\W`   | `\W` | &nbsp;
`\s` |        | |     |        | `\s` | &nbsp;
`\S` |        | |     |        | `\S` | &nbsp;
`\d` |        | |     |        | `\d` | &nbsp;
`\D` |        | |     |        | `\D` | &nbsp;
`\<` |        | |     | `\<`   |      | &nbsp; 
`\>` |        | |     | `\>`   |      | &nbsp;
`\y` |        | |     | `\y`   |      | &nbsp;
`\B` |        | |     | `\B`   | `\b` | &nbsp;
`*?` || | | | `*?` | &nbsp;
`+?` || | | | `+?` | &nbsp;
`??` || | | | `?` | &nbsp;
`{`_i_`}?` || | | | `{`_i_`}?` | &nbsp;
`{`_i_`,}?` || | | | `{`_i_`,}?` | &nbsp;
`{`_i_`,`_j_`}?` || | | | `{`_i_`,`_j_`}?` | &nbsp;
`*+` || | | | `*+` | &nbsp;
`++` || | | | `++` | &nbsp;
`?+` || | | | `?+` | &nbsp;
`{`_i_`}+` || | | | `{`_i_`}+` | &nbsp;
`{`_i_`,}+` || | | | `{`_i_`,}+` | &nbsp;
`{`_i_`,`_j_`}+` || | | | `{`_i_`,`_j_`}+` | &nbsp;
`[[:` ... `:]]` || | | | `[[:` ... `:]]` | &nbsp;
`(?[` ... `])` || | | | `(?[` ... `])` | &nbsp;
`(?:`_x_`)` || | | | `(?:`_x_`)` | &nbsp;
`(?=`_x_`)` || | | | `(?=`_x_`)` | &nbsp;
`(?!`_x_`)` || | | | `(?!`_x_`)` | &nbsp;
`(?<=`_x_`)` || | | | `(?<=`_x_`)` | &nbsp;
`(?<!`_x_`)` || | | | `(?<!`_x_`)` | &nbsp;
`\n` |  |       | `\n` | | | &nbsp;
`\1`, `\2`, ... || | `\1`, `\2`, ... |  | | &nbsp;


