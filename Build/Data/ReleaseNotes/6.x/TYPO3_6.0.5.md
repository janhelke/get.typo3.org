Release Notes for TYPO3 6.0.5
=============================

This document contains information about TYPO3 version 6.0.5 which was
released on May 3rd, 2013.

News
----

This release is a bug fix release.

Notes
-----

This is a combined release of TYPO3 CMS 4.5.26, 4.7.11 and 6.0.5.

Download
--------

<https://typo3.org/download/>

MD5 checksums
-------------

    266a46064648faa00145efaffada4aae  blankpackage-6.0.5.tar.gz
    07c171c8caa7d77d425b4f28606e8924  blankpackage-6.0.5.zip
    593025ee397dc5a0b917805d541aeb58  dummy-6.0.5.tar.gz
    e02dd712dc795a41352b3f25a4b38fa2  dummy-6.0.5.zip
    96768a1efe6f65e500ac19a6f66d7035  typo3_src+dummy-6.0.5.zip
    b37620d591d57332e1791bdcf1bd4396  typo3_src-6.0.5.tar.gz
    85b6e5b92cb59358826d08f082dfb64c  typo3_src-6.0.5.zip

Upgrading
---------

The [usual upgrading
procedure](https://docs.typo3.org/typo3cms/InstallationGuide/) applies.
No database updates are necessary.

Changes
-------

Here is a list of what was fixed since [6.0.4](TYPO3_6.0.4 "wikilink"):

    2013-05-03  a9f6ab6                  [RELEASE] Release of TYPO3 6.0.5 (TYPO3 Release Team)
    2013-05-02  044c30e  #43735          [TASK] Reduce severity for set_no_cache() from core (Georg Ringer)
    2013-05-01  23187dd  #38879          [BUGFIX] InlineSettings broken if extJs not loaded (Benjamin Mack)
    2013-04-30  63a6f54                  [TASK] Raise submodule pointer (TYPO3 Release Team)
    2013-04-29  ea23451  #42901          [BUGFIX] Filter for groups not working after revisit (Wouter Wolters)
    2013-04-29  13ca597  #47681          [BUGFIX] Revert abusive deprecation (Francois Suter)
    2013-04-28  c01a7ba  #47621          [TASK] Update URLs to documentation (Wouter Wolters)
    2013-04-27  0965bda  #47529          [BUGFIX] Empty columns in Page Module view cause warnings (Christian Zenker)
    2013-04-27  742932a                  [TASK] Raise submodule pointer (Anja Leichsenring)
    2013-04-25  0918bd9                  [TASK] Raise submodule pointer (TYPO3 Release Team)
    2013-04-22  a8d4bac                  [TASK] Set TYPO3 version to 6.0-dev (TYPO3 Release Team)
    2013-04-22  1687956                  [RELEASE] Release of TYPO3 6.0.5rc1 (TYPO3 Release Team)
    2013-04-22  5bddd9a                  [TASK] Raise submodule pointer (TYPO3 Release Team)
    2013-04-22  295a327  #47449          [BUGFIX] Incomplete mock raises PHP 5.4 warning (Christian Kuhn)
    2013-04-22  c18160e  #47409          [BUGFIX] Select label element from suggest-list (Stefan Neufeind)
    2013-04-22  780e7dd  #47274          [BUGFIX] RTE: Tab key in Chrome inserts weird SPAN tags (Stanislas Rolland)
    2013-04-20  61c5e9b  #40731          [BUGFIX] Suggest wizard: Display record icon (Nicole Cordes)
    2013-04-19  977bb0a  #45254          [BUGFIX] excludeUidList not checked for ifsub state (Frederik Vosberg)
    2013-04-14  c9a27c2  #47140          [BUGFIX] ProcessedFile/Thumbnail is always regenerated (Oliver Hader)
    2013-04-14  00c8f0c  #47145          [BUGFIX] TypoScript stripProfile not forwarded to ProcessedFile (Oliver Hader)
    2013-04-13  4150527  #47189          [BUGFIX] Catch correct exception if file has been removed (Georg Ringer)
    2013-04-13  7790b12                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-04-13  c40805d  #36793          [TASK] Add/drop usage of preg_quote() where needed (Stefan Neufeind)
    2013-04-13  5facaea  #47184          [BUGFIX] Inefficient cache handling in LocalizationFactory (Christian Kuhn)
    2013-04-13  c82d918                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-04-13  8b7ff01                  [BUGFIX] Language cache is not cleared anymore (Oliver Hader)
    2013-04-13  75d4261  #47181          [BUGFIX] Empty clear cache command logged (Oliver Hader)
    2013-04-13  3439e95  #46205          [BUGFIX] Cache file could not be written on concurrent actions (Oliver Hader)
    2013-04-13  6d7fc2d                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-04-13  4062234  #38600          [BUGFIX] Fix Non-static method tslib_cObj::calc() (Wouter Wolters)
    2013-04-13  f5ddbf6  #38601          [BUGFIX] Fix Non-static method tslib_cObj::getKey() (Wouter Wolters)
    2013-04-13  0847df3  #38602          [BUGFIX] Fix Non-static method tslib_cObj::enableFields() (Wouter Wolters)
    2013-04-13  a701005                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-04-12  246b13e  #44484          [BUGFIX] Don't set empty from-name when sending email (Stefan Neufeind)
    2013-04-12  f0c8f89                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-04-12  1c58b86  #21288          [BUGFIX] Flash uploader doesn't work in Filelist clickmenus (Lorenz Ulrich)
    2013-04-12  919ccff                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-04-12  b907308  #47160          [TASK] Remove last mentions of t3lib_formmail (Christian Kuhn)
    2013-04-12  90c3038  #46278          [BUGFIX] Deprecate forgotten t3lib classes (Christian Kuhn)
    2013-04-12  832551b  #47157          [BUGFIX] Namespace forgotten t3lib_formmail (Christian Kuhn)
    2013-04-12  86b3560                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-04-10  e9520d5  #39248          [BUGFIX] Make fetchUserRecord callable without username (Robert Heel)
    2013-04-09  ca9df6e  #47082          [BUGFIX] Correct naming of TYPO3 database backend test (Christian Kuhn)
    2013-04-09  05b55cc                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-04-09  a9d3a5b  #15771          [BUGFIX] Numeric check for upper/lower bound of flexform-values (Anja Leichsenring)
    2013-04-07  e710f62  #47007          [BUGFIX] File collection should request update after changing the storage (Philipp Gampe)
    2013-04-07  f11699d  #42223          [BUGFIX] Images from non-local storages are not displayed (Steffen Ritter)
    2013-04-07  a4abc47  #46274          [BUGFIX] EM: add visual feedback for download+install (Felix Kopp)
    2013-04-07  68a113b  #47012          [BUGFIX] Function buildUrl does not handle port setting (Nicole Cordes)
    2013-04-07  7dde3eb  #42996          [BUGFIX] Adjust category exception message to namespaces (Benjamin Mack)
    2013-04-07  1eec6dc  #46596          [BUGFIX] IndexerService does not set creating user (Steffen Ritter)
    2013-04-07  8065390  #46965          [BUGFIX] Illegal string offset in EditDocumentController (Philipp Gampe)
    2013-04-06  1b284b7  #38705          [BUGFIX]  Hide move placeholder in WS preview (Benjamin Mack)
    2013-04-06  efd4292  #46435          [TASK] Small clean up in the page tree code (Dmitry Dulepov)
    2013-04-06  879da98  #46999          [BUGFIX] Write config to extTables destroys HTML output (Philipp Gampe)
    2013-04-06  35fd78e  #47002          [BUGFIX] Warning in getCompressedTCarray due to missing extTables.php (Philipp Gampe)
    2013-04-06  8ebc9ae  #46853          [TASK] Move code for clearing text fields to jquery plugin (Jost Baron)
    2013-04-06  d7ed7bd  #45467          [BUGFIX] Fix wrong string formatting (Fabien Udriot)
    2013-04-06  51fca3f  #46996          [BUGFIX] EM ConstantsView crashs with dep/faulty types. (Alexander Opitz)
    2013-04-06  d0f802c  #43291          [BUGFIX] BE login form gives warnings in RteHtmlParser (Jigal van Hemert)
    2013-04-06  938b504  #46997          [TASK] Sort version column enabled as default (Anja Leichsenring)
    2013-04-06  458c00f  #46977          [BUGFIX] EM: sorting in dataTable incorrect (Wouter Wolters)
    2013-04-06  f56233e  #42106          [BUGFIX] swiftmaileradapter should ignore empty headers (Stefan Neufeind)
    2013-04-06  ed988a8  #45221          [BUGFIX] Fix processed files if original has special chars (Helmut Hummel)
    2013-04-06  34f30db  #46983          [BUGFIX] EM manual links open in the same window (Philipp Gampe)
    2013-04-06  8efa2f6  #46984          [BUGFIX] BackendUtility::calcAge returns negative value for 0 (Nicole Cordes)
    2013-04-06  47dcd13  #46976          [TASK] EM: remove nested pagination in showAllVersions (Felix Kopp)
    2013-04-06  c46f2a9  #45748          [BUGFIX] Get folder object if a path is given (Ivan Kartolo)
    2013-04-06  1433faf  #46979          [BUGFIX] EM: increased visual significance of Upload .t3x (Felix Kopp)
    2013-04-06  91fe224  #46588          [BUGFIX][EM] Fix failing unit tests (Christian Kuhn)
    2013-04-06  d871648  #46978          [BUGFIX] EM: show versions link to read manual (Felix Kopp)
    2013-04-06  679641e  #46958          [BUGFIX] EM: configuration view CSS corrections (Felix Kopp)
    2013-04-06  aa502f9  #43241          [BUGFIX] saltedpasswords not installed by default (Nicole Cordes)
    2013-04-06  a96cd0a  #46972          [BUGFIX] Fix phpdoc after namespacing (Philipp Gampe)
    2013-04-06  5422a0a  #46967          [BUGFIX] EM: reduce prominence of state column (Felix Kopp)
    2013-04-06  52f3bf1  #46971          [TASK] EM: easy access to showAllVersions (Felix Kopp)
    2013-04-06  c56ecf9                  Revert "[BUGFIX] Throw Exception if typo3 extension repository is not defined" (Christian Kuhn)
    2013-04-06  4d44159  #46444          [BUGFIX] Sorting of file links CE is broken (Nicole Cordes)
    2013-04-06  cffa4fd  #46586          [BUGFIX] Automatic creation of processed files folder fails (Andreas Wolf)
    2013-04-06  c4733a0  #46962          [BUGFIX] Extension Manager does not use calcAge (Benjamin Mack)
    2013-04-05  5cc0580  #46573          [BUGFIX][EM] Fix of last update time after update (Jost Baron)
    2013-04-05  59f9963  #46524          [TASK][EM] More readable "time since last update"-strings (Jost Baron)
    2013-04-05  c6319f1  #45245          [BUGFIX] EM: Update button -> display version (Thomas Löffler)
    2013-04-05  c24f31b  #42849          [BUGFIX] Throw Exception if typo3 extension repository is not defined (Sascha Egerer)
    2013-04-05  f38e2e6  #46021,#46953   [BUGFIX] EM: Colorpicker in extension configuration is broken (Wouter Wolters)
    2013-04-05  adb2097  #46955          [BUGFIX] EM: fix state columns' CSS (Felix Kopp)
    2013-04-05  e467e39  #46582          [BUGFIX] Read permission check for folders is broken (Nicole Cordes)
    2013-04-05  f007375  #46605          [BUGFIX] RTE: Magic Images are put in root folder (Benjamin Mack)
    2013-04-05  422550f  #28741          [BUGFIX] Respect line breaks in stdWrap.cropHTML (Alexander Stehlik)
    2013-04-05  edb9fd3  #44288          [FEATURE] Add delete button in file list (Benjamin Mack)
    2013-04-05  90733dd  #45703          [BUGFIX] respect rootLevel=-1 in exec_foreign_table_where_query (Stefan Froemken)
    2013-04-05  335831f  #46948          [TASK] EM: Remove contentWrap container (Felix Kopp)
    2013-04-05  da8f1e3  #46951          [TASK] EM: Add title to "Show all versions" icon (Wouter Wolters)
    2013-04-05  278a0ed  #46575          [BUGFIX] Error in filelist for Storage context menu (Nicole Cordes)
    2013-04-05  bef89a6  #46949          [BUGFIX] Add version title in showAllVersion view (Anja Leichsenring)
    2013-04-05  5b8035f  #39919          [TASK] EM: extension info within "Get Extensions" (Felix Kopp)
    2013-04-05  725e630  #46941          [BUGFIX] Move EM extension configuration save button to DocHeader (Anja Leichsenring)
    2013-04-05  d5bc670  #46938          [BUGFIX] EM: Add return link to showAllVersions (Felix Kopp)
    2013-04-05  842cd76  #46934          [TASK] EM: Modules deserve headlines (Felix Kopp)
    2013-04-05  a925e5b  #46931          [BUGFIX] Move EM tabs to function menu (Felix Kopp)
    2013-04-05  2f22b9d  #46942          [TASK] EM: Remove search form in showAllVersions (Felix Kopp)
    2013-04-05  c79eeb3  #33651          [BUGFIX] Fix breaking t3editor by using hsc() (Georg Ringer)
    2013-04-05  3a56664  #46591          [BUGFIX] Caching framework tables depends on ext_tables.sql (Nicole Cordes)
    2013-04-05  b8c3d45  #45928          [BUGFIX] Extension manager styling (Felix Kopp)
    2013-04-05  7765942  #26753          [BUGFIX] List module shows thumbs on CEs of type text (Mario Rimann)
    2013-04-03  f3e5fff  #39135          [BUGFIX] Let Upgrade wizard recognize $GLOBALS['TYPO3_CONF_VARS'] (Anja Leichsenring)
    2013-04-02  bfd6b78                  [TASK] Raise submodule pointer (TYPO3 Release Team)
    2013-04-02  1da7354  #43382          [TASK] Optimize clearing file backend caches (Oliver Hader)
    2013-04-01  c05fe21                  [TASK] Remove explicit strict test from TypoScriptParserTest (Oliver Hader)
    2013-04-01  91783bd  #46795          [!!!][BUGFIX] Scope of ProcessedFile cannot be modified (Oliver Hader)
    2013-04-01  0fe3945  #46839          [TASK] Integrate basic TypoScript parsing test (Oliver Hader)
    2013-04-01  fa2c8b2                  [TASK] Adapt ArrayConstraints in IndexerTest (Steffen Ritter)
    2013-04-01  2f72201  #45982          [BUGFIX] PHP filesystem functions are locale dependent (Steffen Ritter)
    2013-04-01  3d64329  #24582          [BUGFIX] Accept alternative notations for setDBinit (Michael Stucki)
    2013-04-01  66dc994  #36719          [BUGFIX] Javascript for TMENU_LAYERS and GMENU_LAYERS missing (Michael Stucki)
    2013-03-31  46cde8a  #46821          [TASK] Detect APC and APCu correctly (Stefan Neufeind)
    2013-03-31  c8714f0  #44485          [BUGFIX] Sending fails on multiple email-addresses (Stefan Neufeind)
    2013-03-31  18c28be  #46373          [BUGFIX] Fix of Close-button in flash messages (Jost Baron)
    2013-03-31  ab1f90d  #46817          [TASK] WincacheBackend: Add a "Testing"-context to the tests (Stefan Neufeind)
    2013-03-30  cfd53f6  #46768          [BUGFIX][Cache] Wincache backend class constructor (Christian Kuhn)
    2013-03-28  106cd20  #46530          [!!!][BUGFIX] Crop-Scaled images have wrong file content type (Oliver Hader)
    2013-03-27  dddf13d  #46535          [BUGFIX] Image rendering of non-existing files throws exception (Oliver Hader)
    2013-03-27  1c9901f  #46718          [BUGFIX] Wrong variable name used (Georg Ringer)
    2013-03-27  8e9d7f9  #45805          [TASK] Increase Web>List title column width (Felix Kopp)
    2013-03-27  11553c8  #46568          [BUGFIX] Subfolders must use the identifier as identifier (Georg Ringer)
    2013-03-27  1bcedde  #46555          [BUGFIX] Settings for local drivers are not shown by default (Nicole Cordes)
    2013-03-27  b139de7  #46532          [BUGFIX] Title includes html tags (Nicole Cordes)
    2013-03-26  3edbf52                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-03-26  2e35142  #43410          [BUGFIX] Remove needless "x " on TER-search (Stefan Neufeind)
    2013-03-26  7279443  #46584          [BUGFIX] Segfaults on object comparisons (Andreas Wolf)
    2013-03-26  d7c25af                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-03-26  6646e4f  #46250          [BUGFIX] Exception with EXT:sys_note is installed (Oliver Hader)
    2013-03-25  3bfe200  #45162          [BUGFIX] Extbase Plugin for Indexed Search not working (Matthias Nitsch)
    2013-03-24  57d3c1a                  [TASK] Fix failing unit tests for LocalDriver (Andreas Wolf)
    2013-03-24  7607382  #46497          [BUGFIX] FAL Upgrade Wizards do not set pid (Benjamin Mack)
    2013-03-24  43b2b7b  #46604          [BUGFIX] Default upload folder should be user_upload/ (Benjamin Mack)
    2013-03-24  8be37d5  #46603          [BUGFIX] Folder Tree does not respect _temp_ and _recycler_ (Benjamin Mack)
    2013-03-24  883e92e  #46587          [BUGFIX] Resource storage does not emit signals (Andreas Wolf)
    2013-03-23  6e7769c  #46564          [BUGFIX] Copy and move folders between storages is broken (Nicole Cordes)
    2013-03-23  58d76c8  #36792          [BUGFIX] Update sys_refindex to reflect typolink to file in RTE content (Benjamin Mack)
    2013-03-22  dcd60aa  #44732          [BUGFIX] fallbackRendering is always called (Simon Schaufelberger)
    2013-03-22  7d95aa3                  [TASK] Small cleanup in Boostrap.php (Michael Stucki)
    2013-03-22  64226f1  #46541          [BUGFIX] Sorting files in filelist is case sentive (Nicole Cordes)
    2013-03-20  3418d4d  #45140          [BUGFIX] Fix .zip-export on windows and add unit test (Jost Baron)
    2013-03-20  7218ab0  #46075          [BUGFIX] ExtDirectApi uses an undefined variable (Dmitry Dulepov)
    2013-03-19  a8117c0  #36405          [BUGFIX] Usage of deprecated returnFilemounts() (Markus Klein)
    2013-03-19  027ba83  #46077          [BUGFIX] BELog module error: "vsprintf(): Too few arguments" (Dmitry Dulepov)
    2013-03-18  1387046  #43186          [TASK] Use minimised version of jquery.dataTables-1.9.4 (Stefan Neufeind)
    2013-03-18  d632c28                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-03-18  b9d7fea  #41280          [BUGFIX] Media element not working with FAL (Andreas Schütte)
    2013-03-17  fa0b04c  #46361          [BUGFIX] Fix PHP warning in BackendUtility::lockRecords (Helmut Hummel)
    2013-03-16  e64683c  #46292          [BUGFIX] HMENU rendering uses old tslib_ class names (Christian Kuhn)
    2013-03-16  7718387  #25292          [BUGFIX] Make sure XML parser is created everytime when needed (Christian Kuhn)
    2013-03-16  a3936a7                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-03-15  0d5119f  #46115          [BUGFIX] Importing extensions from repository fails (Christian Kuhn)
    2013-03-15  6f4b778  #31953          [BUGIFX] Extra output block backend thumbnails (Francois Suter)
    2013-03-15  1484023  #45833          Revert "[BUGFIX] Fix wrong column title in web>list for field colpos" (Christian Kuhn)
    2013-03-15  333ced6                  [TASK] Raise submodule pointer (Christian Kuhn)
    2013-03-14  8b7b603  #44672          [BUGFIX] LanguageController has "mixed" type annotations (Wouter Wolters)
    2013-03-14  70587c5  #46267          [BUGFIX] Skip unreliable APC test on PHP versions below 5.3.4 (Christian Kuhn)
    2013-03-14  2859391  #46264          [BUGFIX] Add .htaccess file to ext:extensionmanager/Resources/Private (Christian Kuhn)
    2013-03-14  2db1c48  #45795          [BUGFIX] Toolbar items with separator: fix white-space (Felix Kopp)
    2013-03-14  746bac8  #44626          [BUGFIX] Numeric translation keys aren't translated right in XML files (Reinhard Führicht)
    2013-03-13  082208c  #39127          [BUGFIX] Translation of a form makes the form wizard unusable (Mario Rimann)
    2013-03-13  35c038b  #43906          [BUGFIX] Exception when deleted file is in clipboard (Andreas Wolf)
    2013-03-13  171761f  #45319          [BUGFIX] inject* methods in FAL inhibit use of Extbase object manager (Andreas Wolf)
    2013-03-12  71686a8                  [TASK] Raise submodule pointer (TYPO3 Release Team)
    2013-03-11  4e65a12  #46155          [BUGFIX] Old files of filelist extension are wrong (Wouter Wolters)
    2013-03-11  0ea503a  #46030          [TASK] Show better error messages on failed TER update (Jost Baron)
    2013-03-11  561822a  #46029          [TASK] Make the update-from-TER link more visible (Jost Baron)
    2013-03-11  072e438  #46158          [BUGFIX] Handle symlink on extension update (Philipp Gampe)
    2013-03-11  0c5cd69  #46160          [TASK] More descriptive error message on file upload failure (Philipp Gampe)
    2013-03-10  0d0a17b  #46161          [BUGFIX] Correct check for extTables script (Francois Suter)
    2013-03-08  ad96958  #45887          [BUGFIX] Typo in sys_log TCA (Christian Kuhn)
    2013-03-08  3570c57  #46119          [BUGFIX] Wrong cmd example in INSTALL.txt (Markus Klein)
    2013-03-08  3986b9f  #45135          [BUGFIX] Install Tool: Error message gives wrong info (Thomas Löffler)
    2013-03-08  970a33b  #45826          [BUGFIX] Fix SQL syntax (Michael Stucki)
    2013-03-08  64f5f36  #36597          [BUGFIX] Allow Setting colorspace in the Install Tool. (Anja Leichsenring)
    2013-03-07  ffb9347  #43361          [BUGFIX] Deactivating "install" extension leads to exceptions (Wouter Wolters)
    2013-03-07  3a2844e  #36904,#26141   [BUGFIX] RTE: Empty paragraphs are not correctly transformed (Stanislas Rolland)
    2013-03-07  4973b07  #45595          [BUGFIX] Clearing cache from toolbar fails in IE8 (Andreas Kießling)
    2013-03-07  51cae9e  #44454          [BUGFIX] pageNotFound_handling never happens (Thorben Kapp)
    2013-03-07  e11d541  #46074          [BUGFIX] ExtensionManagementUtility tries to include non-existing files (Dmitry Dulepov)
    2013-03-07  c266e22  #46085          [TASK] Update copyright year to 2013 (Ernesto Baschny)
    2013-03-07  a0e7582  #46085          [TASK] Update copyright year to 2013 (Ernesto Baschny)
    2013-03-07  c33f974                  [TASK] Set TYPO3 version to 6.0.5-dev (TYPO3 Release Team)
    2013-03-07  92844e8                  [RELEASE] Release of TYPO3 6.0.4 (TYPO3 Release Team)


