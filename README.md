# Ayuna Skills

This project provides agent skills to manage projects using golang, python and typescript languages.
The following skills are available and follow the standard [Agent Skills](https://agentskills.io/specification) structure.

1. **ayuna-coding-guide**: Best practices, naming conventions, recommended tools and libraries for
   golang, python, and typescript projects.
2. Other skills to be added (...coming soon)

## How to install

You can use one of the following ways to install the skills.

### Using `skills` tool

#### Interactive installation

You can install the skills interactively using the following command.
Always select `ayuna-coding-guide` skill as that is the dependency for rest of the skills.

```bash
npx skills add ayunaoss/ayuna-skills
```

#### Non-interactive installation

Install a desired skill as follows.

```bash
## Always install the recommended dependency
npx skills add your-username/ayuna-skills --skill ayuna-coding-guide

## Install the desired skill
npx skills add your-username/ayuna-skills --skill <skill-name>
```

### Adding skill manually

Clone the repo into a temporary location and copy the required skills folders into your project's `.agents/skills/`
folder. Always add `ayuna-coding-guide` skill as that is the dependency for rest of the skills.
