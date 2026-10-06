---
layout: default
title: Members Only
---

<div id="password-gate" class="password-gate">
  <div class="password-container">
    <h2>Members Area</h2>
    <p>Enter the password to access member resources.</p>
    <input type="password" id="password-input" placeholder="Enter password" onkeypress="checkPassword(event)">
    <button onclick="checkPassword()">Access</button>
    <p id="password-error" class="error-message"></p>
  </div>
</div>

<div id="members-content" class="members-content" style="display: none;">

  <!-- ACCORDION SECTION 1: Carnegie Hall recordings -->
 <div class="accordion-item">
  <button class="accordion-header" onclick="toggleAccordion(this)">
    <span class="accordion-title">Professional Videos of the Carnegie Hall Performance June 28, 2026</span>
    <span class="accordion-icon">+</span>
  </button>

  <div class="accordion-body">

    <p>
      <a href="https://drive.google.com/file/d/1G-j1c4ihoTXJi6506OeiBrx0BNnBZ4hu/view?usp=drive_link"
         target="_blank"
         rel="noopener noreferrer">
        Star Spangled Banner (pieced together videos)
      </a>
    </p>

    <p>
      <a href="https://drive.google.com/file/d/1hYaqnqSCJB2ggcfZiqj6W9ufdGMMTrZf/view?usp=drive_link"
         target="_blank"
         rel="noopener noreferrer">
        Clip from Raiders March
      </a>
    </p>

    <p>
      <a href="https://drive.google.com/file/d/1ne6D-BrGWClglZSiMviKUk0F8BTE98LM/view?usp=drive_link"
         target="_blank"
         rel="noopener noreferrer">
        Clip from Star Wars Theme
      </a>
    </p>

    <p>
      <a href="https://drive.google.com/file/d/1ZUztaUoHzQt6Axorfs0pzmgqfjuHXE76/view?usp=drive_link"
         target="_blank"
         rel="noopener noreferrer">
        Applause in the Carnegie Balconies
      </a>
    </p>

  </div>
</div>

  <!-- ACCORDION SECTION 2: MUSIC & RECORDINGS -->
  <div class="accordion-item">
    <button class="accordion-header" onclick="toggleAccordion(this)">
      <span class="accordion-title">Parts & Recordings</span>
      <span class="accordion-icon">+</span>
    </button>
    <div class="accordion-body">
      <h4>Download your Music for our upcoming concert</h4>
      <p><a href="https://drive.google.com/drive/u/0/folders/17xr0agQjJwa7wOqleQky7oUYhl5lEOia" target="_blank" class="btn-link">📁 Access Music Google Drive</a></p>
      <p><a href="https://classiccityband.org/concerts">Performance Dates</a></p>
  </div>
</div>
<!-- ACCORDION SECTION 3: REHEARSAL SCHEDULE -->
<div class="accordion-item">
  <button class="accordion-header" onclick="toggleAccordion(this)">
    <span class="accordion-title">Rehearsal Schedule</span>
    <span class="accordion-icon">+</span>
  </button>
  <div class="accordion-body">
    <p><strong>Weekly Rehearsals:</strong> Tuesdays 6:30 PM - 8:30 PM</p>
    <p><strong>Location:</strong> Cedar Shoals High School Bandroom</p>
    <p><a href="{{ '/assets/documents/Fall2026schedule.pdf' | relative_url }}" target="_blank" class="btn-link">Fall 2026 Schedule</a></p>
    <p><a href="{{ '/assets/documents/Holiday2026schedule.pdf' | relative_url }}" target="_blank" class="btn-link">Holiday Concert 2026 Schedule</a></p>
    <p><a href="{{ '/assets/documents/Spring2027schedule.pdf' | relative_url }}" target="_blank" class="btn-link">Spring 2027 Schedule</a></p>
    <p><em>Schedules updated as needed</em></p>
  </div>
</div>

  <!-- ACCORDION SECTION 4: CONCERT ATTIRE -->
  <div class="accordion-item">
    <button class="accordion-header" onclick="toggleAccordion(this)">
      <span class="accordion-title">Concert Attire Guidelines</span>
      <span class="accordion-icon">+</span>
    </button>
    <div class="accordion-body">
      <h4>Outdoor Gig</h4>
      <ul>
        <li>White polo shirt</li>
        <li>Khaki bottoms</li>
        <li>Comfortable shoes</li>
      </ul>
      <h4>Concert Black</h4>
      <ul>
        <li>All black, professional clothing</li>
      </ul>
      <h4>Tuxedo</h4>
      <ul>
        <li>Black tuxedo jacket and pants</li>
        <li>White tuxedo shirt</li>
        <li>Black bowtie and cumberbund</li>
        <li>Black socks and Black shoes</li>
        <li>Note: Holiday concerts <i>may</i> have additional allowances</li>
        <li>For more information, including dress for those not wearing a tuxedo, see <a href="https://en.wikipedia.org/wiki/Black_tie" target="_blank">"Black Tie" dress code</a></li>
      </ul>
    </div>
  </div>
<!-- ACCORDION SECTION 6: SECTION LEADERS -->
<div class="accordion-item">
  <button class="accordion-header" onclick="toggleAccordion(this)">
    <span class="accordion-title">Section Leaders</span>
    <span class="accordion-icon">+</span>
  </button>
  <div class="accordion-body">
    <p><em>Contact your section leader with questions or to report absences:</em></p>
    <table class="leaders-table">
      <thead>
        <tr>
          <th>Name</th>
          <th>Instrument</th>
          <th>Email</th>
          <th>Phone</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Lee Carmon</td>
          <td>Flute</td>
          <td><a href="mailto:Lcarmon@charter.net">Lcarmon@charter.net</a></td>
          <td> (706) 338-7794</td>
        </tr>
        <tr>
          <td>Heidi Nibbelink</td>
          <td>Oboe</td>
          <td><a href="mailto:Heidinoelle17@gmail.com">Heidinoelle17@gmail.com</a></td>
          <td>(706) 818-2904</td>
        </tr>
        <tr>
          <td>Anita Cook</td>
          <td>Clarinet</td>
          <td><a href="mailto:acook530@att.net">acook530@att.net</a></td>
          <td>(706) 372-5390</td>
        </tr>
        <tr>
          <td>Kenneth Reid</td>
          <td>Clarinet</td>
          <td><a href="mailto:kreid41@gmail.com">kreid41@gmail.com</a></td>
          <td>(706) 658-6451</td>
        </tr>
        <tr>
          <td>Cynthia Cone</td>
          <td>Saxophone</td>
          <td><a href="mailto:Cynlee63@aol.com">Cynlee63@aol.com</a></td>
          <td>(803) 719-6003</td>
        </tr>
        <tr>
          <td>Karen Castleberry</td>
          <td>Horn</td>
          <td><a href="mailto:kycastleberryod@aim.com">kycastleberryod@aim.com</a></td>
          <td>(404) 229-3244</td>
        </tr>
        <tr>
          <td>Jerry Shannon</td>
          <td>Trumpet</td>
          <td><a href="mailto:jshannon13@gmail.com">jshannon13@gmail.com</a></td>
          <td>(612) 298-0003</td>
        </tr>
        <tr>
          <td>Davis Clark</td>
          <td>Trombone</td>
          <td><a href="mailto:davisbclark@gmail.com">davisbclark@gmail.com</a></td>
          <td>(706) 308-6147</td>
        </tr>
        <tr>
          <td>David Stone</td>
          <td>Euphonium</td>
          <td><a href="mailto:dkstone@earthlink.net">dkstone@earthlink.net</a></td>
          <td>(706) 255-8384</td>
        </tr>
        <tr>
          <td>Tom Hodges</td>
          <td>Tuba</td>
          <td><a href="mailto:tomhodges25@gmail.com">tomhodges25@gmail.com</a></td>
          <td>(706) 318-8580</td>
        </tr>
        <tr>
          <td>Barbara Reid</td>
          <td>Percussion</td>
          <td><a href="mailto:bkreid1953@gmail.com">bkreid1953@gmail.com</a></td>
          <td>(706) 248-8495</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
  
  <!-- ACCORDION SECTION 5: BYLAWS & DOCUMENTS -->
  <div class="accordion-item">
    <button class="accordion-header" onclick="toggleAccordion(this)">
      <span class="accordion-title">Bylaws & Documents</span>
      <span class="accordion-icon">+</span>
    </button>
    <div class="accordion-body">
      <p><a href="{{ '/assets/documents/bylaws.pdf' | relative_url }}" class="btn-link" target="_blank">The Bylaws</a><br>
      <em>Last updated: 6/3/26</em></p>
      <p><a href="{{ '/assets/documents/Inc_Exp_Summ_073126.pdf' | relative_url }}" class="btn-link" target="_blank">Income / Expense Summary PY 25-26</a><br>
      <em>Last updated: 7/31/26</em></p>
      <p><a href="{{ '/assets/documents/FY_27_Budget.pdf' | relative_url }}" class="btn-link" target="_blank">FY 2027 Budget</a><br>
      <em>Last updated: 9/23/26</em></p>
      <p><a href="{{ '/assets/documents/Sponsorship_Fundraising_Letter.pdf' | relative_url }}" class="btn-link" target="_blank">Sponsorship Fundraising Letter</a><br>
      <em>Last updated: 9/9/26</em></p>
    </div>
  </div>

<!-- ACCORDION SECTION 7: RECOMMENDED INSTRUMENT REPAIR -->
  <div class="accordion-item">
    <button class="accordion-header" onclick="toggleAccordion(this)">
      <span class="accordion-title">Recommended Instrument Repair</span>
      <span class="accordion-icon">+</span>
    </button>
    <div class="accordion-body">
      <p><em>Music Repair Shops, as recommended by Classic City Band members:</em></p>
      <ul class="recordings-list">
        <li><strong><a href="https://northgeorgiaband.com"  target="_blank" rel="noopener noreferrer">North Georgia Band</a></strong> is located in Tucker, GA.</li>
        <li><strong><a href="https://www.maxwellmusicsupply.com/" target="_blank" rel="noopener noreferrer">Maxwell Music Supply</a></strong> is located in Elberton, GA. Phone number is: 706.213.7766</li>
        <li><strong><a href="https://www.brassinstrumentworkshop.com/" target="_blank" rel="noopener noreferrer">Brass Instrument Workshop</a></strong> is located in Marietta, GA. Phone number is: 770.565.9949</li>
        <li><strong><a href="https://www.ngahornworks.com/" target="_blank" rel="noopener noreferrer">North Georgia Horn Works</a></strong> is located in Kennesaw, GA. Phone number is: 678.324.7727</li>
      </ul>
      <p><em>Last updated: 7/13/26</em></p>
    </div>
  </div>
</div>

<script>
  // PASSWORD PROTECTION
  const CORRECT_PASSWORD = "Fanfare";

  function checkPassword(event) {
    if (event && event.key !== "Enter") return;
    
    const password = document.getElementById("password-input").value;
    const errorMsg = document.getElementById("password-error");
    
    if (password === CORRECT_PASSWORD) {
      document.getElementById("password-gate").style.display = "none";
      document.getElementById("members-content").style.display = "block";
      localStorage.setItem("members-access", "true");
    } else {
      errorMsg.textContent = "Incorrect password. Try again.";
      document.getElementById("password-input").value = "";
    }
  }

  // CHECK IF ALREADY LOGGED IN
  window.addEventListener("load", function() {
    if (localStorage.getItem("members-access") === "true") {
      document.getElementById("password-gate").style.display = "none";
      document.getElementById("members-content").style.display = "block";
    }
  });

  // ACCORDION FUNCTIONALITY
  function toggleAccordion(button) {
    const body = button.nextElementSibling;
    const icon = button.querySelector(".accordion-icon");
    const isOpen = body.style.display === "block";
    
    // Close all other accordion sections
    document.querySelectorAll(".accordion-body").forEach(el => {
      el.style.display = "none";
    });
    document.querySelectorAll(".accordion-icon").forEach(el => {
      el.textContent = "+";
    });
    
    // Toggle current section
    if (!isOpen) {
      body.style.display = "block";
      icon.textContent = "−";
    }
  }
</script>
