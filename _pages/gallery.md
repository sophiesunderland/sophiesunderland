---
title: "Gallery"
layout: page
permalink: /gallery/
---

<div class="photo-grid">

<div>
  <img src="/images/IMG_4774.jpg" alt="Luangwa, Zambia">
  <p>Luangwa, Zambia</p>
</div>

<div>
  <img src="/images/IMG_4541.jpg" alt="Luangwa, Zambia">
  <p>Mosi-oa-Tunya National Park</p>
</div>

<div>
  <img src="/images/IMG_4405.jpg" alt="Luangwa, Zambia">
  <p>Kamwala market, Zambia </p>
</div>

<div>
  <img src="/images/IMG_1298.jpg" alt="Luangwa, Zambia">
  <p>Kalandula Falls, Angola</p>
</div>

</div>

<style>
.photo-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 30px;
}

.photo-grid figure {
  background: white;
  padding: 12px;
  padding-bottom: 20px;
  box-shadow: 0 4px 12px rgba(0,0,0,.15);
  transform: rotate(-1deg);
}

.photo-grid figure:nth-child(even) {
  transform: rotate(1deg);
}

.photo-grid img {
  width: 100%;
  aspect-ratio: 1/1;
  object-fit: cover;
}

.photo-grid figcaption {
  text-align: center;
 