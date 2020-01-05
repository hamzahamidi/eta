## Ideas

- Should we put `;` after `exec` commands?
- Switch to `=` for interpolate syntax?
- Use one of these RegExps (use the first unless it somehow breaks) to capture groups while looping through powerchars.:

```
(?:[^]*?|(?:'(?:\\[\s\w"'\\`]|[^\n\r'\\])*?'|`(?:\\[\s\w"'\\`]|[^\\`])*?`|"(?:\\[\s\w"'\\`]|[^\n\r"\\])*?"))*?(?:([|()]|=>)|\/\*[^]*?\*\/|((\/)?(-|_)?}}))

(?:(?:'(?:\\[\s\w"'\\`]|[^\n\r'\\])*?'|`(?:\\[\s\w"'\\`]|[^\\`])*?`|"(?:\\[\s\w"'\\`]|[^\n\r"\\])*?")|\/\*[^]*?\*\/|[^])*?(?:([|()]|=>)|((\/)?(-|_)?}}))
```