# Exercism GDScript Track

[![Configlet](https://github.com/exercism/gdscript/actions/workflows/configlet.yml/badge.svg)](https://github.com/exercism/gdscript/actions/workflows/configlet.yml) [![.github/workflows/test.yml](https://github.com/exercism/gdscript/actions/workflows/test.yml/badge.svg)](https://github.com/exercism/gdscript/actions/workflows/test.yml)

Exercism exercises in GDScript.

## Testing

To set up for testing, clone https://github.com/exercism/gdscript-test-runner and move its contents to `/opt/exercism/gdscript/test-runner`:

```sh
git clone https://github.com/exercism/gdscript-test-runner.git
sudo mkdir -p /opt/exercism/gdscript/
sudo mv gdscript-test-runner/ /opt/exercism/gdscript/test-runner/
```

To test the exercises, run `godot --headless -s bin/verify-exercises.gd`.
This command will iterate over all exercises and check to see if their exemplar/example implementation passes all the tests.

### Track linting

[`configlet`](https://exercism.org/docs/building/configlet) is an Exercism-wide tool for working with tracks. You can download it by running:

```shell
./bin/fetch-configlet
```

Run its [`lint` command](https://exercism.org/docs/building/configlet/lint) to verify if all exercises have all the necessary files and if config files are correct:

```shell
$ ./bin/configlet lint

The lint command is under development.
Please re-run this command regularly to see if your track passes the latest linting rules.

Basic linting finished successfully:
- config.json exists and is valid JSON
- config.json has these valid fields:
    language, slug, active, blurb, version, status, online_editor, key_features, tags
- Every concept has the required .md files
- Every concept has a valid links.json file
- Every concept has a valid .meta/config.json file
- Every concept exercise has the required .md files
- Every concept exercise has a valid .meta/config.json file
- Every practice exercise has the required .md files
- Every practice exercise has a valid .meta/config.json file
- Required track docs are present
- Required shared exercise docs are present
```
