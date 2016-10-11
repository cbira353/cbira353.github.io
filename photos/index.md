---
layout: photos
modified: 2016-09-26
images:
  - image_path: /images/archway.jpg
    title: Archway
  - image_path: /images/big-ferns.jpg
    title: Big Ferns
  - image_path: /images/ricefield.jpg
    title: Rice Field
  - image_path: /images/sprite.jpg
    title: Pan
  - image_path: /images/buddha.jpg
    title: Big Buddha
  - image_path: /images/japanese-banner.jpg
    title: Festival Banner
  - image_path: /images/japanese-lady.jpg
    title: Japanese Lady
  - image_path: /images/japanese-house.jpg
    title: Japanese House
  - image_path: /images/grasshopper2.jpg
    title: Grasshopper
  - image_path: /images/market.jpg
    title: Open Market
  - image_path: /images/rain.jpg
    title: Rain in the Tropics
  - image_path: /images/fall-in-bbrae.jpg
    title: Fall
  - image_path: /images/hongkong-cleaning.jpg
    title: Street Cleaning - Hong Kong
  - image_path: /images/hk-tugboat.jpg
    title: Hong Kong Tugboat
  - image_path: /images/enzo.jpg
    title: Enzo
---


<ul class="photo-gallery">
  {% for image in page.images %}
    <img src="{{ image.image_path }}" alt="{{ image.title}}">{{ image.title}}
  {% endfor %}
</ul>