# taskfile-things
playing around with taskfile  https://taskfile.dev

## What is taskfile
Taskfile is a task runner and build tool designed to be simpler and easier to use than traditional tools like GNU Make. It operates with a single binary called task and requires no additional dependencies. Taskfile allows to define tasks using a YAML schema in a Taskfile.yml file.
We will focus on CI/CD stuff here

- Homepage: https://taskfile.dev
- Git Repo: https://github.com/go-task/task 

## How to Install:
just look here: https://taskfile.dev/installation/


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

## Taskfile for CI/CD
E.g. there are multiple projects with different deployment processes and various CI/CD platforms. Instead of writing complete CI/CD processes on the platforms (GH Action, Gitlab CI/CD, Jenkins...) identify most common and repetitive tasks and create a Taskfile template with all the different modules for various types of development cycle tasks in the CI/CD process and reuse it for all projects by including those modules from the Taskfile.

This can reduce the number of pipeline steps and also avoids writing complex scripts in CI/CD files.

## Tipps before getting startet
You should be familiar with:
- Docker
- Git
- Basic Bash/Linux commands
- YAML: as Taskfile are written in YAML
- CI/CD: Basic understanding of CI/CD pipelines, how they work, and the basic application deployment process