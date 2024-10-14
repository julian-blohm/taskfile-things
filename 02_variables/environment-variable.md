# Variables in Taskfile

It is possibler to use environment variables (e.g. from `.env` files), set variable in taskfile, use system environment variables, override variables using CLI arguments... let's see how


- Variables can be overriden using arguments e.g. `task world MYWORLD=Earth`
- If you want to use a system variable you can also export the variable and hav it as default: `export MYWORLD=Earth`; then execute `task world`
- system environment variables will override the values defined in the .env file e.g.
    - `.env` has `ENDPOINT=testing.com`
    - system environment variable: `export ENDPOINT=dev.com`
    - => dev.com would be used
