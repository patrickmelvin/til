You can save the current position of your cursor with a feature called a "mark". Each file has a set of marks identified with lowercase letters which map to a location in the current file. There are also a global set of marks which each map to a location within a single file.

You can set a mark by pressing `m`, followed by the letter you are mapping the location to. For example, `ma` would map the location to the letter a, and you will move to that location whenever you call that mark within that file. `mA` would map the cursor location to A globally, and the cursor will move back to that location whenever that mark is called within any file.

Marks can be called by typing either an apostrophe or backtick, followed by the letter that the mark is mapped to. So `` `a`` will jump to the location that a is mapped to within the file and `` `A`` will open the file that A belongs to and jump to the location that it is mapped to. Apostrophes jump to the line that the mark belongs to and backticks jump to the line and column of the mark.

You can list current marks with the `:marks` command.

You can cycle through lowercase marks with `]` and `[`

| Command | Description                                      |
|---------|--------------------------------------------------|
| `['`    | Jump to previous line with lowercase mark        |
| ``]` `` | Jump to next line and column with lowercase mark |
| `5]'`   | Jump to the fifth lowercase mark after cursor    |

Vim sets a number of marks automatically:

| Command   | Description                                               |
|-----------|-----------------------------------------------------------|
| `` `.``   | Jump to position of last change in current buffer         |
| `` `"``   | Jump to position where last exited current buffer         |
| `` `0``   | Jump to positon in last file edited                       |
| `` `1``   | Jump to position in second to last file edited            |
| `` ` ` `` | Jump to position in current buffer where last jumped from |
| `` `[``   | Jump to beginning of previously changed/yanked text       |
| `` `>``   | Jump to end of last visual selection

You can delete marks either by deleting the line that they are on, or by calling the `:delmarks` or `delm` commands.

| Command        | Description                                   |
|----------------|-----------------------------------------------|
| `:delmarks aA` | Delete marks `a` and `A`                      |
| `:delm a-d`    | Delete marks `a` through `d`                  |
| `:delmarks!`   | Delete all lowercase marks for current buffer |