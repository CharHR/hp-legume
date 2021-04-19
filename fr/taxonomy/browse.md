---
layout: documentation
sideNavigation: fr.sidenav.taxonomy
title: Browse
permalink: /fr/taxonomy/browse
description: Lorem markdownum spatium limes indefessus neque at orat aestuat
klass: fullwidth
lang-ref: species-browse
---

<!--react and gbif component-->
<script src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
<script src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>

<script src="https://cdn.jsdelivr.net/gh/CatalogueOfLife/portal-components@{{site.col.version}}/umd/col-browser.min.js" ></script>

<div id="tree"></div>

<script>
'use strict';
const e = React.createElement;
class Tree extends React.Component {

    render() {

      return e(
        ColBrowser.Tree,
        { 
          catalogueKey: '{{site.col.catalogueKey}}',
          pathToTree: '/fr/taxonomy/browse',
          pathToSearch: '/fr/taxonomy/search',
          pathToTaxon: '/fr/taxonomy/taxon/',
          defaultTaxonKey: '{{site.col.defaultTaxonKey}}',
          citation: 'top'
        }
      );
    }
  }

const domContainer = document.querySelector('#tree');
ReactDOM.render(e(Tree), domContainer);
</script>