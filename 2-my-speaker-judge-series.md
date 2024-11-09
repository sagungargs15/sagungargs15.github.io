---
layout: default
title: "speaker-judge-series"
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Thumbnail Grid with Lightbox</title>
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
</head>
<body>

<div class="grid-container">
  <!-- Thumbnails (100 Images) -->
  <!-- Replace 'imageX.jpg' with actual image paths -->
  <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-1.jpeg" alt="Thumbnail 1" onclick="openLightbox('image1.jpg')">
  <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-2.jpeg" alt="Thumbnail 2" onclick="openLightbox('image2.jpg')">
  <!-- Repeat the above line for each image up to 100 -->
  <!-- Example below up to 10, just duplicate to make 100 total -->
  <img src="image3.jpg" alt="Thumbnail 3" onclick="openLightbox('image3.jpg')">
  <img src="image4.jpg" alt="Thumbnail 4" onclick="openLightbox('image4.jpg')">
  <img src="image5.jpg" alt="Thumbnail 5" onclick="openLightbox('image5.jpg')">
  <img src="image6.jpg" alt="Thumbnail 6" onclick="openLightbox('image6.jpg')">
  <img src="image7.jpg" alt="Thumbnail 7" onclick="openLightbox('image7.jpg')">
  <img src="image8.jpg" alt="Thumbnail 8" onclick="openLightbox('image8.jpg')">
  <img src="image9.jpg" alt="Thumbnail 9" onclick="openLightbox('image9.jpg')">
  <img src="image10.jpg" alt="Thumbnail 10" onclick="openLightbox('image10.jpg')">
  <!-- Continue adding images up to 100 thumbnails -->
</div>

<!-- Lightbox Overlay -->
<div class="lightbox-overlay" id="lightboxOverlay">
  <span class="close-btn" onclick="closeLightbox()">&times;</span>
  <img id="lightboxImage" src="" alt="Large View">
</div>

<script>
  // Function to open lightbox with selected image
  function openLightbox(imageSrc) {
    document.getElementById('lightboxImage').src = imageSrc;
    document.getElementById('lightboxOverlay').style.display = 'flex';
  }

  // Function to close lightbox
  function closeLightbox() {
    document.getElementById('lightboxOverlay').style.display = 'none';
  }
</script>

</body>
</html>


## Speaking/Judge Series: Sagun Garg

A. **May 2024**: Sagun has been nominated as a Speaker at Bitcoin Asia Hong Kong conference: Topic of Miniscript: Future of Inheritance in Bitcoin

B.**Jan 2024**: Nominated as Judge for Tenity incubator in Singapore for selecting various startups, Inriskable was shortlisted for the name screening & source of wealth use case in the private bank space, a proof of concept within the Bank Julius Baer Innovation Lab in the Singapore office

C.**Sep 2023**: I mentored an incoming batch of entrepreneurs at Tenity, in Zurich Switzerland with a master class on Venture Capital and Entrepreneurship. Ran a masterclass for batch of 50+ Entrepreneurs on the Topic

D.**June 2023**: I was nominated as round 1 Judge of AI in Finance Hackcelerator SG competition, conducted by MAS, for various startups. I closely worked with KOK Li Wen for evaluations at Fintech & Innovation Group of MAS

   here..more to be updated soon