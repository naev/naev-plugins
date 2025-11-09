# NAEV PLUGINS

This repository is meant to be a place to centralize a list of approved
plugins. If you want to make changes such as adding plugins or updating their
information, please open a pull request to do so.

## How to Use Plugins

*Due to a lack of a proper plugin manager ([help wanted!](https://codeberg.org/naev/naev/issues/2180)), installation has to be
done manually at the moment.*

### Manual Install

Installation is as simple as dropping the plugin `.zip` file (or entire
directory, such as git clone) into your plugin directory. You can find your
plugin directory by running Naev, clicking on options, then clicking on
plugins. When you launch Naev, it should automatically detect the plugins and
load them. You can check loaded plugins by looking at the plugins tab in the
options menu.

## Plugin Information Format

The plugin information format is a stub of the `plugin.toml` that is necessary
in each plugin with additional information on where to get the plugin. For this
repository, only a few fields are necessary. In particular, a complete example
is shown below.

```toml
identifier = "ExampleTC"
name = "Sea of Mayonnaise"
source = { git = "https://codeberg.org/naev/plugin-total-conversion-example.git" }
metadata = "https://codeberg.org/naev/plugin-total-conversion-example/raw/branch/main/plugin.toml"
```

To obtain the plugin you can either use a `<git>` node indicating that the link is to a git repository, or you can use a `<link>` to directly link to a zip file to download. A summary of the available nodes is shown below:

1. `identifier`: Specifies the unique identifier of the plugin. Should not overlap with any other existing plugins, and be short and concise.
1. `name`: Full name of the plugin.
1. `source`: Specifies where the main repository is stored. This can be either a git repository with `{ git = "..." }` or a direct download with `{ download = "..." }`.
1. `metadata`: Where the plugin metadata is located. This should be a path to directly download the `plugin.toml` of the plugin, and will be used by the plugin manager to find new information and update the plugin.
