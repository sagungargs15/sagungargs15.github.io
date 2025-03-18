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
</style>


<div class="grid-container">
  <!-- Thumbnails (100 Images) -->
  <!-- Replace 'imageX.jpg' with actual image paths -->
  <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-1.jpeg" alt="Thumbnail 1" onclick="openLightboxThumbnail(1)">
  <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-2.jpeg" alt="Thumbnail 2" onclick="openLightboxThumbnail(2)">
  <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-1.png" alt="Thumbnail 3" onclick="openLightboxThumbnail(3)">
  <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-interoperability-lightningconnect-hongkong-1.png" alt="Thumbnail 4" onclick="openLightboxThumbnail(4)">
  <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-1.png" alt="Thumbnail 5" onclick="openLightboxThumbnail(5)">
  <img src="https://sagungarg.com/assets/img/2025-jan-speaker-series-sagun-garg-usa-jan2025-digitalassets-halborn-securitysummit-newyork-3.png" alt="Thumbnail 6" onclick="openLightboxThumbnail(6)">
  <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-1.png" alt="Thumbnail 7" onclick="openLightboxThumbnail(7)">
  <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-1.png" alt="Thumbnail 8" onclick="openLightboxThumbnail(8)">
  <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-1.png" alt="Thumbnail 9" onclick="openLightboxThumbnail(9)">
  <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-bitcoinconference-3.png" alt="Thumbnail 10" onclick="openLightboxThumbnail(10)">
  <img src="https://sagungarg.com/assets/img/2024-sep-speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-1.png" alt="Thumbnail 11" onclick="openLightboxThumbnail(11)">
  <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-2.jpeg" alt="Thumbnail 12" onclick="openLightboxThumbnail(12)">

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

<!-- Lightbox Overlay -->
<div class="lightboxthumbnail-overlay" id="lightboxOverlaythumbnail">
  <span class="close-btn" onclick="closeLightbox()">&times;</span>
  <img id="lightboxImage" src="" alt="Large View">
</div>

## Stay tuned...More talks will be updated soon...
- 💬 **Speaker/Judging/Presenter Series**: 

  <!-- Tab Navigation -->
  <div class="tab-container">
    <button class="tab-button" onclick="openTab(event, 'tab-btc')">Bitcoin</button>
    <button class="tab-button" onclick="openTab(event, 'tab-aiml')">AI/ML</button>
    <button class="tab-button" onclick="openTab(event, 'tab-fndr')">Founder</button>
    <button class="tab-button" onclick="openTab(event, 'tab-avc')">Angel/VC</button>
  </div>

    <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>February 2025: Digital Assets Week in Hong Kong after Consensus Conference Week</h2>
    <p>Topic: "Are Custody Providers Adequately Supporting the Needs of Tokenization"</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2025-feb-peaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-5.png" alt="Image 5" onclick="openLightbox(4)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-6.png" alt="Image 6" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2025-feb-speaker-series-sagun-garg-HK-feb2025-digitalassetsweek-tokenization-custody-julietmedia-hongkong-7.png" alt="Image 7" onclick="openLightbox(4)">
      </div>
    </div>  

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>February 2025: Bitcoin Lightning Connect Summit in Hong Kong during Consensus Conference Week</h2>
    <p>Topic: "​Breaking Barriers: How Lightning Unlocks P2P Money"</p>
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
    <p>Topic: "Enhancing DLT Security: Strategies for Risk, Compliance, and Financial Integrity"</p>
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
    <h2>December 2025: Bitcoin Institutional Day - Abu Dhabi, UAE</h2>
    <p>Topic: "Bitcoin Venture Capital and Private Equity"</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-vc-panel-abu-dhabi-financial-week-4.png" alt="Image 4" onclick="openLightbox(3)">
      </div>
    </div>  

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>December 2025: Bitcoin Institutional Day - Abu Dhabi, UAE</h2>
    <p>Topic: "Bitcoin the Real Fintech"</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-as-fintech-abu-dhabi-financial-week-adfw-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-as-fintech-abu-dhabi-financial-week-adfw-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-as-fintech-abu-dhabi-financial-week-adfw-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-as-fintech-abu-dhabi-financial-week-adfw-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-institutional-day-bitcoin-as-fintech-abu-dhabi-financial-week-adfw-5.png" alt="Image 5" onclick="openLightbox(4)">
      </div>
    </div>  

  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>December 2025: Bitcoin MENA Conference in Abu Dhabi</h2>
    <p>Topic: "Building the Tools for Institutional Adoption: Hardware and Software"</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2024-dec-bitcoin-mena-conference-bitcoin-institutional-infra-tools-abu-dhabi-financial-week-adfw-5.png" alt="Image 5" onclick="openLightbox(4)">
      </div>
    </div>  


  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>October 2024: Masterclass at NUS MBA Business School</h2>
    <p>Topic: "Microstrategy: Modern Corporate Finance Case Study on Bitcoin Treasury"</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-5.png" alt="Image 5" onclick="openLightbox(4)">
      </div>
    </div>   
 
    <!-- Extra Space vertical padding  -->
  
  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>October 2024: Launch of AI CTO Program: Singapore Google Office Panel Discussion</h2>
    <p>Topic: Building a Sustainable COE - AI CTO Program</p>  
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-1.png" alt="Image 1" onclick="openLightbox(5)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-2.png" alt="Image 2" onclick="openLightbox(6)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-3.png" alt="Image 3" onclick="openLightbox(7)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-4.png" alt="Image 4" onclick="openLightbox(8)">
        <img src="https://sagungarg.com/assets/img/2024-oct-speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-5.png" alt="Image 5" onclick="openLightbox(9)">
      </div> 
  </div>
   
    <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>October 2024: Tab Conference 6 2024 at Georgia Tech - Atlanta Talk</h2>
    <p>Topic: Architectural Nuances for Bitcoin Enterprise Custody for Institutions/Orgs (Small/Medium) on Bitcoin Standard - Self Sovereignty for “Corporate Plebs & Non-Profits</p> 
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-1.png" alt="Image 1" onclick="openLightbox(10)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-2.png" alt="Image 2" onclick="openLightbox(11)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-3.png" alt="Image 3" onclick="openLightbox(12)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-4.png" alt="Image 4" onclick="openLightbox(13)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-georgia-atlanta-tabconf6-usa-october2024-bitcoinconference-5.png" alt="Image 5" onclick="openLightbox(14)">
      </div> 
  </div>
  
    <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>October 2024: Bitcoin Conference 2024 at Amsterdam Panel amongst industry experts</h2>
    <p>Topic: Bitcoin Wealth & Inheritance</p> 
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-1.png" alt="Image 1" onclick="openLightbox(15)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-2.png" alt="Image 2" onclick="openLightbox(16)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-3.png" alt="Image 3" onclick="openLightbox(17)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-4.png" alt="Image 4" onclick="openLightbox(18)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-5.png" alt="Image 5" onclick="openLightbox(19)">
      </div> 
  </div>

    <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>September 2024: Podcast with OnRamp MENA on Intersection of AI and Bitcoin exploring the Hyperdeflation and Hyperbitcoinization scenarios</h2>
    <p>Topic: Intersection of Bitcoin and AI: How AI will cause Hyperdeflation & Bitcoin will help measure wealth in a HyperBitcoinization world</p>
    <p>Are these two ideas two sides of the same Coin and why corporates will move on to Enterprise Custody Multsig, Mult-jurisdiction and multi-agents setup on Bitcoin Standard</p>
    <a href="https://youtu.be/kvX7QBVNL_M?si=UNpcI7ah2jbgIfy5" target="_blank" rel="noopener noreferrer">YouTube</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/podcast-series-sagun-garg-onramp-mena-uae-september2024-bitcoin-ai-ml-hyperdeflation-hyperbitcoinization-1.png" alt="Image 1" onclick="openLightbox(18)">
        <img src="https://sagungarg.com/assets/img/podcast-series-sagun-garg-onramp-mena-uae-september2024-bitcoin-ai-ml-hyperdeflation-hyperbitcoinization-2.png" alt="Image 2" onclick="openLightbox(19)">
        <img src="https://sagungarg.com/assets/img/podcast-series-sagun-garg-onramp-mena-uae-september2024-bitcoin-ai-ml-hyperdeflation-hyperbitcoinization-3.png" alt="Image 3" onclick="openLightbox(20)">
      </div> 
  </div>
 
    <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>September 2024: Presentation talk at Lightning Returns Bitcoin Conference in Singapore</h2>
    <p>Topic: Technological Progress Driven HyperDeflation, Bitcoin Hyperbitcoinization Era & Future of Wealth Banking"</p>
    <a href="https://youtu.be/GLLea0GZ_ro?si=ZZHXTWStD6V4Yt8n" target="_blank" rel="noopener noreferrer">YouTube</a>
      <div class="scroll-container">  
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-singapore-september2024-bitcoinconference-weekoftoken2049-2024-1.jpeg" alt="Image 1" onclick="openLightbox(21)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-singapore-september2024-bitcoinconference-weekoftoken2049-2024-2.jpeg" alt="Image 2" onclick="openLightbox(22)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-singapore-september2024-bitcoinconference-weekoftoken2049-2024-3.jpeg" alt="Image 3" onclick="openLightbox(23)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-singapore-september2024-bitcoinconference-weekoftoken2049-2024-4.jpeg" alt="Image 4" onclick="openLightbox(24)">
      </div> 
  </div> 

    <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>September 2024: Presentation at Thailand Bitcoin Conference (TBC 2024)</h2>
    <p>Topic: Intersection of Bitcoin and AI: How AI will cause Hyperdeflation & Bitcoin will help measure wealth in a HyperBitcoinization world</p>
    <a href="https://youtu.be/g_qglws0r38?si=ubn1mnNTodtC55pn" target="_blank" rel="noopener noreferrer">YouTube</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-thailand-september2024-bitcoinconference-bangkok-2024-1.png" alt="Image 1" onclick="openLightbox(25)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-thailand-september2024-bitcoinconference-bangkok-2024-2.png" alt="Image 2" onclick="openLightbox(26)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-thailand-september2024-bitcoinconference-bangkok-2024-3.png" alt="Image 3" onclick="openLightbox(27)">
      </div> 
  </div> 

    <!-- Extra Space vertical padding  -->

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>September 2024: Panel talk with industry experts organised by ABS and MAS</h2>
    <p>Topic: Unlocking the Future: Key Considerations and Path to Capture Generative AI Value</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-1.png" alt="Image 1" onclick="openLightbox(28)">
        <img src="https://sagungarg.com/assets/img/speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-2.png" alt="Image 2" onclick="openLightbox(29)">
        <img src="https://sagungarg.com/assets/img/speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-3.png" alt="Image 3" onclick="openLightbox(30)">
      </div> 
  </div>    

    <!-- Extra Space vertical padding  -->

  <div id="tab-avc" class="tab-content" style="display: block;">
    <h2>August2024: Guest lecturer at Singapore Management University to batch of industry VC professionals</h2>
    <p>Topic: Market Overview & Global Perspectives and Advanced Certificate in Venture Capital</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-1.jpeg" alt="Image 1" onclick="openLightbox(31)">
        <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-2.jpeg" alt="Image 2" onclick="openLightbox(32)">
        <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-3.jpeg" alt="Image 3" onclick="openLightbox(33)">
        <img src="https://sagungarg.com/assets/img/guest-lecturer-university-singapore-smu-advanced-certificate-in-venture-capital-4.jpeg" alt="Image 4" onclick="openLightbox(34)">
      </div> 
  </div> 

    <!-- Extra Space vertical padding  -->
  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>August2024: Evaluator for the Global FinTech Hackcelerator at Singapore Fintech Festival</h2>
    <p>Topic: Judge & Evaluator for AI Startups for applications in Singapore Fintetc Festival (SFF 2024)</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/judge-series-sagungarg-singapore-sff-ai-hackcelerator-2024-challenge-1.png" alt="Image 1" onclick="openLightbox(35)">
        <img src="https://sagungarg.com/assets/img/judge-series-sagungarg-singapore-sff-ai-hackcelerator-2024-challenge-2.png" alt="Image 2" onclick="openLightbox(36)">
      </div> 
  </div>  

    <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>July2024: Panel discussion on mainstage at Bitcoin Nashville Conference with Caitlin Long, Miles Paschini and Sagun Garg</h2>
    <p>Topic: Bitcoin's Role in Traditional Banks</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-1.png" alt="Image 1" onclick="openLightbox(37)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-2.png" alt="Image 2" onclick="openLightbox(38)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-3.png" alt="Image 3" onclick="openLightbox(39)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-4.png" alt="Image 4" onclick="openLightbox(40)">
      </div>  
  </div> 

  <!-- Extra Space vertical padding  -->

  <div id="tab-avc" class="tab-content" style="display: block;">
    <h2>July2024: Industry Competition in GenAI LLMs: Google + EDB(Economic Development Board) - Industry Competition AI Trailblazers</h2>
    <p>Topic: GenAI Narrative builder for protfolio re-assement for switching positions using factual references of internal publications</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/presenter-series-singapore-google-edb-AI-llm-genai-trailblazers-competition-1.png" alt="Image 1" onclick="openLightbox(41)">
        <img src="https://sagungarg.com/assets/img/presenter-series-singapore-google-edb-AI-llm-genai-trailblazers-competition-2.png" alt="Image 2" onclick="openLightbox(42)">
        <img src="https://sagungarg.com/assets/img/presenter-series-singapore-google-edb-AI-llm-genai-trailblazers-competition-3.png" alt="Image 3" onclick="openLightbox(43)">
        <img src="https://sagungarg.com/assets/img/presenter-series-singapore-google-edb-AI-llm-genai-trailblazers-competition-4.png" alt="Image 4" onclick="openLightbox(44)">
      </div>
  </div>  

  <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>May2024: Panel discussion at Bitcoin Conference Asia 2024 - Hong Kong</h2>
    <p>Topic: Miniscript & Bitcoin Inheritance Planning</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-1.png" alt="Image 1" onclick="openLightbox(45)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-2.png" alt="Image 2" onclick="openLightbox(46)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-3.png" alt="Image 3" onclick="openLightbox(47)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-4.png" alt="Image 4" onclick="openLightbox(48)">
      </div>
  </div>  

  <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>May2024: Students from Indiana University - Kelley School of Business</h2>
    <p>Topic: Fireside Chat on Bitcoin, Crypto and Tokenization</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-singapore-students-business-school-sagungarg-Bitcoin-Digital-Assets-1.png" alt="Image 1" onclick="openLightbox(49)">
        <img src="https://sagungarg.com/assets/img/speaker-series-singapore-students-business-school-sagungarg-Bitcoin-Digital-Assets-2.png" alt="Image 2" onclick="openLightbox(50)">
        <img src="https://sagungarg.com/assets/img/speaker-series-singapore-students-business-school-sagungarg-Bitcoin-Digital-Assets-3.png" alt="Image 3" onclick="openLightbox(51)">
        <img src="https://sagungarg.com/assets/img/speaker-series-singapore-students-business-school-sagungarg-Bitcoin-Digital-Assets-4.png" alt="Image 4" onclick="openLightbox(52)">
      </div>
  </div>  

  <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>March2024: Guest speaker organised by Plug & Play Tech Center & Aelf Blockchain on Layer 2 solutions on Bitcoin</h2>
    <p>Topic: Web3: Blockhain and RWA Tokenization</p>
    <a href="https://www.linkedin.com/posts/sagungarg_web3-defi-tokenisation-activity-7172541301182197760-ZBvB" target="_blank" rel="noopener noreferrer">Linkedin Post</a>
    <a href="https://www.plugandplaytechcenter.com/" target="_blank" rel="noopener noreferrer">Plug & Play Tech Center</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-march2024-plugandplay-aelf-web3-from-web2-journey-singapore-1.png" alt="Image 1" onclick="openLightbox(53)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-march2024-plugandplay-aelf-web3-from-web2-journey-singapore-2.png" alt="Image 2" onclick="openLightbox(54)">
      </div>
  </div>  

  <!-- - **February 2024**: SG-HK Corporate Innovation Program for Tenity Funded Startups

    ![pic](https://sagungarg.com/assets/img/speaker-series-sagun-garg-master-class-tenity-singapore-corporate-innovation-partnerships.png) -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>January2024: Investor - Judge for Tenity Singapore Incubation Batch 7</h2>
    <p>Theme of Startups Pitching: Fintech, Insurtech, or RegTech, DeepTech, Web3, Sustainable Finance, LegalTech, CryptoFinance startups</p>
    <a href="https://www.tenity.com/programs/singapore-incubation-batch-7" target="_blank" rel="noopener noreferrer">Link To Event</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-tenity-singapore-incubation-batch7-1.png" alt="Image 1" onclick="openLightbox(55)">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-tenity-singapore-incubation-batch7-2.png" alt="Image 2" onclick="openLightbox(56)">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-tenity-singapore-incubation-batch7-3.png" alt="Image 2" onclick="openLightbox(57)">
      </div>
  </div> 

  <!-- Extra Space vertical padding  -->

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>December2023: Singapore SMU professor doing a Series for Bank Julius Baer Employees</h2>
    <p>Topic: Intersection of Web3 and AI for Digital Assets</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-web3-singapore-smu-professor.png" alt="Image 1" onclick="openLightbox(60)">
      </div>
  </div> 

  <!-- Extra Space vertical padding  -->

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>Decemberh2023: Competition: Corporate Innovation Challenge at Singapore Fintech Festival - Launchpad Team - Bank Julius Baer</h2>
    <p>Topic: GenAI: Using LLMs building Impactful Corporate Cost Saving Applications</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/competition-sagun-garg-sff-launchpad-booth-sophie-product-1.png" alt="Image 1" onclick="openLightbox(61)">
      </div>
  </div> 

  <!-- Extra Space vertical padding  -->

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>November2023: Investor - Judge at Carta Investor program at Singapore Fintech Festival 2023</h2>
    <p>Investor: Meeting and Guiding startups shortlisted bt Carta for pitching at Singapore Fintech Festival </p>
    <a href="https://www.fintechfestival.sg/investor-hours" target="_blank" rel="noopener noreferrer">Link To Event</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-carta-investor-ambassador-sff-2023-1.png" alt="Image 1" onclick="openLightbox(62)">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-carta-investor-ambassador-sff-2023-2.png" alt="Image 2" onclick="openLightbox(63)">
      </div>
  </div> 

<!-- Extra Space vertical padding  -->

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>November2023: Speaker - At Hustle Fund Angel Squad event in Singapore in November 2023</h2>
    <p>Topic: Evolution of Bitcoin and Web3 in next coming 1 year </p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-hustlefund-angelsquad-crypto-nov2023-1.png" alt="Image 1" onclick="openLightbox(64)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-hustlefund-angelsquad-crypto-nov2023-2.png" alt="Image 2" onclick="openLightbox(65)">
      </div>
  </div>

<!-- Extra Space vertical padding  -->

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>July2023: Judge for Hackcelerator AI Startup Competition organised by Singapore Govt through MAS </h2>
    <p>Judge: for MAS AI Competition to evaluate global Startups for upcoming SFF 2023 Singapore startups !</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/judge-series-sagungarg-singapore-mas-ai-fintech-challenge.png" alt="Image 1" onclick="openLightbox(66)">
      </div>
  </div>

<!-- Extra Space vertical padding  -->

  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>June2023: Speaker - Master Class in Zurich for, Tenity(formerly F10 Batch)</h2>
    <p>Judge: for MAS AI Competition to evaluate global Startups for upcoming SFF 2023 Singapore startups ! </p>
    <a href="https://www.tenity.com" target="_blank" rel="noopener noreferrer">Tenity Accelerator</a>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-zurich-master-class-tenity-batch-jun2023.png" alt="Image 1" onclick="openLightbox(67)">
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