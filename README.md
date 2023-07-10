# KiCAD Project Template

This project template for [KiCAD](https://www.kicad.org) is powered by [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/), a powerful tool that creates projects from project templates.

## Getting Started

First, you will need Python installed on your system. This should already be installed if you have KiCAD, but if not, you can download it from [here](https://www.python.org/downloads/).

You can either use my Python script (https://github.com/ShirkyBooi/CreateKiCADProject) or CLI as described below.

With Python installed, you can then install Cookiecutter using pip, the Python package manager. Open a terminal and run the following command:

```sh
pip install "cookiecutter>=1.4.0"`
```

Next, navigate to the directory where you want to create your new KiCAD project and run the following command:

```sh
cookiecutter https://github.com/ShirkyBooi/CreateKiCADProject
```

Or if you have used the template before, you can simply run:

```sh
cookiecutter CreateKiCADProject
```

If there have been changes to the repository since you last used the template, please use the first command and answer "yes" when prompted to redownload the template.

You will be prompted for the following information:

Project Name
Project Repo URL: The URL assigned to the project.
Project Description
Author Name: The name of the engineer.
Department: The team responsible for the project.
After providing this information, Cookiecutter will create a new KiCAD project in the current directory.

You can then initialize this new project as a Git repository, add all the files, commit them, set the remote repository to the URL that was assigned, and finally push everything to the master branch of the remote repository. At this point you can remove the remaining cookiecutter artifacts, such as Makefile, mkdocs.yml, poetry.lock and pyproject.toml. Though I have automated this in my Python Script.

```sh
cd your_project_name
git init
git add .
git commit -m "Initial commit"
git remote add origin your_project_repo_url
git push -u origin master
```

## Open KiCad and open the project

If you have performed the steps above, you should now be able to open KiCad and open the new project.
Please check the README within your generated project for more information.

## Contribution

Contributions to the KiCAD Project Template are very welcome! You can contribute in several ways:

- Reporting a bug: Please provide as much details as possible to reproduce the bug. This includes the version of the template, your operating system, steps to reproduce the bug, and, if available, error messages.

- Suggesting enhancements: Do you have an idea for a new feature, or for an improvement of an existing feature? Let us know!

- Contributing code: If you would like to contribute code (either to fix a bug or to implement a new feature), please follow these steps:

  1. Create a new branch on which to make your changes.

  3. Make your changes, commit them to your branch, and push the commits to your branch.

  4. Open a Pull Request for your changes.

## Author

This program was origionally created by [Stephen Eaton](https://github.com/madeinoz67).

It was adapted by [Ethan Shirk](https://github.com/ShirkyBooi).
