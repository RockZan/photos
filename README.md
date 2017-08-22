How to Use:
* On the home page, there are three images which are put on rotation. These are called "slider images." If you go to the photos/img/slider/ folder, you can add or remove pictures for up to three pictures to use for your slider.
* When you redirect to the overall gallery page, you'll see different albums with pictures used to represent each album. If you go to the photos/gallery/albums/ folder, you can see the main pictures that are used to represent each album. These pictures will automatically be resized.
* If you go to the photos/gallery/archive/ folder, you'll see folders called "g01", "g02", etc. Each of these folders has all the photos for those respective albums. You will insert any photos you want in these folders.
* If you go to the photos/gallery/gallery01/ folder, you'll want to pay attention to these attributes at the section at the top of the page because these will be used to describe and reference an individual album:
    * title - The title you will see at the top of the page once you click on an album
    * description - The caption that will appear under the title (not the album-title)
    * album-title - The title of the album that you will see when you hover over the title on the main gallery page and what you will see at the top of the specific album page
    * images:
        * image_path - The path that will be used for an individual image
        * caption - The caption/description for a picture
* Now let's say you want to create a new gallery for pictures of cats. In order to do this, you must
    * 1) Add the main picture you would like to use for the album cover into photos/gallery/albums
    * 2) Create a folder in the photos/gallery/archive directory called "cats" with all your cat pictures
    * 3) Create a folder in the photos/gallery/ directory called "cats-gallery" or the like, and copy the index.html file from photos/gallery/gallery01 and paste it into "gallery04" file
    * 4) In the index.html section denoted by ---, if you had 3 cats pictures in the archive directory, you can edit it to look something like
    
    \---
    layout: page
    title: "Cats"
    description: "Cats Meow"
    active: gallery
    header-img: "img/gallery-bg.jpg"
    album-title: "Cats"
    images:
     \- image_path: /gallery/archive/cats/yellow-cat.jpg
       caption: A Yellow Cat
     \- image_path: /gallery/archive/cats/blue-cat.jpg
       caption: A Blue Cat
     \- image_path: /gallery/archive/cats/red-cat.jpg
       caption: A Red Cat
    \---
    
    * 5) Add to the index.html file and make it look like:
    
    \---
    layout: page
    title: "ALBUMS"
    description: ""
    active: gallery
    header-img: "img/gallery-bg.jpg"
    images:
     \- image_path: /gallery/albums/alb01.jpg
       gallery-folder: /gallery/gallery01/
       gallery-name: Cars
       gallery-date: July 2015
     \- image_path: /gallery/albums/P7290027.jpg
       gallery-folder: /gallery/gallery02/
       gallery-name: Dogs
       gallery-date: June 2015
     \- image_path: /gallery/albums/P8210107.jpg
       gallery-folder: /gallery/gallery03/
       gallery-name: Solar Eclipse
       gallery-date: August 2017
     \- image_path: /gallery/albums/main-cat-picture.jpg
       gallery-folder: /gallery/cats-gallery/
       gallery-name: Cats Gallery
       gallery-date: June 2099
    \---

**License**

The MIT License (MIT)

Copyright (c) 2014 Filippo Oretti, Dario Andrei

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

