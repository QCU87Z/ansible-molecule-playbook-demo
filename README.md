# Molecule testing example for testing an Ansible playbook

![CI](https://github.com/QCU87Z/ansible-molecule-playbook-demo/workflows/CI/badge.svg)

This is an example of how to set up molecule to test a playbook rather than a role. Based off video from geerlingguy

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

## Example run

[![asciicast](https://asciinema.org/a/usiHI9djiwmQHZD7ouzsctJ9y.svg)](https://asciinema.org/a/usiHI9djiwmQHZD7ouzsctJ9y)
