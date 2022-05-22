---
title: "TMUX"
tags:
- how-to
- Linux
---

- [大抄](http://www.dayid.org/comp/tm.html)
- New session with a name: `tmux new -s foo`
- List alive session, there can be multiple sessions: `tmux ls`
- Attach a session: `tmux attach -t remote`

- In-tmux prefix: `Ctrl+b`
- Cut a splitting pane
    - `Ctrl+b "`  split to top/bottom
    - `Ctrl+b %`  left/right
- Creating windows (virtual desktop) and switching
     * New window `Ctrl+b c`
     * previous window `Ctrl+b p`
     * `Ctrl+b n  # Next window`
- Scrolling: `Ctrl+b Up / Down / PgUp / PgDn`, q to exit
- Adjusting pane: `Ctrl+b Ctrl+arrow`
- Leaving session: `Ctrl+b d(D)`, D for prompt