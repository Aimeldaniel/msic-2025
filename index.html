<?php include "header.html"; ?>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="clock/style.css" />
  <title>MSIC - Malaysian Standard Industrial Code</title>

  <style>
    body { font-family: Arial, sans-serif; background: #f9f9f9; margin: 0; padding: 0; text-align: center; }
    header { margin: 20px 0; position: relative; }
    .window-box { display: inline-block; border: 2px solid #000; border-radius: 5px; padding: 20px 40px; margin: 20px auto; background: #fff; box-shadow: 4px 4px 0px #000; }
    .window-box h1 { margin: 0; font-size: 28px; }
    .window-box p { margin: 0; font-style: italic; font-size: 14px; }
    .btn-container { margin-top: 30px; display: flex; flex-wrap: wrap; justify-content: center; gap: 40px; }
    .btn { display: inline-block; padding: 15px 40px; font-size: 18px; font-weight: bold; border: 2px solid #000; border-radius: 10px; background: #fff; cursor: pointer; box-shadow: 4px 4px 0px #000; transition: all 0.2s; text-decoration: none; color: black; }
    .btn:hover { background: #f0f0f0; transform: translateY(-3px); }

    /* Comparison Page */
    .comparison-container { display: flex; flex-wrap: wrap; justify-content: space-around; margin: 30px auto; max-width: 1000px; }
    .comparison-box { flex: 1 1 45%; background: #b3e5f5; border-radius: 8px; padding: 20px; margin: 10px; }
    .comparison-box h2 { font-size: 20px; margin-bottom: 15px; }
    .search-bar { display: flex; align-items: center; background: #fff; border: 2px solid #777; border-radius: 20px; padding: 5px 15px; }
    .search-bar input { border: none; flex: 1; padding: 10px; border-radius: 20px; outline: none; }

    footer { position: fixed; bottom: 0; left: 0; width: 100%; background: #007a8e; color: #fff; text-align: center; padding: 10px; }

    /* Language Switcher */
    .lang-switch { position: absolute; top: 15px; right: 15px; padding: 8px 15px; background: #007a8e; color: white; border: none; border-radius: 8px; cursor: pointer; }

    /* Table styles */
    table { width: 95%; margin: 20px auto; border-collapse: collapse; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 12px rgba(0,0,0,0.1); font-size: 14px; background: #fff; }
    th { background: #007a8e; color: white; font-weight: bold; text-transform: uppercase; padding: 12px; text-align: left; }
    td { padding: 12px; border-bottom: 1px solid #e0e0e0; }
    tr:nth-child(even) { background: #f9f9f9; }
    tr:hover { background: #e3f2fd; transition: 0.2s; }
    .no-results { color: #c62828; font-weight: bold; margin-top: 20px; font-size: 16px; }
  </style>
</head>
<body>
  
  <!-- HEADER -->
  <header>
    <div class="header-container">
      <div class="window-box">
        <h1>MSIC</h1>
        <p id="subtitle">MALAYSIAN STANDARD INDUSTRIAL CODE</p>
      </div>
      <button class="lang-switch" onclick="toggleLanguage()">BM</button>
    </div>
  </header> 

  <!-- HOME PAGE -->
  <div class="btn-container">
    <a href="#search" class="btn" id="btn-search">Search</a>
    <a href="#comparison" class="btn" id="btn-comparison">Comparison</a>
    <a href="#settings" class="btn" id="btn-settings">Settings</a>
  </div>

  <!-- SEARCH PAGE -->
  <section id="search" style="display: none; margin-top: 40px">
    <h2 id="search-title">Search MSIC</h2>
    <div class="search-bar" style="max-width: 600px; margin: auto">
      <input type="text" id="searchInput" placeholder="Type MSIC code or description..." onkeyup="searchCode()" />
    </div>
    <div id="results"></div>
  </section>

  <!-- COMPARISON PAGE -->
  <section id="comparison" style="display: none; margin-top: 40px">
    <h2 id="comparison-title">Compare MSIC</h2>
    <div class="search-bar" style="max-width: 600px; margin: auto">
      <input type="text" id="compareInput" placeholder="Type MSIC code or description..." onkeyup="compareMSIC()" />
    </div>
    <div id="compareResults"></div>
  </section>

  <!-- SETTINGS PAGE -->
  <section id="settings" style="display: none; margin-top: 40px">
    <h2 id="settings-title">Settings</h2>
    <p><b>Language:</b> English / Bahasa Malaysia</p>
    <p><b>Theme:</b> Light / Dark (Coming soon)</p>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>@StatsMalaysia | ASEAN 2025 | Malaysia Madani</p>
  </footer>

  <script src="clock/script.js"></script>

  <script>
  let msicData = [];
  let msicData2 = [];

  // Load JSON files
  fetch("msic25.json")
    .then(response => response.json())
    .then(data => { msicData = data; })
    .catch(err => console.error("Error loading JSON:", err));

  fetch("comparisonmsic.json")
    .then(response => response.json())
    .then(data => { msicData2 = data; })
    .catch(err => console.error("Error loading JSON:", err));

  // Search function
  function searchCode() {
    const input = document.getElementById("searchInput").value.trim().toLowerCase();
    const resultsDiv = document.getElementById("results");

    const filtered = msicData.filter(item =>
      item["MSIC 2025"].toLowerCase().includes(input) ||
      item["DESCRIPTION 2025"].toLowerCase().includes(input) ||
      item["DESCRIPTION 2025 KEGUNAAN MSBR"]?.toLowerCase().includes(input) ||
      item["SECTION DESCRIPTION"].toLowerCase().includes(input)
    );

    if (filtered.length === 0) {
      resultsDiv.innerHTML = '<p class="no-results">No results found.</p>';
      return;
    }

    let html = `
      <table>
        <tr>
          <th id="tbl-section">Section</th>
          <th id="tbl-sec-desc">Section Description</th>
          <th id="tbl-msic2025">MSIC 2025</th>
          <th id="tbl-desc2025">Description 2025</th>
          <th id="tbl-msbr">Description (MSBR)</th>
        </tr>
    `;

    filtered.forEach(item => {
      html += `
        <tr>
          <td>${item["SECTION 2025"]}</td>
          <td>${item["SECTION DESCRIPTION"]}</td>
          <td>${item["MSIC 2025"]}</td>
          <td>${item["DESCRIPTION 2025"]}</td>
          <td>${item["DESCRIPTION 2025 KEGUNAAN MSBR"] || ""}</td>
        </tr>
      `;
    });

    html += "</table>";
    resultsDiv.innerHTML = html;
  }

  // Comparison function
  function compareMSIC() {
    const query = document.getElementById("compareInput").value.toLowerCase();
    const resultsDiv = document.getElementById("compareResults");
    resultsDiv.innerHTML = "";

    const results = msicData2.filter(item =>
      item["MSIC 2008"].toLowerCase().includes(query) ||
      item["DESCRIPTION MSIC 2008"].toLowerCase().includes(query) ||
      item["MSIC 2025"].toLowerCase().includes(query) ||
      item["DESCRIPTION 2025"].toLowerCase().includes(query)
    );

    if (results.length === 0) {
      resultsDiv.innerHTML = '<p class="no-results">No results found.</p>';
      return;
    }

    let html = `
      <table>
        <tr>
          <th id="tbl-msic2008">MSIC 2008</th>
          <th id="tbl-desc2008">Description 2008</th>
          <th id="tbl-msic2025c">MSIC 2025</th>
          <th id="tbl-desc2025c">Description 2025</th>
        </tr>
    `;

    results.forEach(item => {
      html += `
        <tr>
          <td>${item["MSIC 2008"]}</td>
          <td>${item["DESCRIPTION MSIC 2008"]}</td>
          <td>${item["MSIC 2025"]}</td>
          <td>${item["DESCRIPTION 2025"]}</td>
        </tr>
      `;
    });

    html += "</table>";
    resultsDiv.innerHTML = html;
  }

  // Page navigation
  const sections = document.querySelectorAll("section");
  const buttons = document.querySelectorAll(".btn-container a");

  buttons.forEach((btn) => {
    btn.addEventListener("click", (e) => {
      e.preventDefault();
      sections.forEach((sec) => (sec.style.display = "none"));
      const target = document.querySelector(btn.getAttribute("href"));
      if (target) target.style.display = "block";
      window.scrollTo(0, 0);
    });
  });

  // Language toggle
  let currentLang = "EN";
  function toggleLanguage() {
    if (currentLang === "EN") {
      document.getElementById("subtitle").innerText = "Kod Piawaian Perindustrian Malaysia";
      document.getElementById("btn-search").innerText = "Carian";
      document.getElementById("btn-comparison").innerText = "Perbandingan";
      document.getElementById("btn-settings").innerText = "Tetapan";
      document.getElementById("search-title").innerText = "Carian MSIC";
      document.getElementById("comparison-title").innerText = "Perbandingan MSIC";
      document.getElementById("settings-title").innerText = "Tetapan";

      // table headers
      document.getElementById("tbl-section").innerText = "Seksyen";
      document.getElementById("tbl-sec-desc").innerText = "Keterangan Seksyen";
      document.getElementById("tbl-msic2025").innerText = "MSIC 2025";
      document.getElementById("tbl-desc2025").innerText = "Keterangan 2025";
      document.getElementById("tbl-msbr").innerText = "Keterangan (MSBR)";

      document.getElementById("tbl-msic2008").innerText = "MSIC 2008";
      document.getElementById("tbl-desc2008").innerText = "Keterangan 2008";
      document.getElementById("tbl-msic2025c").innerText = "MSIC 2025";
      document.getElementById("tbl-desc2025c").innerText = "Keterangan 2025";

      currentLang = "BM";
      document.querySelector(".lang-switch").innerText = "EN";
    } else {
      document.getElementById("subtitle").innerText = "MALAYSIAN STANDARD INDUSTRIAL CODE";
      document.getElementById("btn-search").innerText = "Search";
      document.getElementById("btn-comparison").innerText = "Comparison";
      document.getElementById("btn-settings").innerText = "Settings";
      document.getElementById("search-title").innerText = "Search MSIC";
      document.getElementById("comparison-title").innerText = "Compare MSIC";
      document.getElementById("settings-title").innerText = "Settings";

      // table headers
      document.getElementById("tbl-section").innerText = "Section";
      document.getElementById("tbl-sec-desc").innerText = "Section Description";
      document.getElementById("tbl-msic2025").innerText = "MSIC 2025";
      document.getElementById("tbl-desc2025").innerText = "Description 2025";
      document.getElementById("tbl-msbr").innerText = "Description (MSBR)";

      document.getElementById("tbl-msic2008").innerText = "MSIC 2008";
      document.getElementById("tbl-desc2008").innerText = "Description 2008";
      document.getElementById("tbl-msic2025c").innerText = "MSIC 2025";
      document.getElementById("tbl-desc2025c").innerText = "Description 2025";

      currentLang = "EN";
      document.querySelector(".lang-switch").innerText = "BM";
    }
  }
  </script>
</body>
</html>
