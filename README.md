Spear Education Docker Exec Action
====================================
Runs a command inside of the project's configured docker environment

**Requires a .buildconfig file**

## Examples
```
  - id: composer-validate
    name: Validate composer.json and composer.lock
    uses: speareducation/action-docker-exec@main
    with:
      command: composer validate | tee .ci-results/composer-validation.txt
```

```
  - id: run-script
    name: Runs an arbitrary entrypoint script
    uses: speareducation/action-docker-exec@main
    with:
      entrypointFile: ./entrypoint.sh
```