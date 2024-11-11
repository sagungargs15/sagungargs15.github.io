---
layout: default
---

<style>
    /* Grid Container */
    .grid-container {
      display: grid;
      grid-template-columns: repeat(10, 1fr);
      gap: 5px;
      max-width: 100%;
      margin: auto;
    }
    
    /* Thumbnail Styling */
    .grid-container img {
      width: 100%;
      height: auto;
      cursor: pointer;
      transition: transform 0.2s;
    }

    /* Hover Effect */
    .grid-container img:hover {
      transform: scale(1.05);
    }

    /* Lightbox Overlay */
    .lightbox-overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      justify-content: center;
      align-items: center;
      z-index: 10;
    }

    /* Lightbox Image */
    .lightbox-overlay img {
      max-width: 90%;
      max-height: 90%;
    }

    /* Close Button */
    .close-btn {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 30px;
      color: #fff;
      cursor: pointer;
    }
</style>


<div class="grid-container">
  <!-- Thumbnails (100 Images) -->
  <!-- Replace 'imageX.jpg' with actual image paths -->
  <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-1.jpeg" alt="Thumbnail 1" onclick="openLightbox(1)">
  <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-2.jpeg" alt="Thumbnail 2" onclick="openLightbox(2)">
  <!-- Repeat the above line for each image up to 100 -->
  <!-- Example below up to 10, just duplicate to make 100 total -->
  <!-- <img src="image3.jpg" alt="Thumbnail 3" onclick="openLightbox(3)">
  <img src="image4.jpg" alt="Thumbnail 4" onclick="openLightbox(4)">
  <img src="image5.jpg" alt="Thumbnail 5" onclick="openLightbox(5)">
  <img src="image6.jpg" alt="Thumbnail 6" onclick="openLightbox(6)">
  <img src="image7.jpg" alt="Thumbnail 7" onclick="openLightbox(7)">
  <img src="image8.jpg" alt="Thumbnail 8" onclick="openLightbox(8)">
  <img src="image9.jpg" alt="Thumbnail 9" onclick="openLightbox(9)">
  <img src="image10.jpg" alt="Thumbnail 10" onclick="openLightbox(10)"> -->
  <!-- Continue adding images up to 100 thumbnails -->
</div>

<!-- Lightbox Overlay -->
<div class="lightbox-overlay" id="lightboxOverlay">
  <span class="close-btn" onclick="closeLightbox()">&times;</span>
  <img id="lightboxImage" src="" alt="Large View">
</div>

<script>
  // Store the images in an array
  const images = document.querySelectorAll('.scroll-container img');
  let currentImageIndex = 0;
  let isLightboxOpen = false;

  // Open the lightbox with the clicked image
  function openLightbox(index) {
    currentImageIndex = index;  // Set the current index to the clicked image
    var lightbox = document.getElementById('lightbox');
    var lightboxImg = document.getElementById('lightbox-img');
    
    // Set the clicked image's source to the lightbox image
    lightboxImg.src = images[currentImageIndex].src;
    
    // Show the lightbox
    lightbox.style.display = 'flex';
    isLightboxOpen = true; // Mark lightbox as open
    
    // Disable background scroll when lightbox is open
    document.body.style.overflow = 'hidden';
  }

  // Close the lightbox
  function closeLightbox() {
    var lightbox = document.getElementById('lightbox');
    
    // Hide the lightbox
    lightbox.style.display = 'none';
    isLightboxOpen = false; // Mark lightbox as closed
    
    // Re-enable background scroll
    document.body.style.overflow = '';
  }

  // Change the image (backward or forward)
  function changeImage(direction) {
    // Calculate the next image index
    currentImageIndex = (currentImageIndex + direction + images.length) % images.length;
    
    var lightboxImg = document.getElementById('lightbox-img');
    lightboxImg.src = images[currentImageIndex].src;  // Update the lightbox image
  }

  // Add event listener for keyboard navigation
  document.addEventListener('keydown', function(event) {
    if (isLightboxOpen) {
      event.preventDefault(); // Prevent default arrow key behavior (e.g., scrolling)
      
      if (event.key === 'ArrowRight') {
        changeImage(1); // Go to next image
      } else if (event.key === 'ArrowLeft') {
        changeImage(-1); // Go to previous image
      } else if (event.key === 'Escape') {
        closeLightbox(); // Close the lightbox when Escape is pressed
      }
    }
  });
</script>

## Speaking/Judge Series: Sagun Garg

A. **May 2024**: Sagun has been nominated as a Speaker at Bitcoin Asia Hong Kong conference: Topic of Miniscript: Future of Inheritance in Bitcoin

B.**Jan 2024**: Nominated as Judge for Tenity incubator in Singapore for selecting various startups, Inriskable was shortlisted for the name screening & source of wealth use case in the private bank space, a proof of concept within the Bank Julius Baer Innovation Lab in the Singapore office

C.**Sep 2023**: I mentored an incoming batch of entrepreneurs at Tenity, in Zurich Switzerland with a master class on Venture Capital and Entrepreneurship. Ran a masterclass for batch of 50+ Entrepreneurs on the Topic

D.**June 2023**: I was nominated as round 1 Judge of AI in Finance Hackcelerator SG competition, conducted by MAS, for various startups. I closely worked with KOK Li Wen for evaluations at Fintech & Innovation Group of MAS

   here..more to be updated soon