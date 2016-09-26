---
layout: photos
modified: 2016-09-26
images:
  - image_path: /images/archway.jpg
    title: Archway
  - image_path: /images/big-ferns.jpg
    title: Big Ferns
  - image_path: /images/buddha.jpg
    title: Big Buddha
  - image_path: /images/japanese-banner.jpg
    title: Festival Banner
  - image_path: /images/japanese-lady.jpg
    title: Japanese Lady
  - image_path: /images/grasshopper.jpg
    title: Grasshopper
  - image_path: /images/japanese-house.jpg
    title: Japanese House
  - image_path: /images/market.jpg
    title: Open Market
  - image_path: /images/rain.jpg
    title: Rain in the Tropics
---


<ul class="photo-gallery">
  {% for image in page.images %}
    <li><img src="{{ image.image_path }}" alt="{{ image.title}}"/></li>
  {% endfor %}
</ul>