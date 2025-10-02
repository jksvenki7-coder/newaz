# newaz<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>JKS Group Business Platform Fixed</title>
<style>
  body {
    background: #20242b;
    color: #fff;
    font-family: 'Segoe UI', Arial, sans-serif;
    margin: 0;
    padding: 0;
  }
  header {
    background: #141b29;
    color: #00e1ff;
    font-size: 2.3rem;
    font-weight: 700;
    letter-spacing: 2px;
    padding: 20px 0;
    text-align: center;
    text-shadow: 0 0 22px #0fccfcbb;
  }
  nav {
    display: flex;
    justify-content: center;
    gap: 15px;
    padding: 10px 0;
    background: #141b29;
    border-bottom: 2px solid #00e1ff;
  }
  nav button {
    background: none;
    border: 2.5px solid #0fccfc;
    border-radius: 10px;
    color: #0fccfc;
    cursor: pointer;
    font-weight: 700;
    padding: 12px 22px;
    font-size: 1rem;
    user-select: none;
    transition: all 0.3s ease;
  }
  nav button:hover {
    background: #0fccfc;
    color: #202733;
  }
  main {
    max-width: 1100px;
    margin: 30px auto 60px auto;
    padding: 0 15px;
  }
  .dashboard {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(260px,1fr));
    gap: 40px 48px;
    max-width: 930px;
    margin: 30px auto 0 auto;
  }
  .folder-card, .service-card, .category-card {
    background: #23273b;
    border: 3px solid #ffe27f;
    border-radius: 18px;
    padding: 40px 30px;
    font-size: 1.3em;
    font-weight: 700;
    color: #ffe27f;
    box-shadow: 0 0 22px 5px #ffe27fab, 0 7px 42px #102733d8;
    text-align: center;
    cursor: pointer;
    user-select: none;
    transition: all 0.3s ease;
    min-width: 240px;
  }
  .folder-card:hover, .service-card:hover, .category-card:hover {
    background: #ffe27f;
    color: #222a39;
    box-shadow: 0 0 42px 13px #0fccfcbb, 0 8px 42px #23536fab;
    border-color: #0fccfc;
    font-weight: 900;
    transform: scale(1.07);
  }
  .section-title {
    color: #ffe27f;
    font-size: 1.8rem;
    font-weight: 700;
    letter-spacing: 1.2px;
    margin-bottom: 32px;
    text-align: center;
    text-shadow: 0 0 18px #ffe27fac;
  }
  .service-list, .events-categories {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(210px,1fr));
    gap: 26px;
    justify-content: center;
    margin-bottom: 40px;
    margin-top: 28px;
  }
  form.contact-form {
    max-width: 480px;
    margin: 20px auto 50px;
    background: #172440;
    padding: 30px 35px;
    border-radius: 18px;
    border: 2px solid #00e1ff99;
    color: #afdfff;
    font-size: 1.1em;
  }
  form.contact-form label {
    font-weight: 700;
    margin-bottom: 10px;
    display: block;
    color: #8dc5ff;
  }
  form.contact-form input,
  form.contact-form textarea,
  form.contact-form select {
    width: 100%;
    font-size: 16px;
    padding: 14px 18px;
    margin-bottom: 24px;
    border-radius: 10px;
    background: #0f1f3a;
    border: 1.7px solid #38abf7;
    color: #cde4ff;
    box-sizing: border-box;
    resize: vertical;
    outline: none;
    transition: background-color 0.27s ease, border-color 0.3s ease;
  }
  form.contact-form input:focus,
  form.contact-form textarea:focus,
  form.contact-form select:focus {
    background-color: #1b3e7a;
    border-color: #00aeff;
  }
  form.contact-form button {
    width: 100%;
    padding: 18px 0px;
    font-weight: 900;
    font-size: 1.28em;
    color: #192b3a;
    background-color: #00e1ff;
    border: none;
    border-radius: 15px;
    cursor: pointer;
    transition: background-color 0.28s ease;
  }
  form.contact-form button:hover {
    background-color: #3de1ff;
  }
  .back-btn {
    display: block;
    margin: 35px auto 16px;
    width: max-content;
    padding: 20px 70px;
    font-weight: 900;
    font-size: 1.25em;
    color: #202733;
    cursor: pointer;
    border-radius: 18px;
    background-color: #ffe27f;
    border: 3px solid #ffe27f;
    box-shadow: 0 0 32px 10px #ffe27f89;
    user-select: none;
    text-align: center;
    transition: all 0.3s ease;
  }
  .back-btn:hover {
    background-color: #00e1ff;
    color: #fff;
    border-color: #00e1ff;
    box-shadow: 0 0 40px 14px #00e1ffcc;
  }
  video#video {
    max-width: 100%;
    border-radius: 14px;
    border: 2px solid #00e1ff9f;
    margin-top: 22px;
  }
  #map {
    max-width: 640px;
    height: 460px;
    margin: 28px auto 56px auto;
    border-radius: 14px;
    border: 3px solid #00e1ff91;
    box-shadow: 0 0 36px 18px #00e1ff52;
  }
  #photoOutput img {
    max-width: 320px;
    border-radius: 16px;
  }
  @media (max-width: 900px) {
    .dashboard, .service-list, .events-categories {
      grid-template-columns: 1fr;
      gap: 26px;
    }
    .folder-card, .service-card, .category-card {
      width: 95%;
      font-size: 1.22rem;
      padding: 38px 22px;
    }
  }
</style>
</head>

<body>
<header>JKS Group of Business</header>

<nav>
  <button onclick="showPage('dashboard')">Dashboard</button>
  <button onclick="showPage('profile')">Profile</button>
  <button onclick="showPage('wallet')">Wallet</button>
  <button onclick="showPage('orders')">Orders</button>
  <button onclick="showPage('camera')">Camera</button>
  <button onclick="showPage('maps')">Google Maps</button>
</nav>

<main>
  <section id="dashboard" class="dashboard"></section>
  
  <section id="profile" style="display:none;">
    <h2 class="section-title">Profile</h2>
    <form class="contact-form" onsubmit="return false;">
      <label>Name:</label><input id="profileName" type="text" />
      <label>Email:</label><input id="profileEmail" type="email" />
      <label>Phone:</label><input id="profilePhone" type="tel" />
      <label>Address:</label><textarea id="profileAddress" rows="3"></textarea>
      <button type="button" onclick="alert('Profile saved!')">Save</button>
    </form>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>
  
  <section id="wallet" style="display:none;">
    <h2 class="section-title">Wallet</h2>
    <p>Balance: ₹<span id="walletBalance">10000</span></p>
    <form class="contact-form" onsubmit="addMoney(event)">
      <label>Add Money:</label>
      <input id="addMoneyInput" type="number" min="1" required />
      <button type="submit">Add Funds</button>
    </form>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>
  
  <section id="orders" style="display:none;">
    <h2 class="section-title">Orders</h2>
    <table style="width: 100%; border-collapse: collapse; background: #1c2238; color: #fff; border-radius: 8px; overflow: hidden;">
      <thead>
        <tr><th style="padding: 14px;">Order ID</th><th>Product / Service</th><th>Status</th></tr>
      </thead>
      <tbody>
        <tr><td>001</td><td>Pizza</td><td style="color: #3eff9d;">Delivered</td></tr>
        <tr><td>002</td><td>Car Wash</td><td style="color: #ffe27f;">Pending</td></tr>
        <tr><td>003</td><td>Loan Enquiry</td><td style="color: #0bcfff;">In Progress</td></tr>
      </tbody>
    </table>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>
  
  <section id="serviceView" style="display:none; flex-direction: column; align-items: center;">
    <h2 class="section-title" id="serviceTitle"></h2>
    <div class="service-list" id="serviceList"></div>
    <form class="contact-form" id="contactForm" style="display:none;">
      <label>Name:</label>
      <input type="text" id="userName" required />
      <label>Mobile:</label>
      <input type="tel" id="userPhone" maxlength="10" pattern="[6-9][0-9]{9}" required />
      <label>Message:</label>
      <textarea id="userMessage" rows="4" required></textarea>
      <button type="button" onclick="submitContactForm()">Submit WhatsApp</button>
      <button class="back-btn" onclick="backToServiceList()">Back to Services</button>
    </form>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>
  
  <section id="eventsView" style="display:none; flex-direction: column; align-items: center;">
    <h2 class="section-title" id="eventsCategoryTitle"></h2>
    <div class="events-categories" id="eventsCategories"></div>
    <div class="service-list" id="eventsServiceList"></div>
    <form id="eventContactForm" class="contact-form" style="display:none;">
      <label>Name:</label>
      <input id="eventsUserName" type="text" required />
      <label>Mobile:</label>
      <input id="eventsUserPhone" type="tel" maxlength="10" pattern="[6-9][0-9]{9}" required />
      <div id="customFields"></div>
      <label>Message:</label>
      <textarea id="eventsUserMessage" rows="4" required></textarea>
      <button type="button" onclick="submitEventsForm()">Submit WhatsApp</button>
      <button type="button" class="back-btn" onclick="backToEventsCategory()">Back</button>
    </form>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>
  
  <section id="ecomView" style="display:none;">
    <div class="section-title">My E-commerce</div>
    <nav style="margin-bottom: 18px;">
      <button onclick="openEcomCategory('Groceries')">Groceries</button>
      <button onclick="openEcomCategory('Food')">Food</button>
      <button onclick="openEcomCategory('Pharmacy')">Pharmacy</button>
      <button onclick="showPage('camera')" style="margin-left: 30px;">Camera</button>
      <button onclick="showPage('maps')">Google Maps</button>
    </nav>
    <div class="service-list" id="ecomServiceList"></div>
    <form id="ecomOrderForm" class="contact-form" style="display:none;">
      <h3 id="ecomOrderTitle"></h3>
      <label>Name:</label>
      <input name="name" type="text" required />
      <label>Mobile:</label>
      <input name="phone" type="tel" maxlength="10" pattern="[6-9][0-9]{9}" required />
      <label>Order Details:</label>
      <textarea name="orderDetails" rows="3" required></textarea>
      <label>Delivery Address:</label>
      <textarea name="address" required></textarea>
      <button type="submit">Order WhatsApp</button>
      <button type="button" class="back-btn" onclick="backToEcomServices()">Back</button>
    </form>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>
  
  <section id="rechargeView" style="display:none;">
    <h2 class="section-title">Recharge & Pay Bills</h2>
    <div class="service-list" id="rechargeServiceList"></div>
    <form id="rechargeOrderForm" class="contact-form" style="display:none;">
      <h3 id="rechargeOrderTitle"></h3>
      <label>Name:</label>
      <input name="rname" type="text" required />
      <label>Mobile:</label>
      <input name="rphone" type="tel" maxlength="10" pattern="[6-9][0-9]{9}" required />
      <label>Details:</label>
      <textarea name="rdetails" rows="3" required></textarea>
      <label>Address (optional):</label>
      <textarea name="raddress"></textarea>
      <button type="submit">Pay via WhatsApp</button>
      <button type="button" class="back-btn" onclick="backToRechargeServices()">Back</button>
    </form>
    <button class="back-btn" onclick="showPage('dashboard')">Back to Dashboard</button>
  </section>
  
  <section id="camera" style="display:none; text-align:center;">
    <h2 class="section-title">Camera</h2>
    <video id="video" autoplay muted playsinline></video>
    <div style="margin: 20px 0;">
      <button onclick="switchCamera()">Switch Camera</button>
      <button onclick="capturePhoto()">Capture Photo</button>
    </div>
    <canvas id="canvas"></canvas>
    <div id="photoOutput" style="margin-top: 20px;"></div>
    <button class="back-btn" onclick="showPage('dashboard')">Back</button>
  </section>
  
  <section id="maps" style="display:none; text-align:center;">
    <h2 class="section-title">Google Maps</h2>
    <iframe
      id="map"
      width="100%"
      height="460"
      style="border:0; border-radius:14px; margin:28px auto 52px; box-shadow:0 0 36px 18px #00e1ff52;"
      loading="lazy"
      allowfullscreen
      referrerpolicy="no-referrer-when-downgrade"
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3806.272668041566!2d78.48261611487654!3d17.385044788065196!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bcb9736285f645f%3A0xf4dae048bfe79116!2sHyderabad!5e0!3m2!1sen!2sin!4v1633072783551!5m2!1sen!2sin"
    ></iframe>
    <button class="back-btn" onclick="showPage('dashboard')">Back</button>
  </section>
</main>

<script>
const folders = [
  { id: "ecommerce", label: "My E-commerce" },
  { id: "events", label: "Events & Catering" },
  { id: "courier", label: "Courier & Ride Booking" },
  { id: "job", label: "Job Consultancy & Services" },
  { id: "tours", label: "Tours & Travels" },
  { id: "realestate", label: "Real Estate & Construction" },
  { id: "investment", label: "Investment & Business" },
  { id: "loans", label: "Loans & Insurance" },
  { id: "home", label: "Home Services" },
  { id: "rechargeView", label: "Recharge & Pay Bills" }
];
const moduleServices = {
  courier: ["Courier Booking", "Ride Booking", "Tracking", "Support", "Rental Vehicles"],
  job: ["Job Search", "Post Resume", "Local Jobs", "Non-Local Jobs", "PG & Hostel", "Services Marketplace"],
  tours: ["Tour Bookings", "Custom & Regular Tours", "Stay Booking", "Vehicle Booking", "Train/Bus/Flight Tickets"],
  realestate: ["Buy", "Sell", "Rent", "Key Services", "Construction", "Industry"],
  investment: ["Gold", "Silver", "Real Estate", "Business Opportunity", "Mutual Funds"],
  loans: ["Loan Enquiry", "Car Insurance", "Bike Insurance", "Housing Loans", "Personal Loans", "Health Insurance"],
  home: [
    "CC Camera Installation",
    "Computer Repair",
    "Car Wash",
    "Mobile Repair",
    "Chef Services",
    "Bouncers",
    "Bike Mechanic",
    "Car Mechanic",
    "Electrician",
    "Painter",
    "Plumber",
    "Driver"
  ]
};
const ecom = {
  Groceries: ["Milk", "Meat", "Fruits", "Vegetables", "Flowers", "Others"],
  Food: ["Biriyani", "Tiffins", "Ice Cream", "Pizza", "Burgers", "Rolls"],
  Pharmacy: ["Medicines", "Health Products", "Supplements", "Care Products"]
};
const eventsCategories = {
  package: [
    { name: "Silver", amount: "50k - 160k" },
    { name: "Gold", amount: "150k - 300k" },
    { name: "Diamond", amount: "500k - 5M" },
    { name: "Platinum", amount: "500k - 800k" }
  ],
  customized: [
    "Decoration",
    "Catering",
    "Photography & Videography",
    "Anchor & Actors",
    "DJ & Singers",
    "Guest House",
    "Chocolate & Cake",
    "Games & Entertainment",
    "Jewellery",
    "Invitation Cards",
    "Vehicles",
    "Return Gifts",
    "Makeup Artist",
    "Mehandi Artist",
    "Clothing & Accessories"
  ],
  premium: [
    "Decoration",
    "Catering",
    "Photography & Videography",
    "Anchor & Actors",
    "DJ & Singers",
    "Guest House",
    "Chocolate & Cake",
    "Games & Entertainment",
    "Jewellery",
    "Invitation Cards",
    "Vehicles",
    "Return Gifts",
    "Makeup Artist",
    "Mehandi Artist",
    "Clothing & Accessories"
  ]
};
const rechargeServices = ["Mobile Recharge", "DTH Recharge", "Electricity Bill", "Water Bill", "Gas Bill"];

let currentModule = "";
let currentService = "";
let currentEcomCategory = "";
let currentEventCategory = "";
let currentEventService = "";
let currentRechargeService = "";

function showPage(page) {
  document.querySelectorAll("main > section").forEach((s) => (s.style.display = "none"));
  document.getElementById(page).style.display = "block";
  if (page === "dashboard") renderDashboard();
  else if (page === "events") openEventsDashboard();
  else if (page === "ecommerce") openEcomDashboard();
  else if (page === "camera") startCamera();
  else if (page === "maps" && !window.mapLoaded) {
    initMap();
    window.mapLoaded = true;
  } else if (page === "rechargeView") openRechargeDashboard();
}

function renderDashboard() {
  const dash = document.getElementById("dashboard");
  dash.innerHTML = "";
  folders.forEach((f) => {
    const div = document.createElement("div");
    div.className = "folder-card";
    div.textContent = f.label;
    div.onclick = () => openModule(f.id);
    dash.appendChild(div);
  });
}

function openModule(mod) {
  currentModule = mod;
  currentService = "";
  if (mod === "events") {
    openEventsDashboard();
    return;
  }
  if (mod === "ecommerce") {
    openEcomDashboard();
    return;
  }
  if (mod === "rechargeView") {
    openRechargeDashboard();
    return;
  }
  const listEl = document.getElementById("serviceList");
  listEl.innerHTML = "";
  (moduleServices[mod] || []).forEach((svc) => {
    const d = document.createElement("div");
    d.className = "service-card";
    d.textContent = svc;
    d.onclick = () => openContactForm(svc);
    listEl.appendChild(d);
  });
  document.getElementById("serviceTitle").textContent = folders.find((f) => f.id === mod)?.label || "";
  showPage("serviceView");
}

function openContactForm(service) {
  currentService = service;
  document.getElementById("serviceList").style.display = "none";
  const form = document.getElementById("contactForm");
  form.style.display = "block";
  document.getElementById("contactTitle").textContent = "Contact for " + service;
  clearInputs(["userName", "userPhone", "userMessage"]);
}

function backToServiceList() {
  document.getElementById("contactForm").style.display = "none";
  document.getElementById("serviceList").style.display = "grid";
}

function submitContactForm() {
  const name = document.getElementById("userName").value.trim();
  const phone = document.getElementById("userPhone").value.trim();
  const message = document.getElementById("userMessage").value.trim();
  if (!name || !phone || !message) {
    alert("Please fill all fields.");
    return;
  }
  const waMsg = `Name: ${encodeURIComponent(name)}%0APhone: ${encodeURIComponent(phone)}%0AService: ${encodeURIComponent(currentService)}%0AMessage: ${encodeURIComponent(message)}`;
  window.open(`https://api.whatsapp.com/send?phone=918977143043&text=${waMsg}`, "_blank");
}

function clearInputs(ids) {
  ids.forEach((id) => {
    const el = document.getElementById(id);
    if (el) el.value = "";
  });
}

function openEventsDashboard() {
  currentEventCategory = "";
  currentEventService = "";
  document.getElementById("dashboard").style.display = "none";
  document.getElementById("serviceView").style.display = "none";
  document.getElementById("ecomView").style.display = "none";
  document.getElementById("rechargeView").style.display = "none";
  document.getElementById("eventsView").style.display = "flex";
  const catsDiv = document.getElementById("eventsCategories");
  catsDiv.innerHTML = "";
  ["package", "customized", "premium"].forEach((cat) => {
    const d = document.createElement("div");
    d.className = "category-card";
    d.textContent = cat.charAt(0).toUpperCase() + cat.slice(1);
    d.onclick = () => openEventsCategory(cat);
    catsDiv.appendChild(d);
  });
  document.getElementById("eventsServiceList").innerHTML = "";
  document.getElementById("eventContactForm").style.display = "none";
  document.getElementById("eventsCategoryTitle").textContent = "Events & Catering Categories";
}

function openEventsCategory(cat) {
  currentEventCategory = cat;
  currentEventService = "";
  const svcList = document.getElementById("eventsServiceList");
  document.getElementById("eventContactForm").style.display = "none";
  svcList.style.display = "grid";
  svcList.innerHTML = "";
  if (cat === "package") {
    eventsCategories.package.forEach((pkg) => {
      const d = document.createElement("div");
      d.className = "service-card";
      d.textContent = `${pkg.name} (${pkg.amount})`;
      d.onclick = () => openEventContactForm(pkg.name, cat);
      svcList.appendChild(d);
    });
  } else {
    eventsCategories[cat].forEach((svc) => {
      const d = document.createElement("div");
      d.className = "service-card";
      d.textContent = svc;
      d.onclick = () => openEventContactForm(svc, cat);
      svcList.appendChild(d);
    });
  }
  document.getElementById("eventsCategoryTitle").textContent = cat.charAt(0).toUpperCase() + cat.slice(1) + " Services";
}

function openEventContactForm(service, category) {
  currentEventService = service;
  document.getElementById("eventsServiceList").style.display = "none";
  const form = document.getElementById("eventContactForm");
  form.style.display = "block";
  document.getElementById("eventsContactTitle").textContent = "Contact for " + service;
  document.getElementById("eventsUserName").value = "";
  document.getElementById("eventsUserPhone").value = "";
  document.getElementById("eventsUserMessage").value = "";
  const customFields = document.getElementById("customFields");
  if (category === "customized") {
    customFields.innerHTML = `
      <label>Budget:</label>
      <select id="eventsBudget" required>
        <option value="">Select Budget</option>
        <option>10k to 50k</option>
        <option>50k to 1L</option>
        <option>1L to 5L</option>
        <option>5L to 10L</option>
        <option>Above 10L</option>
      </select>
      <label>Capacity:</label>
      <select id="eventsCapacity" required>
        <option value="">Select Capacity</option>
        <option>5-30 people</option>
        <option>30-60 people</option>
        <option>60-90 people</option>
        <option>90-130 people</option>
        <option>Above 130 people</option>
      </select>`;
  } else {
    customFields.innerHTML = "";
  }
}

function backToEventsCategory() {
  document.getElementById("eventContactForm").style.display = "none";
  document.getElementById("eventsServiceList").style.display = "grid";
}

function submitEventsForm() {
  const name = document.getElementById("eventsUserName").value.trim();
  const phone = document.getElementById("eventsUserPhone").value.trim();
  const message = document.getElementById("eventsUserMessage").value.trim();
  let budget = "";
  let capacity = "";
  if (currentEventCategory === "customized") {
    budget = document.getElementById("eventsBudget").value;
    capacity = document.getElementById("eventsCapacity").value;
    if (!budget || !capacity) {
      alert("Please select budget and capacity");
      return;
    }
  }
  if (!name || !phone || !message) {
    alert("Please fill all fields");
    return;
  }
  let whatsappMsg = `Name: ${encodeURIComponent(name)}%0APhone: ${encodeURIComponent(phone)}%0AService: ${encodeURIComponent(
    currentEventService
  )}%0ACategory: ${encodeURIComponent(currentEventCategory)}%0AMessage: ${encodeURIComponent(message)}`;
  if (budget) whatsappMsg += `%0ABudget: ${encodeURIComponent(budget)}`;
  if (capacity) whatsappMsg += `%0ACapacity: ${encodeURIComponent(capacity)}`;
  window.open(`https://api.whatsapp.com/send?phone=918977143043&text=${whatsappMsg}`, "_blank");
}

function openEcomDashboard() {
  currentEcomCategory = "";
  document.getElementById("dashboard").style.display = "none";
  document.getElementById("serviceView").style.display = "none";
  document.getElementById("eventsView").style.display = "none";
  document.getElementById("rechargeView").style.display = "none";
  document.getElementById("ecomView").style.display = "block";
  document.getElementById("ecomServiceList").innerHTML = "";
  document.getElementById("ecomOrderForm").style.display = "none";
}

function openEcomCategory(cat) {
  currentEcomCategory = cat;
  const svcList = document.getElementById("ecomServiceList");
  svcList.innerHTML = "";
  (ecom[cat] || []).forEach((service) => {
    const d = document.createElement("div");
    d.className = "service-card";
    d.textContent = service;
    d.onclick = () => openEcomOrderForm(cat, service);
    svcList.appendChild(d);
  });
  document.getElementById("ecomOrderForm").style.display = "none";
  svcList.style.display = "grid";
}

function openEcomOrderForm(cat, service) {
  document.getElementById("ecomOrderForm").style.display = "block";
  document.getElementById("ecomOrderTitle").textContent = `Order ${service} in ${cat}`;
  document.getElementById("ecomOrderForm").onsubmit = (e) => submitOrderForm(e, cat, service);
}

function backToEcomServices() {
  document.getElementById("ecomOrderForm").style.display = "none";
}

function submitOrderForm(e, cat, service) {
  e.preventDefault();
  const form = e.target;
  const name = form.name.value.trim();
  const phone = form.phone.value.trim();
  const details = form.orderDetails.value.trim();
  const address = form.address.value.trim();
  if (!name || !phone || !details || !address) {
    alert("Please fill all order form fields");
    return;
  }
  const msg = `Order from JKS E-commerce%0ACategory: ${cat}%0AProduct: ${service}%0AName: ${name}%0APhone: ${phone}%0AOrder Details: ${details}%0AAddress: ${address}`;
  window.open(`https://api.whatsapp.com/send?phone=918977143043&text=${encodeURIComponent(msg)}`, "_blank");
}

const rechargeServices = ["Mobile Recharge", "DTH Recharge", "Electricity Bill", "Water Bill", "Gas Bill"];

function openRechargeDashboard() {
  currentRechargeService = "";
  document.getElementById("dashboard").style.display = "none";
  document.getElementById("serviceView").style.display = "none";
  document.getElementById("eventsView").style.display = "none";
  document.getElementById("ecomView").style.display = "none";
  document.getElementById("rechargeView").style.display = "block";
  const svcList = document.getElementById("rechargeServiceList");
  svcList.innerHTML = "";
  rechargeServices.forEach((ser) => {
    const d = document.createElement("div");
    d.className = "service-card";
    d.textContent = ser;
    d.onclick = () => openRechargeOrderForm(ser);
    svcList.appendChild(d);
  });
  document.getElementById("rechargeOrderForm").style.display = "none";
}

function openRechargeOrderForm(service) {
  currentRechargeService = service;
  document.getElementById("rechargeServiceList").style.display = "none";
  const form = document.getElementById("rechargeOrderForm");
  form.style.display = "block";
  document.getElementById("rechargeOrderTitle").textContent = "Pay for " + service;
  const inputs = form.querySelectorAll("input, textarea");
  inputs.forEach((item) => (item.value = ""));
  form.onsubmit = submitRechargeOrderForm;
}

function backToRechargeServices() {
  document.getElementById("rechargeOrderForm").style.display = "none";
  document.getElementById("rechargeServiceList").style.display = "grid";
}

function submitRechargeOrderForm(e) {
  e.preventDefault();
  const form = e.target;
  const name = form.rname.value.trim();
  const phone = form.rphone.value.trim();
  const details = form.rdetails.value.trim();
  const address = form.raddress.value.trim();
  if (!name || !phone || !details) {
    alert("Please fill all required fields");
    return;
  }
  let msg = `Recharge and Bill Payment%0AService: ${currentRechargeService}%0AName: ${name}%0APhone: ${phone}%0ADetails: ${details}%0AAddress: ${address}`;
  window.open(`https://api.whatsapp.com/send?phone=918977143043&text=${encodeURIComponent(msg)}`, "_blank");
}

let currentStream = null;
let usingFrontCamera = true;

function startCamera() {
  const video = document.getElementById("video");
  if (currentStream) currentStream.getTracks().forEach((t) => t.stop());
  navigator.mediaDevices
    .getUserMedia({ video: { facingMode: usingFrontCamera ? "user" : "environment" } })
    .then((stream) => {
      currentStream = stream;
      video.srcObject = stream;
      video.play();
    })
    .catch(() => alert("Camera access denied or unavailable"));
}

function switchCamera() {
  usingFrontCamera = !usingFrontCamera;
  startCamera();
}

function capturePhoto() {
  const video = document.getElementById("video");
  const canvas = document.getElementById("canvas");
  canvas.width = video.videoWidth;
  canvas.height = video.videoHeight;
  const ctx = canvas.getContext("2d");
  ctx.drawImage(video, 0, 0);
  const dataUrl = canvas.toDataURL();
  document.getElementById("photoOutput").innerHTML = `<img src="${dataUrl}" style="max-width:320px;border-radius:12px;">`;
}

function addMoney(e) {
  e.preventDefault();
  const amountInput = document.getElementById("addMoneyInput");
  const amount = parseFloat(amountInput.value);
  if (isNaN(amount) || amount <= 0) {
    alert("Enter a valid amount");
    return;
  }
  let balance = parseFloat(document.getElementById("walletBalance").innerText);
  balance += amount;
  document.getElementById("walletBalance").innerText = balance.toFixed(2);
  alert(`₹${amount.toFixed(2)} added to wallet.`);
  amountInput.value = "";
}

function initMap() {
  // No API key needed for embed - iframe used instead for reliability:
}
document.addEventListener("DOMContentLoaded", () => {
  showPage("dashboard");
});
</script>
</body>
</html>
