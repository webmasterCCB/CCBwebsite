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
  <section class="carnegie-section donors-section">
      <h2>Donors Are Amazing!</h2>
      <p>We are so blessed to have the support of the Athens-Clarke County community. Thank you so much! We did it!</p>
    </section>
  </div>

  <!-- SECTION 2: PHOTO GRID -->
  <section class="carnegie-section">
    <h2>Moments from Carnegie Hall (more to come!)</h2>
      <div class="photo-item" onclick="openLightbox(0)">
        <figure>
          <img src="{{ '/assets/images/carnegie-1.jpg' | relative_url }}" alt="Beautiful, venerable Carnegie Hall from the street." style="max-width: 350px; height: auto;">
          <figcaption>Beautiful, old Carnegie Hall from the street.</figcaption>
        </figure>
      </div>
      <div class="photo-item" onclick="openLightbox(1)">
        <figure>
          <img src="{{ '/assets/images/carnegie-2.jpg' | relative_url }}" alt="A photo of Classic City Band members waiting to go in the stage door of Carnegie Hall. Taken on July 28, 2026 by David Floyd" style="max-width: 350px; height: auto;">>
          <figcaption>We are lined up here for our Sunday morning rehearsal. Feeling excited and ready to see the inside in person for the first time (and oh gosh it was beautiful!)</figcaption>
        </figure>
      </div>
      <div class="photo-item" onclick="openLightbox(2)">
        <figure>
          <img src="{{ '/assets/images/carnegie-3.jpg' | relative_url }}" alt="Photo from the stage inside Carnegie Hall of Michael Brewer, conductor of the Classic City Band. Taken by David Floyd July 28, 2026"style="max-width: 350px; height: auto;">
          <figcaption>Michael Brewer prepares us for rehearsal.</figcaption>
        </figure>
      </div>
      <div class="photo-item" onclick="openLightbox(3)">
        <figure>
          <img src="{{ '/assets/images/carnegie-4.jpg' | relative_url }}" alt="Photo of a 'you are here' poster outside Carnegie Hall."style="max-width: 350px; height: auto;">
          <figcaption>"You are here." Yes, we were!</figcaption>
        </figure>
      </div>
    </div>
  </section>

</div>

<!-- LIGHTBOX MODAL -->
<div id="lightbox" class="lightbox">
  <span class="lightbox-close" onclick="closeLightbox()">&times;</span>
  <span class="lightbox-prev" onclick="prevImage()">&#10094;</span>
  <span class="lightbox-next" onclick="nextImage()">&#10095;</span>
  <div class="lightbox-content">
    <img id="lightbox-image" src="" alt="">
    <div id="lightbox-caption"></div>
  </div>
</div>

<script>
  const images = [
    {
      src: "{{ '/assets/images/carnegie-1.jpg' | relative_url }}",
      caption: "Beautiful, venerable Carnegie Hall from the street."
    },
    {
      src: "{{ '/assets/images/carnegie-2.jpg' | relative_url }}",
      caption: "We are lined up here for our Sunday morning rehearsal. Feeling excited and ready to see the inside in person for the first time (and oh gosh it was beautiful!)"
    },
    {
      src: "{{ '/assets/images/carnegie-3.jpg' | relative_url }}",
      caption: "Michael Brewer prepares us for rehearsal."
    },
    {
      src: "{{ '/assets/images/carnegie-4.jpg' | relative_url }}",
      caption: '"You are here." Yes, we were!'
    }
  ];

  let currentImageIndex = 0;

  function openLightbox(index) {
    currentImageIndex = index;
    const lightbox = document.getElementById("lightbox");
    const img = document.getElementById("lightbox-image");
    const caption = document.getElementById("lightbox-caption");
    
    img.src = images[index].src;
    caption.textContent = images[index].caption;
    lightbox.style.display = "flex";
    document.body.style.overflow = "hidden";
  }

  function closeLightbox() {
    const lightbox = document.getElementById("lightbox");
    lightbox.style.display = "none";
    document.body.style.overflow = "auto";
  }

  function nextImage() {
    currentImageIndex = (currentImageIndex + 1) % images.length;
    const img = document.getElementById("lightbox-image");
    const caption = document.getElementById("lightbox-caption");
    img.src = images[currentImageIndex].src;
    caption.textContent = images[currentImageIndex].caption;
  }

  function prevImage() {
    currentImageIndex = (currentImageIndex - 1 + images.length) % images.length;
    const img = document.getElementById("lightbox-image");
    const caption = document.getElementById("lightbox-caption");
    img.src = images[currentImageIndex].src;
    caption.textContent = images[currentImageIndex].caption;
  }

  // Arrow key navigation
  document.addEventListener("keydown", function(event) {
    const lightbox = document.getElementById("lightbox");
    if (lightbox.style.display === "flex") {
      if (event.key === "ArrowRight") nextImage();
      if (event.key === "ArrowLeft") prevImage();
      if (event.key === "Escape") closeLightbox();
    }
  });

  // Close lightbox when clicking outside the image
  document.getElementById("lightbox").addEventListener("click", function(event) {
    if (event.target === this) closeLightbox();
  });
</script>
