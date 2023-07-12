---
name: Bug report
about: Create a bug report
title: "[BUG]: "
labels: "bug"
assignees: UbioZur
body:
  - type: textarea
    id: Environement
    attributes:
      label: Your Environment
      description: Tell us about your environment.
      placeholder: "OS information: uname -a \n Ansible information: ansible --version"
    validations:
      required: true
  - type: textarea
    id: expected
    attributes:
      label: Expected Behaviour
      description: A clear and concise description of what you expected to happen.
    validations:
      required: true
  - type: textarea
    id: reproduce
    attributes:
      label: Steps to reproduce
      description: Steps to reproduce the behavior
    validations:
      required: true
  - type: textarea
    id: reproduce
    attributes:
      label: Steps to reproduce
      description: Steps to reproduce the behavior
      placeholder: "1. Go to '...' \n 2. Click on '....' \n 3. ...
4. See error"

---

**Screenshots**
If applicable, add screenshots to help explain your problem.

**Additional context**
Add any other context about the problem here.
