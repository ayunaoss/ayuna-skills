# Ayuna Skills

This project provides agent skills to manage projects using golang, python and typescript languages. The following skills are available and follow the standard [Agent Skills](https://agentskills.io/specification) structure.

1. **ayuna-common-guidelines**: Common programming best practices, naming convensions, and project structuring.
2. **ayuna-go-library**: Skills for golang based library project
3. **ayuna-py-library**: Skills for python based library project
4. **ayuna-ts-library**: Skills for typescript based library project
5. **ayuna-go-service**: Skills for golang based service or application project
6. **ayuna-py-service**: Skills for python based service or application project
7. **ayuna-ts-service**: Skills for typescript based service or application project

## How to install

You can use one of the following ways to install the skills.

### Using `skills` tool

#### Interactive installation

You can install the skills interactively using the following command. Always select `ayuna-common-guidelines` skill as that is the dependency for rest of the skills.

```bash
npx skills add ayunaoss/ayuna-skills
```

For example, to install `ayuna-ts-service` skill, select both `ayuna-common-guidelines` and `ayuna-ts-service` options in the interactive prompt that appears.

#### Non-interactive installation

You can install any desired skill using the following command.

```bash
## <skill-name> corresponds to one of the skills listed above
npx skills add your-username/ayuna-skills --skill <skill-name>
```

For example, to install `ayuna-go-service` skill, you can run the following commands from within your project folder.

```bash
## Always install the recommended dependency
npx skills add your-username/ayuna-skills --skill ayuna-common-guidelines

## Install the target skill
npx skills add your-username/ayuna-skills --skill ayuna-go-service
```

### Adding skill manually

Clone the repo into a temporary location and copy the required skills folders into your project's `.agents/skills/` folder. Always add `ayuna-common-guidelines` skill as that is the dependency for rest of the skills.

For example, to use `ayuna-py-library` skill, copy both `ayuna-common-guidelines` and `ayuna-py-library` skill folders into your project's `.agents/skills/` folder.
