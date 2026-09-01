# Untap and Priority
One of the issues we found while testing is that there needs to be some kind of restriction on how often someone can trigger a global untap.
- Ensuring that you have priority while untapping without coat meant that you could untap, take an action that doesn’t pass prio, and untap again infinitely.
- When we require untap itself to pass prio, we found that the disadvantaged player who is out of actions is effectively passing prio to a stronger opponent with a fresh board.
- When untap passes prio but *isn’t global,* it means creatures that should be tapped for having taken actions are now free to respond.
- When a single player untap is triggered on receiving prio (and resolving the stack) the game does not have the back and forth action that I designed abilities to be used with.

What we learned is primarily:
- Passing prio and untap need to happen separately, because otherwise usually only one creature does stuff per untap.
- There needs to be a limit on how often you can trigger an untap.
- Untap can’t be the last thing a player does before passing.

For now, I’m thinking that the solution is:
- Global untap.
- One untap “charge” per prio received.
- Untap at sorcery speed.

Effectively, the priority token should be two sided, like a clean/dirty magnet on a washing machine, and you can flip it once to spend your untap (which is global) and retain priority.