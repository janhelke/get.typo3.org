Release Notes for TYPO3 4.4
===========================

This document contains information about TYPO3 version 4.4 which was
released on June 22, 2010.

Notes
-----

Find more details in the [4.4 Release
Notes](https://typo3.org/download/release-notes/typo3-44/).

Download
--------

<https://typo3.org/download/>

MD5 checksums
-------------

    4dd74797de492d9d8c234f7394c089a8  dummy-4.4.0.tar.gz
    07630d2dee1732bd78a7175baff1c19e  dummy-4.4.0.zip
    665b1a28ad1dfecd07ffef799f54fc52  typo3_src-4.4.0.tar.gz
    fb386311ab6e8485d7314d72cd4fb84e  typo3_src-4.4.0.zip
    e8cb99173e3281187a6e503f109f503a  typo3_src+dummy-4.4.0.zip
    9db5f7c868f5492b7ed50f744c484adb  introductionpackage-4.4.0.zip

Upgrading
---------

The usual upgrading procedure applies: After exchanging the TYPO3
source, make sure to run the upgrade procedures of the Database Analyzer
and the Update Wizard in the Install Tool. After this, delete all
`temp_*` files in `typo3conf/`; otherwise the Backend might look
completely unstyled.

Please have a look at the [upgrade wizard](Upgrade "wikilink"), if you
have any questions.

News
----

    ************************************************************************
    CHANGES & IMPROVEMENTS between TYPO3 4.3 and 4.4
    (for technical details see ChangeLog)
    ************************************************************************

    === General ===

        * Versioning: "Page" and "Branch" versioning has been disabled for all
          installations, because it is deprecated since TYPO3 4.2. If you still
          use one of these versioning types, make sure to set
          $TYPO3_CONF_VARS['BE']['elementVersioningOnly'] = FALSE in your
          localconf.php. Please be aware that this option will vanish with
          TYPO3 4.6 and that "Page" and "Branch" versioning is neither supported
          nor maintained any longer.

        * Versioning: The dummy "draft workspace" has been disabled for all
          installations. If you need it you can enable it again in the
          extension configuration of the "version" extension.

        * All CSS and JS files in the TYPO3 Backend are compressed now. This
          means that they are added up to a single file without unnecessary
          whitespace. This will reduce the count of requests drastically, which
          eventually leads to faster loading and better performance.
          CAUTION: If compressionLevel is configured
          ($TYPO3_CONF_VARS[TYPO3_MODE]['compressionLevel'] = 1 [1-9 for compression
          level or TRUE for "enabled"]) the files will be served with gzip compression.
          Be sure to enable / uncomment the needed configuration in your .htaccess file,
          also found in misc/advanced.htaccess.

            <FilesMatch "\.js\.gzip$">
              AddType "text/javascript" .gzip
            </FilesMatch>
            <FilesMatch "\.css\.gzip$">
              AddType "text/css" .gzip
            </FilesMatch>
            AddEncoding gzip .gzip

          IMPORTANT: If you have any trouble accessing the Backend after upgrading
          to TYPO3 4.4, make sure to clear the typo3temp/ directory manually or through
          the TYPO3 install tool.

        * There is now a complete new Backend skin for all backend modules,
          the login screen and the install tool. It is still called "t3skin",
          however due to the use of icon sprites and the refactoring of the
          CSS files, it is not possible anymore to run the TYPO3 Backend
          with the old backend skin (from 3.x) or with the look and feel from
          previous 4.x versions.
          If you have not installed any skins in your system, you will now see
          a completely unstyled TYPO3 Backend, no unneeded additional styles
          are loaded.

        * The static templates for some basic designs, that were part of the
          TYPO3 Core since TYPO3 3.5 are now moved to a system extension that
          is not included by default. If you are using one of these templates
          (GLUECK, GREEN, CANDIDATE etc) or one of the old table-based layouts
          for rendering content (like content (default) or plaintext rendering),
          make sure to install the system extension ("statictemplate") via the
          Install Tool.

        * The RTE has undergone major changes as UI components have been transformed
          into ExtJS widgets:
            1. The RTE framework becomes an ExtJS Panel comprising the toolbar,
               the iframe, the textarea and the status bar. All components
               are ExtJS objects.
            2. When BE textareas are resizable, the framework is resizable as
               a whole. In the FE, the framework is always resizable.
            3. The toolbar dropdowns become ExtJS ComboBoxes.
            4. The context menu becomes a configurable ExtJS Menu.
            5. Color palettes become ExtJS ColorPalettes.
            6. All dialogue windows become ExtJS windows.

        * The install tool is visually refactored and updated. It has now a
          different look and feel when accessing from outside the TYPO3 Backend
          and from within to be integrated better in the rest of the Backend.
          Also, the 1-2-3 installer process is now cleaned up to be in sync with
          the new UI elements. There is also a new hook in the installing
          process that allows to add or modify the existing steps in the
          installer to add more configuration options to a custom TYPO3 installation.

        * The task center module and all its components like Actions and Notes
          has undergone a complete refactoring, both visually and code-wise,
          and now has a clean API to add more elements to it.

        * Automatic version-numbers of CSS and JS files to avoid caching problems:
          This feature provides automatic numbering of CSS and JS files using the
          files modified timestamp. This way the file reference will change when a
          CSS or JS files is changed, and by this the browser and proxy will re-cache
          the file. This feature can be configured to include the timestamp within the
          filename (before .ext) or as a parameter to the file (default).
          If versioning is done directly inside the filename (by setting
          $TYPO3_CONF_VARS[BE][versionNumberInFilename] = TRUE) you need the
          following line as the first rewrite rule in .htaccess:

            # Rule for versioned static files (see $TYPO3_CONF_VARS[BE][versionNumberInFilename])
            RewriteCond %{REQUEST_FILENAME} !-f
            RewriteCond %{REQUEST_FILENAME} !-d
            RewriteRule ^(.+)\.(\d+)\.(php|js|css|png|jpg|gif|gzip)$ $1.$3 [L]

          IMPORTANT: This rule has to be the very first rule to work properly,
          at least it has to be placed before the "^typo3..." rewrite rule
          Developers can use this API for versioning of files in their own backend mods,
          by calling t3lib_div::createVersionNumberedFilename or using the core API
          for including files in the page renderer class.

        * Support for GDlib 1.x was completely dropped. Only GDlib 2.x is supported now,
          which is bundled with most PHP installations.

        * HTML5 is now officially supported. For the Frontend output simply use
          these two TypoScript lines in your Setup:

            config.doctype = html_5
            config.xmlprologue = none

          Backend modules also allow HTML5 configuration, simply choose the doktype:

            $this->doc->docType = 'html_5';


    === Backend ===

        * The TYPO3 Backend was moved into an ExtJS Viewport. This is one of the
          first steps in a sequence to ExtJSify the complete Backend. Currently
          this gives you the possibility to create your own left sidebar,
          like the page tree, in your backend modules. Also you can extend the
          viewport easily with own code to create e.g. a collapsable module menu.
          More information can be found in the TYPO3 Wiki and the official ExtJS
          viewport documentation. See these links:

            https://wiki.typo3.org/TYPO3Viewport
            http://www.extjs.com/deploy/dev/docs/

        * Inline Records (IRRE Elements) are now loaded on demand, meaning only when
          they are opened. This should speed up the editing process drastically.

        * The t3editor code completion DB was updated to reflect the latest additions.
          Also the syntax highlighting engine is now extracted from the system extension
          so it can be used in other places of the TYPO3 Core as well.

        * A donation notice will be shown to administrators in the TYPO3 Backend
          on login after using TYPO3 for more than three months. This behaviour
          can be disabled completely - see $TYPO3_CONF_VARS[BE][allowDonateWindow].

        * Most Icons used in the TYPO3 Backend are now rendered through so-called
          sprites. Instead of loading many image tags with single icons and therefore
          many http requests there are now only 6 sprite images (a sprite image is a
          big image with all icons included) that need to be loaded in the Backend.
          Image-tags got replaced by spans using the big sprite images with background
          and offset functionality. This reduces the HTTP and fileheader overhead of
          about 90% which results in a blasting fast Backend. For details about the
          new Icon Sprite API, have a look at t3lib/class.t3lib_iconworks.php.

        * The "bigButtons" (Edit page properties, Move page, ...) in the Page module
          are now disabled by default to have a cleaner interface. The old
          behavior can be restored by setting mod.web_layout.disableBigButtons = 0
          in UserTSconfig or PageTSconfig.

        * The interface "backend_old" was completely removed. This was the BE interface
          from 4.1. As it wasn't maintained and didn't worked correct, all references
          are removed, so remaining interfaces for login are backend and frontend.

        * The extension manager option "Enable extensions without review (basic security
          check)" was completely removed as most extensions in TER weren't reviewed on
          a regular basis. Thus, when searching for an extension in TER through the
          Extension Manager, all matching extensions, not regarding the review state,
          are shown up.

    === Frontend ===

        * Indexed search no longer puts a double wrap around search rules in the
          advanced search form. This may require style changes if a default indexed
          search is used.

        * The system extensions "CSS Styled Content" (css_styled_content) and
          "Frontend User Login" (felogin) now have new manuals that reflect the
          current state of the extension.

        * The browser condition in TypoScript now delivers reliable information
          about the client browser. So now it's possible to make a condition
          for usage of Firefox, or even a webkit based browser.


    === Compatibility ===

        * Extbase: has been updated to support "Single Table Inheritance" which is
          a breaking change. In TYPO3 4.3, Extbase made a "best guess" for the table
          name if it was not the lowercased class name (simply by crawling the class
          hierarchy upwards trying to find a mapping rule or table). This "magic"
          was removed because It was very hard to understand what was happening;
          especially if there was an error. This behaviour is now changed and you
          define the recordType and the tableName through TypoScript now. See the
          typo3.projecty.typo3v4mvc mailing list for more details on this topic.

        * Extbase: Template filenames are expected to be UpperCamelCased from now on.
          Before, they were expected to be all lowercase. For a grace period there
          is still a fallback mechanism, so that your old template filenames will
          still work. But you should rename your templates from "myaction.html"
          to "MyAction.html" to make sure, that it still works in upcoming versions
          of Fluid!  A message to the deprecation log is generated in case an "old"
          template name is found.

        * Support for GDlib 1.x was completely dropped, only GDlib 2.x is supported,
          which is bundled with most PHP installations.

        * Versioning: "Page" and "Branch" versioning has been disabled for all
          installations, because it is deprecated since TYPO3 4.2. If you still
          use one of these versioning types, make sure to set
          $TYPO3_CONF_VARS['BE']['elementVersioningOnly'] = FALSE in your
          localconf.php. Please be aware that this option will vanish with
          TYPO3 4.6 and that "Page" and "Branch" versioning is neither supported
          nor maintained any longer.


    === Development ===

        * In t3lib_extMgm there is now a way to retrieve the version of an
          extension through the method getExtensionVersion($extensionKey).

        * t3lib_div now provides the constants LF, CR, CRLF and TAB which can be
          used to improve code readability.

        * The ExtDirect specification was implemented in the Backend of TYPO3.
          You can use it in your own backend modules. Details about the specification
          can be found in the TYPO3 Wiki and on the ExtJS site.
          See the links:

            https://wiki.typo3.org/ExtDirect
            http://www.extjs.com/products/js/direct.php

        * There are new hooks available for you to use: t3lib_page::getRecordOverlay,
          t3lib_page::getPageOverlay, several new hooks in the impexp extension,
          alt_doc::makeEditForm() to enable further access-restrictions,
          in tslib_fe::settingLanguage(), in tslib_content, and in tslib_menu for
          further filtering of menu items

        * The newly introduced Flash messages in TYPO3 4.3 are now also available
          as JavaScript messages done by ExtJS and available in the global
          TYPO3 backend JS space.

        * There is now a new API for sending emails. t3lib_utility_Mail::mail()
          serves as a proxy for the PHP mail() function, and is now the recommended
          way for sending emails, in order to have a central place to use a
          different mailing engine.

        * The debug in the TYPO3 Backend was enhanced. There is a new debug console,
          which will show each debug in a single tab. The console will pop up
          as soon a debug statement is present.

        * t3lib_div::debug(): Removed the feature of passing an integer
          as $header (second argument) to add multiple br-tags.

        * There is a new API in place to generate HTML <span> tags with corresponding
          CSS classes in order to display previously created sprite images in
          the right background position. Make sure to have a look at
          "t3lib_iconWorks::getSpriteIconForRecord($table, $row)",
          "t3lib_iconWorks::getSpriteIconForFile('myimage.png')", and
          "t3lib_iconWorks::getSpriteIcon('actions-document-open')".


    === TypoScript changes ===

        * It is now possible to configure an alternative "parameter" for filelinks
          when using jumpURLs


    === DBAL ===

        * It is now possible to use the 1-2-3 installer process to configure a
          website running MSSQL, Oracle or PostgreSQL as TYPO3 database. TYPO3
          automatically detects available database drivers and presents them in
          a convenient driver dropdown list.


    === Backend skin ===

        * There is now a complete new Backend skin for all backend modules,
          the login screen and the install tool. It is still called "t3skin",
          however due to the use of icon sprites and the refactoring of the
          CSS files, it is not possible anymore to run the TYPO3 Backend
          with the old backend skin (from 3.x) or with the look and feel from
          previous 4.x versions.
          If you have not installed any skins in your system, you will now see
          a completely unstyled TYPO3 Backend, no unneeded additional styles
          are loaded.

        * CSS files in the TYPO3 Backend are now separated in structure
          CSS statements (definitions for margin, padding, width, height) and
          visual (like formatting colors, fonts, border and backgrounds).

        * Skins now have to register themselves by adding an entry
          $TBE_STYLES['skins'][$_EXTKEY]. By default, all CSS files from
          subdirectories stylesheets/structure/ and stylesheets/visual/ are
          included, additional directories can be added by setting
          $TBE_STYLES['skins'][$_EXTKEY]['stylesheetDirectories'].

        * Most Icons used in the TYPO3 Backend are now rendered through so-called
          sprites. Instead of loading many image tags with single icons and therefore
          many http requests there are now only 6 sprite images (a sprite image is a
          big image with all icons included) that need to be loaded in the Backend.
          Image-tags got replaced by spans using the big sprite images with background
          and offset functionality. This reduces the HTTP and fileheader overhead of
          about 90% which results in a blasting fast Backend. For details about the
          new Icon Sprite API, have a look at t3lib/class.t3lib_iconworks.php.


