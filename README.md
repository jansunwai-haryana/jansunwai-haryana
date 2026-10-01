# 🇮🇳 JanSunwai Haryana

### आपकी शिकायत, आपकी आवाज़ — समाधान तक निगरानी

JanSunwai Haryana एक प्रस्तावित नागरिक शिकायत एवं निगरानी मंच है,
जिसका उद्देश्य नागरिकों को अपनी समस्याओं को व्यवस्थित तरीके से
दर्ज करने और उनकी स्थिति Track करने की सुविधा देना है।

---

## 🌐 मुख्य सुविधाएँ

- 📝 शिकायत दर्ज करना
- 🔎 Complaint ID से शिकायत Track करना
- 📍 जिला चुनने की सुविधा
- 🏢 संबंधित विभाग चुनना
- 📎 फोटो / दस्तावेज़ upload करने की सुविधा
- 📊 शिकायत की वर्तमान स्थिति
- 🔄 Reopen / Appeal सुविधा
- 📱 Mobile Friendly Design

---

## 📋 शिकायत की प्रक्रिया

एक शिकायत निम्न चरणों से गुजर सकती है:

1. शिकायत दर्ज
2. सत्यापन
3. विभाग को भेजी गई
4. अधिकारी को आवंटित
5. कार्रवाई
6. निस्तारण
7. अपील / Reopen

---

## 🆔 Complaint ID

शिकायत दर्ज होने के बाद नागरिक को एक
unique Complaint ID दी जाती है।

उदाहरण:

`JSH-2026-123456`

इसी ID का उपयोग शिकायत की स्थिति देखने के लिए किया जा सकता है।

---

## ⚠️ महत्वपूर्ण सूचना

यह वर्तमान में एक **Private / Proposed Citizen Platform
Prototype** है।

यह Government of Haryana या CM Window का आधिकारिक पोर्टल नहीं है।

यह prototype किसी सरकारी विभाग की ओर से शिकायत पर
कार्रवाई की गारंटी नहीं देता।

भविष्य में संबंधित सरकारी विभागों के साथ औपचारिक
authorization / integration होने पर इसे आधिकारिक
प्रणाली से जोड़ा जा सकता है।

---

## 💻 Technology

इस prototype में:

- HTML
- CSS
- JavaScript
- Browser Local Storage

का उपयोग किया गया है।

---

## 🚀 Future Development

भविष्य के version में निम्न सुविधाएँ जोड़ी जा सकती हैं:

- 🔐 Mobile OTP Login
- 🗄️ Real Database
- 👨‍💼 Admin Dashboard
- 🏢 Department Dashboard
- 📤 वास्तविक File Upload
- 📱 SMS / WhatsApp Notifications
- 🔔 Complaint Status Notifications
- 📊 District-wise Dashboard
- 📈 Department Performance Reports
- 🔄 Appeal & Reopen System
- 🗺️ Location / GPS Support
- 🔑 अधिकारी Login
- 🧾 Complaint History

---

## 📞 Contact

**Project:** JanSunwai Haryana

**Tagline:**  
आपकी शिकायत, आपकी आवाज़ — समाधान तक निगरानी

---

## © Copyright

© 2026 JanSunwai Haryana

Private Prototype.
<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>JanSunwai Haryana | आपकी शिकायत, आपकी आवाज़</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: Arial, "Noto Sans Devanagari", sans-serif;
    }

    body {
      background: #f4f7fb;
      color: #172033;
      line-height: 1.6;
    }

    header {
      background: linear-gradient(135deg, #123c69, #176b87);
      color: white;
      padding: 18px 5%;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 3px 12px rgba(0,0,0,.15);
    }

    .nav {
      max-width: 1100px;
      margin: auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;
    }

    .logo {
      font-size: 22px;
      font-weight: 800;
    }

    .logo small {
      display: block;
      font-size: 11px;
      font-weight: normal;
      opacity: .9;
    }

    nav {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
      justify-content: center;
    }

    nav button {
      background: transparent;
      color: white;
      border: 1px solid rgba(255,255,255,.4);
      padding: 8px 12px;
      border-radius: 7px;
      cursor: pointer;
    }

    nav button:hover {
      background: rgba(255,255,255,.15);
    }

    .hero {
      background: linear-gradient(135deg, #e8f5ff, #ffffff);
      padding: 65px 5%;
      text-align: center;
    }

    .hero-content {
      max-width: 850px;
      margin: auto;
    }

    .hero h1 {
      font-size: clamp(30px, 6vw, 52px);
      color: #123c69;
      margin-bottom: 12px;
    }

    .hero p {
      font-size: 18px;
      color: #4d5b6a;
      margin-bottom: 25px;
    }

    .tagline {
      color: #176b87;
      font-weight: bold;
      margin-bottom: 25px;
    }

    .btn {
      display: inline-block;
      border: none;
      border-radius: 9px;
      padding: 13px 22px;
      margin: 5px;
      font-size: 15px;
      font-weight: bold;
      cursor: pointer;
      background: #176b87;
      color: white;
    }

    .btn:hover {
      opacity: .9;
      transform: translateY(-1px);
    }

    .btn.secondary {
      background: white;
      color: #176b87;
      border: 1px solid #176b87;
    }

    section {
      padding: 50px 5%;
    }

    .container {
      max-width: 1050px;
      margin: auto;
    }

    .section-title {
      text-align: center;
      margin-bottom: 30px;
    }

    .section-title h2 {
      color: #123c69;
      font-size: 30px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .card {
      background: white;
      padding: 22px;
      border-radius: 13px;
      box-shadow: 0 4px 18px rgba(0,0,0,.07);
      text-align: center;
    }

    .card .icon {
      font-size: 35px;
      margin-bottom: 10px;
    }

    .card h3 {
      color: #123c69;
      margin-bottom: 8px;
    }

    .form-box {
      background: white;
      padding: 28px;
      border-radius: 15px;
      box-shadow: 0 4px 20px rgba(0,0,0,.08);
      max-width: 850px;
      margin: auto;
    }

    .form-group {
      margin-bottom: 17px;
    }

    label {
      display: block;
      font-weight: bold;
      margin-bottom: 6px;
      color: #26364a;
    }

    input,
    select,
    textarea {
      width: 100%;
      padding: 12px;
      border: 1px solid #ccd5df;
      border-radius: 8px;
      font-size: 15px;
      outline: none;
      background: white;
    }

    input:focus,
    select:focus,
    textarea:focus {
      border-color: #176b87;
      box-shadow: 0 0 0 2px rgba(23,107,135,.1);
    }

    textarea {
      min-height: 130px;
      resize: vertical;
    }

    .track-box {
      max-width: 650px;
      margin: auto;
      background: white;
      padding: 28px;
      border-radius: 15px;
      box-shadow: 0 4px 20px rgba(0,0,0,.08);
    }

    #result {
      margin-top: 20px;
    }

    .status-box {
      background: #eef8f2;
      border-left: 5px solid #20834c;
      padding: 18px;
      border-radius: 8px;
    }

    .timeline {
      margin-top: 18px;
    }

    .timeline-item {
      padding: 12px 15px;
      border-left: 3px solid #176b87;
      margin-left: 8px;
      margin-bottom: 10px;
      background: #f7fafc;
    }

    .about {
      background: #eef5fa;
    }

    .notice {
      background: #fff8df;
      border: 1px solid #e8cf72;
      padding: 18px;
      border-radius: 10px;
      margin-top: 20px;
    }

    footer {
      background: #123c69;
      color: white;
      padding: 30px 5%;
      text-align: center;
    }

    footer p {
      margin: 5px;
      opacity: .9;
    }

    .hidden {
      display: none;
    }

    .success {
      background: #e8f8ee;
      border: 1px solid #9bd2ad;
      color: #176b3d;
      padding: 15px;
      border-radius: 8px;
      margin-top: 15px;
    }

    .error {
      background: #fff0f0;
      border: 1px solid #e1aaaa;
      color: #a12626;
      padding: 15px;
      border-radius: 8px;
      margin-top: 15px;
    }

    @media (max-width: 800px) {
      .cards {
        grid-template-columns: repeat(2, 1fr);
      }

      .nav {
        flex-direction: column;
      }

      nav {
        width: 100%;
      }
    }

    @media (max-width: 500px) {
      .cards {
        grid-template-columns: 1fr;
      }

      section {
        padding: 38px 4%;
      }

      .form-box,
      .track-box {
        padding: 20px;
      }

      nav button {
        font-size: 12px;
        padding: 7px 9px;
      }
    }
  </style>
</head>

<body>

<!-- HEADER -->
<header>
  <div class="nav">

    <div class="logo">
      जनसुनवाई हरियाणा
      <small>JanSunwai Haryana</small>
    </div>

    <nav>
      <button onclick="goTo('home')">Home</button>
      <button onclick="goTo('complaint')">शिकायत दर्ज करें</button>
      <button onclick="goTo('track')">शिकायत Track करें</button>
      <button onclick="goTo('about')">About</button>
    </nav>

  </div>
</header>


<!-- HERO -->
<section class="hero" id="home">

  <div class="hero-content">

    <h1>जनसुनवाई हरियाणा</h1>

    <div class="tagline">
      आपकी शिकायत, आपकी आवाज़ — समाधान तक निगरानी
    </div>

    <p>
      नागरिक शिकायतों को व्यवस्थित रूप से दर्ज करने,
      ट्रैक करने और उनकी स्थिति देखने के लिए प्रस्तावित नागरिक मंच।
    </p>

    <button class="btn" onclick="goTo('complaint')">
      📝 शिकायत दर्ज करें
    </button>

    <button class="btn secondary" onclick="goTo('track')">
      🔎 शिकायत Track करें
    </button>

  </div>

</section>


<!-- FEATURES -->
<section>

  <div class="container">

    <div class="section-title">
      <h2>हम क्या सुविधा देते हैं?</h2>
    </div>

    <div class="cards">

      <div class="card">
        <div class="icon">📝</div>
        <h3>शिकायत दर्ज</h3>
        <p>अपनी समस्या की जानकारी दर्ज करें।</p>
      </div>

      <div class="card">
        <div class="icon">🔎</div>
        <h3>Track करें</h3>
        <p>Complaint ID से शिकायत की स्थिति देखें।</p>
      </div>

      <div class="card">
        <div class="icon">📊</div>
        <h3>Status</h3>
        <p>शिकायत किस चरण में है, देखें।</p>
      </div>

      <div class="card">
        <div class="icon">🔄</div>
        <h3>Appeal</h3>
        <p>समस्या का समाधान न होने पर पुनः अनुरोध करें।</p>
      </div>

    </div>

  </div>

</section>


<!-- COMPLAINT -->
<section id="complaint">

  <div class="container">

    <div class="section-title">
      <h2>📝 शिकायत दर्ज करें</h2>
      <p>नीचे अपनी शिकायत की जानकारी भरें।</p>
    </div>

    <div class="form-box">

      <form id="complaintForm">

        <div class="form-group">
          <label>नाम *</label>
          <input type="text" id="name" required placeholder="अपना नाम लिखें">
        </div>

        <div class="form-group">
          <label>मोबाइल नंबर *</label>
          <input
            type="tel"
            id="mobile"
            required
            maxlength="10"
            placeholder="10 अंकों का मोबाइल नंबर">
        </div>

        <div class="form-group">
          <label>जिला *</label>

          <select id="district" required>

            <option value="">जिला चुनें</option>

            <option>Ambala</option>
            <option>Bhiwani</option>
            <option>Charkhi Dadri</option>
            <option>Faridabad</option>
            <option>Fatehabad</option>
            <option>Gurugram</option>
            <option>Hisar</option>
            <option>Jhajjar</option>
            <option>Jind</option>
            <option>Kaithal</option>
            <option>Karnal</option>
            <option>Kurukshetra</option>
            <option>Mahendragarh</option>
            <option>Nuh</option>
            <option>Palwal</option>
            <option>Panchkula</option>
            <option>Panipat</option>
            <option>Rewari</option>
            <option>Rohtak</option>
            <option>Sirsa</option>
            <option>Sonipat</option>
            <option>Yamunanagar</option>

          </select>

        </div>

        <div class="form-group">
          <label>विभाग *</label>

          <select id="department" required>

            <option value="">विभाग चुनें</option>
            <option>शिक्षा विभाग</option>
            <option>जन स्वास्थ्य विभाग</option>
            <option>बिजली विभाग</option>
            <option>नगर पालिका / नगर निगम</option>
            <option>लोक निर्माण विभाग</option>
            <option>पुलिस विभाग</option>
            <option>राजस्व विभाग</option>
            <option>कृषि विभाग</option>
            <option>पंचायत विभाग</option>
            <option>अन्य</option>

          </select>

        </div>

        <div class="form-group">
          <label>शिकायत का विषय *</label>

          <input
            type="text"
            id="subject"
            required
            placeholder="शिकायत का विषय लिखें">

        </div>

        <div class="form-group">
          <label>शिकायत का विवरण *</label>

          <textarea
            id="description"
            required
            placeholder="अपनी पूरी समस्या विस्तार से लिखें"></textarea>

        </div>

        <div class="form-group">
          <label>फोटो / दस्तावेज़</label>

          <input
            type="file"
            id="document"
            accept="image/*,.pdf,.doc,.docx">

        </div>

        <button class="btn" type="submit">
          शिकायत जमा करें
        </button>

      </form>

      <div id="complaintMessage"></div>

    </div>

  </div>

</section>


<!-- TRACK -->
<section id="track">

  <div class="container">

    <div class="section-title">
      <h2>🔎 शिकायत Track करें</h2>
      <p>अपनी Complaint ID डालकर स्थिति देखें।</p>
    </div>

    <div class="track-box">

      <input
        type="text"
        id="trackId"
        placeholder="उदाहरण: JSH-2026-123456">

      <button
        class="btn"
        onclick="trackComplaint()">
        Track Complaint
      </button>

      <div id="result"></div>

    </div>

  </div>

</section>


<!-- ABOUT -->
<section class="about" id="about">

  <div class="container">

    <div class="section-title">
      <h2>ℹ️ JanSunwai Haryana के बारे में</h2>
    </div>

    <div class="form-box">

      <p>
        <strong>JanSunwai Haryana</strong> एक प्रस्तावित नागरिक
        शिकायत एवं निगरानी मंच है, जिसका उद्देश्य नागरिकों को
        अपनी समस्याओं को व्यवस्थित तरीके से दर्ज और ट्रैक करने
        की सुविधा देना है।
      </p>

      <div class="notice">

        <strong>महत्वपूर्ण सूचना:</strong>

        <br><br>

        यह वेबसाइट वर्तमान में एक
        <strong>निजी / प्रस्तावित नागरिक मंच का prototype</strong> है।

        <br><br>

        यह Government of Haryana या CM Window का आधिकारिक
        पोर्टल नहीं है और किसी सरकारी विभाग की ओर से
        शिकायत पर कार्रवाई की गारंटी नहीं देता।

        <br><br>

        भविष्य में सरकारी विभाग के साथ औपचारिक integration /
        authorization होने पर इसकी सुविधाओं को आधिकारिक
        प्रणाली से जोड़ा जा सकता है।

      </div>

    </div>

  </div>

</section>


<!-- FOOTER -->
<footer>

  <p><strong>JanSunwai Haryana</strong></p>

  <p>
    आपकी शिकायत, आपकी आवाज़ — समाधान तक निगरानी
  </p>

  <p>
    © 2026 JanSunwai Haryana — Private Prototype
  </p>

</footer>


<script>

  /*
   * DEMO DATABASE
   * -------------------------
   * शिकायतें browser के localStorage में save होंगी।
   * असली website में server/database की जरूरत होगी।
   */

  function generateComplaintId() {

    const year = new Date().getFullYear();

    const number = Math.floor(
      100000 + Math.random() * 900000
    );

    return `JSH-${year}-${number}`;
  }


  function goTo(id) {

    const element = document.getElementById(id);

    if (element) {
      element.scrollIntoView({
        behavior: "smooth"
      });
    }

  }


  document
    .getElementById("complaintForm")
    .addEventListener("submit", function(event) {

      event.preventDefault();

      const name =
        document.getElementById("name").value.trim();

      const mobile =
        document.getElementById("mobile").value.trim();

      const district =
        document.getElementById("district").value;

      const department =
        document.getElementById("department").value;

      const subject =
        document.getElementById("subject").value.trim();

      const description =
        document.getElementById("description").value.trim();

      const documentFile =
        document.getElementById("document").files[0];

      if (!/^[0-9]{10}$/.test(mobile)) {

        document.getElementById(
          "complaintMessage"
        ).innerHTML = `
          <div class="error">
            कृपया सही 10 अंकों का मोबाइल नंबर डालें।
          </div>
        `;

        return;
      }


      const complaintId = generateComplaintId();


      const complaint = {

        id: complaintId,

        name: name,

        mobile: mobile,

        district: district,

        department: department,

        subject: subject,

        description: description,

        fileName:
          documentFile
            ? documentFile.name
            : "",

        status: "दर्ज",

        date:
          new Date().toLocaleString("hi-IN")

      };


      const oldComplaints =
        JSON.parse(
          localStorage.getItem("janSunwaiComplaints")
        ) || [];


      oldComplaints.push(complaint);


      localStorage.setItem(
        "janSunwaiComplaints",
        JSON.stringify(oldComplaints)
      );


      document.getElementById(
        "complaintMessage"
      ).innerHTML = `

        <div class="success">

          <strong>✅ शिकायत सफलतापूर्वक दर्ज हो गई!</strong>

          <br><br>

          आपकी Complaint ID:

          <br>

          <strong style="font-size:22px;">
            ${complaintId}
          </strong>

          <br><br>

          इस ID को सुरक्षित रखें। इसी से आप
          अपनी शिकायत Track कर सकते हैं।

        </div>

      `;


      document
        .getElementById("complaintForm")
        .reset();

    });


  function trackComplaint() {

    const id =
      document
        .getElementById("trackId")
        .value
        .trim()
        .toUpperCase();


    const complaints =
      JSON.parse(
        localStorage.getItem("janSunwaiComplaints")
      ) || [];


    const complaint =
      complaints.find(
        item => item.id === id
      );


    if (!complaint) {

      document.getElementById(
        "result"
      ).innerHTML = `

        <div class="error">

          ❌ इस Complaint ID से कोई
          demo complaint नहीं मिली।

          <br><br>

          ध्यान दें: इस prototype में
          शिकायत उसी browser/device में
          stored रहती है जिसमें वह दर्ज की गई थी।

        </div>

      `;

      return;
    }


    document.getElementById(
      "result"
    ).innerHTML = `

      <div class="status-box">

        <h3>शिकायत मिली ✅</h3>

        <br>

        <p>
          <strong>Complaint ID:</strong>
          ${complaint.id}
        </p>

        <p>
          <strong>नाम:</strong>
          ${complaint.name}
        </p>

        <p>
          <strong>जिला:</strong>
          ${complaint.district}
        </p>

        <p>
          <strong>विभाग:</strong>
          ${complaint.department}
        </p>

        <p>
          <strong>विषय:</strong>
          ${complaint.subject}
        </p>

        <p>
          <strong>स्थिति:</strong>
          ${complaint.status}
        </p>

        <p>
          <strong>दर्ज करने की तारीख:</strong>
          ${complaint.date}
        </p>

        <div class="timeline">

          <div class="timeline-item">
            ✅ शिकायत दर्ज
          </div>

          <div class="timeline-item">
            ⏳ सत्यापन — लंबित
          </div>

          <div class="timeline-item">
            ⏳ विभाग को भेजी गई — लंबित
          </div>

          <div class="timeline-item">
            ⏳ अधिकारी को आवंटित — लंबित
          </div>

          <div class="timeline-item">
            ⏳ कार्रवाई — लंबित
          </div>

          <div class="timeline-item">
            ⏳ निस्तारण / अपील
          </div>

        </div>

      </div>

    `;

  }

</script>

</body>
</html>
