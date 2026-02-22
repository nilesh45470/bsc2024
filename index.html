<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Information Directory</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* CSS Reset & Base Styles */
        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fafc;
            color: #334155;
            line-height: 1.5;
            -webkit-font-smoothing: antialiased;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            overflow-x: hidden; 
            width: 100vw;
            max-width: 100%;
        }

        /* Top Navigation */
        .top-navbar {
            background-color: #ffffff;
            border-bottom: 1px solid #e2e8f0;
            padding: 1rem 2rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .brand-container { display: flex; align-items: center; gap: 1rem; }
        .top-navbar h1 { font-size: 1.25rem; font-weight: 600; color: #0f172a; }
        .badge-total {
            background-color: #e0e7ff; color: #4f46e5;
            padding: 0.25rem 0.75rem; border-radius: 9999px;
            font-size: 0.85rem; font-weight: 600;
        }

        /* Search Trigger Button */
        .nav-search-btn {
            background-color: #f1f5f9;
            color: #475569;
            border: 1px solid #e2e8f0;
            padding: 0.6rem 1.2rem;
            border-radius: 9999px;
            font-size: 0.95rem;
            font-weight: 500;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.2s ease;
        }
        .nav-search-btn:hover { background-color: #e2e8f0; color: #0f172a; }
        .nav-search-btn svg { width: 18px; height: 18px; }

        /* Main Container */
        .container { width: 100%; margin: 0 auto; padding: 2rem; flex-grow: 1; }

        /* Full Screen Search Overlay */
        .search-overlay {
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            background-color: rgba(15, 23, 42, 0.4);
            backdrop-filter: blur(4px);
            z-index: 1000;
            display: flex; justify-content: center; align-items: flex-start;
            padding-top: 10vh;
            opacity: 0; pointer-events: none;
            transition: opacity 0.3s ease;
        }

        .search-overlay.active { opacity: 1; pointer-events: all; }

        .search-modal {
            background: #ffffff;
            width: 90%; max-width: 700px;
            border-radius: 12px;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
            transform: translateY(-20px);
            transition: transform 0.3s cubic-bezier(0.16, 1, 0.3, 1);
            display: flex; flex-direction: column;
            overflow: hidden;
            max-height: 80vh; 
        }

        .search-overlay.active .search-modal { transform: translateY(0); }

        .search-input-group {
            display: flex; align-items: center;
            padding: 1rem 1.5rem;
            border-bottom: 1px solid #e2e8f0;
            background-color: #ffffff;
            z-index: 2;
        }
        .search-icon-svg { color: #94a3b8; width: 22px; height: 22px; margin-right: 12px; }
        
        #studentNameInput {
            flex-grow: 1; border: none; font-size: 1.1rem;
            color: #0f172a; outline: none; background: transparent;
        }
        #studentNameInput::placeholder { color: #94a3b8; }

        /* Modern Circular Close Icon */
        .close-search-btn {
            background: #f1f5f9; border: none; color: #64748b;
            width: 32px; height: 32px; border-radius: 50%;
            display: flex; justify-content: center; align-items: center;
            cursor: pointer; transition: all 0.2s; margin-left: 10px;
        }
        .close-search-btn:hover { background: #e2e8f0; color: #ef4444; }

        /* Search Results inside Modal */
        #searchResults { 
            overflow-y: auto; display: none; flex-grow: 1; 
            background: #ffffff; padding-bottom: 1rem;
            -webkit-overflow-scrolling: touch; /* Smooth scroll on iOS */
        }
        #searchResults.visible { display: block; }
        #searchResults ul { list-style: none; }
        #searchResults ul li {
            padding: 1rem 1.5rem; border-bottom: 1px solid #f8fafc;
            cursor: pointer; font-size: 0.95rem; color: #334155;
            display: flex; justify-content: space-between; align-items: center;
        }
        #searchResults ul li:hover { background-color: #f8fafc; color: #0f172a; }
        .search-prn-badge { font-size: 0.8rem; background: #e0f2fe; color: #0284c7; padding: 2px 8px; border-radius: 12px; }
        .no-results { padding: 1.5rem; text-align: center; color: #64748b; font-size: 0.95rem; }

        /* Top Profile Card */
        #studentProfile {
            background: #ffffff; border: 1px solid #e2e8f0; border-left: 4px solid #3b82f6;
            border-radius: 8px; padding: 2rem; margin-bottom: 2rem;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05); display: none;
            transition: opacity 0.3s ease, transform 0.3s ease;
        }
        #studentProfile.visible { display: block; animation: slideDownProfile 0.4s cubic-bezier(0.16, 1, 0.3, 1); }

        /* Shared Profile Layout */
        .profile-header {
            display: flex; justify-content: space-between; align-items: center;
            margin-bottom: 1.25rem; padding-bottom: 0.75rem; border-bottom: 1px solid #f1f5f9;
        }
        .profile-header h4 { font-size: 1.15rem; color: #0f172a; font-weight: 600; }
        .close-profile-btn { background: none; border: none; font-size: 1.2rem; cursor: pointer; color: #94a3b8; }
        .close-profile-btn:hover { color: #ef4444; }

        .profile-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 1.5rem; }
        .profile-field { display: flex; flex-direction: column; }
        .profile-field strong { font-size: 0.7rem; text-transform: uppercase; color: #64748b; margin-bottom: 0.25rem; font-weight: 600;}
        .profile-field span { font-size: 0.95rem; color: #0f172a; font-weight: 500; word-break: break-word; }

        /* Data Table */
        .table-card {
            background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px;
            overflow: hidden; box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1); width: 100%;
        }

        .table-scroll-container { max-height: 75vh; overflow-y: auto; overflow-x: hidden; width: 100%; }
        table { width: 100%; border-collapse: collapse; text-align: left; table-layout: auto; }
        
        th {
            background-color: #f8fafc; padding: 0.875rem 1rem; font-size: 0.75rem;
            font-weight: 600; text-transform: uppercase; color: #64748b;
            border-bottom: 1px solid #e2e8f0; position: sticky; top: 0;
            z-index: 10; cursor: pointer; user-select: none;
        }
        th:hover { background-color: #f1f5f9; color: #0f172a; }

        td {
            padding: 0.875rem 1rem; font-size: 0.875rem; color: #334155;
            border-bottom: 1px solid #f1f5f9; word-break: break-word; overflow-wrap: break-word;
        }

        th:nth-child(1), td:nth-child(1) { width: 40px; text-align: center; color: #94a3b8; font-size: 0.75rem; padding: 0.5rem; }
        td:nth-child(2) { font-weight: 500; color: #0f172a; } 
        td:nth-child(4) { font-family: monospace; font-size: 0.9em; color: #475569; }

        tbody tr.student-row { transition: background-color 0.2s ease; cursor: pointer; }
        tbody tr.student-row:hover { background-color: #f8fafc; }
        tbody tr.student-row.active-row { background-color: #e0f2fe; border-left: 3px solid #0ea5e9; }

        /* Inline Detail Profile (Accordion) */
        .inline-detail-row { background-color: #f8fafc; }
        .inline-detail-row td { padding: 0 !important; border-bottom: 1px solid #e2e8f0; }
        
        .inline-profile-card {
            padding: 1.5rem 2rem; background: #ffffff;
            border-top: 1px solid #e0f2fe; box-shadow: inset 0 4px 6px -4px rgba(0, 0, 0, 0.05);
            animation: slideDownProfile 0.3s cubic-bezier(0.16, 1, 0.3, 1) forwards;
            transform-origin: top;
        }

        @keyframes slideDownProfile {
            from { opacity: 0; transform: scaleY(0.95); max-height: 0; padding-top: 0; padding-bottom: 0; }
            to { opacity: 1; transform: scaleY(1); max-height: 500px; }
        }

        /* Scrollbar */
        ::-webkit-scrollbar { width: 6px; height: 6px; }
        ::-webkit-scrollbar-track { background: transparent; }
        ::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #94a3b8; }

        /* Responsive - Mobile/Tablet adjustments */
        @media (max-width: 768px) {
            .container { padding: 1rem; }
            th, td { padding: 0.5rem 0.25rem; font-size: 0.75rem; }
            th { font-size: 0.6rem; letter-spacing: 0; }
            .inline-profile-card, #studentProfile { padding: 1rem; }
            .top-navbar { padding: 1rem; }
            .nav-search-btn span { display: none; } 
            .nav-search-btn { padding: 0.6rem; }
            
            /* Convert Search Modal to Full-Screen App view on Mobile */
            .search-overlay { padding-top: 0; }
            .search-modal {
                width: 100%; height: 100%; max-width: none; border-radius: 0;
                max-height: 100vh;
            }
        }
    </style>
</head>
<body>

    <header class="top-navbar">
        <div class="brand-container">
            <h1>Student Directory</h1>
            <span class="badge-total" id="totalCount">Total: 0</span>
        </div>
        
        <button class="nav-search-btn" onclick="openSearch()">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <circle cx="11" cy="11" r="8"></circle>
                <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
            </svg>
            <span>Search</span>
        </button>
    </header>

    <div id="searchOverlay" class="search-overlay" onclick="handleOverlayClick(event)">
        <div class="search-modal" onclick="event.stopPropagation()">
            <div class="search-input-group">
                <svg class="search-icon-svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <circle cx="11" cy="11" r="8"></circle>
                    <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
                </svg>
                
                <input type="text" id="studentNameInput" placeholder="Search name, PRN, email, or mobile..." onkeyup="handleSearchInput(event)">
                
                <button class="close-search-btn" onclick="closeSearch()" title="Close Search">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="width: 16px; height: 16px;">
                        <line x1="18" y1="6" x2="6" y2="18"></line>
                        <line x1="6" y1="6" x2="18" y2="18"></line>
                    </svg>
                </button>
            </div>
            <div id="searchResults"></div>
        </div>
    </div>

    <main class="container">
        <div id="studentProfile"></div>

        <div class="table-card">
            <div class="table-scroll-container" id="tableScrollContainer">
                <table id="mainTable">
                    <thead>
                        <tr>
                            <th onclick="sortTable(0)" title="Sort Original">#</th>
                            <th onclick="sortTable(1)">Name</th>
                            <th onclick="sortTable(2)">Category</th>
                            <th onclick="sortTable(3)">PRN No.</th>
                            <th onclick="sortTable(4)">Address</th>
                            <th onclick="sortTable(5)">Blood Grp</th>
                            <th onclick="sortTable(6)">Email ID</th>
                            <th onclick="sortTable(7)">Mobile No.</th>
                            <th onclick="sortTable(8)">DOB</th>
                        </tr>
                    </thead>
                    <tbody id="studentTableBody">
                        <tr class="student-row"><td>1</td><td>Aaware Prajakta Anil</td><td>OBC</td><td>2024015400331491</td><td>Shindi</td><td>O+</td><td>prajaktaaware684@gmail.com</td><td>8600951543</td><td>07 June 2006</td></tr>
                        <tr class="student-row"><td>2</td><td>Agnihotri Sanyukta Laxmikant</td><td></td><td>2024015400336526</td><td></td><td></td><td></td><td></td><td>22 April 2005</td></tr>
                        <tr class="student-row"><td>3</td><td>Ahire Gaurav Ganesh</td><td>OBC</td><td>2024015400350252</td><td>Waghdu</td><td>B+</td><td>ahire623@gmail.com</td><td>9529759898</td><td></td></tr>
                        <tr class="student-row"><td>4</td><td>Ahire Harshadada Nana</td><td>SC</td><td>2024015400331219</td><td>Mehunbare</td><td>O+</td><td>harshadaa213@gmail.com</td><td>7822866539</td><td></td></tr>
                        <tr class="student-row"><td>5</td><td>Ahire Kunal Bapu</td><td>SC</td><td>2024015400332076</td><td>Ranjangaon</td><td>B+</td><td>kunalahire283@gmail.com</td><td>9561244610</td><td>17 March 2007</td></tr>
                        <tr class="student-row"><td>6</td><td>Ahire Rutuja Satish</td><td>OBC</td><td>2024015400353045</td><td>Tambhole</td><td>B+</td><td>rg322700701@gmail.com</td><td>9322700701</td><td></td></tr>
                        <tr class="student-row"><td>7</td><td>Ahirrao Amruta Himmat</td><td>OBC</td><td>2024015400331556</td><td>Khadakiseem</td><td>O+</td><td>krishnaahirao832@gmail.com</td><td>7447504352</td><td></td></tr>
                        <tr class="student-row"><td>8</td><td>Andholkar Srushti Vinod</td><td>OBC</td><td>2024015400342287</td><td>Chalisgaon</td><td>B+</td><td>srushtiandholkar@gmail.com</td><td>8975826609</td><td></td></tr>
                        <tr class="student-row"><td>9</td><td>Atif Khan Nasir Khan</td><td>UR</td><td>2024015400350492</td><td>Chalisgaon</td><td></td><td>khanaatef37@gmail.com</td><td>7507860933</td><td></td></tr>
                        <tr class="student-row"><td>10</td><td>Baig Saniya Mirza Amjad Baig</td><td></td><td>2024015400342322</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>11</td><td>Baig Zafar Abdul Wahed</td><td></td><td>2024015400351762</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>12</td><td>Bairagi Sakshi Dharmadas</td><td></td><td>2024015400342562</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>13</td><td>Bangale Vaidhahi Vijay</td><td>OBC</td><td>2024015400342411</td><td>Waghali</td><td>O+</td><td>vaidhahibangale3@gmail.com</td><td>7030682101</td><td></td></tr>
                        <tr class="student-row"><td>14</td><td>Barve Pallavi Bausaheb</td><td>OBC</td><td>2024015400331413</td><td>Shindi</td><td>O+</td><td>bhausahebbarve888@gmail.com</td><td>9503842980</td><td>03 July 2007</td></tr>
                        <tr class="student-row"><td>15</td><td>Bhalerao Diksha Ganesh</td><td></td><td>2024015400350372</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>16</td><td>Bhoite Tulsi Mahendra</td><td></td><td>2024015400331107</td><td>Bhavali</td><td>B+</td><td></td><td>9370412557</td><td></td></tr>
                        <tr class="student-row"><td>17</td><td>Birari Rushikesh Ravindra</td><td>OBC</td><td>2024015400342426</td><td>Nagardeola</td><td>A+</td><td>patilrushikeshr5@gmail.com</td><td>9209275700</td><td></td></tr>
                        <tr class="student-row"><td>18</td><td>Borse Gayatri Gorakshanath</td><td>OBC</td><td>2024015400342264</td><td>Daskebardi</td><td>B+</td><td>gorakhborse149@gmail.com</td><td>9511825138</td><td></td></tr>
                        <tr class="student-row"><td>19</td><td>Chaudhari Tejashree Chandrakant</td><td></td><td>2024015400330038</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>20</td><td>Chavan Chetan Nandkishor</td><td></td><td>2024015400331483</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>21</td><td>Chavan Gayatri Aaba</td><td>OBC</td><td>2024015400347741</td><td>Pimparkheda</td><td>O+</td><td>atul14486@gmail.com</td><td>7776015275</td><td></td></tr>
                        <tr class="student-row"><td>22</td><td>Chavan Prem Anil</td><td></td><td>2024015400330166</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>23</td><td>Chavan Sakshi Kiran</td><td>OBC</td><td>2024015400352452</td><td>Hingone</td><td>A+</td><td>kiranchvan019990@gmail.com</td><td></td><td>03 October 2005</td></tr>
                        <tr class="student-row"><td>24</td><td>Chavan Sandesh Vinayakrao</td><td></td><td>2024015400330069</td><td>Ranjangaon</td><td></td><td></td><td></td><td></td></tr> 
                        <tr class="student-row"><td>25</td><td>Chavhan Rohit Ratilal</td><td>OBC</td><td>2024015400331692</td><td>Bhadgaon</td><td>O-</td><td>chavenratilal@gmail.com</td><td>8806768055</td><td></td></tr>
                        <tr class="student-row"><td>26</td><td>Daund Pratiksha Ganesh</td><td></td><td>2024015400347691</td><td>Shindi</td><td>B+</td><td>pratikshadaund09@gmail.com</td><td>8407970578</td><td></td></tr>
                        <tr class="student-row"><td>27</td><td>Deokar Asmita Narayan</td><td></td><td>2024015400330093</td><td>Palasare</td><td></td><td>asmitadeokar5@gmail.com</td><td>8407970578</td><td></td></tr>
                        <tr class="student-row"><td>28</td><td>Deokar Hitesh Dattatray</td><td>OBC</td><td>2024015400350414</td><td>Nandgaon</td><td>AB+</td><td>hiteshdeokar143@gmail.com</td><td>8668325979</td><td></td></tr>
                        <tr class="student-row"><td>29</td><td>Deokar Shubhangi Sunilrao</td><td>SBC</td><td>2024015400330576</td><td>Palasare</td><td>A+</td><td>shybangideokar80@gmail.com</td><td>8007271688</td><td></td></tr>
                        <tr class="student-row"><td>30</td><td>Deore Devyani Bhimsing</td><td></td><td>2024015400331274</td><td>Pimpri</td><td>A+</td><td>bhimsingdeokar@gmail.com</td><td>8766981767</td><td></td></tr>
                        <tr class="student-row"><td>31</td><td>Deore Sakshi Pradip</td><td></td><td>2024015400331081</td><td>Kargaon</td><td>A+</td><td>pradipdeore0007@gmail.com</td><td>9850279436</td><td></td></tr>
                        <tr class="student-row"><td>32</td><td>Desale Tanmay Diliprao</td><td>OBC</td><td>2024015400350484</td><td>Bramanshevga</td><td></td><td>desaleking5132@gmail.com</td><td>9307210232</td><td></td></tr>
                        <tr class="student-row"><td>33</td><td>Deshmukh Jayashree Umeshrao</td><td></td><td>2024015400331121</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>34</td><td>Deshmukh Kalyani Hemant</td><td></td><td>2024015400330085</td><td>Mehunbare</td><td>O+</td><td>hemantdeshmukh5498@gmail.com</td><td>8446778580</td><td></td></tr>
                        <tr class="student-row"><td>35</td><td>Deshmukh Sai Sanjay</td><td></td><td>2024015400331452</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>36</td><td>Dhangar Aniket Dipak</td><td></td><td>2024015400342515</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>37</td><td>Dhangar Chetana Somnath</td><td></td><td>2024015400352444</td><td></td><td></td><td></td><td></td><td>29 December 2006</td></tr>
                        <tr class="student-row"><td>38</td><td>Dhangar Shishupal Nimba</td><td>DTNT</td><td>2024015400336573</td><td>Akhatwade</td><td>O+</td><td>dhangarvijaya1@gmail.com</td><td>7498239474</td><td></td></tr>
                        <tr class="student-row"><td>39</td><td>Dusane Diksha Sunil</td><td></td><td>2024015400331564</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>40</td><td>Gaikwad Disha Bhanudas</td><td></td><td>2024015400330611</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>41</td><td>Gaikwad Komal Prakash</td><td>OBC</td><td>2024015400331637</td><td>Pimparkheda</td><td>O+</td><td>komalgaikwaqd02@gmail.com</td><td>8805529988</td><td></td></tr>
                        <tr class="student-row"><td>42</td><td>Gawali Chaitanya Anil</td><td></td><td>2024015400330626</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>43</td><td>Gawali Prachi Kishor</td><td></td><td>2024015400331018</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>44</td><td>Gawali Pravin Dattu</td><td></td><td>2024015400350317</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>45</td><td>Gore Siddhi Pradip</td><td>OBC</td><td>2024015400331517</td><td>Chalisgaon</td><td>A+</td><td>siddhipagare678@gmail.com</td><td>7387762134</td><td></td></tr>
                        <tr class="student-row"><td>46</td><td>Gore Vedant Amol</td><td></td><td>2024015400341632</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>47</td><td>Gosavi Mansi Ramchandra</td><td>OBC</td><td>2024015400331177</td><td>Chalisgaon</td><td>B+</td><td>mansigosavi3172006@gmail.com</td><td>9850329811</td><td></td></tr>
                        <tr class="student-row"><td>48</td><td>Ingale Ganesh Satish</td><td></td><td>2024015400342306</td><td>Hirapur</td><td>B+</td><td>ganeshingale9309@gmail.com</td><td>9356802851</td><td></td></tr>
                        <tr class="student-row"><td>49</td><td>Jadhav Chitali Aaba</td><td></td><td>2024015400347613</td><td>Mundkheda</td><td>O+</td><td></td><td>9970972201</td><td></td></tr>
                        <tr class="student-row"><td>50</td><td>Jadhav Chitali Ekhanath</td><td>OBC</td><td>2024015400342272</td><td>Tambhole</td><td>B+</td><td>jadhavkuldip62@gmail.com</td><td>8767373411</td><td></td></tr>
                        <tr class="student-row"><td>51</td><td>Jadhav Premkumar Pandurang</td><td>OBC</td><td>2024015400331049</td><td>Pimparkheda</td><td></td><td>premjadhav9373@gmail.com</td><td>9373295729</td><td></td></tr>
                        <tr class="student-row"><td>52</td><td>Jadhav Poonam Madan</td><td>SC</td><td>2024015400347497</td><td>Bilakhed</td><td>A+</td><td></td><td>9209466642</td><td></td></tr>
                        <tr class="student-row"><td>53</td><td>Jadhav Sakshi Ravindra</td><td></td><td>2024015400331997</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>54</td><td>Jadhav Yash Vijay</td><td>SC</td><td>2024015400332001</td><td>Chalisgaon</td><td>B+</td><td>premjadhav9373@gmail.com</td><td>8237204091</td><td></td></tr>
                        <tr class="student-row"><td>55</td><td>Jagtap Chaitali Dagadu</td><td>OBC</td><td>2024015400342376</td><td>Pimparkheda</td><td>O+</td><td>chaitalijagtap2103@gmail.com</td><td>7620662706</td><td></td></tr>
                        <tr class="student-row"><td>56</td><td>Jagtap Roshani Anil</td><td></td><td>2024015400351754</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>57</td><td>Kadam Samir Sadu</td><td></td><td>2024015400342105</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>58</td><td>Kapdane Vaishnavi Aniln</td><td>OBC</td><td>2024015400331297</td><td>Chalisgaon</td><td>B+</td><td>kapadanevaishnavi@gmail.com</td><td>9423344160</td><td>25 April 2006</td></tr>
                        <tr class="student-row"><td>59</td><td>Katkar Jayshri Pravin</td><td></td><td>2024015400330051</td><td>Nagardevla</td><td>AB+</td><td>jayashrikatkar59@gmail.com</td><td>7558658310</td><td></td></tr>
                        <tr class="student-row"><td>60</td><td>Kavde Asavari Dipak</td><td>OBC</td><td>2024015400331703</td><td>Chitegaon</td><td>O+</td><td>dipakkavade4607@gmail.com</td><td>9561283628</td><td></td></tr>
                        <tr class="student-row"><td>61</td><td>Khairnar Harshad Bhagwat</td><td></td><td>2024015400331227</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>62</td><td>Khan Irfan Khaleel</td><td>UR</td><td>2024015400331332</td><td>Piparkhed</td><td></td><td>khanirfangt@gmail.com</td><td>8080402813</td><td></td></tr>
                        <tr class="student-row"><td>63</td><td>Khan Misbah Firoz</td><td></td><td>2024015400347675</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>64</td><td>Khan Samir Akil</td><td></td><td>2024015400331974</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>65</td><td>Khan Zulfin Rais</td><td></td><td>2024015400331316</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>66</td><td>Khatik Sahil Yunus</td><td>UR</td><td>2024015400331324</td><td>Chalisgaon</td><td></td><td>khatiksahil9021@gmail.com</td><td>9021891628</td><td>6 June 2005</td></tr>
                        <tr class="student-row"><td>67</td><td>Koli Amol Raju</td><td></td><td>2024015400330603</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>68</td><td>Koli Samadhan Anil</td><td></td><td>2024015400347725</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>69</td><td>Kumavat Jyoti Suresh</td><td>OBC</td><td>2024015400347377</td><td>Chalisgaon</td><td>AB+</td><td>vidhyakumavat22@gmail.com</td><td>8830183623</td><td></td></tr>
                        <tr class="student-row"><td>70</td><td>Kumavat Nandini Somnath</td><td>OBC</td><td>2024015400332029</td><td>Beldarvadi</td><td>B+</td><td>nanadinikumavat691@gmail.com</td><td>7620579189</td><td></td></tr>
                        <tr class="student-row"><td>71</td><td>Kumavat Roshan Sambhaji</td><td></td><td>2024015400330762</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>72</td><td>Kumavat Shruti Dipak</td><td></td><td>2024015400331266</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>73</td><td>Kumavat Vishakhha Bhausaheb</td><td>DTNT</td><td>2024015400341624</td><td>Beldarvadi</td><td>B+</td><td>vishakhakumavat580@gmail.com</td><td>9699813541</td><td></td></tr>
                        <tr class="student-row"><td>74</td><td>Kuvar Gayatri Bhaiyasaheb</td><td>OBC</td><td>2024015400347683</td><td>Khadakiseem</td><td>B+</td><td>patilbhaiyyasaheb7@gmail.com</td><td>9970389982</td><td></td></tr>
                        <tr class="student-row"><td>75</td><td>Magar Rushikesh Sanjay</td><td></td><td>2024015400330077</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>76</td><td>Mahajan Hitesh Sharad</td><td>OBC</td><td>2024015400331742</td><td>Bhadgaon</td><td>AB+</td><td>sharadmali864@gmail.com</td><td>7767828516</td><td></td></tr>
                        <tr class="student-row"><td>77</td><td>Mahajan Kalpesh Santosh</td><td></td><td>2024015400331533</td><td>Nagardevla</td><td>B+</td><td>kdwarkadhish369@gmail.com</td><td>8550948172</td><td></td></tr>
                        <tr class="student-row"><td>78</td><td>Mahajan Nikita Ravindra</td><td>OBC</td><td>2024015400331676</td><td>Patonda</td><td>B+</td><td>mahajanikita2006@gmail.com</td><td>9503735744</td><td>21 November 2006</td></tr>
                        <tr class="student-row"><td>79</td><td>Mahajan Priti Janardhan</td><td>OBC</td><td>2024015400332084</td><td>Bhagaon</td><td>B+</td><td>deeptijm04@gmail.com</td><td>8459747834</td><td></td></tr>
                        <tr class="student-row"><td>80</td><td>Mahajan Roshani Shalik</td><td>OBC</td><td>2024015400342217</td><td>Patonda</td><td>B+</td><td>mahajanroshani592@gmail.com</td><td>9922707185</td><td>26 December 2005</td></tr>
                        <tr class="student-row"><td>81</td><td>Mahajan Saurav Kishor</td><td></td><td>2024015400342554</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>82</td><td>Mahale Kirti Indrasing</td><td></td><td>2024015400350395</td><td>Pimpri</td><td>B-</td><td>kirtimahale09@gmail.com</td><td>9860974116</td><td></td></tr>
                        <tr class="student-row"><td>83</td><td>Mali Ghansham Narayan</td><td></td><td>2024015400342337</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>84</td><td>Mali Rushikesh Vikas</td><td>OBC</td><td>2024015400350387</td><td>Daskebardi</td><td></td><td>rushikeshmali274@gmail.com</td><td>8830664245</td><td></td></tr>
                        <tr class="student-row"><td>85</td><td>Mali Vaibhavi Kailas</td><td></td><td>2024015400342183</td><td></td><td></td><td></td><td></td><td>27 January 2006</td></tr>
                        <tr class="student-row"><td>86</td><td>Mande Mayuri Dnyaneshwar</td><td>OBC</td><td>2024015400331467</td><td>Shindi</td><td></td><td>mandem9730@gmail.com</td><td>9730263096</td><td>14 July 2006</td></tr>
                        <tr class="student-row"><td>87</td><td>Mande Raj Pandurang</td><td>OBC</td><td>2024015400342577</td><td>Shindi</td><td>O-</td><td>mandepandurang3@gmail.com</td><td>8788251864</td><td></td></tr>
                        <tr class="student-row"><td>88</td><td>Marathe Shaileja Somnath</td><td></td><td>2024015400342136</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>89</td><td>Mohammad Danish Shaikh</td><td></td><td>2024015400331951</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>90</td><td>Mohim Vishal Rajendra</td><td></td><td>2024015400331308</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>91</td><td>Mulla Huneja Ifrajoddin</td><td>OBC</td><td>2024015400342225</td><td>Patonda</td><td></td><td>mulla.csn.@gmail.com</td><td>7620860031</td><td></td></tr>
                        <tr class="student-row"><td>92</td><td>Nerkar Nikhil Madhukar</td><td>OBC</td><td>2024015400341597</td><td>Ranjangaon</td><td>A+</td><td>nikhilnerkar442@gmail.com</td><td>9021820317</td><td>19 December 2006</td></tr>
                        <tr class="student-row"><td>93</td><td>Nevare Vijaya Sharad</td><td></td><td>2024015400342314</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>94</td><td>Nikam Kunal Mahendra</td><td>OBC</td><td>2024015400330642</td><td>Chinchgavhan</td><td>A+</td><td>kunalmahendranikam006@gmail.com</td><td>7620086836</td><td></td></tr>
                        <tr class="student-row"><td>95</td><td>Nikam Sakshi Dharmaraj</td><td>SC</td><td>2024015400342295</td><td>Patna</td><td></td><td>sachindharmaraj9588@gmail.com</td><td></td><td></td></tr>
                        <tr class="student-row"><td>96</td><td>Nikumbh Pooja Ravindra</td><td></td><td>2024015400331154</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>97</td><td>Padolkar Tejaswini Babulal</td><td>OBC</td><td>2024015400331111</td><td>Waghali</td><td></td><td>amolsonawane2406@gmail.com</td><td>7385629545</td><td></td></tr>
                        <tr class="student-row"><td>98</td><td>Paedeshi Achal Subhash</td><td>OBC</td><td>2024015400348984</td><td>Jamda</td><td></td><td>kp8789520@gmail.com</td><td>9226598986</td><td></td></tr>
                        <tr class="student-row"><td>99</td><td>Pardeshi Alok Chandrakant</td><td>OBC</td><td>2024015400342403</td><td>Ranjangaon</td><td></td><td></td><td></td><td>16 May 2007</td></tr>
                        <tr class="student-row"><td>100</td><td>Pardeshi Kajal Santosh</td><td>DTNT</td><td>2024015400330584</td><td>Chalisgaon</td><td></td><td></td><td>9960176028</td><td></td></tr>
                        <tr class="student-row"><td>101</td><td>Patil Ashwini Rajendra</td><td>OBC</td><td>2024015400341616</td><td>Wakadi</td><td>AB-</td><td>aash1234patil@gmail.com</td><td>9021973371</td><td></td></tr>
                        <tr class="student-row"><td>102</td><td>Patil Bhagyashri Sukhalal</td><td></td><td>2024015400352405</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>103</td><td>Patil Dimple Ravindra</td><td>OBC</td><td>2024015400330101</td><td>Deoli</td><td>AB+</td><td>dimpalpatil1010@gmail.com</td><td>9529949622</td><td></td></tr>
                        <tr class="student-row"><td>104</td><td>Patil Divya Bhagwat</td><td></td><td>2024015400336542</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>105</td><td>Patil Divya Manohar</td><td>OBC</td><td>2024015400342604</td><td>Ozar</td><td>A+</td><td>manishamanoharpatil@gmail.com</td><td>9764657280</td><td></td></tr>
                        <tr class="student-row"><td>106</td><td>Patil Gayatri Dipak</td><td></td><td>2024015400350244</td><td>Patonda</td><td>A+</td><td>9p6926395@gmail.com</td><td>9730518034</td><td></td></tr>
                        <tr class="student-row"><td>107</td><td>Patil Ghanshyam Bharat</td><td></td><td>2024015400331371</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>108</td><td>Patil Gorakhnath Kailas</td><td></td><td>2024015400331595</td><td>Nagradeola</td><td>B+</td><td>gorakhnathp19@gmail.com</td><td>7058121482</td><td></td></tr>
                        <tr class="student-row"><td>109</td><td>Patil Harshada Pravin</td><td></td><td>2024015400347501</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>110</td><td>Patil Jagruti Nandan</td><td></td><td>2024015400330141</td><td>Chalisgaon</td><td></td><td>nandanpatil1982@gmail.com</td><td>9021770253</td><td></td></tr>
                        <tr class="student-row"><td>111</td><td>Patil Jayesh Sunil</td><td>OBC</td><td>2024015400342241</td><td>Nagardevla</td><td>B+</td><td>jp7270779@gmail.com</td><td>7798994464</td><td></td></tr>
                        <tr class="student-row"><td>112</td><td>Patil Kalyani Ravindra</td><td>OBC</td><td>2024015400331386</td><td>Borkheda</td><td>A+</td><td>surekhaahirrao392@gmail.com</td><td>7972706779</td><td></td></tr>
                        <tr class="student-row"><td>113</td><td>Patil Kusum Sham</td><td>OBC</td><td>2024015400342256</td><td>Londhe</td><td>B+</td><td>nileshnikam310@gmail.com</td><td>9834248785</td><td></td></tr>
                        <tr class="student-row"><td>114</td><td>Patil Lokesh Vikas</td><td></td><td>2024015400331444</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>115</td><td>Patil Mansi Samadhan</td><td></td><td>2024015400331347</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>116</td><td>Patil Mansi Sandip</td><td>OBC</td><td>2024015400347636</td><td>Malshevaga</td><td>O+</td><td>mansipatil92700@gmail.com</td><td></td><td></td></tr>
                        <tr class="student-row"><td>117</td><td>Patil Mayuri Arun</td><td>OBC</td><td>2024015400350437</td><td>Khadkiseem</td><td>A+</td><td>mayurispatil1112@gmail.com</td><td>9860588731</td><td></td></tr>
                        <tr class="student-row"><td>118</td><td>Patil Nikita Gonesh</td><td>OBC</td><td>2024015400331201</td><td>Chalisgaon</td><td>O+</td><td>nikitapatil0305@gmail.com</td><td></td><td></td></tr>
                        <tr class="student-row"><td>119</td><td>Patil Nikita Shivaji</td><td></td><td>2024015400350476</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>120</td><td>Patil Parth Vijay</td><td>VJNT</td><td>2024015400331235</td><td>Shindwadi</td><td></td><td></td><td>9322470545</td><td>27 July 2006</td></tr>
                        <tr class="student-row"><td>121</td><td>Patil Pavan Pravin</td><td></td><td>2024015400342191</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>122</td><td>Patil Payal Manoj</td><td>OBC</td><td>2024015400331421</td><td>Kherde</td><td>O+</td><td>mp7006472@gmail.com</td><td>9359714705</td><td>4 July 2006</td></tr>
                        <tr class="student-row"><td>123</td><td>Patil Pooja Kishor</td><td>OBC</td><td>2024015400331502</td><td>Borkheda</td><td>A+</td><td>patilpooja47480@gmail.com</td><td>8485881163</td><td></td></tr>
                        <tr class="student-row"><td>124</td><td>Patil Pratiksha Bharat</td><td>OBC</td><td>2024015400330657</td><td>Borkheda</td><td></td><td>patilpratiksha5893@gmail.com</td><td>9503199281</td><td>9 March 2006</td></tr>
                        <tr class="student-row"><td>125</td><td>Patil Rahul Ananda</td><td></td><td>2024015400331935</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>126</td><td>Patil Raj Prashant</td><td>OBC</td><td>2024015400331436</td><td>Deshmukhwadi</td><td>A+</td><td>raj880844@gmail.com</td><td>8767902594</td><td></td></tr>
                        <tr class="student-row"><td>127</td><td>Patil Sakshi Arun</td><td></td><td>2024015400342167</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>128</td><td>Patil Saurav Santosh</td><td>OBC</td><td>2024015400350445</td><td>Bhadgaon</td><td></td><td>sauravspatil1007@gmail.com</td><td>9158563942</td><td></td></tr>
                        <tr class="student-row"><td>129</td><td>Patil Shailesh Pradip</td><td></td><td>2024015400330561</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>130</td><td>Patil Shivani Yashavant</td><td></td><td>2024015400331572</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>131</td><td>Patil Sneha Sunil</td><td>OBC</td><td>2024015400331711</td><td>Chalisgaon</td><td>O+</td><td>snehaspatil2022@gmail.com</td><td>9822260216</td><td></td></tr>
                        <tr class="student-row"><td>132</td><td>Patil Swami Ambadas</td><td></td><td>2024015400331282</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>133</td><td>Patil Swati Nilkanth</td><td></td><td>2024015400347702</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>134</td><td>Patil Tanmay Rajesh</td><td></td><td>2024015400330021</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>135</td><td>Patil Tanvi Babanrow</td><td>OBC</td><td>2024015400341647</td><td>Borkeda</td><td>A+</td><td>patiltanvi864@gmail.com</td><td>8010752931</td><td></td></tr>
                        <tr class="student-row"><td>136</td><td>Patil Trushna Yogesh</td><td>OBC</td><td>2024015400330119</td><td>Bilakhed</td><td></td><td>patiltrusha43@gmail.com</td><td>9022769533</td><td></td></tr>
                        <tr class="student-row"><td>137</td><td>Patil Vaishnavi Manoher</td><td>OBC</td><td>2024015400330158</td><td>Borkeda</td><td>B+</td><td>manahorpatil2121@gmail.com</td><td>7387232464</td><td></td></tr>
                        <tr class="student-row"><td>138</td><td>Patil Vishal Subhash</td><td></td><td>2024015400331525</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>139</td><td>Patil Vivek Samadhan</td><td></td><td>2024015400347861</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>140</td><td>Pawar Datta Nagraj</td><td></td><td>2024015400331912</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>141</td><td>Pawar Kaveri Hiraman</td><td>VJNT</td><td>2024015400331031</td><td>Vadgaon</td><td>O+</td><td>hiramanpawar06@gmail.com</td><td></td><td></td></tr>
                        <tr class="student-row"><td>142</td><td>Pawar Mahesh Dnyaneshwar</td><td></td><td>2024015400347667</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>143</td><td>Pawar Mohini Gorakh</td><td>OBC</td><td>2024015400347764</td><td>Nhave</td><td>AB+</td><td>gp160138@gmail.com</td><td>9764579308</td><td></td></tr>
                        <tr class="student-row"><td>144</td><td>Pawar Puja Dattatray</td><td>VJNT</td><td>2024015400331541</td><td>Vadgaon</td><td>O+</td><td>patildattatray910@gmail.com</td><td></td><td></td></tr>
                        <tr class="student-row"><td>145</td><td>Pawar Sakshi Mukesh</td><td>OBC</td><td>2024015400331475</td><td>Tambhole</td><td>B+</td><td>sakshimukesh735070@gmail.com</td><td>7822955365</td><td></td></tr>
                        <tr class="student-row"><td>146</td><td>Pawar Sanika Sunil</td><td>OBC</td><td>2024015400331405</td><td>Dhamangaon</td><td>B+</td><td>sunilbalajipawar107@gmail.com</td><td>8010124005</td><td></td></tr>
                        <tr class="student-row"><td>147</td><td>Pawar Tushar Sachin</td><td></td><td>2024015400330131</td><td>Shindi</td><td>B+</td><td>tusharpawar2209@gmail.com</td><td>7620218704</td><td></td></tr>
                        <tr class="student-row"><td>148</td><td>Pawar Vishal Ravindra</td><td></td><td>2024015400330127</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>149</td><td>Pilore Mahesh Bhausaheb</td><td></td><td>2024015400331193</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>150</td><td>Rajput Chetna Bhimsing</td><td>DTNT</td><td>2024015400347652</td><td>Mehunbare</td><td>B+</td><td>rajputchetna795@gmail.com</td><td>9209749683</td><td></td></tr>
                        <tr class="student-row"><td>151</td><td>Rajput Kalyani Nitin</td><td></td><td>2024015400336534</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>152</td><td>Rajput Mitali Ravindra</td><td></td><td>2024015400347362</td><td>Chalisgaon</td><td></td><td>rajashrirajput6@gmail.com</td><td>8888540571</td><td></td></tr>
                        <tr class="student-row"><td>153</td><td>Rajput Pradip Subhash</td><td></td><td>2024015400351777</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>154</td><td>Rajput Priti Nilesh</td><td></td><td>2024015400331185</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>155</td><td>Rajput Sonali Vijay</td><td>DTNT</td><td>2024015400330665</td><td>Bangaon</td><td></td><td>pardeshibarku@gmail.com</td><td>985070701</td><td></td></tr>
                        <tr class="student-row"><td>156</td><td>Rathod Kartik Kalu</td><td></td><td>2024015400330634</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>157</td><td>Rathod Nitin Suresh</td><td></td><td>2024015400341856</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>158</td><td>Salunkhe Divya Sanjay</td><td>OBC</td><td>2024015400347482</td><td>Mahunbare</td><td></td><td>divya16csn@gmail.com</td><td>9689962573</td><td></td></tr>
                        <tr class="student-row"><td>159</td><td>Salunkhe Supriya Ankush</td><td>OBC</td><td>2024015400341872</td><td>Mehunbare</td><td>O+</td><td>supriyasalunke7757@gmail.com</td><td>7757860745</td><td></td></tr>
                        <tr class="student-row"><td>160</td><td>Savalkar Snehal Nana</td><td>OBC</td><td>2024015400331394</td><td>Patonda</td><td>B+</td><td>snehalsavarkar98@gmail.com</td><td>9021229275</td><td></td></tr>
                        <tr class="student-row"><td>161</td><td>Shaikh Affan Javed</td><td></td><td>2024015400331982</td><td>Bhadgaon</td><td></td><td>aadfuuzz85658@gmail.com</td><td>8800423551</td><td></td></tr>
                        <tr class="student-row"><td>162</td><td>Shaikh Alfiya Shaikh</td><td></td><td>2024015400341601</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>163</td><td>Shaikh Aman Aarif</td><td></td><td>2024015400351804</td><td>Chalisgaon</td><td>B+</td><td>amanshekhcsn@gmail.com</td><td>9579142270</td><td></td></tr>
                        <tr class="student-row"><td>164</td><td>Shaikh Arkan Zubair</td><td></td><td>2024015400342345</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>165</td><td>Shaikh Farhan Sagir</td><td></td><td>2024015400331966</td><td>Chalisgaon</td><td>O+</td><td>farhanskar@gmail.com</td><td>9021011203</td><td></td></tr>
                        <tr class="student-row"><td>166</td><td>Shaikh Maseera Mazhar</td><td></td><td>2024015400342384</td><td>Chalisgaon</td><td>A+</td><td>masirashaikhmasina@gmail.com</td><td>7378603033</td><td></td></tr>
                        <tr class="student-row"><td>167</td><td>Shaikh Mohammad Affan</td><td></td><td>2024015400342233</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>168</td><td>Shaikh Muskan Shakir</td><td></td><td>2024015400348953</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>169</td><td>Shinde Sarthak Sunil</td><td></td><td>2024015400341887</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>170</td><td>Sonawane Ajay Vijay</td><td></td><td>2024015400330673</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>171</td><td>Sonawane Bhushan Vithal</td><td></td><td>2024015400330592</td><td>Tarwade</td><td></td><td>bhushsankoli792@gmail.com</td><td>9209236908</td><td></td></tr>
                        <tr class="student-row"><td>172</td><td>Sonawane Om Ravindra</td><td></td><td>2024015400332037</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>173</td><td>Sonawane Yogaraj Kailas</td><td></td><td>2024015400351785</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>174</td><td>Suryawanshi Anita Sahebrao</td><td>OBC</td><td>2024015400347853</td><td>Wagali</td><td>A+</td><td>anitasuryawanshi746@gmail.com</td><td>7249580177</td><td></td></tr>
                        <tr class="student-row"><td>175</td><td>Suryawanshi Divya Kiran</td><td>OBC</td><td>2024015400347717</td><td>Pimparkheda</td><td>B+</td><td>divyasuryawanshi405@gmail.com</td><td>9975628384</td><td></td></tr>
                        <tr class="student-row"><td>176</td><td>Suryawanshi Gaurav Pradip</td><td></td><td>2024015400347814</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>177</td><td>Suryawanshi Himanshu Ravindra</td><td>OBC</td><td>2024015400347733</td><td>Alwadi</td><td>B+</td><td>suryawanshihimanshu4488@gmail.com</td><td>7558421217</td><td></td></tr>
                        <tr class="student-row"><td>178</td><td>Suryawanshi Jagdish Narendra</td><td></td><td>2024015400331943</td><td></td><td></td><td></td><td></td><td>15 March 2007</td></tr>
                        <tr class="student-row"><td>179</td><td>Suryawanshi Nilesh Suresh</td><td>OBC</td><td>2024015400342585</td><td>Ranjangaon</td><td>O+</td><td>nusur424@gmail.com</td><td>8600562335</td><td>18 July 2005</td></tr>
                        <tr class="student-row"><td>180</td><td>Suryawanshi Nisha Anil</td><td>OBC</td><td>2024015400331065</td><td>Pimparkheda</td><td>O+</td><td>nishu06049807@gamil.com</td><td>9890405532</td><td></td></tr>
                        <tr class="student-row"><td>181</td><td>Thakur Gayatri Gorakh</td><td>ST</td><td>2024015400347594</td><td>Nhave</td><td>A+</td><td>gorakhnaththakur8@gmail.com</td><td>9834877122</td><td></td></tr>
                        <tr class="student-row"><td>182</td><td>Thase Harshada Vishwanath</td><td>OBC</td><td>2024015400331614</td><td>Pimparkheda</td><td>A+</td><td>harshadathube@gmail.com</td><td>9604544715</td><td></td></tr>
                        <tr class="student-row"><td>183</td><td>Thube Ashwini Ravindra</td><td></td><td>2024015400347772</td><td></td><td></td><td></td><td></td><td></td></tr>
                        <tr class="student-row"><td>184</td><td>Upalkar Harshal Anil</td><td>OBC</td><td>2024015400342063</td><td>Patonda</td><td>O+</td><td>upalkarharshalcsn@gmail.com</td><td>9665201370</td><td>11 March 2006</td></tr>
                        <tr class="student-row"><td>185</td><td>Yeole Chaitali Govind</td><td>OBC</td><td>2024015400350422</td><td>Ranjangaon</td><td>B+</td><td>chaitaliyeole16@gmail.com</td><td>7447462045</td><td></td></tr>
                        <tr class="student-row"><td>186</td><td>Zagade Yogesh Sanjay</td><td>OBC</td><td>2024015400341895</td><td>Patonda</td><td>A+</td><td>yogeshzagade332@gmail.com</td><td>7841871030</td><td></td></tr>
                        <tr class="student-row"><td>187</td><td>Zodage Vikas Gorakh</td><td>OBC</td><td>2024015400341582</td><td>Rahipuri</td><td></td><td>vikaszodage7226@gmail.com</td><td>9359112459</td><td></td></tr>
                    </tbody>
                </table>
            </div>
        </div>
    </main>

    <script>
        const allStudentsData = [];
        let sortDirection = false;

        // Initialize Data and Scroll Listeners on Load
        document.addEventListener('DOMContentLoaded', () => {
            const tableBody = document.getElementById('studentTableBody');
            const rows = tableBody.querySelectorAll('tr.student-row');
            
            document.getElementById('totalCount').textContent = `Total: ${rows.length}`;

            rows.forEach((row, i) => {
                row.setAttribute('data-id', i);
                const cells = row.getElementsByTagName('td');
                const student = {
                    id: i,
                    srNo: cells[0].textContent || '',
                    name: cells[1].textContent || '-',
                    category: cells[2].textContent || '-',
                    prnNo: cells[3].textContent || '-',
                    address: cells[4].textContent || '-',
                    bloodGroup: cells[5].textContent || '-',
                    emailId: cells[6].textContent ? cells[6].textContent.toLowerCase() : '-',
                    mobileNo: cells[7].textContent || '-',
                    dob: cells[8].textContent || '-',
                };
                allStudentsData.push(student);
                
                // Clicking a row opens the inline profile
                row.addEventListener('click', () => toggleInlineProfile(row, student));
            });

            // --- Scroll Event Listeners for Premium UX ---

            // 1. Hide Mobile Keyboard when scrolling inside Search Results
            document.getElementById('searchResults').addEventListener('scroll', () => {
                document.getElementById('studentNameInput').blur();
            });

            // 2. Hide Full-Screen Search if user scrolls the main background (rare, but good fallback)
            window.addEventListener('scroll', () => {
                if (document.getElementById('searchOverlay').classList.contains('active')) {
                    closeSearch();
                }
            });

            // 3. Automatically close Top Search Profile when scrolling down the table
            document.getElementById('tableScrollContainer').addEventListener('scroll', () => {
                if (document.getElementById('searchOverlay').classList.contains('active')) {
                    closeSearch();
                }
                closeTopProfile(); // Hides search result details when checking table
            });
        });

        // --- Full Screen Search Modal Logic ---

        function openSearch() {
            const overlay = document.getElementById('searchOverlay');
            overlay.classList.add('active');
            
            // Auto focus input when opened
            setTimeout(() => {
                document.getElementById('studentNameInput').focus();
            }, 100);
        }

        function closeSearch() {
            document.getElementById('searchOverlay').classList.remove('active');
        }

        // Close overlay if clicking the blurred background outside the modal
        function handleOverlayClick(event) {
            if (event.target.id === 'searchOverlay') {
                closeSearch();
            }
        }

        function handleSearchInput(event) {
            const inputField = document.getElementById('studentNameInput');
            const input = inputField.value.toLowerCase().trim();
            
            if (event.key === 'Escape') {
                closeSearch();
                return;
            }

            if (input === "") {
                document.getElementById('searchResults').classList.remove('visible'); 
                document.getElementById('searchResults').innerHTML = ''; 
            } else {
                searchStudent(input);
            }
        }

        function searchStudent(input) {
            const searchResultsDiv = document.getElementById('searchResults');
            
            const matchingStudents = allStudentsData.filter(s => 
                s.name.toLowerCase().includes(input) ||
                s.prnNo.toLowerCase().includes(input) ||
                s.emailId.toLowerCase().includes(input) || 
                s.mobileNo.includes(input)
            );

            if (matchingStudents.length > 0) {
                let resultsHtml = '<ul>';
                matchingStudents.forEach((student) => {
                    resultsHtml += `
                        <li onclick="openTopProfile(${student.id})">
                            <strong>${student.name}</strong>
                            <span class="search-prn-badge">${student.prnNo}</span>
                        </li>`;
                });
                resultsHtml += '</ul>';
                searchResultsDiv.innerHTML = resultsHtml;
                searchResultsDiv.classList.add('visible'); 
            } else {
                searchResultsDiv.innerHTML = '<div class="no-results">No matching records found.</div>';
                searchResultsDiv.classList.add('visible'); 
            }
        }

        // --- Profile Display Logic ---

        function closeAllInlineProfiles() {
            document.querySelectorAll('tr.student-row').forEach(tr => tr.classList.remove('active-row'));
            document.querySelectorAll('.inline-detail-row').forEach(el => el.remove());
        }

        function closeTopProfile() {
            const profile = document.getElementById('studentProfile');
            if (profile.classList.contains('visible')) {
                profile.classList.remove('visible');
                setTimeout(() => {
                    if (!profile.classList.contains('visible')) {
                        profile.innerHTML = ''; // Safely clear after transition
                    }
                }, 400); 
            }
        }

        // Triggered by selecting a result from the Search Modal
        function openTopProfile(studentId) {
            closeSearch(); // Hide full-screen search
            closeAllInlineProfiles(); // Close any open rows in the table
            
            const student = allStudentsData.find(s => s.id === studentId);
            const topProfileDiv = document.getElementById('studentProfile');
            
            if (student) {
                topProfileDiv.innerHTML = `
                    <div class="profile-header">
                        <h4>Profile: ${student.name}</h4>
                        <button class="close-profile-btn" onclick="closeTopProfile()">
                            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="width: 20px; height: 20px;">
                                <line x1="18" y1="6" x2="6" y2="18"></line>
                                <line x1="6" y1="6" x2="18" y2="18"></line>
                            </svg>
                        </button>
                    </div>
                    <div class="profile-grid">
                        <div class="profile-field"><strong>SR.No.</strong> <span>${student.srNo}</span></div>
                        <div class="profile-field"><strong>PRN No.</strong> <span>${student.prnNo}</span></div>
                        <div class="profile-field"><strong>Category</strong> <span>${student.category}</span></div>
                        <div class="profile-field"><strong>Blood Group</strong> <span>${student.bloodGroup}</span></div>
                        <div class="profile-field"><strong>Date of Birth</strong> <span>${student.dob}</span></div>
                        <div class="profile-field"><strong>Mobile No.</strong> <span>${student.mobileNo}</span></div>
                        <div class="profile-field" style="grid-column: 1 / -1;"><strong>Email ID</strong> <span>${student.emailId}</span></div>
                        <div class="profile-field" style="grid-column: 1 / -1;"><strong>Full Address</strong> <span>${student.address}</span></div>
                    </div>
                `;
                
                topProfileDiv.classList.add('visible');
                window.scrollTo({ top: 0, behavior: 'smooth' });
            }
        }

        // Triggered by clicking a row in the Table directly
        function toggleInlineProfile(rowElement, student) {
            const isAlreadyOpen = rowElement.classList.contains('active-row');
            
            closeAllInlineProfiles();
            closeTopProfile(); // Close search profile to prevent double-display

            if (!isAlreadyOpen) {
                rowElement.classList.add('active-row');
                
                const detailRow = document.createElement('tr');
                detailRow.className = 'inline-detail-row';
                
                detailRow.innerHTML = `
                    <td colspan="9">
                        <div class="inline-profile-card">
                            <div class="profile-header">
                                <h4>${student.name}</h4>
                                <button class="close-profile-btn" onclick="closeAllInlineProfiles()">
                                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="width: 20px; height: 20px;">
                                        <line x1="18" y1="6" x2="6" y2="18"></line>
                                        <line x1="6" y1="6" x2="18" y2="18"></line>
                                    </svg>
                                </button>
                            </div>
                            <div class="profile-grid">
                                <div class="profile-field"><strong>PRN No.</strong> <span>${student.prnNo}</span></div>
                                <div class="profile-field"><strong>Category</strong> <span>${student.category}</span></div>
                                <div class="profile-field"><strong>Blood Group</strong> <span>${student.bloodGroup}</span></div>
                                <div class="profile-field"><strong>Date of Birth</strong> <span>${student.dob}</span></div>
                                <div class="profile-field"><strong>Mobile No.</strong> <span>${student.mobileNo}</span></div>
                                <div class="profile-field"><strong>Email ID</strong> <span>${student.emailId}</span></div>
                                <div class="profile-field" style="grid-column: 1 / -1;"><strong>Full Address</strong> <span>${student.address}</span></div>
                            </div>
                        </div>
                    </td>
                `;
                
                rowElement.parentNode.insertBefore(detailRow, rowElement.nextSibling);
                
                // Small scroll adjustment so the inline profile is fully visible
                const container = document.getElementById('tableScrollContainer');
                const rowRect = detailRow.getBoundingClientRect();
                const containerRect = container.getBoundingClientRect();
                
                if(rowRect.bottom > containerRect.bottom) {
                    container.scrollBy({ top: rowRect.bottom - containerRect.bottom + 20, behavior: 'smooth' });
                }
            }
        }

        // --- Table Sorting ---
        function sortTable(columnIndex) {
            closeAllInlineProfiles(); 

            const table = document.querySelector("#mainTable tbody");
            const rows = Array.from(table.querySelectorAll('tr.student-row'));
            
            sortDirection = !sortDirection;

            rows.sort((a, b) => {
                let valA = a.cells[columnIndex].innerText.toLowerCase();
                let valB = b.cells[columnIndex].innerText.toLowerCase();

                if (!isNaN(valA) && !isNaN(valB) && valA !== "" && valB !== "") {
                    valA = parseFloat(valA);
                    valB = parseFloat(valB);
                }

                if (valA < valB) return sortDirection ? -1 : 1;
                if (valA > valB) return sortDirection ? 1 : -1;
                return 0;
            });

            table.innerHTML = "";
            rows.forEach(row => table.appendChild(row));
        }
    </script>
</body>
</html>
