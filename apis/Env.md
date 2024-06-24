## Env API

The `Env` class parses and provides values from a local .env file.  
It supports the `dotenvy` syntax, except `export` keyword. For details, see [here](https://hexdocs.pm/dotenvy/dotenv-file-format.html).   
This class extends the Java `Map<String, String>` type to provide a seamless experience in languages that support native map access.

### Example usage in RhinoJS

+ Local .env file:
```dotenv
TEST1=Hello
TEST2=World!

FORMATTED="Goodbye ${TEST2}"
```
+ Script:
```js
Object.keys(Env) // ["TEST1", "TEST2", "FORMATTED"]

Env.TEST1     // "Hello"
Env['TEST2']  // "World!"
Env.FORMATTED // "Goodbye World!"
```