#brute-force 

High-Performance word generator with a per-position configurable charset

For each position of the generated password candidates we need to configure a placeholder. If a password we want to crack has the length 8, our mask must consist of 8 placeholders.

- A mask is a simple string that configures the keyspace of the password candidate engine using placeholders.
- A placeholder can be either a custom charset variable, a built-in charset variable or a static letter.
- A variable is indicated by the ? letter followed by one of the built-in charset (l, u, d, s, a) or one of the custom charset variable names (1, 2, 3, 4).
- A static letter is not indicated by a letter. An exception is if we want the static letter ? itself, which must be written as ??.

