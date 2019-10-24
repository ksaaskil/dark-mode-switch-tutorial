# Light-dark theme tutorial

[Source](https://dev.to/ananyaneogi/create-a-dark-light-mode-switch-with-css-variables-34l8).

## Build SCSS

### Manually

```bash
./build-sass.sh
```

### With `watchman`

#### Init

Watch the project:

```bash
watchman watch-project .
```

List projects:

```bash
watchman watch-list
```

Add a trigger with the simple syntax:

```bash
watchman -- trigger . build-sass '*.scss' -- bash build-sass.sh
```

Alternatively, add the trigger from JSON:

```bash
watchman trigger -j < sass-trigger.json
```

#### Clean-up

Delete the trigger:

```bash
watchman trigger-del . build-sass
```

Unwatch project:

```bash
watchman watch-del .
```
