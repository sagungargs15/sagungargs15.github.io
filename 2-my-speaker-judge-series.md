---
layout: default
---

<style>

  /* Reset default margins and padding */
  h2, p, .tab-content {
    margin: 0;
    padding: 0;
  }

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
    /* width: 100%;
    height: auto;
    cursor: pointer; */
    width: 50px;
    height: 50px;
    cursor: pointer; /* Show that image is clickable */
    transition: transform 0.2s;
    margin-right: 5px; /* Spacing between images */
    border: 2px solid white; /* Border around images */
    border-radius: 5px; /* Optional: adds rounded corners */
    padding: 5px; /* Optional: space between image and border */
  }

  /* Hover Effect */
  .grid-container img:hover {
    transform: scale(1.05);
  }

  /* Lightbox Overlay */
  .lightboxthumbnail-overlay {
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
  .lightboxthumbnail-overlay img {
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

  .tab-container {
    display: flex;
    border-bottom: 2px solid #e0e0e0;
    padding: 0 16px;
    background-color: #f1f1f1;
  }

  /* Tab Styling */
  .tab {
    padding: 10px 20px;
    margin-right: 4px;
    cursor: pointer;
    color: #333;
    font-weight: 500;
    background-color: #e8e8e8;
    border: 1px solid #d0d0d0;
    border-bottom: none;
    border-radius: 8px 8px 0 0;
    transition: background-color 0.3s, color 0.3s;
  }

  .tab.active {
    color: white;
    background-color: #2F73BA; /* Matches blue color in the image */
    border-color: #2F73BA;
  }

  .tab:hover {
    background-color: #d9e8f8; /* Slightly lighter blue for hover effect */
  }

  /* Content container styling */
  .tab-content {
    display: none;
    padding: 20px;
    margin-bottom: 20px; /* Adjust this value to control spacing between sections */
  }

  .tab-content.active {
    display: block;
  }

  /* Scrollable container styles */
  .scroll-container {
    width: 100%;
    max-width: 100%;
    overflow-x: auto;
    white-space: nowrap;
    border: 1px solid white; /* Changed border color to white */
    padding: 10px; /* Added padding inside the container */
    margin-bottom: 10px; /* Adjust spacing between images */
  }

  .scroll-container img {
    width: 200px;
    height: 150px;
    object-fit: cover;
    display: inline-block;
    cursor: pointer; /* Show that image is clickable */
    margin-right: 10px; /* Spacing between images */
    border: 2px solid white; /* Border around images */
    border-radius: 5px; /* Optional: adds rounded corners */
    padding: 5px; /* Optional: space between image and border */
  }

  /* Lightbox container (hidden by default) */
  .lightbox {
    display: none; /* Hidden until clicked */
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8); /* Black background with transparency */
    justify-content: center;
    align-items: center;
    z-index: 1000; /* Ensure it appears above other elements */
  }

  /* Fullscreen image inside the lightbox */
  .lightbox img {
    max-width: 90%;
    max-height: 90%;
    object-fit: contain;
    box-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
  }

  /* Close button */
  .lightbox-close {
    position: absolute;
    top: 20px;
    right: 30px;
    font-size: 30px;
    color: white;
    cursor: pointer;
  }

  /* Navigation arrows */
  .arrow {
    position: absolute;
    top: 50%;
    font-size: 50px;
    color: black; /* Change arrow color to black */
    cursor: pointer;
    user-select: none;
    z-index: 1001;
  }

  .arrow-left {
    left: 30px;
  }

  .arrow-right {
    right: 30px;
  }

  .arrow:hover {
  color: gray; /* Changes arrow color when hovered */
  }

  /* Add this to your existing style section */
  .topic-badge {
    display: inline-block;
    background-color: #2F73BA; /* Matches your existing blue theme */
    color: white;
    padding: 8px 16px;
    border-radius: 20px;
    font-weight: 500;
    margin: 10px 0;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    font-size: 0.95em;
    letter-spacing: 0.3px;
  }

  .topic-badge:before {
    content: "📌 "; /* Adds a pin emoji before the topic */
  }
</style>

## Speaking/Judge Series: Sagun Garg

***

<div class="grid-container">
  <!-- Thumbnails (100 Images) -->
  <!-- Replace 'imageX.jpg' with actual image paths -->
 
  <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-gftn-elevandi-insights-building-trust-ai-era-1.png" alt="Thumbnail 1" onclick="openLightbox(0)">
  <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-gftn-elevandi-insights-building-trust-ai-era-2.png" alt="Thumbnail 2" onclick="openLightbox(1)">
  <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-carta-investor-hours-1.png" alt="Thumbnail 3" onclick="openLightbox(2)">
  <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-carta-investor-hours-2.png" alt="Thumbnail 4" onclick="openLightbox(3)">
  <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-custody-digital-assets-1.png" alt="Thumbnail 5" onclick="openLightbox(4)">
  <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-custody-digital-assets-2.png" alt="Thumbnail 6" onclick="openLightbox(5)">
  <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-institutional-demand-1.png" alt="Thumbnail 7" onclick="openLightbox(6)">
  <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-institutional-demand-2.png" alt="Thumbnail 8" onclick="openLightbox(7)"> 
  <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-1.png" alt="Thumbnail 9" onclick="openLightbox(8)">
  <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-interoperability-lightningconnect-hongkong-1.png" alt="Thumbnail 10" onclick="openLightbox(9)">

  <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-1.png" alt="Thumbnail 11" onclick="openLightbox(10)">
  <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-3.png" alt="Thumbnail 12" onclick="openLightbox(11)">
  <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-1.png" alt="Thumbnail 13" onclick="openLightbox(12)">
  <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-1.png" alt="Thumbnail 14" onclick="openLightbox(13)">
  <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-1.png" alt="Thumbnail 15" onclick="openLightbox(14)">
  
  <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-3.png" alt="Thumbnail 16" onclick="openLightbox(15)">
  <img src="https://sagungarg.com/assets/img/2024-sep-podcast-series-sagun-garg-onramp-mena-uae-september2024-bitcoin-ai-ml-hyperdeflation-hyperbitcoinization-2.png" alt="Thumbnail 17" onclick="openLightbox(16)">
  <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-sagun-garg-thailand-september2024-bitcoinconference-bangkok-2024-1.png" alt="Thumbnail 18" onclick="openLightbox(17)">
  <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-sagun-garg-singapore-september2024-bitcoinconference-weekoftoken2049-2024-1.png" alt="Thumbnail 19" onclick="openLightbox(18)">
  <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-1.png" alt="Thumbnail 20" onclick="openLightbox(19)">
  
  
  <img src="https://sagungarg.com/assets/img/2024-aug-guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-2.png" alt="Thumbnail 21" onclick="openLightbox(20)">
  <img src="https://sagungarg.com/assets/img/2024-aug-guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-2.png" alt="Thumbnail 22" onclick="openLightbox(21)">
  <img src="https://sagungarg.com/assets/img/2024-july-speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-1.png" alt="Thumbnail 23" onclick="openLightbox(22)">
  <img src="https://sagungarg.com/assets/img/2024-july-speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-2.png" alt="Thumbnail 24" onclick="openLightbox(23)">
  <img src="https://sagungarg.com/assets/img/2024-july-presenter-series-singapore-google-edb-ai-llm-genai-trailblazers-competition-1.png" alt="Thumbnail 25" onclick="openLightbox(24)">

  <img src="https://sagungarg.com/assets/img/2024-july-presenter-series-singapore-google-edb-ai-llm-genai-trailblazers-competition-2.png" alt="Thumbnail 26" onclick="openLightbox(25)">
  <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-1.png" alt="Thumbnail 27" onclick="openLightbox(26)">
  <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-2.png" alt="Thumbnail 28" onclick="openLightbox(27)">
  <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-singapore-students-business-school-sagungarg-bitcoin-digital-assets-1.png" alt="Thumbnail 29" onclick="openLightbox(28)">
  <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-singapore-students-business-school-sagungarg-bitcoin-digital-assets-2.png" alt="Thumbnail 30" onclick="openLightbox(29)">

  <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-bitcoin-as-new-reserve-asset-1.png" alt="Thumbnail 26" onclick="openLightbox(30)">
  <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-bitcoin-as-new-reserve-asset-2.png" alt="Thumbnail 27" onclick="openLightbox(31)">
  <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-web-festival-bitcoin-in-new-pizza-age-1.png" alt="Thumbnail 28" onclick="openLightbox(32)">
  <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-web-festival-bitcoin-in-new-pizza-age-2.png" alt="Thumbnail 29" onclick="openLightbox(33)">
  <img src="https://sagungarg.com/assets/img/2024-sep-guest-lecturer-university-nus-academia-lecture-investing-using-machine-learning-alternative-data-1.png" alt="Thumbnail 30" onclick="openLightbox(34)">

  <img src="https://sagungarg.com/assets/img/2024-july-presenter-series-singapore-google-edb-ai-llm-genai-trailblazers-competition-2.png" alt="Thumbnail 26" onclick="openLightbox(35)">
  <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-1.png" alt="Thumbnail 27" onclick="openLightbox(36)">
  <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-2.png" alt="Thumbnail 28" onclick="openLightbox(37)">
  <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-singapore-students-business-school-sagungarg-bitcoin-digital-assets-1.png" alt="Thumbnail 29" onclick="openLightbox(38)">
  <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-singapore-students-business-school-sagungarg-bitcoin-digital-assets-2.png" alt="Thumbnail 30" onclick="openLightbox(39)">

  
  <!-- Repeat the above line for each image up to 100 -->
  <!-- Example below up to 10, just duplicate to make 100 total -->
  <!-- <img src="image3.jpg" alt="Thumbnail 3" onclick="openLightbox(3)">
  <img src="image4.jpg" alt="Thumbnail 4" onclick="openLightboxThumbnail(4)">
  <img src="image5.jpg" alt="Thumbnail 5" onclick="openLightboxThumbnail(5)">
  <img src="image6.jpg" alt="Thumbnail 6" onclick="openLightboxThumbnail(6)">
  <img src="image7.jpg" alt="Thumbnail 7" onclick="openLightboxThumbnail(7)">
  <img src="image8.jpg" alt="Thumbnail 8" onclick="openLightboxThumbnail(8)">
  <img src="image9.jpg" alt="Thumbnail 9" onclick="openLightboxThumbnail(9)">
  <img src="image10.jpg" alt="Thumbnail 10" onclick="openLightboxThumbnail(10)"> -->
  <!-- Continue adding images up to 100 thumbnails -->
</div>

***

  <!-- Tab Navigation -->
  <!-- <div class="tab-container">
    <button class="tab-button" onclick="openTab(event, 'tab-btc')">Bitcoin</button>
    <button class="tab-button" onclick="openTab(event, 'tab-aiml')">AI/ML</button>
    <button class="tab-button" onclick="openTab(event, 'tab-fndr')">Founder</button>
    <button class="tab-button" onclick="openTab(event, 'tab-avc')">Angel/VC</button>
  </div> -->

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>April 2025: Web3 Festival in Hong Kong at the Bitcoin Stage</h2>
    <div class="topic-badge">Bitcoin as next global reserve asset</div>
    <div class="scroll-container">
      <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-bitcoin-as-new-reserve-asset-1.png" alt="Image 1" onclick="openLightbox(0)">
      <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-bitcoin-as-new-reserve-asset-2.png" alt="Image 2" onclick="openLightbox(1)">
      <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-bitcoin-as-new-reserve-asset-3.png" alt="Image 3" onclick="openLightbox(2)">
      <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-bitcoin-as-new-reserve-asset-4.png" alt="Image 4" onclick="openLightbox(3)">
      <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-bitcoin-as-new-reserve-asset-5.png" alt="Image 5" onclick="openLightbox(3)">
    </div>
  </div>  
---
  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>April 2025: Web3 Festival in Hong Kong at the Bitcoin Stage</h2>
    <div class="topic-badge">Bitcoin pizza in new Age</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-web-festival-bitcoin-in-new-pizza-age-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-web-festival-bitcoin-in-new-pizza-age-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-web-festival-bitcoin-in-new-pizza-age-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-web-festival-bitcoin-in-new-pizza-age-4.png" alt="Image 4" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2025-apr-hongkong-bitcoin-stage-web-festival-bitcoin-in-new-pizza-age-5.png" alt="Image 5" onclick="openLightbox(2)">
      </div>
  </div>  
---
  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>February 2025: Fintech Live Virtual Conference in Singapore</h2>
    <div class="topic-badge">Bitcoin and lightning payments is the new fintech?</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-singapore-fintech-live-conference-bitcoin-lightning-payments-new-fintech-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-singapore-fintech-live-conference-bitcoin-lightning-payments-new-fintech-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-singapore-fintech-live-conference-bitcoin-lightning-payments-new-fintech-3.png" alt="Image 3" onclick="openLightbox(2)">
      </div>
  </div>
---  
  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>February 2025: Digital Assets Week in Hong Kong after Consensus Conference Week</h2>
    <div class="topic-badge">Are Custody Providers Adequately Supporting the Needs of Tokenization</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-5.png" alt="Image 5" onclick="openLightbox(5)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-6.png" alt="Image 6" onclick="openLightbox(6)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-7.png" alt="Image 7" onclick="openLightbox(7)">
      </div>
  </div>  

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>February 2025: Bitcoin Lightning Connect Summit in Hong Kong during Consensus Conference Week</h2>
    <div class="topic-badge">Breaking Barriers: How Lightning Unlocks P2P Money</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-interoperability-lightningconnect-hongkong-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-interoperability-lightningconnect-hongkong-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-interoperability-lightningconnect-hongkong-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-interoperability-lightningconnect-hongkong-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-interoperability-lightningconnect-hongkong-5.png" alt="Image 5" onclick="openLightbox(4)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-interoperability-lightningconnect-hongkong-6.png" alt="Image 6" onclick="openLightbox(5)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-interoperability-lightningconnect-hongkong-7.png" alt="Image 7" onclick="openLightbox(6)">
      </div>
  </div>  


  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>January 2025: Halborn Digital Assets Security Summit at NYSE, New York, USA</h2>
    <p>"Enhancing DLT Security: Strategies for Risk, Compliance, and Financial Integrity"</p>
    <div class="topic-badge">Bitcoin as next global reserve asset</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-5.png" alt="Image 5" onclick="openLightbox(4)">
        <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-6.png" alt="Image 6" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-7.png" alt="Image 7" onclick="openLightbox(4)">
      </div>
  </div>  

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>December 2024: Bitcoin Institutional Day - Abu Dhabi, UAE</h2>
    <div class="topic-badge">Bitcoin Venture Capital and Private Equity</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-4.png" alt="Image 4" onclick="openLightbox(3)">
      </div>
  </div>  

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>December 2024: Bitcoin Institutional Day - Abu Dhabi, UAE</h2>
    <div class="topic-badge">Bitcoin the Real Fintech</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-as-fintech-abu-dhabi-financial-week-adfw-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-as-fintech-abu-dhabi-financial-week-adfw-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-as-fintech-abu-dhabi-financial-week-adfw-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-as-fintech-abu-dhabi-financial-week-adfw-4.png" alt="Image 4" onclick="openLightbox(3)">
      </div>
  </div>  

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>December 2024: Bitcoin MENA Conference in Abu Dhabi</h2>
    <div class="topic-badge">Building the Tools for Institutional Adoption: Hardware and Software</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-4.png" alt="Image 4" onclick="openLightbox(3)">
      </div>
  </div>  

  <div id="tab-aiml" class="tab-content" style="display: block;">  
    <h2>November 2024: GFTN Elevandi Insights Forum during Singapore Fintech Festival</h2>
    <div class="topic-badge">Building Trust in Era of AI: Fostering Public Private Collaboration to Scale AI Responsibly</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-gftn-elevandi-insights-building-trust-ai-era-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-gftn-elevandi-insights-building-trust-ai-era-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-gftn-elevandi-insights-building-trust-ai-era-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-gftn-elevandi-insights-building-trust-ai-era-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-gftn-elevandi-insights-building-trust-ai-era-5.png" alt="Image 5" onclick="openLightbox(4)">
      </div>
  </div>  

  <div id="tab-avc" class="tab-content" style="display: block;">  
    <h2>November 2024: Carta Investor Hours for Founders during Singapore Fintech Festival</h2>
    <div class="topic-badge">Zero To One Angel Investments & Mentorship</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-carta-investor-hours-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-carta-investor-hours-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-carta-investor-hours-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-nov-singapore-fintech-festival-carta-investor-hours-4.png" alt="Image 4" onclick="openLightbox(3)">
      </div>
  </div>  

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>November 2024: Digital Assets Week</h2>
    <div class="topic-badge">The Future of the Digital Asset Custody Landscape</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-custody-digital-assets-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-custody-digital-assets-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-custody-digital-assets-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-custody-digital-assets-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-custody-digital-assets-5.png" alt="Image 5" onclick="openLightbox(4)">
      </div>
  </div> 

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>November 2024: Digital Assets Week</h2>
    <div class="topic-badge">Institutional Investment Trends in Cryptocurrency Demand and Access</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-institutional-demand-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-institutional-demand-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-nov-digital-assets-week-singapore-fintech-festival-juliet-media-institutional-demand-3.png" alt="Image 3" onclick="openLightbox(2)">
      </div>
  </div>     

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>October 2024: Masterclass at NUS MBA Business School</h2>
    <div class="topic-badge">Microstrategy: Modern Corporate Finance Case Study on Bitcoin Treasury</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-5.png" alt="Image 5" onclick="openLightbox(4)">
      </div>
    </div>   
  
  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>October 2024: Launch of AI CTO Program: Singapore Google Office Panel Discussion</h2>
    <div class="topic-badge">Building a Sustainable COE - AI CTO Program</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-1.png" alt="Image 1" onclick="openLightbox(5)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-2.png" alt="Image 2" onclick="openLightbox(6)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-3.png" alt="Image 3" onclick="openLightbox(7)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-4.png" alt="Image 4" onclick="openLightbox(8)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-5.png" alt="Image 5" onclick="openLightbox(9)">
      </div> 
  </div>

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>October 2024: Tab Conference 6 2024 at Georgia Tech - Atlanta Talk</h2>
    <div class="topic-badge">Architectural Nuances for Bitcoin Enterprise Custody for Institutions/Orgs</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-1.png" alt="Image 1" onclick="openLightbox(10)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-2.png" alt="Image 2" onclick="openLightbox(11)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-3.png" alt="Image 3" onclick="openLightbox(12)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-4.png" alt="Image 4" onclick="openLightbox(13)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-5.png" alt="Image 5" onclick="openLightbox(14)">
      </div> 
  </div>

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>October 2024: Bitcoin Conference 2024 at Amsterdam Panel amongst industry experts</h2>
    <div class="topic-badge">Bitcoin Wealth & Inheritance</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-1.png" alt="Image 1" onclick="openLightbox(15)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-2.png" alt="Image 2" onclick="openLightbox(16)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-3.png" alt="Image 3" onclick="openLightbox(17)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-4.png" alt="Image 4" onclick="openLightbox(18)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-5.png" alt="Image 5" onclick="openLightbox(19)">
      </div> 
  </div>

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>September 2024: Podcast with OnRamp on Intersection of AI and Bitcoin exploring the Hyperdeflation and Hyperbitcoinization scenarios</h2>
    <a href="https://youtu.be/kvX7QBVNL_M?si=UNpcI7ah2jbgIfy5" target="_blank" rel="noopener noreferrer">YouTube</a>
    <div class="topic-badge">Intersection of Bitcoin and AI: How AI will cause Hyperdeflation & Bitcoin will help measure wealth</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-sep-podcast-series-sagun-garg-onramp-mena-uae-september2024-bitcoin-ai-ml-hyperdeflation-hyperbitcoinization-1.png" alt="Image 1" onclick="openLightbox(18)">
        <img src="https://sagungarg.com/assets/img/2024-sep-podcast-series-sagun-garg-onramp-mena-uae-september2024-bitcoin-ai-ml-hyperdeflation-hyperbitcoinization-2.png" alt="Image 2" onclick="openLightbox(19)">
        <img src="https://sagungarg.com/assets/img/2024-sep-podcast-series-sagun-garg-onramp-mena-uae-september2024-bitcoin-ai-ml-hyperdeflation-hyperbitcoinization-3.png" alt="Image 3" onclick="openLightbox(20)">
      </div> 
  </div>

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>September 2024: Lecture at NUS in course: Investing Using Machine Learning and Alternative Data course!</h2>
    <div class="topic-badge">Future of Wealth Banking using AI/ML & Alternative Data</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-sep-guest-lecturer-university-nus-academia-lecture-investing-using-machine-learning-alternative-data-1.png" alt="Image 1" onclick="openLightbox(18)">
        <img src="https://sagungarg.com/assets/img/2024-sep-guest-lecturer-university-nus-academia-lecture-investing-using-machine-learning-alternative-data-1.png" alt="Image 2" onclick="openLightbox(19)">
        <img src="https://sagungarg.com/assets/img/2024-sep-guest-lecturer-university-nus-academia-lecture-investing-using-machine-learning-alternative-data-1.png" alt="Image 3" onclick="openLightbox(20)">
      </div> 
  </div>

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>September 2024: Presentation talk at Lightning Returns Bitcoin Conference in Singapore</h2>
    <div class="topic-badge">Tech Driven HyperDeflation, Bitcoin Hyperbitcoinization Era & Future of Wealth Banking</div>
    <a href="https://youtu.be/GLLea0GZ_ro?si=ZZHXTWStD6V4Yt8n" target="_blank" rel="noopener noreferrer">YouTube</a>
      <div class="scroll-container">  
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-sagun-garg-singapore-september2024-bitcoinconference-weekoftoken2049-2024-1.png" alt="Image 1" onclick="openLightbox(21)">
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-sagun-garg-singapore-september2024-bitcoinconference-weekoftoken2049-2024-2.png" alt="Image 2" onclick="openLightbox(22)">
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-sagun-garg-singapore-september2024-bitcoinconference-weekoftoken2049-2024-3.png" alt="Image 3" onclick="openLightbox(23)">
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-sagun-garg-singapore-september2024-bitcoinconference-weekoftoken2049-2024-4.png" alt="Image 4" onclick="openLightbox(24)">
      </div> 
  </div> 

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>September 2024: Presentation at Thailand Bitcoin Conference (TBC 2024)</h2>
    <div class="topic-badge">Intersection of Bitcoin and AI: How AI will cause Hyperdeflation & Bitcoin will help measure wealth</div>
    <a href="https://youtu.be/g_qglws0r38?si=ubn1mnNTodtC55pn" target="_blank" rel="noopener noreferrer">YouTube</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-sagun-garg-thailand-september2024-bitcoinconference-bangkok-2024-1.png" alt="Image 1" onclick="openLightbox(25)">
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-sagun-garg-thailand-september2024-bitcoinconference-bangkok-2024-2.png" alt="Image 2" onclick="openLightbox(26)">
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-sagun-garg-thailand-september2024-bitcoinconference-bangkok-2024-3.png" alt="Image 3" onclick="openLightbox(27)">
      </div> 
  </div> 

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>September 2024: Panel talk with industry experts organised by ABS and MAS</h2>
    <div class="topic-badge">Unlocking the Future: Key Considerations and Path to Capture Generative AI Value</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-1.png" alt="Image 1" onclick="openLightbox(28)">
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-2.png" alt="Image 2" onclick="openLightbox(29)">
        <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-3.png" alt="Image 3" onclick="openLightbox(30)">
      </div> 
  </div>    

  <div id="tab-avc" class="tab-content" style="display: block;">
    <h2>August2024: Guest lecturer at Singapore Management University to batch of industry VC professionals</h2>
    <div class="topic-badge">Market Overview & Global Perspectives(Advanced Certificate in Venture Capital)</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-aug-guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-1.png" alt="Image 1" onclick="openLightbox(31)">
        <img src="https://sagungarg.com/assets/img/2024-aug-guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-2.png" alt="Image 2" onclick="openLightbox(32)">
        <img src="https://sagungarg.com/assets/img/2024-aug-guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-3.png" alt="Image 3" onclick="openLightbox(33)">
        <img src="https://sagungarg.com/assets/img/2024-aug-guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-4.png" alt="Image 4" onclick="openLightbox(34)">
      </div> 
  </div> 

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>August2024: Evaluator for the Global FinTech Hackcelerator at Singapore Fintech Festival</h2>
    <div class="topic-badge">Judge & Evaluator for AI Startups for applications in Singapore Fintech Festival (SFF 2024)</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-aug-judge-series-sagungarg-singapore-sff-ai-hackcelerator-2024-challenge-1.png" alt="Image 1" onclick="openLightbox(35)">
        <img src="https://sagungarg.com/assets/img/2024-aug-judge-series-sagungarg-singapore-sff-ai-hackcelerator-2024-challenge-2.png" alt="Image 2" onclick="openLightbox(36)">
      </div> 
  </div>  

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>July2024: Panel discussion on mainstage at Bitcoin Nashville Conference with Caitlin Long, Miles Paschini and Sagun Garg</h2>
    <div class="topic-badge">Bitcoin's Role in Traditional Banks</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-july-speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-1.png" alt="Image 1" onclick="openLightbox(37)">
        <img src="https://sagungarg.com/assets/img/2024-july-speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-2.png" alt="Image 2" onclick="openLightbox(38)">
        <img src="https://sagungarg.com/assets/img/2024-july-speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-3.png" alt="Image 3" onclick="openLightbox(39)">
        <img src="https://sagungarg.com/assets/img/2024-july-speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-4.png" alt="Image 4" onclick="openLightbox(40)">
      </div>  
  </div> 

  <div id="tab-avc" class="tab-content" style="display: block;">
    <h2>July2024: Industry Competition in GenAI LLMs: Google + EDB(Economic Development Board) - Industry Competition AI Trailblazers</h2>
    <div class="topic-badge">GenAI Narrative builder for portfolio re-assesment factually matching internal house view</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-july-presenter-series-singapore-google-edb-ai-llm-genai-trailblazers-competition-1.png" alt="Image 1" onclick="openLightbox(41)">
        <img src="https://sagungarg.com/assets/img/2024-july-presenter-series-singapore-google-edb-ai-llm-genai-trailblazers-competition-2.png" alt="Image 2" onclick="openLightbox(42)">
        <img src="https://sagungarg.com/assets/img/2024-july-presenter-series-singapore-google-edb-ai-llm-genai-trailblazers-competition-3.png" alt="Image 3" onclick="openLightbox(43)">
        <img src="https://sagungarg.com/assets/img/2024-july-presenter-series-singapore-google-edb-ai-llm-genai-trailblazers-competition-4.png" alt="Image 4" onclick="openLightbox(44)">
      </div>
  </div>

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>May2024: Panel discussion at Bitcoin Conference Asia 2024 - Hong Kong</h2>
    <div class="topic-badge">Miniscript & Bitcoin Inheritance Planning</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-1.png" alt="Image 1" onclick="openLightbox(45)">
        <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-2.png" alt="Image 2" onclick="openLightbox(46)">
        <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-3.png" alt="Image 3" onclick="openLightbox(47)">
        <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-4.png" alt="Image 4" onclick="openLightbox(48)">
      </div>
  </div>

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>May2024: Students from Indiana University - Kelley School of Business</h2>
    <div class="topic-badge">Fireside Chat on Bitcoin, Crypto and Tokenization</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-singapore-students-business-school-sagungarg-bitcoin-digital-assets-1.png" alt="Image 1" onclick="openLightbox(49)">
        <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-singapore-students-business-school-sagungarg-bitcoin-digital-assets-2.png" alt="Image 2" onclick="openLightbox(50)">
        <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-singapore-students-business-school-sagungarg-bitcoin-digital-assets-3.png" alt="Image 3" onclick="openLightbox(51)">
        <img src="https://sagungarg.com/assets/img/2024-may-speaker-series-singapore-students-business-school-sagungarg-bitcoin-digital-assets-4.png" alt="Image 4" onclick="openLightbox(52)">
      </div>
  </div>

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>March2024: Guest speaker organised by Plug & Play Tech Center & Aelf Blockchain on Layer 2 solutions on Bitcoin</h2>
    <div class="topic-badge">Blockhain and RWA Tokenization</div>
    <a href="https://www.linkedin.com/posts/sagungarg_web3-defi-tokenisation-activity-7172541301182197760-ZBvB" target="_blank" rel="noopener noreferrer">Linkedin Post</a>
    <a href="https://www.plugandplaytechcenter.com/" target="_blank" rel="noopener noreferrer">Plug & Play Tech Center</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-mar-speaker-series-sagun-garg-march2024-plugandplay-aelf-web3-from-web2-journey-singapore-1.png" alt="Image 1" onclick="openLightbox(53)">
        <img src="https://sagungarg.com/assets/img/2024-mar-speaker-series-sagun-garg-march2024-plugandplay-aelf-web3-from-web2-journey-singapore-2.png" alt="Image 2" onclick="openLightbox(54)">
      </div>
  </div>

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>January2024: Investor - Judge for Tenity Singapore Incubation Batch 7</h2>
    <div class="topic-badge">Startup Judging Panel</div>
    <a href="https://www.tenity.com/programs/singapore-incubation-batch-7" target="_blank" rel="noopener noreferrer">Link To Event</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-jan-judge-sagun-garg-tenity-singapore-incubation-batch7-1.png" alt="Image 1" onclick="openLightbox(55)">
        <img src="https://sagungarg.com/assets/img/2024-jan-judge-sagun-garg-tenity-singapore-incubation-batch7-2.png" alt="Image 2" onclick="openLightbox(56)">
      </div>
  </div>

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>December2023: Singapore SMU professor doing a Series for Bank Julius Baer Employees</h2>
    <div class="topic-badge">Intersection of Web3 and AI for Digital Assets</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2023-nov-speaker-series-sagun-garg-web3-singapore-smu-professor.png" alt="Image 1" onclick="openLightbox(60)">
      </div>
  </div>

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>Decemberh2023: Competition: Corporate Innovation Challenge at Singapore Fintech Festival - Launchpad Team - Bank Julius Baer</h2>
    <div class="topic-badge">GenAI: Using LLMs building Impactful Corporate Cost Saving Applications</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2023-nov-competition-sagun-garg-sff-launchpad-booth-sophie-product-1.png" alt="Image 1" onclick="openLightbox(61)">
      </div>
  </div>

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>November2023: Investor - Judge at Carta Investor program at Singapore Fintech Festival 2023</h2>
    <div class="topic-badge">Zero To One Angel Investments & Mentorship</div>
    <a href="https://www.fintechfestival.sg/investor-hours" target="_blank" rel="noopener noreferrer">Link To Event</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2023-nov-judge-sagun-garg-carta-investor-ambassador-sff-2023-1.png" alt="Image 1" onclick="openLightbox(62)">
        <img src="https://sagungarg.com/assets/img/2023-nov-judge-sagun-garg-carta-investor-ambassador-sff-2023-2.png" alt="Image 2" onclick="openLightbox(63)">
      </div>
  </div>

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>November2023: Speaker - At Hustle Fund Angel Squad event in Singapore in November 2023</h2>
    <div class="topic-badge">Evolution of Bitcoin and Web3 in next coming 1 year</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2023-nov-speaker-series-sagun-hustlefund-angelsquad-crypto-nov2023-1.png" alt="Image 1" onclick="openLightbox(64)">
        <img src="https://sagungarg.com/assets/img/2023-nov-speaker-series-sagun-hustlefund-angelsquad-crypto-nov2023-2.png" alt="Image 2" onclick="openLightbox(65)">
      </div>
  </div>

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>July2023: Judge for Hackcelerator AI Startup Competition organised by Singapore Govt through MAS </h2>
    <div class="topic-badge">MAS AI Competition to evaluate global Startups for upcoming SFF 2023</div>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2023-july-judge-series-sagungarg-singapore-mas-ai-fintech-challenge.png" alt="Image 1" onclick="openLightbox(66)">
      </div>
  </div>

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>June2023: Speaker - Master Class in Zurich for, Tenity(formerly F10 Batch)</h2>
    <div class="topic-badge">Customer Money versus VC Money</div>
    <a href="https://www.tenity.com" target="_blank" rel="noopener noreferrer">Tenity Accelerator</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2023-jun-speaker-series-sagun-zurich-master-class-tenity-batch-jun2023.png" alt="Image 1" onclick="openLightbox(67)">
      </div>
  </div>

<!-- Lightbox container -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <span class="lightbox-close" onclick="closeLightbox()">&times;</span>
  <span class="arrow arrow-left" onclick="event.stopPropagation(); changeImage(-1)">&#10094;</span>
  <img id="lightbox-img" src="" alt="" onclick="event.stopPropagation();">
  <span class="arrow arrow-right" onclick="event.stopPropagation(); changeImage(1)">&#10095;</span>
</div>


<script>
  // // Store the images in an array
  // const images = document.querySelectorAll('.scroll-container img');
  // let currentImageIndex = 0;
  // let isLightboxOpen = false;

  // // Open the lightbox with the clicked image
  // function openLightbox(index) {
  //   currentImageIndex = index;  // Set the current index to the clicked image
  //   var lightbox = document.getElementById('lightbox');
  //   var lightboxImg = document.getElementById('lightbox-img');
    
  //   // Set the clicked image's source to the lightbox image
  //   lightboxImg.src = images[currentImageIndex].src;
    
  //   // Show the lightbox
  //   lightbox.style.display = 'flex';
  //   isLightboxOpen = true; // Mark lightbox as open
    
  //   // Disable background scroll when lightbox is open
  //   document.body.style.overflow = 'hidden';
  // }

  // // Close the lightbox
  // function closeLightbox() {
  //   var lightbox = document.getElementById('lightbox');
    
  //   // Hide the lightbox
  //   lightbox.style.display = 'none';
  //   isLightboxOpen = false; // Mark lightbox as closed
    
  //   // Re-enable background scroll
  //   document.body.style.overflow = '';
  // }

  // // Change the image (backward or forward)
  // function changeImage(direction) {
  //   // Calculate the next image index
  //   currentImageIndex = (currentImageIndex + direction + images.length) % images.length;
    
  //   var lightboxImg = document.getElementById('lightbox-img');
  //   lightboxImg.src = images[currentImageIndex].src;  // Update the lightbox image
  // }

  // // Add event listener for keyboard navigation
  // document.addEventListener('keydown', function(event) {
  //   if (isLightboxOpen) {
  //     event.preventDefault(); // Prevent default arrow key behavior (e.g., scrolling)
      
  //     if (event.key === 'ArrowRight') {
  //       changeImage(1); // Go to next image
  //     } else if (event.key === 'ArrowLeft') {
  //       changeImage(-1); // Go to previous image
  //     } else if (event.key === 'Escape') {
  //       closeLightbox(); // Close the lightbox when Escape is pressed
  //     }
  //   }
  // });

  // Tab functionality
  function openTab(event, tabId) {
    // Hide all tab contents and remove active class from tabs
    document.querySelectorAll('.tab-content').forEach(content => content.style.display = 'none');
    document.querySelectorAll('.tab').forEach(tab => tab.classList.remove('active'));
    
    // Show the selected tab content and set the clicked tab as active
    document.getElementById(tabId).style.display = 'block';
    event.currentTarget.classList.add('active');
  }

  // Store the images in an array
  const images = document.querySelectorAll('.scroll-container img');
  let currentImageIndex = 0;
  let isLightboxOpen = false;

  // Open the lightbox with the clicked image
  function openLightbox(index) {
    // Get all images from both grid and scroll containers
    const allImages = [...document.querySelectorAll('.grid-container img'), 
                       ...document.querySelectorAll('.scroll-container img')];
    
    currentImageIndex = index;
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    
    // Set the clicked image's source to the lightbox image
    lightboxImg.src = allImages[currentImageIndex].src;
    
    // Show the lightbox
    lightbox.style.display = 'flex';
    isLightboxOpen = true;
    
    // Disable background scroll
    document.body.style.overflow = 'hidden';
  }

  // Close the lightbox
  function closeLightbox() {
    var lightbox = document.getElementById('lightbox');
    
    // Hide the lightbox
    lightbox.style.display = 'none';
    isLightboxOpen = false;
    
    // Re-enable background scroll
    document.body.style.overflow = '';
  }

  // Change the image (backward or forward)
  function changeImage(direction) {
    const allImages = [...document.querySelectorAll('.grid-container img'), 
                       ...document.querySelectorAll('.scroll-container img')];
                       
    currentImageIndex = (currentImageIndex + direction + allImages.length) % allImages.length;
    
    const lightboxImg = document.getElementById('lightbox-img');
    lightboxImg.src = allImages[currentImageIndex].src;
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



A. **May 2024**: Sagun has been nominated as a Speaker at Bitcoin Asia Hong Kong conference: Topic of Miniscript: Future of Inheritance in Bitcoin

B.**Jan 2024**: Nominated as Judge for Tenity incubator in Singapore for selecting various startups, Inriskable was shortlisted for the name screening & source of wealth use case in the private bank space, a proof of concept within the Bank Julius Baer Innovation Lab in the Singapore office

C.**Sep 2023**: I mentored an incoming batch of entrepreneurs at Tenity, in Zurich Switzerland with a master class on Venture Capital and Entrepreneurship. Ran a masterclass for batch of 50+ Entrepreneurs on the Topic

D.**June 2023**: I was nominated as round 1 Judge of AI in Finance Hackcelerator SG competition, conducted by MAS, for various startups. I closely worked with KOK Li Wen for evaluations at Fintech & Innovation Group of MAS