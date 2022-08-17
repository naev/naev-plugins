# NAEV PLUGINS

This repository is meant to be a place to centralize a list of approved
plugins. If you want to make changes such as adding plugins or updating their
information, please open a pull request to do so.

## Plugin Information Format

The plugin information format is a stub of the `plugin.xml` that is necessary in each plugin with additional information on where to get the plugin. In particular, an example is shown below.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<plugin name="Sea of Mayonnaise">
 <author>Naev DevTeam</author>
 <www>https://github.com/naev/total_conversion_plugin_example</www>
 <git>https://github.com/naev/total_conversion_plugin_example</git>
</plugin>
```

To obtain the plugin you can either use a `<git>` node indicating that the link is to a git repository, or you can use a `<link>` to directly link to a zip file to download.

