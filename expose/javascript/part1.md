## Part 1

1. values added: 20
2. final result: 20
3. Sometimes you shouldn't use var because it is function-scoped instead of block-scoped. It can leak outside of blocks which can cause some bugs.
4. values added: 20
5. This throws an error. "let" is block-scoped so result only exists inside the if block.
6. This throws an error. "const" cannot be reassigned after it is declared, so the error is thrown at line 7 before line 9 is reached.
7. Never reached either, so another error is thrown at line 7.
