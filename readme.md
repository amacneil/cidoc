Cidoc Sphinx theme
==================

[Sphinx](http://sphinx.pocoo.org/) is an open-source documentation generator. This means you can
write your documentation in [ReStructuredText](http://docutils.sourceforge.net/docs/user/rst/quickstart.html)
format, and easily generate HTML or PDF output. It simplifies documenting your projects, and helps keep
presentation of your documentation separate from your design.

The Cidoc theme is designed to add a consistent style to [CodeIgniter](http://codeigniter.com/)
and [ExpressionEngine](http://expressionengine.com/) documentation. It was forked from the
original [eldocs theme](https://github.com/EllisLab/CodeIgniter/tree/develop/user_guide_src/source/_themes/eldocs)
included with the official CodeIgniter release, and is licensed under the [Open Software License v3.0](http://www.opensource.org/licenses/OSL-3.0).

The reason for moving this to a separate project is that the eldocs theme included with CodeIgniter
is very specific to EllisLab's needs. This theme is designed to be customizable, and can be used
on any project.

Usage
-----

To use the cidoc theme in your projects, simply include it as a submodule. For example, assuming your
Sphinx documentation is stored in `user_guide_src/`, you could add the theme to your project using
the following commands:

	mkdir user_guide_src/_themes
	git submodule add git@github.com:adrianmacneil/cidoc.git user_guide_src/_themes/cidoc

Then make sure you include the following lines in your `user_guide_src/conf.py` file:

	html_theme_path = ['_themes']
	html_theme = 'cidoc'

Customization
-------------

The Cidoc theme is designed to be completely customizable for your project, while retaining a consistent
style that your users are familiar with. To pass options to the theme, you must add the following code to
your `user_guide_src/conf.py` file:

	html_theme_options = {
		# theme options are added to this array, in the format
		# "option_name": "option_value"
	}

The following options are currently available:

* `sitesearch_url`: The URL which Google Site Search in the top right of your documentation will use. If left blank, Google Site Search will not appear.

More theme options will be added in future versions.
