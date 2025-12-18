# magento2-weltpixel-fullpagescroll

### Installation

Dependencies:
 - magento2-weltpixel-backend (see https://github.com/Weltpixel/magento2-weltpixel-backend)

With composer:

```sh
$ composer config repositories.welpixel-magento2-weltpixel-backend git https://github.com/Weltpixel/magento2-weltpixel-backend.git
$ composer require weltpixel/magento2-weltpixel-backend:dev-master

$ composer config repositories.welpixel-magento2-weltpixel-fullpagescroll git https://github.com/Weltpixel/magento2-weltpixel-fullpagescroll.git
$ composer require weltpixel/magento2-weltpixel-fullpagescroll:dev-master
```

Manually:

Important: Ensure you also install the shared Backend module. If it's already installed, you can skip this. Details in the repo at https://github.com/Weltpixel/magento2-weltpixel-backend.

Copy the zip into the app/code/WeltPixel/FullPageScroll directory

#### After installation by either means, enable the extension by running following commands:

```sh
$ php bin/magento module:enable WeltPixel_FullPageScroll --clear-static-content
$ php bin/magento setup:upgrade
```

### Documentation

For detailed documentation, please visit: https://weltpixel.com/resources/ModuleDoc/Magento2/FullPageScroll/User-Guide-WeltPixel-Full-Page-Scroll-Magento2.html


<hr/>
Insert in all desired with FullPageScroll CMS Pages following content
 
 ```
 {{block class="WeltPixel\FullPageScroll\Block\FullPageScroll" name="fullpagescroll" template="WeltPixel_FullPageScroll::fullpagescroll.phtml"}}
 ```
 <br/>
 Create each section as a CMS Block.
 <br/>
 CMS Block Identifier must have the following format:
 <br/>
 fullpagescroll_cmspageurlkey_sectionorder
 
 ```
 fullpagescroll_home_section1
 fullpagescroll_home_section2
 ```
 <br/>
 Each section created as a CMS Block can containe all type of content (text, images, ...).
 <br/>
 The first image from the CMS Block is always set as a background of current section and the rest of the images will be displayed as section content.
 
 <br/>
 <br/>
 The sections of a specific page will be displayed in alphabetical order based on CMS Block <strong>Identifier</strong> name
