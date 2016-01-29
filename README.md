# Block Visibility Helper Object

## Installation
1. Enable this module.

## Example usage in the block visibility form:

    <?php
    if (class_exists('BlockVisibility')) {
      $obj = new BlockVisibility();
      $obj->show_if_nid(4391);
      $obj->show_if_alias('rss-feeds');
      $obj->hide_if_alias('library', 'library/browse');
      $obj->show_if_alias_regex('/^library\/.+/');
      
      return $obj->isVisible();
    }


In the above example there are four rules.  The first rule to match will be returned by `isVisible()`.  The first rule determines the default value; if the first rule is show then the default will be the opposite and will be used if no rules match.
