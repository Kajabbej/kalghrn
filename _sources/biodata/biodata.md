# Biodata Saya & Dosen Pengampu

```{raw} html
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;800&display=swap" rel="stylesheet">

<div class="bio-wrapper">
    <!-- KARTU 1: MAHASISWA -->
    <div class="bio-card" id="cardMhs">
        <div class="bio-card-glow mhs-glow"></div>
        
        <div class="bio-card-header">
            <div class="avatar-container">
                <div class="avatar-ring mhs-ring"></div>
                <img class="avatar-img" src="../_static/myprofile.jpg" alt="Moh. Ghufron">
            </div>
            <h2 class="bio-name mhs-name">Moh. Ghufron</h2>
            <p class="bio-tagline">Student & Tech Enthusiast</p>
        </div>
        
        <div class="bio-tabs">
            <button class="tab-btn active" onclick="switchTab(event, 'tab-profil-mhs', 'cardMhs')">Profil</button>
            <button class="tab-btn" onclick="switchTab(event, 'tab-about-mhs', 'cardMhs')">Tentang Saya</button>
            <button class="tab-btn" onclick="switchTab(event, 'tab-contact-mhs', 'cardMhs')">Kontak</button>
        </div>
        
        <div class="bio-card-body">
            <!-- TAB 1: PROFIL -->
            <div id="tab-profil-mhs" class="tab-content active">
                <div class="info-grid">
                    <div class="info-item mhs-border">
                        <span class="info-label">NIM</span>
                        <span class="info-val">250411100196</span>
                    </div>
                    <div class="info-item mhs-border">
                        <span class="info-label">Program Studi</span>
                        <span class="info-val">Teknik Informatika</span>
                    </div>
                    <div class="info-item mhs-border">
                        <span class="info-label">Fakultas</span>
                        <span class="info-val">Teknik</span>
                    </div>
                    <div class="info-item mhs-border">
                        <span class="info-label">Universitas</span>
                        <span class="info-val">Universitas Trunojoyo Madura</span>
                    </div>
                </div>
            </div>
            
            <!-- TAB 2: ABOUT -->
            <div id="tab-about-mhs" class="tab-content">
                <p class="about-text">
                    Halo! Saya adalah mahasiswa yang tertarik dalam bidang <strong>Komputasi, Aljabar Linear, dan Pemrograman Web</strong>. Website ini dibuat sebagai sarana untuk mendokumentasikan proses pembelajaran, tugas, dan implementasi visual dari matematika komputasi.
                </p>
                <div class="skills-tag">
                    <span class="tag mhs-tag">Python</span>
                    <span class="tag mhs-tag">NumPy</span>
                    <span class="tag mhs-tag">Linear Algebra</span>
                    <span class="tag mhs-tag">HTML/CSS</span>
                    <span class="tag mhs-tag">JavaScript</span>
                </div>
            </div>
            
            <!-- TAB 3: CONTACT -->
            <div id="tab-contact-mhs" class="tab-content">
                <div class="social-links">
                    <a href="mailto:ghufron@example.com" class="social-btn email">
                        <svg class="social-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
                        <span>Email</span>
                    </a>
                    <a href="https://github.com/Kajabbej" target="_blank" class="social-btn github">
                        <svg class="social-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>
                        <span>GitHub</span>
                    </a>
                    <a href="#" target="_blank" class="social-btn linkedin">
                        <svg class="social-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg>
                        <span>LinkedIn</span>
                    </a>
                </div>
            </div>
        </div>
    </div>

    <!-- KARTU 2: DOSEN -->
    <div class="bio-card lecturer-card" id="cardDsn">
        <div class="bio-card-glow dsn-glow"></div>
        
        <div class="bio-card-header">
            <div class="avatar-container">
                <div class="avatar-ring dsn-ring"></div>
                <img class="avatar-img" src="../_static/dosen.jpg" alt="Mula'ab, S.Si., M.Kom.">
            </div>
            <h2 class="bio-name dsn-name">Mula'ab, S.Si., M.Kom.</h2>
            <p class="bio-tagline">Dosen Aljabar Linear</p>
        </div>
        
        <div class="bio-tabs">
            <button class="tab-btn active" onclick="switchTab(event, 'tab-profil-dsn', 'cardDsn')">Profil</button>
            <button class="tab-btn" onclick="switchTab(event, 'tab-about-dsn', 'cardDsn')">Tentang Dosen</button>
            <button class="tab-btn" onclick="switchTab(event, 'tab-contact-dsn', 'cardDsn')">Kontak</button>
        </div>
        
        <div class="bio-card-body">
            <!-- TAB 1: PROFIL -->
            <div id="tab-profil-dsn" class="tab-content active">
                <div class="info-grid">
                    <div class="info-item dsn-border">
                        <span class="info-label">NIP / NIDN</span>
                        <span class="info-val">197305202002121001</span>
                    </div>
                    <div class="info-item dsn-border">
                        <span class="info-label">Program Studi</span>
                        <span class="info-val">Teknik Informatika</span>
                    </div>
                    <div class="info-item dsn-border">
                        <span class="info-label">Fakultas</span>
                        <span class="info-val">Teknik</span>
                    </div>
                    <div class="info-item dsn-border">
                        <span class="info-label">Universitas</span>
                        <span class="info-val">Universitas Trunojoyo Madura</span>
                    </div>
                </div>
            </div>
            
            <!-- TAB 2: ABOUT -->
            <div id="tab-about-dsn" class="tab-content">
                <p class="about-text">
                    Dosen pengampu mata kuliah **Komputasi Aljabar Linear** yang membimbing mahasiswa dalam memahami konsep ruang vektor, eliminasi Gaussian, dekomposisi matriks, dan implementasi algoritmanya menggunakan teknologi komputasi.
                </p>
                <div class="skills-tag">
                    <span class="tag dsn-tag">Linear Algebra</span>
                    <span class="tag dsn-tag">Matrix Theory</span>
                    <span class="tag dsn-tag">Numerical Methods</span>
                    <span class="tag dsn-tag">Academic Research</span>
                </div>
            </div>
            
            <!-- TAB 3: CONTACT -->
            <div id="tab-contact-dsn" class="tab-content">
                <div class="social-links">
                    <a href="mailto:dosen@domain.com" class="social-btn email-dsn">
                        <svg class="social-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
                        <span>Email Akademik</span>
                    </a>
                    <a href="https://scholar.google.com" target="_blank" class="social-btn scholar-dsn">
                        <svg class="social-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path></svg>
                        <span>Google Scholar</span>
                    </a>
                </div>
            </div>
        </div>
    </div>
</div>

<style>
/* WRAPPER & LAYOUT */
.bio-wrapper {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 30px;
    width: 100%;
    max-width: 960px;
    margin: 0 auto;
    padding: 30px 10px;
    font-family: 'Outfit', sans-serif;
    perspective: 1000px;
}

/* BASE CARD STYLING */
.bio-card {
    background: linear-gradient(135deg, rgba(24, 30, 46, 0.93) 0%, rgba(15, 20, 32, 0.97) 100%);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border-radius: 28px;
    padding: 40px 30px;
    color: #f8fafc;
    position: relative;
    overflow: hidden;
    transition: transform 0.1s ease, box-shadow 0.3s ease, border-color 0.3s ease;
    transform-style: preserve-3d;
}

/* STUDENT CARD (Cyan accent) */
.bio-card {
    border: 1px solid rgba(0, 242, 254, 0.25);
    box-shadow: 0 25px 50px -12px rgba(0, 242, 254, 0.15), 0 0 40px rgba(0, 242, 254, 0.05);
}
.bio-card:hover {
    border-color: rgba(0, 242, 254, 0.5);
    box-shadow: 0 30px 60px -12px rgba(0, 242, 254, 0.25), 0 0 50px rgba(0, 242, 254, 0.1);
}

/* LECTURER CARD (Purple accent) */
.bio-card.lecturer-card {
    border: 1px solid rgba(155, 81, 224, 0.25);
    box-shadow: 0 25px 50px -12px rgba(155, 81, 224, 0.15), 0 0 40px rgba(155, 81, 224, 0.05);
}
.bio-card.lecturer-card:hover {
    border-color: rgba(155, 81, 224, 0.5);
    box-shadow: 0 30px 60px -12px rgba(155, 81, 224, 0.25), 0 0 50px rgba(155, 81, 224, 0.1);
}

/* GLOW EFFECTS */
.bio-card-glow {
    position: absolute;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    pointer-events: none;
    z-index: 0;
    transition: transform 0.15s ease-out;
}
.mhs-glow {
    background: radial-gradient(circle, rgba(0, 242, 254, 0.15) 0%, transparent 60%);
}
.dsn-glow {
    background: radial-gradient(circle, rgba(155, 81, 224, 0.15) 0%, transparent 60%);
}

.bio-card-header {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    position: relative;
    z-index: 1;
    transform: translateZ(30px);
}

/* AVATAR SYSTEM */
.avatar-container {
    width: 110px;
    height: 110px;
    position: relative;
    margin-bottom: 20px;
}

.avatar-ring {
    position: absolute;
    top: -6px;
    left: -6px;
    right: -6px;
    bottom: -6px;
    border-radius: 50%;
    animation: rotateRing 25s linear infinite;
    opacity: 0.7;
}
.mhs-ring {
    border: 2px dashed #00f2fe;
}
.dsn-ring {
    border: 2px dashed #9b51e0;
}

/* Specificity override for circular crop */
.bio-card .avatar-container img.avatar-img,
.bio-card .avatar-container svg.avatar-img {
    width: 100%;
    height: 100%;
    border-radius: 50% !important;
    object-fit: cover;
    padding: 6px;
}

.bio-card .avatar-container img.avatar-img {
    background: linear-gradient(135deg, rgba(0, 242, 254, 0.15), rgba(155, 81, 224, 0.15));
}
.bio-card .avatar-container svg.avatar-img {
    background: linear-gradient(135deg, rgba(155, 81, 224, 0.15), rgba(244, 63, 94, 0.15));
}

/* NAMES */
.bio-name {
    font-size: 28px;
    font-weight: 800;
    margin: 0;
    background-clip: text !important;
    -webkit-background-clip: text !important;
    -webkit-text-fill-color: transparent !important;
    color: transparent !important;
    letter-spacing: -0.5px;
}
.mhs-name {
    background: linear-gradient(135deg, #00f2fe 0%, #4facfe 50%, #9b51e0 100%);
}
.dsn-name {
    background: linear-gradient(135deg, #9b51e0 0%, #f43f5e 100%);
}

.bio-tagline {
    font-size: 14px;
    margin: 6px 0 0 0;
    color: #94a3b8;
    font-weight: 400;
}

/* TABS SYSTEM */
.bio-tabs {
    display: flex;
    justify-content: space-around;
    background: rgba(255, 255, 255, 0.05);
    border: 1px solid rgba(255, 255, 255, 0.05);
    border-radius: 14px;
    padding: 4px;
    margin: 30px 0 25px 0;
    position: relative;
    z-index: 1;
    transform: translateZ(20px);
}

.tab-btn {
    flex: 1;
    background: none;
    border: none;
    padding: 10px 12px;
    border-radius: 10px;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    color: #94a3b8;
    font-family: inherit;
}
.tab-btn:hover {
    color: #f8fafc;
}

/* Active buttons themed differently */
#cardMhs .tab-btn.active {
    background: linear-gradient(135deg, #00f2fe 0%, #4facfe 100%);
    color: #0f172a;
    font-weight: 700;
    box-shadow: 0 4px 15px rgba(0, 242, 254, 0.4);
}
#cardDsn .tab-btn.active {
    background: linear-gradient(135deg, #9b51e0 0%, #f43f5e 100%);
    color: #ffffff;
    font-weight: 700;
    box-shadow: 0 4px 15px rgba(155, 81, 224, 0.4);
}

.bio-card-body {
    position: relative;
    z-index: 1;
    transform: translateZ(15px);
    min-height: 180px;
}

.tab-content {
    display: none;
    animation: fadeIn 0.4s ease forwards;
}

.tab-content.active {
    display: block;
}

/* INFO GRID */
.info-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 12px;
}

.info-item {
    display: flex;
    flex-direction: column;
    background: rgba(255, 255, 255, 0.03);
    padding: 10px 15px;
    border-radius: 10px;
    border-top: 1px solid rgba(255, 255, 255, 0.02);
    border-right: 1px solid rgba(255, 255, 255, 0.02);
    border-bottom: 1px solid rgba(255, 255, 255, 0.02);
}
.mhs-border { border-left: 3px solid #00f2fe; }
.dsn-border { border-left: 3px solid #9b51e0; }

.info-label {
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    color: #64748b;
    margin-bottom: 2px;
}

.info-val {
    font-size: 14px;
    font-weight: 600;
    color: #e2e8f0;
}

/* ABOUT TEXT */
.about-text {
    font-size: 14px;
    line-height: 1.6;
    margin: 0 0 18px 0;
    color: #cbd5e1;
}

/* TAGS */
.skills-tag {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
}
.tag {
    font-size: 11px;
    padding: 5px 12px;
    border-radius: 20px;
    font-weight: 600;
}
.mhs-tag {
    background: rgba(0, 242, 254, 0.12);
    color: #00e5ff;
    border: 1px solid rgba(0, 242, 254, 0.15);
}
.dsn-tag {
    background: rgba(155, 81, 224, 0.12);
    color: #d8b4fe;
    border: 1px solid rgba(155, 81, 224, 0.15);
}

/* SOCIALS */
.social-links {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.social-btn {
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 14px;
    border-radius: 12px;
    text-decoration: none;
    font-size: 14px;
    font-weight: 600;
    color: #fff;
    transition: all 0.3s ease;
}
.social-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
}

.social-btn.email { 
    background: linear-gradient(135deg, #f857a6 0%, #ff5858 100%); 
    box-shadow: 0 4px 15px rgba(255, 88, 88, 0.2);
}
.social-btn.github { 
    background: linear-gradient(135deg, #1f2937 0%, #111827 100%); 
    box-shadow: 0 4px 15px rgba(17, 24, 39, 0.2);
    border: 1px solid rgba(255, 255, 255, 0.05);
}
.social-btn.linkedin { 
    background: linear-gradient(135deg, #0077b5 0%, #00a0dc 100%); 
    box-shadow: 0 4px 15px rgba(0, 119, 181, 0.2);
}

/* Lecturer specific links */
.social-btn.email-dsn {
    background: linear-gradient(135deg, #9b51e0 0%, #7c3aed 100%);
    box-shadow: 0 4px 15px rgba(124, 58, 237, 0.2);
}
.social-btn.scholar-dsn {
    background: linear-gradient(135deg, #f43f5e 0%, #e11d48 100%);
    box-shadow: 0 4px 15px rgba(225, 29, 72, 0.2);
}

.social-icon {
    width: 20px;
    height: 20px;
}

/* ANIMATIONS */
@keyframes rotateRing {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(12px); }
    to { opacity: 1; transform: translateY(0); }
}
</style>

<script>
function switchTab(evt, tabId, cardId) {
    const card = document.getElementById(cardId);
    if (!card) return;
    
    // Find all tab contents within this specific card and deactivate them
    const tabcontents = card.getElementsByClassName("tab-content");
    for (let i = 0; i < tabcontents.length; i++) {
        tabcontents[i].classList.remove("active");
    }
    
    // Find all tab buttons within this specific card and deactivate them
    const tablinks = card.getElementsByClassName("tab-btn");
    for (let i = 0; i < tablinks.length; i++) {
        tablinks[i].classList.remove("active");
    }
    
    // Show the targeted tab content and activate the current button
    const targetContent = card.querySelector('#' + tabId);
    if (targetContent) {
        targetContent.classList.add("active");
    }
    evt.currentTarget.classList.add("active");
}

function handleTilt(cardId, glowClass) {
    const card = document.getElementById(cardId);
    const glow = card ? card.querySelector(glowClass) : null;
    
    if (card) {
        card.addEventListener('mousemove', (e) => {
            const rect = card.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            const xc = rect.width / 2;
            const yc = rect.height / 2;
            
            const rotateY = ((x - xc) / xc) * 10;
            const rotateX = -((y - yc) / yc) * 10;
            
            card.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
            
            if (glow) {
                glow.style.transform = `translate(${x - rect.width}px, ${y - rect.height}px)`;
            }
        });

        card.addEventListener('mouseleave', () => {
            card.style.transform = 'rotateX(0deg) rotateY(0deg)';
        });
    }
}

// Initialise independent 3D tilt for both cards
handleTilt('cardMhs', '.mhs-glow');
handleTilt('cardDsn', '.dsn-glow');
</script>
```
