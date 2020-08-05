# rush - the really uninteractive shell
Rush is designed to run POSIX scripts, and run them fast. Think of it as a Rust [dash](https://en.wikipedia.org/wiki/Almquist_shell#dash).

I know that the name is overused, but it's too good to pass up.

### // TODO: 
- [X] Simple command execution `ls -ltr`
- [X] Pipes `exa | grep cargo`
- [X] Exit status logic `! false && ls || date`
- [ ] Redirection
    - [X] File descriptor to another `ls error 2>&1`
    - [X] To/from file `date > time.txt` `< Cargo.toml wc`
    - [X] Appending `>>`
    - [X] Here-docs `<<`
    - [ ] Raw, non-io file descriptors `4>&7`
- [ ] Async execution `&`
- [ ] Shell builtins
   - [ ] Normal built-ins
      - [ ] `alias` `unalias`
      - [X] `cd`
      - [ ] etc
   - [ ] Special built-ins
      - [X] `exit`
      - [ ] `exec`
      - [ ] etc
- [ ] Expansions
   - [X] Tilde expansion
   - [ ] Parameter expansion
   - [ ] Command substitution
   - [ ] Arithmetic expansion
- [ ] Variables
- [ ] Quotes
   - [X] Quote recongintion
   - [ ] There's probably more, right?
- [ ] Control flow `if` `for` `while` `case` etc
- [ ] Expand this to-do list


### Decisions to make

* Should this shell replicate commands that are typically built-in but also have system alternatives?
