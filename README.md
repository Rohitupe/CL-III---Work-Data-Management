# Template: Standard Robot Framework

Want to get started using [Robot Framework](https://robocorp.com/docs/languages-and-frameworks/robot-framework/basics) this is the simplest template to start from.

This template robot:

- Uses [Robot Framework](https://robocorp.com/docs/languages-and-frameworks/robot-framework/basics) syntax.
- Includes all the necessary dependencies and initialization commands (`conda.yaml`).
- Provides a simple task template to start from (`tasks.robot`).

## Learning materials

- [All docs related to Robot Framework](https://robocorp.com/docs/languages-and-frameworks/robot-framework)
------------------------------------------------------
# Code to be edited for documentation #

## CODE structure
 -- Code is divided in the prooducer and consumer format == (Using work queue items here))
 - producer will load out all the data needed from the *API*
 - Consumer will perform that loaded data
 - using Shared file to refer to the same code used in Producer - Consumer

------------------------------------------------------

# README for the robot

Describe your robot here. E.g., what it does, what the requirements are, how to run it.

## Development guide

Run the robot locally:

```
rcc run
```

Provide access credentials for Control Room connectivity:

```
rcc configure credentials <your_credentials>
```

Upload to Control Room:

```
rcc cloud push --workspace <workspace_id> --robot <robot_id>
```

### Suggested directory structure

The directory structure given by the template:

```
├── devdata
├── keywords
│   └── keywords.robot
├── libraries
│   └── MyLibrary.py
├── variables
│   └── variables.py
├── conda.yaml
├── robot.yaml
└── tasks.robot
```

where

- `devdata`: A place for all data/material related to development, e.g., test data. Do not put any sensitive data here!
- `keywords`: Robot Framework keyword files.
- `libraries`: Python library code.
- `variables`: Define your robot variables in a centralized place. Do not put any sensitive data here!
- `conda.yaml`: Environment configuration file.
- `robot.yaml`: Robot configuration file.
- `tasks.robot`: Robot Framework task suite - high-level process definition.

In addition to these, you can create your own directories (e.g. `bin`, `tmp`). Add these directories to the `PATH` or `PYTHONPATH` section of `robot.yaml` if necessary.

Logs and artifacts are stored in `output` by default - see `robot.yaml` for configuring this.

Learn how to [handle variables and secrets](https://robocorp.com/docs/development-guide/variables-and-secrets/secret-management).

### Configuration

Give the task name and startup commands in `robot.yaml` with some additional configuration. See [Docs](https://robocorp.com/docs/setup/robot-structure#robot-configuration-file-robot-yaml) for more.

Put all the robot dependencies in `conda.yaml`. These are used for managing the execution environment.

### Additional documentation

See [Robocorp Docs](https://robocorp.com/docs/) for more documentation.

