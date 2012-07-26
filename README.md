# change-inner.el

change-inner gives you vim's `ci` command, building on
[expand-region](https://github.com/magnars/expand-region.el). It is most easily
explained by example:

   function test() {
     return "semantic kill";
   }

With point after the word `semantic`

 * `change-inner "` would kill the contents of the string
 * `change-outer "` would kill the entire string
 * `change-inner {` would kill the return-statement
 * `change-outer {` would kill the entire block

I use `M-i` and `M-o` for this.

## Installation

Start by installing
[expand-region](https://github.com/magnars/expand-region.el).

    (require 'change-inner)
    (global-set-key (kbd "M-i") 'change-inner)
    (global-set-key (kbd "M-o") 'change-outer)

## License

Copyright (C) 2011 Magnar Sveen

Author: Magnar Sveen <magnars@gmail.com>
Keywords: marking region

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
