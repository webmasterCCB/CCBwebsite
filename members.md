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
        <li><strong>June 2, 2026:</strong> Carnegie Hall Final Preparations <a href="#">View</a></li>
        <li><strong>May 26, 2026:</strong> Spring Concert Thank You & Summer Plans <a href="#">View</a></li>
        <li><strong>May 19, 2026:</strong> WUGA Radio Feature & Press Coverage <a href="#">View</a></li>
        <li><strong>May 12, 2026:</strong> Carnegie Hall Rehearsal Schedule Updates <a href="#">View</a></li>
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
      
      <h4>Director's Recording Suggestions</h4>
      <p><em>Michael's recommended recordings and performances for listening/study:</em></p>
      <ul class="recordings-list">
        <li><strong>Short videos about intonation - these are worth your time. Good intonation makes a big difference on impact, even if the audience doesn't know why!</strong></li>
        <li><a href="https://www.youtube.com/watch?v=K2qEdE6wjvM" target="_blank">Just Intonation & Chord Adjustments</a></li>
        <li><a href="https://www.youtube.com/watch?v=Yqa2Hbb_eIs" target="_blank">Equal Temperament vs Just Intonation </a></li>
        <li><a href="https://www.youtube.com/watch?v=VHwnSJTefNo" target="_blank">Just Intonation vs Equal Temperament | Sounds Good</a></li>
        <li><a href="https://www.youtube.com/watch?v=kRui9apjWAY" target="_blank">A Bach prelude in three different temperaments</a></li>
      </ul>
      <p><em>Last updated: June 9, 2026</em></p>
    </div>
  </div>

  <!-- ACCORDION SECTION 3: REHEARSAL SCHEDULE -->
  <div class="accordion-item">
    <button class="accordion-header" onclick="toggleAccordion(this)">
      <span class="accordion-title">Rehearsal Schedule (Detailed schedule coming soon)</span>
      <span class="accordion-icon">+</span>
    </button>
    <div class="accordion-body">
      <p><strong>Weekly Rehearsals:</strong> Tuesdays 6:30 PM - 8:00 PM</p>
      <p><strong>Location:</strong> Ligotti Hall (June 9 and 16, then back to PAC/Orchestra Room)</p>
      <p><a href="{{ '/assets/pdfs/rehearsal-schedule.pdf' | relative_url }}" class="btn-link">📄 Download Full Schedule (PDF)</a></p>
      <p><em>PDF updated: [Date will be updated 2-3x per year]</em></p>
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
