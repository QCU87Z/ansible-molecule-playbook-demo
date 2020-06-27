# Molecule testing example for testing an Ansible playbook

This is an example of how to set up molecule to test a playbook rather than a role.

> This is configured to use docker as the driver

## Commands

```bash
# Setup
molecule init scenario

# Start container and run through play
molecule converge

# Rerun tests
molecule verify

# Login to container
molecule login

# Clean up container
molecule destory

# Full test and clean up
molecule test

# Lint project
molecule lint
```

The project is setup in away that you can swap out the OS of a container with an environment variable

`MOLECULE_DISTRO=debian10 molecule converge` to run tests against a  debian10 based container.
