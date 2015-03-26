=====
Django Simple Plugins
=====

Django Simple Plugins provides a simple yet powerful and configurable tool for adding plugins to your Django project.

Detailed documentation on https://github.com/pistacchio/django-simple-plugins

Quick start
-----------

1. Install with pip install django-simple-plugins

2. Add "plugins" to your INSTALLED_APPS setting like this::

    INSTALLED_APPS = (
        ...
        'plugins',
    )

3. Add a "PLUGINS_DIR" key to your settings like this::
    PLUGINS_DIR = os.path.join(BASE_DIR, 'plugins')

4. Run `python manage.py migrate` to create the plugin models.

5. Create your plugins in the configured directories like simple python files with the following template:

    plugin_type  = 'TYPE 1'
    verbose_name = 'Plugin n 1'

    def run(options, context, input):
        print 'Plugin 1'
        return 'Plugin 1 executed'