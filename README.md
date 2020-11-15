# Ludwig Tumor Atlas

This project contains the source files for the Ludwig Tumor Atlas website.  The site is built using Jekyll, and is structured such that it can be rendered directly in GitHub to display within their GitHub Pages site hosting service.

## Structural Overview

The site (as currently stands) is comprised of 6 Collections:
- **pages** - These provide the content for the top-level pages of the website.  Pages are gathered within the collection for organizational purposes, so that the source files are not left 'loose' at the root of the site.
- **datasets** - These entries provide the source content for the items in the *Data* section of the website, as well as the *Featured Data* module on the homepage.
- **projects** - These provide the content for the *Projects* section of the website.
- **publications** - These provide the content for the *Publications* section of the website. At a minimum, entries should contain front matter that can be used to populate the publication list on the Publications landing page.  They can also contain body content, which can then be displayed as a standalone summary page for the publication.
- **people** - These entries provide the source content for the items in the *People* section of the website.  No standalone pages are build for these items, but body content is displayed within the People landing page list.
- **graphics** - These entries are used whenever a graphic with captioning needs to be displayed.  Each item in the graphics collection has a title assigned, an image, and then body copy which can be marked up as needed, and rendered out as part of the graphic element.

## Image Processing

The site makes use of the [imgix](https://www.imgix.com/) image processing service.  This means that in most cases, the author can upload non-sized images, and the sizing will be managed automatically for them.  The exception to this is if an image is specified directly in the body content of a page, without the use of a *graphic* entry.  In those cases, care should be taken to ensure the image is optimized for web delivery.

## Data Files

The site currently makes use of three data files (contained in the *_data* directory), which can be edited as needed as the site grows over time:
- **menus.yml** - This contains the structure for the main site navigation. Note the use of the *section_id* value.  This is used to trigger menu highlighting for sub-pages within a given section.
- **people.yml** - The *people* entries are grouped on the People landing page according to location.  The locations are specified in the ***people.yml*** file, and the *key* value is assigned to the entries in the *people* collection to form their location associations.
- **publications.yml** - The *publications* entries are grouped by their associated *groups* on the Publications landing page. The groups are specified in the ***publications.yml*** file, and the *key* value is assigned to the entries in the *publications* collection to form their group associations.

## Collection Details

Below is information about the front matter options for each of the site's collections:

### pages ###
- title - The page title (used for SEO purposes)
- permalink - The path to the page
- section_id - Maps to the *section_id* values found in the *menus.yml* file
- layout - Specifies the template for the page (generally should not need to change)