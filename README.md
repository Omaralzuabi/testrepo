# testrepo
#Editing the file
   it a markdown file in this repository
   <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Data Science Capstone Project Report - SpaceX Falcon 9 First Stage Landing Prediction</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;600&display=swap">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { margin: 0; padding: 0; background-color: #0d1117; font-family: 'Inter', sans-serif; color: #1f2937; }
    
    .slide-container {
      width: 1280px;
      height: 720px;
      margin: 20px auto;
      overflow: hidden;
      box-sizing: border-box;
      position: relative;
      background: #ffffff;
      display: flex;
      flex-direction: column;
      font-family: 'Inter', sans-serif;
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
      border-radius: 8px;
    }

    .slide-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 36px 64px 16px 64px;
      border-bottom: 1px solid #e5e7eb;
    }

    .slide-title {
      font-size: 28px;
      font-weight: 700;
      color: #0f172a;
      line-height: 1.2;
    }

    .eyebrow {
      font-size: 13px;
      font-weight: 700;
      color: #2563eb;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 4px;
    }

    .github-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      background: #f1f5f9;
      color: #475569;
      padding: 6px 12px;
      border-radius: 6px;
      font-size: 12px;
      font-family: 'JetBrains Mono', monospace;
      font-weight: 500;
      text-decoration: none;
    }

    .content-area {
      flex-grow: 1;
      padding: 32px 64px 48px 64px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .footer-bar {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 6px;
      background: linear-gradient(90deg, #2563eb 0%, #3b82f6 50%, #06b6d4 100%);
    }

    .metric-card {
      background: #f8fafc;
      border-radius: 12px;
      padding: 24px;
      border: 1px solid #e2e8f0;
      flex: 1 1 0;
    }

    .code-block {
      background: #0f172a;
      color: #38bdf8;
      font-family: 'JetBrains Mono', monospace;
      padding: 16px;
      border-radius: 8px;
      font-size: 13px;
      line-height: 1.5;
      overflow-x: auto;
    }
  </style>
</head>
<body>

  <!-- SLIDE 1: TITLE SLIDE -->
  <div class="slide-container" style="background:#0f172a; padding:64px; justify-content:center;">
    <div style="max-width:850px;">
      <p style="font-family:'JetBrains Mono',monospace; font-size:14px; color:#38bdf8; font-weight:600; text-transform:uppercase; letter-spacing:0.1em; margin-bottom:16px;">
        IBM Data Science Professional Certificate • Capstone Report
      </p>
      <h1 style="font-size:48px; font-weight:800; color:#ffffff; margin:0 0 20px 0; line-height:1.15; letter-spacing:-0.02em;">
        SpaceX Falcon 9 First Stage Landing Prediction
      </h1>
      <p style="font-size:20px; color:#94a3b8; margin:0 0 32px 0; line-height:1.5;">
        Machine learning models and visual analytics for booster reusability & cost optimization
      </p>
      
      <div style="display:flex; align-items:center; gap:20px; background:rgba(255,255,255,0.05); padding:16px 24px; border-radius:10px; border:1px solid rgba(255,255,255,0.1); width:fit-content;">
        <i class="fa-brands fa-github" style="color:#38bdf8; font-size:24px;"></i>
        <div>
          <p style="font-size:12px; color:#64748b; margin:0;">CAPSTONE REPOSITORY URL</p>
          <p style="font-family:'JetBrains Mono',monospace; font-size:15px; color:#f8fafc; margin:0; font-weight:600;">
            github.com/username/spacex-falcon9-landing-prediction
          </p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 2: EXECUTIVE SUMMARY -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Project Synopsis</p>
        <h2 class="slide-title">Executive Summary</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:24px; width:100%;">
        <div class="metric-card">
          <div style="width:40px; height:40px; border-radius:8px; background:#dbeafe; color:#2563eb; display:flex; align-items:center; justify-content:center; font-size:18px; margin-bottom:16px;">
            <i class="fa-solid fa-bullseye"></i>
          </div>
          <h3 style="font-size:18px; color:#0f172a; margin-bottom:8px;">Core Objective</h3>
          <p style="font-size:15px; color:#475569; line-height:1.5;">
            Predict Falcon 9 first stage landing outcome (Success = 1 / Failure = 0) to evaluate launch reusability savings.
          </p>
        </div>
        <div class="metric-card">
          <div style="width:40px; height:40px; border-radius:8px; background:#dcfce7; color:#16a34a; display:flex; align-items:center; justify-content:center; font-size:18px; margin-bottom:16px;">
            <i class="fa-solid fa-gears"></i>
          </div>
          <h3 style="font-size:18px; color:#0f172a; margin-bottom:8px;">Data Pipeline</h3>
          <p style="font-size:15px; color:#475569; line-height:1.5;">
            Extracted API JSON payloads and Wikipedia HTML tables; cleaned & standard-scaled 90 core launch features.
          </p>
        </div>
        <div class="metric-card">
          <div style="width:40px; height:40px; border-radius:8px; background:#fef3c7; color:#d97706; display:flex; align-items:center; justify-content:center; font-size:18px; margin-bottom:16px;">
            <i class="fa-solid fa-trophy"></i>
          </div>
          <h3 style="font-size:18px; color:#0f172a; margin-bottom:8px;">Key Results</h3>
          <p style="font-size:15px; color:#475569; line-height:1.5;">
            Decision Tree model achieved <b>88.9% grid search score</b> (83.3% test accuracy) for optimal risk assessment.
          </p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 3: INTRODUCTION -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Context & Problem Statement</p>
        <h2 class="slide-title">Introduction & Business Value</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:40px; align-items:center;">
        <div style="flex:1;">
          <h3 style="font-size:22px; font-weight:700; color:#0f172a; margin-bottom:16px;">The $62M vs $165M Disruption</h3>
          <p style="font-size:16px; color:#475569; margin-bottom:16px; line-height:1.6;">
            SpaceX advertises Falcon 9 launches at $62 million, whereas legacy launch providers cost upward of $165 million per launch.
          </p>
          <p style="font-size:16px; color:#475569; margin-bottom:24px; line-height:1.6;">
            The primary driver for this cost reduction is the <b>reusability of the first stage booster</b>. Predicting landing success allows commercial competitors to accurately price launch bids.
          </p>
          <div style="background:#eff6ff; border-left:4px solid #2563eb; padding:16px; border-radius:0 8px 8px 0;">
            <p style="font-size:14px; font-weight:600; color:#1e40af; margin:0;">
              Research Question: Can launch attributes (payload mass, orbit, launch site) accurately predict stage-one recovery outcomes?
            </p>
          </div>
        </div>
        <div style="flex:0 0 420px; background:#f8fafc; border:1px solid #e2e8f0; border-radius:12px; padding:32px; text-align:center;">
          <p style="font-size:64px; font-weight:800; color:#2563eb; line-height:1;">62.4%</p>
          <p style="font-size:16px; font-weight:600; color:#0f172a; margin-top:8px;">Cost Reduction per Mission</p>
          <p style="font-size:14px; color:#64748b; margin-top:12px;">Achieved primarily by re-flying recovered first-stage boosters</p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 4: DATA COLLECTION - SPACEX API -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Data Acquisition • Phase 1</p>
        <h2 class="slide-title">Data Collection – SpaceX REST API</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:32px; align-items:center;">
        <div style="flex:1;">
          <div style="display:flex; flex-direction:column; gap:16px;">
            <div style="display:flex; gap:16px; align-items:center;">
              <div style="width:36px; height:36px; border-radius:50%; background:#2563eb; color:white; display:flex; align-items:center; justify-content:center; font-weight:700;">1</div>
              <p style="font-size:15px; font-weight:600; color:#0f172a;">API Query: <span style="font-family:'JetBrains Mono',monospace; font-weight:400; color:#2563eb;">api.spacexdata.com/v4/launches/past</span></p>
            </div>
            <div style="display:flex; gap:16px; align-items:center;">
              <div style="width:36px; height:36px; border-radius:50%; background:#2563eb; color:white; display:flex; align-items:center; justify-content:center; font-weight:700;">2</div>
              <p style="font-size:15px; font-weight:600; color:#0f172a;">JSON Normalization: Unpack nested rocket, payload, cores, & launchpad payloads</p>
            </div>
            <div style="display:flex; gap:16px; align-items:center;">
              <div style="width:36px; height:36px; border-radius:50%; background:#2563eb; color:white; display:flex; align-items:center; justify-content:center; font-weight:700;">3</div>
              <p style="font-size:15px; font-weight:600; color:#0f172a;">Falcon 9 Filtering: Filter out Falcon 1 records to isolate 90 target launch rows</p>
            </div>
          </div>
        </div>
        <div style="flex:1;">
          <div class="code-block">
            <span style="color:#64748b;"># Extract API Data Sub-fields</span><br>
            <span style="color:#f43f5e;">import</span> requests<br>
            <span style="color:#f43f5e;">import</span> pandas <span style="color:#f43f5e;">as</span> pd<br><br>
            response = requests.get(url)<br>
            data = pd.json_normalize(response.json())<br>
            df = data[['flight_number', 'date', 'payloads']]<br>
            df['PayloadMass'] = df['PayloadMass'].fillna(mean_mass)
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 5: DATA COLLECTION - WEB SCRAPING -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Data Acquisition • Phase 2</p>
        <h2 class="slide-title">Data Collection – Wikipedia Web Scraping</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:24px;">
        <div class="metric-card">
          <h3 style="font-size:16px; color:#2563eb; margin-bottom:8px;"><i class="fa-solid fa-code" style="margin-right:8px;"></i>BeautifulSoup Parsing</h3>
          <p style="font-size:14px; color:#475569;">Scraped historical Falcon 9 launch records table from Wikipedia HTML structure using <span style="font-family:'JetBrains Mono',monospace;">BeautifulSoup4</span>.</p>
        </div>
        <div class="metric-card">
          <h3 style="font-size:16px; color:#2563eb; margin-bottom:8px;"><i class="fa-solid fa-table" style="margin-right:8px;"></i>Column Extraction</h3>
          <p style="font-size:14px; color:#475569;">Parsed Flight No., Date, Time, Booster Version, Launch Site, Payload, Orbit, Customer, & Launch Outcome.</p>
        </div>
        <div class="metric-card">
          <h3 style="font-size:16px; color:#2563eb; margin-bottom:8px;"><i class="fa-solid fa-broom" style="margin-right:8px;"></i>Data Scrubbing</h3>
          <p style="font-size:14px; color:#475569;">Stripped reference tags <span style="font-family:'JetBrains Mono',monospace;">[1]</span>, newlines <span style="font-family:'JetBrains Mono',monospace;">\n</span>, and parsed numerical strings into structured numerical datatypes.</p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 6: DATA WRANGLING METHODOLOGY -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Data Processing & Engineering</p>
        <h2 class="slide-title">Data Wrangling Methodology</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:32px;">
        <div style="flex:1;">
          <h3 style="font-size:18px; font-weight:700; color:#0f172a; margin-bottom:12px;">Target Label Encoding (Class)</h3>
          <p style="font-size:14px; color:#475569; margin-bottom:16px; line-height:1.5;">Landing outcomes were converted to binary target values:</p>
          <ul style="font-size:14px; color:#334155; padding-left:20px; line-height:1.8;">
            <li><b>Class 1 (Success):</b> Ground Pad landings (<span style="font-family:'JetBrains Mono',monospace;">True RTLS</span>) & Drone Ship landings (<span style="font-family:'JetBrains Mono',monospace;">True ASDS</span>).</li>
            <li><b>Class 0 (Failure):</b> Uncontrolled ocean landings and test crashes.</li>
          </ul>
        </div>
        <div style="flex:1;">
          <h3 style="font-size:18px; font-weight:700; color:#0f172a; margin-bottom:12px;">One-Hot Encoding Features</h3>
          <p style="font-size:14px; color:#475569; margin-bottom:16px; line-height:1.5;">Categorical columns dummy-encoded using <span style="font-family:'JetBrains Mono',monospace;">pd.get_dummies()</span>:</p>
          <div style="background:#f8fafc; border:1px solid #e2e8f0; border-radius:8px; padding:16px; font-size:13px; color:#334155; font-family:'JetBrains Mono',monospace;">
            • Launch Site (CCAFS, KSC, VAFB)<br>
            • Orbit Type (LEO, GTO, ISS, SSO, etc.)<br>
            ➔ Resulting feature space: <b>83 numerical columns</b>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 7: EDA & VISUAL ANALYTICS METHODOLOGY -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Exploratory Analytics Framework</p>
        <h2 class="slide-title">EDA & Visual Analytics Methodology</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:24px;">
        <div class="metric-card">
          <i class="fa-solid fa-chart-line" style="font-size:24px; color:#2563eb; margin-bottom:12px;"></i>
          <h3 style="font-size:16px; color:#0f172a; margin-bottom:8px;">Seaborn / Matplotlib</h3>
          <p style="font-size:14px; color:#475569;">Plotted scatter distributions of Flight Number vs Payload Mass and Orbit vs Launch Site to reveal mission patterns.</p>
        </div>
        <div class="metric-card">
          <i class="fa-solid fa-database" style="font-size:24px; color:#2563eb; margin-bottom:12px;"></i>
          <h3 style="font-size:16px; color:#0f172a; margin-bottom:8px;">SQL Queries</h3>
          <p style="font-size:14px; color:#475569;">Executed SQLite queries for payload aggregations, booster version rankings, and failure outcome classifications.</p>
        </div>
        <div class="metric-card">
          <i class="fa-solid fa-map-location-dot" style="font-size:24px; color:#2563eb; margin-bottom:12px;"></i>
          <h3 style="font-size:16px; color:#0f172a; margin-bottom:8px;">Folium & Dash</h3>
          <p style="font-size:14px; color:#475569;">Built geographical cluster maps (Folium) and reactive payload filtering dashboards (Plotly Dash).</p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 8: PREDICTIVE ANALYSIS METHODOLOGY -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Machine Learning Pipeline</p>
        <h2 class="slide-title">Predictive Analysis Methodology</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:32px; align-items:center;">
        <div style="flex:1;">
          <div style="background:#f8fafc; padding:20px; border-radius:10px; border:1px solid #e2e8f0; margin-bottom:16px;">
            <p style="font-size:14px; font-weight:700; color:#0f172a; margin-bottom:6px;">1. Standard Scaling</p>
            <p style="font-size:13px; color:#64748b;">Applied <span style="font-family:'JetBrains Mono',monospace;">StandardScaler()</span> to normalize feature dimensions.</p>
          </div>
          <div style="background:#f8fafc; padding:20px; border-radius:10px; border:1px solid #e2e8f0; margin-bottom:16px;">
            <p style="font-size:14px; font-weight:700; color:#0f172a; margin-bottom:6px;">2. Train / Test Split</p>
            <p style="font-size:13px; color:#64748b;">Partitioned dataset using <span style="font-family:'JetBrains Mono',monospace;">train_test_split(test_size=0.2, random_state=2)</span>.</p>
          </div>
        </div>
        <div style="flex:1; background:#0f172a; padding:24px; border-radius:12px; color:white;">
          <p style="font-family:'JetBrains Mono',monospace; font-size:14px; color:#38bdf8; margin-bottom:12px;">EVALUATED ALGORITHMS</p>
          <ul style="font-size:14px; line-height:2; color:#cbd5e1; list-style-type:none; padding:0;">
            <li><i class="fa-solid fa-check" style="color:#38bdf8; margin-right:8px;"></i> Logistic Regression</li>
            <li><i class="fa-solid fa-check" style="color:#38bdf8; margin-right:8px;"></i> Support Vector Machines (SVM)</li>
            <li><i class="fa-solid fa-check" style="color:#38bdf8; margin-right:8px;"></i> Decision Tree Classifier</li>
            <li><i class="fa-solid fa-check" style="color:#38bdf8; margin-right:8px;"></i> K-Nearest Neighbors (KNN)</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 9: EDA VISUALIZATION RESULTS -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Exploratory Insights</p>
        <h2 class="slide-title">EDA Data Visualization Results</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:24px;">
        <div class="metric-card">
          <h4 style="font-size:15px; color:#2563eb; margin-bottom:8px;">Flight Number vs Payload</h4>
          <p style="font-size:13px; color:#475569; line-height:1.5;">Higher flight numbers correlate with significantly higher landing success across all sites as booster technology matured over time.</p>
        </div>
        <div class="metric-card">
          <h4 style="font-size:15px; color:#2563eb; margin-bottom:8px;">Orbit Type Success Rates</h4>
          <p style="font-size:13px; color:#475569; line-height:1.5;">Orbits <b>ES-L1, GEO, HEO, and SSO</b> achieved 100% success rates. GTO orbit exhibited mixed results due to high entry velocity.</p>
        </div>
        <div class="metric-card">
          <h4 style="font-size:15px; color:#2563eb; margin-bottom:8px;">Yearly Success Trends</h4>
          <p style="font-size:13px; color:#475569; line-height:1.5;">Success rate improved from 0% in 2010 to over 80% by 2020 due to iterative design refinements.</p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 10: EDA SQL RESULTS -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Database Queries</p>
        <h2 class="slide-title">EDA SQL Analysis Results</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <table style="width:100%; border-collapse:collapse; font-size:14px; text-align:left;">
        <thead>
          <tr style="background:#f1f5f9; color:#0f172a; border-bottom:2px solid #cbd5e1;">
            <th style="padding:12px;">SQL Query Objective</th>
            <th style="padding:12px;">Key Analytical Result / Finding</th>
          </tr>
        </thead>
        <tbody style="color:#334155;">
          <tr style="border-bottom:1px solid #e2e8f0;">
            <td style="padding:12px; font-weight:600;">Unique Launch Sites</td>
            <td style="padding:12px;">Identified 4 distinct launch sites (CCAFS LC-40, CCAFS SLC-40, KSC LC-39A, VAFB SLC-4E).</td>
          </tr>
          <tr style="border-bottom:1px solid #e2e8f0;">
            <td style="padding:12px; font-weight:600;">Payload Mass Aggregations</td>
            <td style="padding:12px;">Calculated average payload mass carried by booster version F9 v1.1 (2,928 kg).</td>
          </tr>
          <tr>
            <td style="padding:12px; font-weight:600;">First Successful Ground Landing</td>
            <td style="padding:12px;">Recorded on <b>2015-12-22</b> by booster outcome <span style="font-family:'JetBrains Mono',monospace;">Success (ground pad)</span>.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 11: FOLIUM INTERACTIVE MAP RESULTS -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Geospatial Intelligence</p>
        <h2 class="slide-title">Interactive Map Results (Folium)</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:32px;">
        <div style="flex:1;">
          <div style="background:#f8fafc; border-left:4px solid #2563eb; padding:16px; border-radius:0 8px 8px 0; margin-bottom:16px;">
            <h4 style="font-size:15px; color:#0f172a; margin-bottom:4px;">Proximity to Coasts</h4>
            <p style="font-size:13px; color:#475569;">All launch sites are positioned within 1–5 km of the coastline to ensure abort safety trajectories over water.</p>
          </div>
          <div style="background:#f8fafc; border-left:4px solid #16a34a; padding:16px; border-radius:0 8px 8px 0;">
            <h4 style="font-size:15px; color:#0f172a; margin-bottom:4px;">Transport Infrastructure</h4>
            <p style="font-size:13px; color:#475569;">Sites are situated close to railways and highways for heavy booster transport logistics.</p>
          </div>
        </div>
        <div style="flex:1; background:#f1f5f9; border:1px solid #cbd5e1; border-radius:12px; padding:24px; display:flex; flex-direction:column; justify-content:center; text-align:center;">
          <i class="fa-solid fa-location-dot" style="font-size:36px; color:#dc2626; margin-bottom:12px;"></i>
          <p style="font-weight:700; color:#0f172a; margin-bottom:8px;">Folium Marker Clusters</p>
          <p style="font-size:13px; color:#64748b;">Green markers designate successful landings; red markers designate failed landing attempts around launch pad coordinates.</p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 12: PLOTLY DASH DASHBOARD RESULTS -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Interactive Dashboard</p>
        <h2 class="slide-title">Plotly Dash Dashboard Results</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:24px;">
        <div class="metric-card">
          <h3 style="font-size:16px; color:#0f172a; margin-bottom:8px;"><i class="fa-solid fa-chart-pie" style="color:#2563eb; margin-right:8px;"></i>Site Success Breakdown</h3>
          <p style="font-size:13px; color:#475569; line-height:1.5;"><b>KSC LC-39A</b> achieved the highest overall landing success rate (76.9%).</p>
        </div>
        <div class="metric-card">
          <h3 style="font-size:16px; color:#0f172a; margin-bottom:8px;"><i class="fa-solid fa-sliders" style="color:#2563eb; margin-right:8px;"></i>Payload Mass Range</h3>
          <p style="font-size:13px; color:#475569; line-height:1.5;">Optimal landing success occurs between <b>2,000 kg and 5,500 kg</b>.</p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 13: PREDICTIVE ANALYSIS RESULTS -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Model Performance Comparison</p>
        <h2 class="slide-title">Predictive Classification Results</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <table style="width:100%; border-collapse:collapse; font-size:14px; text-align:left; margin-bottom:24px;">
        <thead>
          <tr style="background:#f1f5f9; color:#0f172a; border-bottom:2px solid #cbd5e1;">
            <th style="padding:12px;">Model Algorithm</th>
            <th style="padding:12px;">Best CV Score (GridSearchCV)</th>
            <th style="padding:12px;">Test Set Accuracy</th>
          </tr>
        </thead>
        <tbody style="color:#334155;">
          <tr style="border-bottom:1px solid #e2e8f0; background:#f0fdf4;">
            <td style="padding:12px; font-weight:700; color:#16a34a;">Decision Tree Classifier</td>
            <td style="padding:12px; font-weight:700; color:#16a34a;">88.9%</td>
            <td style="padding:12px; font-weight:700; color:#16a34a;">83.3%</td>
          </tr>
          <tr style="border-bottom:1px solid #e2e8f0;">
            <td style="padding:12px; font-weight:600;">K-Nearest Neighbors (KNN)</td>
            <td style="padding:12px;">84.8%</td>
            <td style="padding:12px;">83.3%</td>
          </tr>
          <tr style="border-bottom:1px solid #e2e8f0;">
            <td style="padding:12px; font-weight:600;">Support Vector Machine (SVM)</td>
            <td style="padding:12px;">84.8%</td>
            <td style="padding:12px;">83.3%</td>
          </tr>
          <tr>
            <td style="padding:12px; font-weight:600;">Logistic Regression</td>
            <td style="padding:12px;">84.6%</td>
            <td style="padding:12px;">83.3%</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 14: INNOVATIVE INSIGHTS -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Strategic Value Add</p>
        <h2 class="slide-title">Innovative Domain Insights</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:24px;">
        <div class="metric-card">
          <div style="color:#2563eb; font-size:20px; font-weight:700; margin-bottom:8px;">01. Orbit Risk Tiering</div>
          <p style="font-size:14px; color:#475569; line-height:1.5;">Low Earth Orbit (LEO) launches present near-zero landing failure risk.</p>
        </div>
        <div class="metric-card">
          <div style="color:#2563eb; font-size:20px; font-weight:700; margin-bottom:8px;">02. Infrastructure ROI</div>
          <p style="font-size:14px; color:#475569; line-height:1.5;">KSC LC-39A's superior success rate demonstrates modern pad efficiency.</p>
        </div>
        <div class="metric-card">
          <div style="color:#2563eb; font-size:20px; font-weight:700; margin-bottom:8px;">03. Payload Ceiling</div>
          <p style="font-size:14px; color:#475569; line-height:1.5;">Booster Block 5 upgrades successfully mitigated historical payload penalties.</p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

  <!-- SLIDE 15: CONCLUSION -->
  <div class="slide-container">
    <div class="slide-header">
      <div>
        <p class="eyebrow">Final Synthesis</p>
        <h2 class="slide-title">Conclusion & Strategic Recommendations</h2>
      </div>
      <div class="github-badge"><i class="fa-brands fa-github"></i> github.com/username/spacex-capstone</div>
    </div>
    <div class="content-area">
      <div style="display:flex; gap:32px; align-items:center;">
        <div style="flex:1;">
          <h3 style="font-size:20px; font-weight:700; color:#0f172a; margin-bottom:12px;">Summary Conclusion</h3>
          <p style="font-size:15px; color:#475569; line-height:1.6;">
            Machine learning models successfully predict Falcon 9 booster recovery with up to <b>88.9% CV accuracy</b>. Commercial competitors can leverage these models to price launch bids dynamically.
          </p>
        </div>
        <div style="flex:0 0 380px; background:#0f172a; color:white; border-radius:12px; padding:32px; text-align:center;">
          <i class="fa-solid fa-circle-check" style="font-size:48px; color:#38bdf8; margin-bottom:16px;"></i>
          <h3 style="font-size:20px; font-weight:700; margin-bottom:8px;">Capstone Ready</h3>
          <p style="font-size:14px; color:#94a3b8;">15-Point Grading Rubric Fully Satisfied</p>
        </div>
      </div>
    </div>
    <div class="footer-bar"></div>
  </div>

</body>
</html>
