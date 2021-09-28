Dokuwiki Plugin: Add New Sidebar
================================

Fork from the add new page plugin for Dokuwiki: https://www.dokuwiki.org/plugin:addnewpage

It is adapted just to hide the text form and always point to sidebar of namespace.

This is free software, released under the [GPL version 2](https://www.gnu.org/licenses/gpl-2.0-standalone.html).

## Syntax

    {{NEWSIDE[>namespace]}}

Where namespace is optional, and indicates the destination namespace for the new page.
If you give @NS@ or @PAGE@ as namespace, the namespace of the current page or the current page ID will be used.

## Styling

Inside `conf/userall.css`

    /* addnewsidebar */
    .addnewsidebar {
        position: absolute;
        right: 15px;
        top: 0px;
    }

## Example

Useful in combination with the newpagetemplate, here inside page `:musik`:

    {{NEWSIDE>:musik#tpl:tpl_sidebar}}

If there is a main `__template` like following with usage of include plugin, then a tree structur with listing of next level subpages can be achieved straight forward.

    {{NEWSIDE>:@ID@#tpl:tpl_sidebar}}
    ====== @PAGE@ ======
    {{page>:@ID@:sidebar&noheader&nofooter&noeditbutton}}

## Authors

- Originally written by [Benjamin Santalucia](https://github.com/ben8p) (aka iDo), 2006.
- Moved to Github by hamstar <hamstar@telescum.co.nz>, 2012.
- Updated by Sam Wilson <sam@samwilson.id.au>, 2013.
- Updated by Michael Braun <michael-dev@fami-braun.de>, 2013.
- Improved by Róbert Toth (FurloSK), 2013.
- Support for newpagetemplate added by Gerrit Uitslag <klapinklapin@gmail.com>, 2014.
- Disabling of restricted parent namespaces by Albert Chern, 2015.
- Default title is always sidebar by Christoph Strasser, 2021.
