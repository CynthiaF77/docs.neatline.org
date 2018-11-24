---
layout: default
---

# Bulk-importing Omeka Items

So far, we've manually created individual Neatline records and associated them with items in the Omeka collection. But what if you already have an existing collection of hundreds or thousands of items? Instead of manually creating Neatline records for each of the items individually, you can just bulk-import part or all of the collection into a Neatline exhibit:

  1. Go to the main exhibits browse page and find the listing for the exhibit.

  2. Click the "Import Omeka Items" link under the exhibit title.

## Defining an item query

This takes you to the item import form. Think of this as a "search" form - you can use any of the available inputs to define a "query" on the Omeka archive that determines which items will be imported into the exhibit. For example, if you have a large archive with multiple collections, you might just be interested in working with one individual collection, and don't want to clutter up the Neatline exhibit with all of the other unrelated items. The fields here work just like the corresponding options in the Omeka advanced search form:

  - Use **Search by a Range of IDs** to specify an individual ID (not so useful) or a range of IDs (more useful), and all items with IDs that fall within the specified range will be imported. This is a good way to import the entire collection all at once - just enter in an indiscriminate query like "1-1000," which, as long as you have fewer than 1,000 items in your collection, will import all the items on the site. This is fine for experimentation, but in the long run, we generally recommend slicing and dicing the items into groups with collections or tags, which often prevents content management problems down the road.

  - Use **Search By Collection** to import to items in a given collection.

  - Use **Search By Type** to import items of a given type

  - Use **Search By Tags** to constrain the import to items that are tagged with **all** of the listed tags.

(Keep in mind that the fields are `AND`'ed together, not `OR`'ed - so, if you select a collection and enter a tag, the import will only match items that are _both_ in the collection _and_ have the tag.)

Once you've defined a search query, click "Import Items" to kick off the import. You'll be taken back to the exhibit's browse page, and you'll see a success notification saying that "The item import was successfully started!"

**Important**: Behind the scenes, this actually kicks off a "background process" that does the heavy lifting of importing the items. This is necessary because it can sometimes take up to 30-40 seconds to import really large collections of items (many thousands), and the process can fail if the web request times out (smaller imports, up to about 1,000 items, will generally finish in just a couple of seconds). When you're first redirected to the exhibits browse view, though, the "# Items" counter for the exhibit will probably still be the same as it was before, since the import was started at the same moment that you were redirected. Refresh the page, though, and you'll see the effect of the background process as it fills in the items.

## What happens if you add new items?

When the import is finished, open the editor for the exhibit. You'll see new listings for all of the records that were matched by the import. When you open the edit form for one of the records, you'll see that the "Omeka ID" field is populated with the ID of a corresponding Omeka item and that the "Title" and "Body" fields are populated with the item title and metadata output. Just as if the records had been manually linked to their parent items, any change to the items will be propagated to the imported records.

But what if you then continue to add new Omeka items to the collection that _would have_ been matched by the original import, and want to synchronize the Neatline exhibit with the new collection of items? Neatline expects this, and makes it easy - if you go back to the "Import Omeka Items" form for the exhibit, you'll see that the original query has been saved, making it possible to re-run the identical query over and over again. When you run the query, **Neatline will never duplicate an existing item-backed record in an exhibit**, meaning that only the newly-added items will be imported.

For example, imagine you import a collection that has 100 items. Later, you add another 20 items to the collection. If you want to vacuum up those new items into the Neatline exhibit, you can just re-run the same import query, and Neatline will _only_ import the 20 new records and ignore the other 100 items that already have corresponding records in the collection.
