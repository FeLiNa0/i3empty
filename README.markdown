# i3empty

Quickly switch to a new numbered workspace.

## i3 config

Place these lines in your i3 config for wrap-around switching:

```
bindsym $mod+Ctrl+Left exec --no-startup-id i3empty.py prev
bindsym $mod+Ctrl+Right exec --no-startup-id i3empty.py next

bindsym $mod+Ctrl+1 exec --no-startup-id i3empty.py next 1
bindsym $mod+Ctrl+2 exec --no-startup-id i3empty.py next 2
bindsym $mod+Ctrl+3 exec --no-startup-id i3empty.py next 3
bindsym $mod+Ctrl+4 exec --no-startup-id i3empty.py next 4
bindsym $mod+Ctrl+5 exec --no-startup-id i3empty.py next 5
bindsym $mod+Ctrl+6 exec --no-startup-id i3empty.py next 6
bindsym $mod+Ctrl+7 exec --no-startup-id i3empty.py next 7
bindsym $mod+Ctrl+8 exec --no-startup-id i3empty.py next 8
bindsym $mod+Ctrl+9 exec --no-startup-id i3empty.py next 9
bindsym $mod+Ctrl+0 exec --no-startup-id i3empty.py next 10
```

## Usage

Run `i3empty.py next` or `i3empty.py prev`.

```
i3empty.py [-h] [-r, --relative REL] [-w, --wrap WRAP]
           [-s, --strict STRICT] [-m, --move MOVE]
           [direction] [number]

Switch to an empty numbered workspace.

positional arguments:
  direction            either next (default) or prev
  number               workspace to start searching from (default: current)

optional arguments:
  -h, --help           show this help message and exit
  -r, --relative REL   use workspace indices, not numbers (default: no)
  -w, --wrap WRAP      if at edge, wrap around to other edge (default: yes)
  -s, --strict STRICT  numbered workspaces have a numeric name (default: yes)
  -m, --move MOVE      move container to new workspace (default: no)
```