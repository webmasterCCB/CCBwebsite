---
layout: default
title: Carnegie Hall 2026
---

<div class="carnegie-page">

  <!-- SECTION 1: WE DID IT -->
  <section class="carnegie-section hero-section">
    <h1>We Did It!</h1>
    <p class="intro-text">We played in Carnegie Hall</p>
    <p>On June 28, 2026, Classic City Band took the stage at one of the world's most prestigious concert venues. It was a dream realized, a moment our musicians will never forget, and a testament to the power of community, dedication, and support.</p>
  </section>

  <!-- SECTION 2: DONORS -->
  <section class="carnegie-section donors-section">
    <h2>Donors Are Amazing!</h2>
    <p>We are so blessed to have the support of the Athens-Clarke County community. Thank you so much! We did it!</p>
  </section>

  <!-- SECTION 3: PHOTO GRID -->
  <section class="carnegie-section">
    <h2>Moments from Carnegie Hall (more to come!)</h2>
    <div class="photo-grid">
      <div class="photo-item" onclick="openLightbox(0)">
        <figure>
          <img src="{{ '/assets/images/carnegie-1.jpg' | relative_url }}" alt="Beautiful, venerable Carnegie Hall from the street." style="max-width: 350px; height: auto;">
          <figcaption>Beautiful, old Carnegie Hall from the street.</figcaption>
        </figure>
      </div>
      <div class="photo-item" onclick="openLightbox(1)">
        <figure>
          <img src="{{ '/assets/images/carnegie-2.jpg' | relative_url }}" alt="A photo of Classic City Band members waiting to go in the stage door of Carnegie Hall. Taken on July 28, 2026 by David Floyd" style="max-width: 350px; height: auto;">
          <figcaption>We are lined up here for our Sunday morning rehearsal. Feeling excited and ready to see the inside in person for the first time (and oh gosh it was beautiful!)</figcaption>
        </figure>
      </div>
      <div class="photo-item" onclick="openLightbox(2)">
        <figure>
          <img src="{{ '/assets/images/carnegie-3.jpg' | relative_url }}" alt="Photo from the stage inside Carnegie Hall of Michael Brewer, conductor of the Classic City Band. Taken by David Floyd July 28, 2026" style="max-width: 350px; height: auto;">
          <figcaption>Michael Brewer prepares us for rehearsal.</figcaption>
        </figure>
      </div>
      <div class="photo-item" onclick="openLightbox(3)">
        <figure>
          <img src="{{ '/assets/images/carnegie-4.jpg' | relative_url }}" alt="Photo of a 'you are here' poster outside Carnegie Hall." style="max-width: 350px; height: auto;">
          <figcaption>"You are here." Yes, we were!</figcaption>
        </figure>
      </div>
    </div>
  </section>

</div>

<!-- LIGHTBOX MODAL -->
<div id="lightbox" class="lightbox">
  ...rest of lightbox code...
</div>
