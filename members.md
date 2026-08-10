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

  <!-- ACCORDION SECTION 1: LATEST EMAIL -->
  <div class="accordion-item">
    <button class="accordion-header" onclick="toggleAccordion(this)">
      <span class="accordion-title">Latest Weekly Email (Coming soon!)</span>
      <span class="accordion-icon">+</span>
    </button>
    <div class="accordion-body">
      <div class="email-preview">
        <p><strong>Subject:</strong> [Latest email subject will appear here]</p>
        <p><strong>Date:</strong> [Date]</p>
        <p><strong>Preview:</strong> [First 100 characters of email content...]</p>
        <p><a href="https://mail.google.com/mail/u/0/#inbox" target="_blank" class="btn-link">Read Full Email</a></p>
      </div>
      <hr>
      <h4>Email Archive</h4>
      <ul class="email-archive">
        <li><strong>June 2, 2026:</strong>Coming Soon<a href="#">View</a></li>
      </ul>
    </div>
  </div>

  <!-- ACCORDION SECTION 2: MUSIC & RECORDINGS -->
  <div class="accordion-item">
    <button class="accordion-header" onclick="toggleAccordion(this)">
      <span class="accordion-title">Parts & Recordings</span>
      <span class="accordion-icon">+</span>
    </button>
    <div class="accordion-body">
      <h4>Download your Music for Independence Day concert (July 3rd in Nicholson)</h4>
      <p><a href="https://drive.google.com/drive/u/0/folders/17xr0agQjJwa7wOqleQky7oUYhl5lEOia" target="_blank" class="btn-link">📁 Access Music Google Drive</a></p>
      
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
          <td>Lee Cormon</td>
          <td>Flute</td>
          <td><a href="mailto:lcormon@charter.net">lcormon@charter.net</a></td>
          <td>(706) 308-6147</td>
        </tr>
        <tr>
          <td>Heidi Nibbelink</td>
          <td>Oboe</td>
          <td><a href="mailto:Heidioneile17@gmail.com">Heidioneile17@gmail.com</a></td>
          <td>(706) 818-2904</td>
        </tr>
        <tr>
          <td>Anita Cook</td>
          <td>Clarinet</td>
          <td><a href="mailto:acook53@gmail.com">acook53@gmail.com</a></td>
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
          <td><a href="mailto:kycastleberry@aim.com">kycastleberry@aim.com</a></td>
          <td>(404) 229-3244</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
  
  <!-- ACCORDION SECTION 5: BYLAWS & DOCUMENTS -->
  <div class="accordion-item">
    <button class="accordion-header" onclick="toggleAccordion(this)">
      <span class="accordion-title">Bylaws & Documents (Coming soon)</span>
      <span class="accordion-icon">+</span>
    </button>
    <div class="accordion-body">
      <p><a href="{{ '/assets/pdfs/bylaws.pdf' | relative_url }}" class="btn-link">📄 Classic City Band Bylaws</a></p>
      <p><em>Last updated: [Date]</em></p>
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
        <li><strong><a href="https://www.brassinstrumentworkshop.com/" target="_blank" rel="noopener noreferrer">Brass Instrument Workshop/a></strong> is located in Marietta, GA. Phone number is: 770.565.9949</li>
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
