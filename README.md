# Role Name

Simple wrapper to execute one-off tasks as part of an Ansible Container build. Great for inserting simple custom tasks that aren't re-useable and would otherwise require an entire role to be used by ansible-container.

**NOTE: This role does not do anything by itself! You must provide at least one task file containing the tasks you want this role to execute!**

Run the following commands
to install the service:

```bash
# Set the working directory to your Ansible Container project root
$ cd myproject

# Install the service
$ ansible-container install marcusianlevine.extra-container-tasks
```

## Requirements

- [Ansible Container](https://github.com/ansible/ansible-container)
- An existing Ansible Container project. To create a project, simply run the following:
    ```bash
    # Create an empty project directory
    $ mkdir myproject

    # Set the working directory to the new directory
    $ cd myproject

    # Initialize the project
    $ ansible-contiainer init
    ```

## Role Variables

### Required

- `task_files`
  - list of files containining Ansible task definitions
  - paths should be relative to the location of `container.yml` (i.e. relative to the directory mounted on the conductor at `/src`)

### Optional

- `vars_files`
  - list of paths to Ansible variable files needed by the provided `task_files`
  - paths should be relative to the location of `container.yml` (i.e. relative to the directory mounted on the conductor at `/src`)

## License

BSD

## Author Information

Written by Marcus Levine for CKM Advisors


