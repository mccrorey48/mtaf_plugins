# mtaf_plugin

These are example plugins for use with mtaf-inspector.

The mtaf-inspector executable is installed by "pip install mtaf" (see
pypi.org/project/mtaf for a more information)).  It provides a GUI for
interacting with a connected Android  device (or emulator), with screen capture
and displayed-element analysis capability to assist in writing Appium tests in
Python for Android devices.

The default capabilities of mtaf-inspector are designed to work with any
Android device and application, but for specific applications, plugins can be
used to extend its capabilities.

When mtaf-inspector starts, it uses adb to query the target for the name of the
current application. If there is a plugin that matches the name in the
plugin directory, it will be loaded.

The name if the plugin for a specific application is constructed by substituting
underscores for periods and adding a ".py" extension. For example, 
if the application is "com.android.chrome", the matching plugin would be 
"com_android_chrome.py".

Plugins must be in a directory named "inspector_plugins", and this directory must
also contain an empty file named "__init__.py". The path to the plugin directory 
can be specified with an entry in the ~/.MtafInspector/config.yml file
(for example, "plugin_dir: /home/mmccrorey/mtaf_plugins/inspector_plugins").
If "plugin_dir" is not defined in config.yml, inspector will try to find the 
"inspector_plugins" module using Python's sys.path list.

The purpose of these simple example plugins is to show how functions, menu items
and other features can be added to mtaf-inspector.




