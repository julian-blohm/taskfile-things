# taskfile-things
playing around with taskfile  https://taskfile.dev

## What is taskfile
Taskfile is a task runner and build tool designed to be simpler and easier to use than traditional tools like GNU Make. It operates with a single binary called task and requires no additional dependencies. Taskfile allows to define tasks using a YAML schema in a Taskfile.yml file.
We will focus on CI/CD stuff here

https://taskfile.dev

## Sample Taskfile
```
# Taskfile.yml
version: '3'

tasks:
  hello:
    cmds:
      - echo 'Hello World from Task!'
    silent: true
```

- the hello task prints "Hello World from Task!" when executed. 
- 'silent: true' suppresses output of the task

## Why Taskfile
Advantages over traditional build tools:
- simplifies task automation with YAML
- Taskfile is a single binary that works across different platforms without additional dependencies
- supports advanced features like task dependencies, variables, and error handling
- Taskfile tasks can be executed directly from the command line, making it easy to integrate with other tools and scripts

