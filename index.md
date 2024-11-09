---
layout: default
---

<style>
  .tab-container {
    display: flex;
    border-bottom: 2px solid #e0e0e0;
    padding: 0 16px;
    background-color: #f1f1f1;
  }

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

## [About](https://sagungarg.com/about) my expertise: CTO/Founder: [Sagun](https://x.com/sagungarg). You can also find me on linkedin [Sagun](https://www.linkedin.com/in/sagungarg)

**Entrepreneurship[(poem)](https://sagungarg.com/0-poem) for me is a self discovery of a polymath within you while you solve a problem creating something: Along the way you sell value to stakeholders, you enagage in resource mobilization & cultivate skewed skills (Polyglot: Programmer in 9+ languages, System Architect, Engineering Manager, Product Owner, Product Manager & DevOps Expert) to deliver a vision inspite of the constraints.**

- 🗣 **Brief**: Currently serving as Global Innovation Director - Software Engineering & Enterprise Architecture at [Bank Julius Baer](https://www.juliusbaer.com/). In my past life I have been a [repeat](https://sagungarg.com/1-previous-startups) Founder/CTO with 3 x startups [DevTools, CareerTech, PropTech] built with AI/ML to craft data products specially in architectures that are characterised by time-series, textual, geospatial, bigdata, nosql & erratic nature of data. I have also played couple of stints of CTO-on-Hire to turn around two(2) pre-Series A startups in Singapore & Hong Kong respectively. 

- 💬 **Speaker/Judging/Presenter Series**: 

  - Stay tuned...More talks will be updated soon...

  <!-- Tab Navigation -->
  <div class="tab-container">
    <button class="tab-button" onclick="openTab(event, 'tab-btc')">Bitcoin</button>
    <button class="tab-button" onclick="openTab(event, 'tab-aiml')">AI/ML</button>
    <button class="tab-button" onclick="openTab(event, 'tab-fndr')">Founder</button>
    <button class="tab-button" onclick="openTab(event, 'tab-avc')">Angel/VC</button>
  </div>


  <div id="tab-btc" class="tab-content" style="display: block;">  
    <h2>October 2024: Masterclass at NUS MBA Business School</h2>
    <p>Topic: "Microstrategy: Modern Corporate Finance Case Study on Bitcoin Treasury</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-1.png" alt="Image 1" onclick="openLightbox(0)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-2.png" alt="Image 2" onclick="openLightbox(1)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-3.png" alt="Image 3" onclick="openLightbox(2)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-4.png" alt="Image 4" onclick="openLightbox(3)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-btc-treasury-microstrategy-saylor-masterclass-talk-nus-mba-business-school-singapore-october2024-5.png" alt="Image 5" onclick="openLightbox(4)">
      </div>
    </div>   

    >     
    <!-- Extra Space vertical padding  -->
  
  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>October 2024: Launch of AI CTO Program: Singapore Google Office Panel Discussion</h2>
    <p>Topic: Building a Sustainable COE - AI CTO Program</p>  
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-bitcoinconference-1.png" alt="Image 1" onclick="openLightbox(5)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-bitcoinconference-2.png" alt="Image 2" onclick="openLightbox(6)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-bitcoinconference-3.png" alt="Image 3" onclick="openLightbox(7)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-bitcoinconference-4.png" alt="Image 4" onclick="openLightbox(8)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-ai-cto-launch-industry-panel-google-office-singapore-october2024-bitcoinconference-5.png" alt="Image 5" onclick="openLightbox(9)">
      </div> 
    </div>
    >     
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
    >     
    <!-- Extra Space vertical padding  -->

  <div id="tab-btc" class="tab-content" style="display: block;">
    <h2>October 2024: Bitcoin Conference 2024 at Amsterdam Panel amongst industry experts</h2>
    <p>Topic: Bitcoin Wealth & Inheritance</p> 
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-1.png" alt="Image 1" onclick="openLightbox(15)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-2.png" alt="Image 2" onclick="openLightbox(16)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-amsterdam-europe-october2024-bitcoinconference-3.png" alt="Image 3" onclick="openLightbox(17)">
      </div> 
    </div>
    >     
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
    >     
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

    >     
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

    >     
    <!-- Extra Space vertical padding  -->
  <div id="tab-aiml" class="tab-content" style="display: block;">
    <h2>September 2024: Panel talk with industry experts organised by ABS and MAS</h2>
    <p>Topic: Unlocking the Future: Key Considerations and Path to Capture Generative AI Value</p>
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-1.png" alt="Image 1" onclick="openLightbox(28)">
        <img src="https://sagungarg.com/assets/img/speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-2.png" alt="Image 2" onclick="openLightbox(29)">
        <img src="https://sagungarg.com/assets/img/speaker-series-panel-sagun-garg-singapore-september2024-ai-ml-conference-abs-mas-2024-3.png" alt="Image 3" onclick="openLightbox(30)">
      </div> 

    >     
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

  - **August 2024**: Evaluator for the Global FinTech Hackcelerator at Singapore Fintech Festival

      > **Topic: "Judge & Evaluator for AI Startups for applications in Singapore Fintetc Festival (SFF 2024)"**

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/judge-series-sagungarg-singapore-sff-ai-hackcelerator-2024-challenge-1.png" alt="Image 1" onclick="openLightbox(35)">
        <img src="https://sagungarg.com/assets/img/judge-series-sagungarg-singapore-sff-ai-hackcelerator-2024-challenge-2.png" alt="Image 2" onclick="openLightbox(36)">
      </div> 

  - **July 2024**: Panel discussion on mainstage at Bitcoin Nashville Conference with Caitlin Long, Miles Paschini and Sagun Garg

      > **Topic: ”Bitcoin's Role in Traditional Banks”**

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-1.png" alt="Image 1" onclick="openLightbox(37)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-2.png" alt="Image 2" onclick="openLightbox(38)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-3.png" alt="Image 3" onclick="openLightbox(39)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-usa-july2024-bitcoinconference-nashville-2024-4.png" alt="Image 4" onclick="openLightbox(40)">
      </div>  

  - **June 2024**: Industry Competition in GenAI LLMs: Google + EDB(Economic Development Board) - Industry Competition AI Trailblazers

      > **Topic: "GenAI Narrative builder for protfolio re-assement for switching positions using factual references of internal publications"**

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/presenter-series-singapore-google-edb-AI-llm-genai-trailblazers-competition-1.png" alt="Image 1" onclick="openLightbox(41)">
        <img src="https://sagungarg.com/assets/img/presenter-series-singapore-google-edb-AI-llm-genai-trailblazers-competition-2.png" alt="Image 2" onclick="openLightbox(42)">
        <img src="https://sagungarg.com/assets/img/presenter-series-singapore-google-edb-AI-llm-genai-trailblazers-competition-3.png" alt="Image 3" onclick="openLightbox(43)">
        <img src="https://sagungarg.com/assets/img/presenter-series-singapore-google-edb-AI-llm-genai-trailblazers-competition-4.png" alt="Image 4" onclick="openLightbox(44)">
      </div>

  - **May 2024**: Panel discussion at Bitcoin Conference Asia 2024 - Hong Kong
    
      > **Topic: "Miniscript & Bitcoin Inheritance Planning"**

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-1.png" alt="Image 1" onclick="openLightbox(45)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-2.png" alt="Image 2" onclick="openLightbox(46)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-3.png" alt="Image 3" onclick="openLightbox(47)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-may2024-miniscript-bitcoin-inheritance-bitcoinconference-hongkong-4.png" alt="Image 4" onclick="openLightbox(48)">
      </div>
    
  - **May 2024**: Students from Indiana University - Kelley School of Business

      > **Topic: Web3 Fireside Chat on Bitcoin Crypto and Tokenization**

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-singapore-students-business-school-sagungarg-Bitcoin-Digital-Assets-1.png" alt="Image 1" onclick="openLightbox(49)">
        <img src="https://sagungarg.com/assets/img/speaker-series-singapore-students-business-school-sagungarg-Bitcoin-Digital-Assets-2.png" alt="Image 2" onclick="openLightbox(50)">
        <img src="https://sagungarg.com/assets/img/speaker-series-singapore-students-business-school-sagungarg-Bitcoin-Digital-Assets-3.png" alt="Image 3" onclick="openLightbox(51)">
        <img src="https://sagungarg.com/assets/img/speaker-series-singapore-students-business-school-sagungarg-Bitcoin-Digital-Assets-4.png" alt="Image 4" onclick="openLightbox(52)">
      </div>

  - **March 2024**: Guest speaker organised by Plug & Play Tech Center & Aelf Blockchain on Layer 2 solutions on Bitcoin

    > **Topic: Web3: Blockhain and RWA Tokenization**
    [Linkedin Post](https://www.linkedin.com/posts/sagungarg_web3-defi-tokenisation-activity-7172541301182197760-ZBvB?utm_source=share&utm_medium=member_desktop) | [Plug & Play Tech Center](https://www.plugandplaytechcenter.com/) | [Aelf Blockchain](https://aelf.com/)

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-march2024-plugandplay-aelf-web3-from-web2-journey-singapore-1.png" alt="Image 1" onclick="openLightbox(53)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-march2024-plugandplay-aelf-web3-from-web2-journey-singapore-2.png" alt="Image 2" onclick="openLightbox(54)">
      </div>

  <!-- - **February 2024**: SG-HK Corporate Innovation Program for Tenity Funded Startups

    ![pic](https://sagungarg.com/assets/img/speaker-series-sagun-garg-master-class-tenity-singapore-corporate-innovation-partnerships.png) -->

  - **January 2024**: Investor - Judge for Tenity Singapore Incubation Batch 7

    > **Theme of Startups Pitching: Fintech, Insurtech, or RegTech, DeepTech, Web3, Sustainable Finance, LegalTech, CryptoFinance startups** | [LINK TO EVENT](https://www.tenity.com/programs/singapore-incubation-batch-7)
      
      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-tenity-singapore-incubation-batch7-1.png" alt="Image 1" onclick="openLightbox(55)">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-tenity-singapore-incubation-batch7-2.png" alt="Image 2" onclick="openLightbox(56)">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-tenity-singapore-incubation-batch7-3.png" alt="Image 2" onclick="openLightbox(57)">
      </div>

  - **December 2023**: Competition: Corporate Innovation Challenge at Singapore Fintech Festival - Launchpad Team - Bank Julius Baer

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-garg-web3-singapore-smu-professor.png" alt="Image 1" onclick="openLightbox(55)">
      </div>

  - **November 2023**: Competition: Corporate Innovation Challenge at Singapore Fintech Festival - Launchpad Team - Bank Julius Baer

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/competition-sagun-garg-sff-launchpad-booth-sophie-product-1.png" alt="Image 1" onclick="openLightbox(55)">
      </div>

  - **November 2023**: Investor - Judge at Carta Investor program at Singapore Fintech Festival 2023

    [LINK TO EVENT](https://www.fintechfestival.sg/investor-hours)

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-carta-investor-ambassador-sff-2023-1.png" alt="Image 1" onclick="openLightbox(55)">
        <img src="https://sagungarg.com/assets/img/judge-sagun-garg-carta-investor-ambassador-sff-2023-2.png" alt="Image 2" onclick="openLightbox(56)">
      </div>
    
  - **November 2023**: Speaker - At Hustle Fund Angel Squad event in Singapore in November 2023 

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-hustlefund-angelsquad-crypto-nov2023-1.png" alt="Image 1" onclick="openLightbox(55)">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-hustlefund-angelsquad-crypto-nov2023-2.png" alt="Image 2" onclick="openLightbox(56)">
      </div>
  
  - **July 2023**: Judge - for MAS AI Competition to evaluate global Startups for upcoming SFF 2023 Singapore startups !

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/judge-series-sagungarg-singapore-mas-ai-fintech-challenge.png" alt="Image 1" onclick="openLightbox(55)">
      </div>
  
  - **June 2023**: Speaker - Master Class in Zurich for, Tenity(https://www.tenity.com/) - formerly F10 Batch

      <div class="scroll-container">
        <img src="https://sagungarg.com/assets/img/speaker-series-sagun-zurich-master-class-tenity-batch-jun2023.png" alt="Image 1" onclick="openLightbox(55)">
      </div>

- ✨ **Current Active Interests**: What keep's me busy these days
  - 💬 &nbsp; Lately my nascent curiosity has been sparked in Quantum Computing influencing the AI/ML space, Gene therapy leveraging AI and private LLMs deployed on edge computing devices. 
  - 🌱 &nbsp;I’m currently experimenting with [Replicate](https://replicate.ai/), [Data Catalogs](https://www.amundsen.io/) & [Vector Search Engines](https://github.com/semi-technologies/weaviate)

- 📝 **Writings**: I like to write newsletter(s), Blog(s) & curate content as note making process to myself
  - **Twitter Curation**: [Twitter](https://twitter.com/sagungarg)
  - **About AI/ML**: [Newsletter](https://polymathai.substack.com)
  - **Startups in General**: [Medium](https://medium.com/@sagungarg)
  - **Linkedin Posts**: [Linkedin](https://www.linkedin.com/in/sagungarg)
  
- 💻 **Serial Entrepreneur x 3**:I am a Tech Entrepreneur at heart (ambidextrous skills to get job done) 
  - **Early Stage Decade Experience**: 11+ years of early stage startup, product and engineering tech stacks.
  - **Bootstrapping**: Startup with Customer Money before seed round
  - **P/M Fit**: Pivoting everything till you hit the target with paying users in a Sizeable market for outsized outcomes
  - **Raising Venture Capital**: Proven track record [Pre-Seed -> Seed -> Pre-SeriesA]
  - **Product Owner**: Experience building & executing Product Roadmaps [Market Sizing, P/M Fit and User Acquisition]
  - **Leading teams**: Building Atleast 20+ developers in CTO capacity
  - **B2B & B2C**: Prior proven experience launching B2C Mobile Products and B2B Enterprise Products 

- ⏱ **CTO-on-Hire x 2**: I have proven ability to turn around AI/ML ventures in CTO-on-Hire capacity. I recently have a track record for two Pre-Series A Startups in Singapore(Supply Chain - Predictive Data Intelligence) and Hong Kong(Ed-Tech - Natural Language Generation Authoring) by stepping in shoes of outgoing Co-Founder/CTO in both ventures respectively to help the Co-Founder/CEO 
  - close Pre-Series A round, 
  - scale prototype to production grade usable product with live users/customers serving fortune 500 customers and 
  - managing engineering teams of 10+ team members. Both startup turn arounds involved managing product strategy, product features, engineering technical debt removal, hiring, devops & technical budgets. It approximately took me 18 months to turn the ship with a lot of support from the team I inherited in these ventures. 

- 💻 **Entrepreneur in Residence x 3**:I have extensive experience as Entrepreneur in Residence in Deeptech products in South East Asia:
  - **Market Sizing**: Define target market, customer persona and go to market strategy
  - **Weekend Prototyping**: Build initial prototype(s) and iterate week on week with user feedback
  - **Cofounder Matching**: Find a Cofounder for the venture with complementary skills
  - **Pitch to VCs**: Investment commitees for initial round of capital
  - **Define KPIs**: Tracking monthly user growth, lead/lag indicators & growth hacking

- 💻 **Hackathons/Competitions**: I am also winner of international Hackathons.
  - **Singapore**: Launchpad's LLM - AI/ML Sophie platform built inside Bank Julius Baer top 6 winner in SFF(Singapore Fintech Festival), 2023 [pic1](https://sagungarg.com/assets/img/sff-launchpad-booth-sophie-product-1.png) & [pic2](https://sagungarg.com/assets/img/sff-launchpad-booth-sophie-product-2.png) 
  - **Singapore**: NEC Labs, 2020 
  - **Singapore**: Microsoft: Global AI/ML Summit, 2019
  - **Mumbai**: India: IIT-B Hackathon, 2015
  - **Dublin**: Web-Summit Alpha Startup Category, 2014
  - **Bangalore**: Poster presentation for VLSI at Intel, 2008
  - **Ahmedabad**: IBM + GIL Project for Gujarat Govt, 2006

## Expert & Specialist in Architecting Systems
- **Data pipelines**: Geospatial, timeseries, streaming  365 days a humming data engine with Validations at data lake level
- **Data Engineering**: AI/ML usecases demand data preparation i.e clean data, wrangle for spotty, missing, malformed, invalid and intermittent empty datapoints
- **Big Data**: Order of billion rows in a single query: Quering datapoints to mathematically handle OLAP processing for B2C or B2B interfaces to run metrics in realtime for users
- **Search Indexes**: Less than 500ms search engine query responses in big payload responses with 100k JSON payloads
- **Predictive Data Intelligence**: Generating and Managing 20 million predictions a day architecture, data warehouses and complex streaming data ingestion

## My Work experience includes
- 💻 **Architecting**: BigData achitectural patterns in AWS Infra jigsaw puzzle
- ⚙️ **Vendor Management** : Navigate "Build vs Buy" to optimise for "startup speed" and avoid "technical debt complexity". This is possible with stable setups for opensource products on BigTech platforms(AWS, Google, Microsoft) with startup credit grants there by direct savings of bills of atleast USD 300k in first 2 years worth of digital infrastructure, developer tools and devops using street smart ideas. 
- 👥 **Mentoring**: Senior engineers, product managers and growth hackers to become leaders by cultivating their skills to manage bigger teams in their respective verticals
- 📋 **Managing Product Roadmaps**: sprints, cost budgets, recruiting, writing detailed specs, product roadmaps and manage release cycles
- 🤖 **Automating**: CI/CD the whole release process to QA, TestFlight, AppStore & Improving the CI/CD pipelines and build times…
- 👥 **Devops**: Improving the PR review experience (using Danger and Vapor Bots to interact with your PRs, among others)
- ⚙️ **Tools**: Providing integration between tools for developers, QA & product (GitHub, JIRA, Lokalize, Figma, TestRails, CI, …)
- ⏱ **Testing Frameworks**: Consulting on testing strategies (project testability, balance between Unit/UI/Snapshot/manual tests, interaction with QA…)
- ✨ And [much more](https://sagungarg.com/0-much-more) 🙂

<!-- Lightbox container -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <span class="lightbox-close" onclick="closeLightbox()">&times;</span>
  <span class="arrow arrow-left" onclick="event.stopPropagation(); changeImage(-1)">&#10094;</span>
  <img id="lightbox-img" src="" alt="" onclick="event.stopPropagation();">
  <span class="arrow arrow-right" onclick="event.stopPropagation(); changeImage(1)">&#10095;</span>
</div>

<script>
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
</script> -->

<!-- Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./2-another-page.html).

[Link to another page copy](./1-previous-startups.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project. -->


<!-- ## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

## Competitions

- 2020 ISPASS Student Travel Award  
- [Research Distinction](https://cns.utexas.edu/undergraduate-education/events/cns-distinctions/2020-distinction-winners#bodun-hucomputer-science) by the College of Natural Sciences


### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
``` -->



