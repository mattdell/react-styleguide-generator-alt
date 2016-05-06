# 3.5.2 (2016-05-06)
  * Adds json-loader to webpack loaders to handle json file types

# 3.5.1 (2016-03-30)
  * Fixes "show all" link issue when serving from sub-directory

# 3.5.0 (2016-02-21)
  * Add feature to give example components initial `props`

# 3.4.0 (2016-02-16)
  * Bumping previous commit to 3.4.0 instead of 3.3.1

# 3.3.1 (2016-02-16)
  * Removes 'vendor' feature from webpack config to allow npm2 compatibility.

# 3.3.0 (2016-02-15)

  * Bumps Babel to 6.5.2. Fixes #9. No more unnecessary semicolons enforcement.

# 3.2.2 (2016-02-05)

  * Filters components without `styleguide` field. Fixes #16: Fails if input files have no styleguide field

# 3.2.1 (2016-01-28)

  * patch version bump so npm shows the latest true version

# 3.2.0 (2016-01-28)

  * Fix issues with babel 6 found in
    * https://github.com/theogravity/react-styleguide-generator-alt/issues/12
    * https://github.com/theogravity/react-styleguide-generator-alt/issues/11

# 3.1.1 (2016-01-11)

  * Change hmr server hostname to 0.0.0.0 so we can use with vagrant/virtualbox

# 2.6.0, 3.1.0 (2016-01-07)

  * Allow passing a Javascript file for the `--config` option. This will allow usage of `webpackConfig` outside of using `gulp` or `grunt`
  * Note that babel 6.4 requires semicolons in your class properties https://github.com/feross/standard/issues/372; packages have been fixed to 6.3 for now due to conflicts with using `standard.

# 2.5.4, 3.0.2 (2015-12-13)

  * Fix "show all" link where it was not using the configured base (if used)

# 2.5.2, 3.0.1 (2015-12-13)

  * Fix syntax highlighting when individual components in the sidebar is selected
  * Adjust component category spacing
  * Add show all link on sidebar

# 3.0.0 (2015-12-13)

  * Support for babel 6. Use the 2.x versions for babel 5 support.

# 2.5.1 (2015-12-13)

  * Show components in each category in the sidebar

# 2.4.0 (2015-12-11)

  * Base exclusion `babel-loader` rule is no longer `path.resolve(process.cwd(), 'node_modules')`, but instead `node_modules`. This is mainly for projects that need to compile guides against directories that contain individually packaged components that have their own `node_modules` directory.

# 2.3.0 (2015-12-08)

  Performance enhancements:

  * separate vendor components into another bundle
  * Cache highlighted nodes so they are not re-processed. For really large pages, the highlighter can take a LOT of time for processing before the page is re-rendered. This fix hopefully resolves most of that.
  * `highlight.js` updated to `9.x`

# 2.2.0 (2015-12-01)

  * Add `webpackConfig` configuration file option to extend the rsg webpack configuration

# 2.1.1 (2015-12-01)

  * Fix issue where the props metadata file was not being written out if no propdocs were defined

# 2.1.0 (2015-11-30)

  * add `transpileIncludes` option to the config to allow for additional rules for babel transpiling

# 2.0.5 (2015-11-24)

  * Fix major bug as a result of renaming the package from fork

# 2.0.0 (2015-11-24)

  * First alt version, forked from `react-styleguide-generator`
  * Removed `browserify` and replaced with `webpack` + hot module replacement
  * Complete overhaul of the core `rsg.js` lib to support `webpack`
  * `react-docgen` generation and asset distribution moved to custom webpack plugins
  * Fixed a bug where using input text boxes and typing into them will shift focus to the search box
