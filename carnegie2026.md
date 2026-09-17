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

<!-- SECTION 3: PHOTO GALLERY -->
<section class="carnegie-section carnegie-gallery-section">
  <h2>Moments from Carnegie Hall</h2>

  <div class="carnegie-gallery">

    <!-- MAIN IMAGE VIEWER -->
    <div class="gallery-viewer">
      <button class="gallery-arrow gallery-prev"
              type="button"
              onclick="prevGalleryImage()"
              aria-label="Previous image">
        &#10094;
      </button>

      <img
        id="gallery-main-image"
        src="{{ '/assets/images/carnegie001.jpg' | relative_url }}"
        alt="Classic City Band at Carnegie Hall, photo 1 of 14">

      <button class="gallery-arrow gallery-next"
              type="button"
              onclick="nextGalleryImage()"
              aria-label="Next image">
        &#10095;
      </button>
    </div>

    <!-- THUMBNAILS -->
    <div id="gallery-thumbnails" class="gallery-thumbnails"></div>

  </div>
</section>

<style>
  .carnegie-gallery {
    width: 100%;
    margin: 0 auto;
  }

  .gallery-viewer {
    position: relative;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #111;
    overflow: hidden;
  }

  #gallery-main-image {
    display: block;
    max-width: 100%;
    max-height: 85vh;
    width: auto;
    height: auto;
    object-fit: contain;
    margin: 0 auto;
  }

  .gallery-arrow {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    z-index: 2;

    width: 52px;
    height: 72px;
    border: 0;
    border-radius: 4px;

    background: rgba(0, 0, 0, 0.45);
    color: white;
    font-size: 36px;
    line-height: 1;
    cursor: pointer;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  .gallery-arrow:hover,
  .gallery-arrow:focus {
    background: rgba(0, 0, 0, 0.75);
  }

  .gallery-prev {
    left: 12px;
  }

  .gallery-next {
    right: 12px;
  }

  .gallery-thumbnails {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 8px;
    margin-top: 12px;
  }

  .gallery-thumbnail {
    width: 100px;
    height: 70px;
    padding: 0;
    border: 3px solid transparent;
    background: none;
    cursor: pointer;
    opacity: 0.7;
    overflow: hidden;
  }

  .gallery-thumbnail img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .gallery-thumbnail:hover {
    opacity: 1;
  }

  .gallery-thumbnail.active {
    border-color: #555;
    opacity: 1;
  }

  @media (max-width: 600px) {
    .gallery-arrow {
      width: 42px;
      height: 60px;
      font-size: 28px;
    }

    .gallery-prev {
      left: 5px;
    }

    .gallery-next {
      right: 5px;
    }

    .gallery-thumbnail {
      width: 75px;
      height: 55px;
    }
  }
</style>

<script>
  const galleryImages = [
    "{{ '/assets/images/carnegie001.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie002.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie003.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie004.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie005.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie006.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie007.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie008.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie009.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie010.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie011.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie012.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie013.jpg' | relative_url }}",
    "{{ '/assets/images/carnegie014.jpg' | relative_url }}"
  ];

  let currentGalleryIndex = 0;

  const mainGalleryImage = document.getElementById("gallery-main-image");
  const thumbnailContainer = document.getElementById("gallery-thumbnails");

  function showGalleryImage(index) {
    currentGalleryIndex =
      (index + galleryImages.length) % galleryImages.length;

    mainGalleryImage.src = galleryImages[currentGalleryIndex];
    mainGalleryImage.alt =
      "Classic City Band at Carnegie Hall, photo " +
      (currentGalleryIndex + 1) +
      " of " +
      galleryImages.length;

    document.querySelectorAll(".gallery-thumbnail").forEach((thumbnail, index) => {
      thumbnail.classList.toggle("active", index === currentGalleryIndex);
    });
  }

  function nextGalleryImage() {
    showGalleryImage(currentGalleryIndex + 1);
  }

  function prevGalleryImage() {
    showGalleryImage(currentGalleryIndex - 1);
  }

  // Build thumbnails automatically from the image list.
  galleryImages.forEach((src, index) => {
    const button = document.createElement("button");
    button.type = "button";
    button.className = "gallery-thumbnail";
    button.setAttribute("aria-label", "View photo " + (index + 1));

    const thumbnail = document.createElement("img");
    thumbnail.src = src;
    thumbnail.alt = "";
    thumbnail.loading = "lazy";

    button.appendChild(thumbnail);

    button.addEventListener("click", function() {
      showGalleryImage(index);
    });

    thumbnailContainer.appendChild(button);
  });

  // Keyboard navigation.
  document.addEventListener("keydown", function(event) {
    if (event.key === "ArrowRight") {
      nextGalleryImage();
    }

    if (event.key === "ArrowLeft") {
      prevGalleryImage();
    }
  });

  // Mark the first thumbnail as selected.
  showGalleryImage(0);
</script>
