<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> PT ASU Group  - Company Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #000;
            color: #fff;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: #000;
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid #333;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 28px;
            font-weight: 700;
        }
        
        .logo span {
            background-color: #fff;
            color: #000;
            padding: 0 5px;
        }
        
        .nav-menu {
            display: flex;
            gap: 20px;
        }
        
        .nav-button {
            background: none;
            border: 1px solid #fff;
            color: #fff;
            padding: 8px 15px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .nav-button:hover {
            background-color: #fff;
            color: #000;
        }
        
        /* Hero Section */
        .hero {
            padding: 100px 0;
            text-align: center;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%23111"/><path d="M0 0L100 100" stroke="%23333" stroke-width="1"/><path d="M100 0L0 100" stroke="%23333" stroke-width="1"/></svg>');
            background-size: cover;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 5px;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 30px;
            color: #ccc;
        }
        
        .hero-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 12px 25px;
            border: none;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .btn-primary {
            background-color: #fff;
            color: #000;
        }
        
        .btn-primary:hover {
            background-color: #ddd;
            transform: translateY(-3px);
        }
        
        .btn-secondary {
            background-color: transparent;
            color: #fff;
            border: 2px solid #fff;
        }
        
        .btn-secondary:hover {
            background-color: #fff;
            color: #000;
            transform: translateY(-3px);
        }
        
        /* Divisions Section */
        .divisions {
            padding: 80px 0;
            background-color: #111;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.5rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            position: relative;
        }
        
        .section-title:after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 2px;
            background-color: #fff;
        }
        
        .division-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .division-card {
            background-color: #000;
            border: 1px solid #333;
            padding: 30px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }
        
        .division-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(255, 255, 255, 0.1);
        }
        
        .division-card:after {
            content: "Klik disini";
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.9);
            color: #000;
            padding: 5px;
            font-size: 0.8rem;
            transform: translateY(100%);
            transition: transform 0.3s ease;
        }
        
        .division-card:hover:after {
            transform: translateY(0);
        }
        
        .division-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #fff;
        }
        
        .division-name {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: #fff;
        }
        
        .division-fullname {
            font-size: 0.9rem;
            color: #aaa;
            margin-bottom: 15px;
        }
        
        .division-buttons {
            display: flex;
            gap: 10px;
            margin-top: 15px;
            flex-wrap: wrap;
            justify-content: center;
        }
        
        .division-btn {
            padding: 6px 12px;
            font-size: 0.8rem;
            background-color: #333;
            color: #fff;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        
        .division-btn:hover {
            background-color: #555;
        }
        
        .website-btn {
            background-color: #25D366;
        }
        
        .website-btn:hover {
            background-color: #128C7E;
        }
        
        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            overflow: auto;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .modal-content {
            background-color: #000;
            margin: 5% auto;
            padding: 30px;
            border: 1px solid #333;
            width: 80%;
            max-width: 800px;
            position: relative;
            transform: translateY(-50px);
            transition: transform 0.3s ease;
        }
        
        .modal-open {
            display: block;
            opacity: 1;
        }
        
        .modal-open .modal-content {
            transform: translateY(0);
        }
        
        .close-button {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.5rem;
            cursor: pointer;
            color: #fff;
            background: none;
            border: none;
            z-index: 1001;
        }
        
        .modal-header {
            margin-bottom: 20px;
            text-align: center;
        }
        
        .modal-icon {
            font-size: 3rem;
            margin-bottom: 15px;
        }
        
        .modal-body {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }
        
        .modal-info {
            margin-bottom: 15px;
        }
        
        .modal-info h4 {
            color: #aaa;
            margin-bottom: 5px;
            font-size: 0.9rem;
        }
        
        .modal-info p {
            font-size: 1.1rem;
        }
        
        .modal-buttons {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin-top: 20px;
            grid-column: 1 / -1;
            flex-wrap: wrap;
        }
        
        /* All Companies Modal */
        .all-companies-modal .modal-content {
            max-width: 1000px;
        }
        
        .companies-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .company-item {
            background-color: #111;
            border: 1px solid #333;
            padding: 20px;
            text-align: center;
            transition: transform 0.3s ease;
            cursor: pointer;
        }
        
        .company-item:hover {
            transform: translateY(-3px);
        }
        
        .company-icon {
            font-size: 2rem;
            margin-bottom: 10px;
        }
        
        /* Contact Section */
        .contact {
            padding: 80px 0;
            background-color: #000;
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .contact-card {
            background-color: #111;
            border: 1px solid #333;
            padding: 30px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .contact-card:hover {
            transform: translateY(-5px);
        }
        
        .contact-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #fff;
        }
        
        .contact-buttons {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        /* Services Section */
        .services {
            padding: 80px 0;
            background-color: #111;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .service-card {
            background-color: #000;
            border: 1px solid #333;
            padding: 30px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
        }
        
        .service-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #fff;
        }
        
        .service-buttons {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin-top: 20px;
        }
        
        /* CTA Section */
        .cta {
            padding: 80px 0;
            text-align: center;
            background-color: #000;
        }
        
        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        /* Footer */
        footer {
            background-color: #000;
            padding: 40px 0;
            text-align: center;
            border-top: 1px solid #333;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .footer-logo {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 20px;
        }
        
        .footer-buttons {
            display: flex;
            gap: 15px;
            margin: 20px 0;
            flex-wrap: wrap;
            justify-content: center;
        }
        
        .footer-btn {
            padding: 8px 15px;
            background-color: #333;
            color: #fff;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        
        .footer-btn:hover {
            background-color: #555;
        }
        
        .copyright {
            color: #777;
            margin-top: 20px;
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 15px;
            }
            
            .nav-menu {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .division-grid {
                grid-template-columns: 1fr;
            }
            
            .modal-body {
                grid-template-columns: 1fr;
            }
            
            .modal-content {
                width: 95%;
                padding: 20px;
            }
            
            .contact-grid, .services-grid {
                grid-template-columns: 1fr;
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .companies-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
            
            .division-buttons, .modal-buttons, .contact-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .division-btn, .footer-btn {
                width: 100%;
                max-width: 200px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo"><span>ASU</span> GROUP</div>
                <div class="nav-menu">
                    <button class="nav-button" onclick="scrollToSection('divisions')">Anak Perusahaan</button>
                    <button class="nav-button" onclick="scrollToSection('services')">Layanan</button>
                    <button class="nav-button" onclick="scrollToSection('contact')">Kontak</button>
                    <button class="nav-button" onclick="showAboutModal()">Tentang Kami</button>
                </div>
            </div>
        </div>
    </header>
    
    <section class="hero">
        <div class="container">
            <h1>Asosiasi Sumber Uang</h1>
            <p>Sebuah holding company yang terdiri dari berbagai anak perusahaan di berbagai sektor industri, dengan fokus pada pertumbuhan dan inovasi berkelanjutan.</p>
            <div class="hero-buttons">
                <button class="btn btn-primary" onclick="scrollToSection('divisions')">Jelajahi Perusahaan</button>
                <button class="btn btn-secondary" onclick="scrollToSection('contact')">Hubungi Kami</button>
                <button class="btn btn-secondary" onclick="showInvestorModal()">Info Investor</button>
                <button class="btn btn-secondary" onclick="showCareerModal()">Karir</button>
                <button class="btn btn-secondary" onclick="showAllCompaniesModal()">Lihat Semua Perusahaan</button>
            </div>
        </div>
    </section>
    
    <section class="divisions" id="divisions">
        <div class="container">
            <h2 class="section-title">Anak Perusahaan</h2>
            
            <div class="division-grid">
                <div class="division-card" data-division="asumsi">
                    <div class="division-icon">🌮</div>
                    <h3 class="division-name">ASUMSI</h3>
                    <p class="division-fullname">Asosiasi Sumber Uang Makan Siang</p>
                    <p>Bidang: Food & Beverage</p>
                    <div class="division-buttons">
                        <button class="division-btn" onclick="showModal('asumsi')">Detail</button>
                        <button class="division-btn" onclick="showLocation('asumsi')">Lokasi</button>
                        <button class="division-btn website-btn" onclick="visitWebsite('asumsi')">Kunjungi Website</button>
                    </div>
                </div>
                
                <div class="division-card" data-division="asupan">
                    <div class="division-icon">🎤</div>
                    <h3 class="division-name">ASUPAN</h3>
                    <p class="division-fullname">Asosiasi Sumber Uang Panggung Hiburan Nasional</p>
                    <p>Bidang: Entertainment</p>
                    <div class="division-buttons">
                        <button class="division-btn" onclick="showModal('asupan')">Detail</button>
                        <button class="division-btn" onclick="showLocation('asupan')">Lokasi</button>
                        <button class="division-btn website-btn" onclick="visitWebsite('asupan')">Kunjungi Website</button>
                    </div>
                </div>
                
                <div class="division-card" data-division="asuplex">
                    <div class="division-icon">🏀</div>
                    <h3 class="division-name">ASUPLEX</h3>
                    <p class="division-fullname">Asosiasi Sumber Uang Pergerakan Lincah & EXtreme</p>
                    <p>Bidang: Olahraga</p>
                    <div class="division-buttons">
                        <button class="division-btn" onclick="showModal('asuplex')">Detail</button>
                        <button class="division-btn" onclick="showLocation('asuplex')">Lokasi</button>
                        <button class="division-btn website-btn" onclick="visitWebsite('asuplex')">Kunjungi Website</button>
                    </div>
                </div>
                
                <div class="division-card" data-division="asuwan">
                    <div class="division-icon">🎮</div>
                    <h3 class="division-name">ASUWAN</h3>
                    <p class="division-fullname">Asosiasi Sumber Uang Warung Anak Ngegame</p>
                    <p>Bidang: Esport</p>
                    <div class="division-buttons">
                        <button class="division-btn" onclick="showModal('asuwan')">Detail</button>
                        <button class="division-btn" onclick="showLocation('asuwan')">Lokasi</button>
                        <button class="division-btn website-btn" onclick="visitWebsite('asuwan')">Kunjungi Website</button>
                    </div>
                </div>
                
                <div class="division-card" data-division="asukses">
                    <div class="division-icon">💼</div>
                    <h3 class="division-name">ASUKSES</h3>
                    <p class="division-fullname">Asosiasi Sumber Uang Konsultan Sukses</p>
                    <p>Bidang: Bisnis Konsultan</p>
                    <div class="division-buttons">
                        <button class="division-btn" onclick="showModal('asukses')">Detail</button>
                        <button class="division-btn" onclick="showLocation('asukses')">Lokasi</button>
                        <button class="division-btn website-btn" onclick="visitWebsite('asukses')">Kunjungi Website</button>
                    </div>
                </div>
                
                <div class="division-card" data-division="asunet">
                    <div class="division-icon">🌐</div>
                    <h3 class="division-name">ASUNET</h3>
                    <p class="division-fullname">Asosiasi Sumber Uang Network</p>
                    <p>Bidang: Layanan Web Server</p>
                    <div class="division-buttons">
                        <button class="division-btn" onclick="showModal('asunet')">Detail</button>
                        <button class="division-btn" onclick="showLocation('asunet')">Lokasi</button>
                        <button class="division-btn website-btn" onclick="visitWebsite('asunet')">Kunjungi Website</button>
                    </div>
                </div>
                
                <div class="division-card" data-division="asupet">
                    <div class="division-icon">🐟🐔</div>
                    <h3 class="division-name">ASUPET</h3>
                    <p class="division-fullname">Asosiasi Sumber Uang Peternakan</p>
                    <p>Bidang: Peternakan dan Perikanan</p>
                    <div class="division-buttons">
                        <button class="division-btn" onclick="showModal('asupet')">Detail</button>
                        <button class="division-btn" onclick="showLocation('asupet')">Lokasi</button>
                        <button class="division-btn website-btn" onclick="visitWebsite('asupet')">Kunjungi Website</button>
                    </div>
                </div>
                
                <div class="division-card" data-division="asustyle">
                    <div class="division-icon">👕</div>
                    <h3 class="division-name">ASUSTYLE</h3>
                    <p class="division-fullname">Asosiasi Sumber Uang Style</p>
                    <p>Bidang: Fashion</p>
                    <div class="division-buttons">
                        <button class="division-btn" onclick="showModal('asustyle')">Detail</button>
                        <button class="division-btn" onclick="showLocation('asustyle')">Lokasi</button>
                        <button class="division-btn website-btn" onclick="visitWebsite('asustyle')">Kunjungi Website</button>
                    </div>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 40px;">
                <button class="btn btn-secondary" onclick="showAllCompaniesModal()">Lihat Semua Perusahaan ASU Group</button>
            </div>
        </div>
    </section>
    
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Layanan Kami</h2>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-handshake"></i></div>
                    <h3>Kemitraan Bisnis</h3>
                    <p>Kami menawarkan peluang kemitraan yang menguntungkan untuk pengusaha.</p>
                    <div class="service-buttons">
                        <button class="division-btn" onclick="showPartnershipModal()">Info Kemitraan</button>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-chart-line"></i></div>
                    <h3>Konsultasi Bisnis</h3>
                    <p>Konsultan ahli kami siap membantu pengembangan bisnis Anda.</p>
                    <div class="service-buttons">
                        <button class="division-btn" onclick="showConsultationModal()">Jadwalkan Konsultasi</button>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-users"></i></div>
                    <h3>Pelatihan & Workshop</h3>
                    <p>Program pelatihan untuk meningkatkan skill dan kompetensi.</p>
                    <div class="service-buttons">
                        <button class="division-btn" onclick="showTrainingModal()">Lihat Jadwal</button>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-headset"></i></div>
                    <h3>Dukungan 24/7</h3>
                    <p>Layanan dukungan pelanggan yang siap membantu kapan saja.</p>
                    <div class="service-buttons">
                        <button class="division-btn" onclick="showSupportModal()">Hubungi Dukungan</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Kontak Kami</h2>
            
            <div class="contact-grid">
                <div class="contact-card">
                    <div class="contact-icon"><i class="fas fa-map-marker-alt"></i></div>
                    <h3>Lokasi</h3>
                    <p>Palembang, Indonesia</p>
                    <div class="contact-buttons">
                        <button class="division-btn" onclick="showMap()">Lihat Peta</button>
                        <button class="division-btn" onclick="showDirections()">Petunjuk Arah</button>
                    </div>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon"><i class="fas fa-phone"></i></div>
                    <h3>Telepon</h3>
                    <p>082175707023</p>
                    <div class="contact-buttons">
                        <button class="division-btn" onclick="callNumber()">Telepon Sekarang</button>
                        <button class="division-btn" onclick="saveContact()">Simpan Kontak</button>
                    </div>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon"><i class="fas fa-envelope"></i></div>
                    <h3>Email</h3>
                    <p>PTAsuGroup@gmail.com</p>
                    <div class="contact-buttons">
                        <button class="division-btn" onclick="sendEmail()">Kirim Email</button>
                        <button class="division-btn" onclick="subscribeNewsletter()">Berlangganan</button>
                    </div>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon"><i class="fab fa-whatsapp"></i></div>
                    <h3>WhatsApp</h3>
                    <p>082175707023</p>
                    <div class="contact-buttons">
                        <button class="division-btn" onclick="openWhatsApp()">Chat WhatsApp</button>
                        <button class="division-btn" onclick="requestMeeting()">Minta Pertemuan</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section class="cta">
        <div class="container">
            <h2>Siap Bermitra dengan Kami?</h2>
            <p>Jadilah bagian dari kesuksesan ASU Group. Hubungi kami sekarang untuk informasi lebih lanjut.</p>
            <div class="cta-buttons">
                <button class="btn btn-primary" onclick="showContactForm()">Hubungi Sekarang</button>
                <button class="btn btn-secondary" onclick="downloadBrochure()">Unduh Brosur</button>
                <button class="btn btn-secondary" onclick="requestMeeting()">Minta Pertemuan via WhatsApp</button>
                <button class="btn btn-secondary" onclick="showFAQ()">FAQ</button>
            </div>
        </div>
    </section>
    
    <!-- Modal Structure -->
    <div class="modal" id="divisionModal">
        <div class="modal-content">
            <button class="close-button">&times;</button>
            <div class="modal-header">
                <div class="modal-icon" id="modalIcon"></div>
                <h2 id="modalTitle"></h2>
                <p id="modalSubtitle"></p>
            </div>
            <div class="modal-body">
                <div class="modal-info">
                    <h4>Bidang Usaha</h4>
                    <p id="modalBusiness"></p>
                </div>
                <div class="modal-info">
                    <h4>Tahun Berdiri</h4>
                    <p id="modalYear"></p>
                </div>
                <div class="modal-info">
                    <h4>Jumlah Karyawan</h4>
                    <p id="modalEmployees"></p>
                </div>
                <div class="modal-info">
                    <h4>Lokasi Kantor</h4>
                    <p id="modalLocation"></p>
                </div>
                <div class="modal-info">
                    <h4>Website</h4>
                    <p id="modalWebsite"></p>
                </div>
                <div class="modal-info" style="grid-column: 1 / -1;">
                    <h4>Deskripsi Perusahaan</h4>
                    <p id="modalDescription"></p>
                </div>
            </div>
            <div class="modal-buttons">
                <button class="division-btn" onclick="hideModal()">Tutup</button>
                <button class="division-btn" id="modalContactBtn">Hubungi Perusahaan</button>
                <button class="division-btn website-btn" id="modalWebsiteBtn">Kunjungi Website</button>
            </div>
        </div>
    </div>
    
    <!-- All Companies Modal -->
    <div class="modal all-companies-modal" id="allCompaniesModal">
        <div class="modal-content">
            <button class="close-button">&times;</button>
            <div class="modal-header">
                <h2>Semua Anak Perusahaan ASU Group</h2>
                <p>Total 8 perusahaan dalam berbagai bidang industri</p>
            </div>
            <div class="companies-grid" id="companiesGrid">
                <!-- Companies will be populated by JavaScript -->
            </div>
            <div class="modal-buttons">
                <button class="division-btn" onclick="hideAllCompaniesModal()">Tutup</button>
                <button class="division-btn" onclick="requestMeeting()">Minta Pertemuan via WhatsApp</button>
            </div>
        </div>
    </div>
    
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo"><span>ASU</span> GROUP</div>
                <p>Holding Company Terdepan dengan Beragam Anak Perusahaan Unggulan</p>
                <div class="footer-buttons">
                    <button class="footer-btn" onclick="scrollToTop()">Kembali ke Atas</button>
                    <button class="footer-btn" onclick="showPrivacyPolicy()">Kebijakan Privasi</button>
                    <button class="footer-btn" onclick="showTerms()">Syarat & Ketentuan</button>
                    <button class="footer-btn" onclick="showAllCompaniesModal()">Semua Perusahaan</button>
                </div>
                <p class="copyright">© 2023 ASU Group. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Data untuk setiap anak perusahaan dengan website yang benar-benar bisa dibuka
        const divisionData = {
            asumsi: {
                icon: "🌮",
                title: "ASUMSI",
                subtitle: "Asosiasi Sumber Uang Makan Siang",
                business: "Food & Beverage",
                year: "2015",
                employees: "250",
                location: "Palembang, Jakarta, Bandung",
                description: "ASUMSI merupakan perusahaan yang bergerak di bidang food and beverage dengan berbagai brand restoran ternama. Kami menyajikan makanan berkualitas dengan cita rasa yang konsisten dan pelayanan terbaik.",
                website: "https://asumsi-group.github.io",
                contact: "082175707023"
            },
            asupan: {
                icon: "🎤",
                title: "ASUPAN",
                subtitle: "Asosiasi Sumber Uang Panggung Hiburan Nasional",
                business: "Entertainment",
                year: "2017",
                employees: "180",
                location: "Palembang, Jakarta, Bali",
                description: "ASUPAN menjadi pelopor dalam industri hiburan dengan mengelola berbagai event musik, comedy show, dan pertunjukan seni lainnya. Kami menghadirkan pengalaman hiburan yang tak terlupakan bagi penonton.",
                website: "https://asupan-entertainment.github.io",
                contact: "082175707024"
            },
            asuplex: {
                icon: "🏀",
                title: "ASUPLEX",
                subtitle: "Asosiasi Sumber Uang Pergerakan Lincah & EXtreme",
                business: "Olahraga",
                year: "2018",
                employees: "150",
                location: "Palembang, Jakarta, Yogyakarta",
                description: "ASUPLEX fokus pada pengembangan fasilitas olahraga ekstrem dan kompetisi atletik. Kami memiliki beberapa arena olahraga indoor dan outdoor serta menyelenggarakan kompetisi reguler.",
                website: "https://asuplex-sports.github.io",
                contact: "082175707025"
            },
            asuwan: {
                icon: "🎮",
                title: "ASUWAN",
                subtitle: "Asosiasi Sumber Uang Warung Anak Ngegame",
                business: "Esport",
                year: "2019",
                employees: "120",
                location: "Palembang, Jakarta, Surabaya",
                description: "ASUWAN adalah pusat gaming dan esport terdepan dengan jaringan warnet gaming premium dan tim esport profesional. Kami mendukung perkembangan bakat-bakat esport Indonesia.",
                website: "https://asuwan-esports.github.io",
                contact: "082175707026"
            },
            asukses: {
                icon: "💼",
                title: "ASUKSES",
                subtitle: "Asosiasi Sumber Uang Konsultan Sukses",
                business: "Bisnis Konsultan",
                year: "2016",
                employees: "90",
                location: "Palembang, Jakarta, Singapore",
                description: "ASUKSES menyediakan jasa konsultasi bisnis strategis untuk perusahaan dari berbagai sektor. Tim konsultan kami terdiri dari para profesional berpengalaman dengan track record sukses.",
                website: "https://asukses-consulting.github.io",
                contact: "082175707027"
            },
            asunet: {
                icon: "🌐",
                title: "ASUNET",
                subtitle: "Asosiasi Sumber Uang Network",
                business: "Layanan Web Server",
                year: "2014",
                employees: "200",
                location: "Palembang, Jakarta, Batam",
                description: "ASUNET menyediakan layanan hosting, cloud server, dan solusi IT infrastructure terpercaya dengan uptime 99.9%. Kami mendukung bisnis digital dengan teknologi terkini.",
                website: "https://asunet-hosting.github.io",
                contact: "082175707028"
            },
            asupet: {
                icon: "🐟🐔",
                title: "ASUPET",
                subtitle: "Asosiasi Sumber Uang Peternakan",
                business: "Peternakan dan Perikanan",
                year: "2015",
                employees: "300",
                location: "Palembang, Bogor, Lampung",
                description: "ASUPET mengoperasikan peternakan modern dan budidaya perikanan dengan standar kualitas tertinggi. Produk kami mencakup daging ayam, telur, ikan segar, dan produk olahan lainnya.",
                website: "https://asupet-farming.github.io",
                contact: "082175707023"
            },
            asustyle: {
                icon: "👕",
                title: "ASUSTYLE",
                subtitle: "Asosiasi Sumber Uang Style",
                business: "Fashion",
                year: "2018",
                employees: "175",
                location: "Palembang, Jakarta, Paris",
                description: "ASUSTYLE adalah brand fashion yang menghadirkan gaya modern dan elegan untuk konsumen muda. Kami menawarkan pakaian berkualitas tinggi dengan desain yang trendi dan timeless.",
                website: "https://asustyle-fashion.github.io",
                contact: "082175707023"
            }
        };

        // Fungsi untuk menampilkan modal
        function showModal(divisionId) {
            const division = divisionData[divisionId];
            if (!division) return;
            
            document.getElementById('modalIcon').textContent = division.icon;
            document.getElementById('modalTitle').textContent = division.title;
            document.getElementById('modalSubtitle').textContent = division.subtitle;
            document.getElementById('modalBusiness').textContent = division.business;
            document.getElementById('modalYear').textContent = division.year;
            document.getElementById('modalEmployees').textContent = division.employees + " orang";
            document.getElementById('modalLocation').textContent = division.location;
            document.getElementById('modalWebsite').textContent = division.website;
            document.getElementById('modalDescription').textContent = division.description;
            
            // Set event listeners untuk tombol modal
            document.getElementById('modalContactBtn').onclick = function() {
                alert(`Hubungi ${division.title} di: ${division.contact}`);
            };
            
            document.getElementById('modalWebsiteBtn').onclick = function() {
                visitWebsite(divisionId);
            };
            
            const modal = document.getElementById('divisionModal');
            modal.classList.add('modal-open');
            
            document.body.style.overflow = 'hidden';
        }

        // Fungsi untuk menyembunyikan modal
        function hideModal() {
            const modal = document.getElementById('divisionModal');
            modal.classList.remove('modal-open');
            
            document.body.style.overflow = 'auto';
        }

        // Fungsi untuk menampilkan semua perusahaan
        function showAllCompaniesModal() {
            const companiesGrid = document.getElementById('companiesGrid');
            companiesGrid.innerHTML = '';
            
            for (const [key, division] of Object.entries(divisionData)) {
                const companyItem = document.createElement('div');
                companyItem.className = 'company-item';
                companyItem.innerHTML = `
                    <div class="company-icon">${division.icon}</div>
                    <h3>${division.title}</h3>
                    <p>${division.subtitle}</p>
                    <p><strong>${division.business}</strong></p>
                    <button class="division-btn website-btn" style="margin-top: 10px;" onclick="visitWebsite('${key}')">Kunjungi Website</button>
                `;
                companyItem.onclick = function() {
                    hideAllCompaniesModal();
                    showModal(key);
                };
                companiesGrid.appendChild(companyItem);
            }
            
            const modal = document.getElementById('allCompaniesModal');
            modal.classList.add('modal-open');
            
            document.body.style.overflow = 'hidden';
        }

        // Fungsi untuk menyembunyikan modal semua perusahaan
        function hideAllCompaniesModal() {
            const modal = document.getElementById('allCompaniesModal');
            modal.classList.remove('modal-open');
            
            document.body.style.overflow = 'auto';
        }

        // Fungsi untuk mengunjungi website perusahaan
        function visitWebsite(divisionId) {
            const division = divisionData[divisionId];
            if (division && division.website) {
                // Membuka website di tab baru
                window.open(division.website, '_blank');
                
                // Menampilkan pesan konfirmasi
                alert(`Mengarahkan ke website ${division.title}: ${division.website}`);
            } else {
                alert('Website tidak tersedia untuk saat ini.');
            }
        }

        // Fungsi untuk scroll ke section tertentu
        function scrollToSection(sectionId) {
            document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
        }

        // Fungsi untuk scroll ke atas
        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Fungsi untuk membuka WhatsApp
        function openWhatsApp() {
            const phoneNumber = "+6282175707023";
            const message = "Halo ASU Group, saya tertarik dengan layanan Anda. apakah Bisa untuk memberi informasi lebih lanjut untuk kita bisa mengadakan kerja sama?";
            const url = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(url, '_blank');
        }

        // Fungsi untuk minta pertemuan via WhatsApp
        function requestMeeting() {
            const phoneNumber = "+6282175707023";
            const message = "Halo pihak ASU group, saya ingin meminta jadwal 2pertemuan untuk membahas kemungkinan kerjasama. Kapan saya bisa menjadwalkan pertemuan?";
            const url = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(url, '_blank');
        }

        // Fungsi-fungsi untuk tombol tambahan
        function showAboutModal() {
            alert("ASU Group adalah holding company terkemuka dengan berbagai anak perusahaan di berbagai sektor industri. Didirikan pada tahun 2010, kami berkomitmen untuk memberikan nilai tambah bagi semua pemangku kepentingan.");
        }

        function showInvestorModal() {
            alert("Informasi untuk investor: Hubungi kami di 082175707023 untuk mendapatkan laporan keuangan dan prospektus investasi.");
        }

        function showCareerModal() {
            alert("Bergabunglah dengan tim ASU Group! Kirim CV dan portofolio Anda ke karir@asugroup.com");
        }

        function showLocation(divisionId) {
            const division = divisionData[divisionId];
            alert(`Lokasi ${division.title}: ${division.location}`);
        }

        function showPartnershipModal() {
            alert("Informasi kemitraan: Hubungi kami di partnership@asugroup.com");
        }

        function showConsultationModal() {
            alert("Jadwalkan konsultasi: Hubungi +6282175707023 atau email ke konsultasi@asugroup.com");
        }

        function showTrainingModal() {
            alert("Jadwal pelatihan dan workshop akan diumumkan melalui website dan media sosial kami.");
        }

        function showSupportModal() {
            alert("Dukungan 24/7: Hubungi +6282175707023 atau email ke support@asugroup.com");
        }

        function showMap() {
            alert("Membuka peta lokasi ASU Group di Palembang.");
        }

        function showDirections() {
            alert("Menampilkan petunjuk arah ke kantor ASU Group.");
        }

        function callNumber() {
            const phoneNumber = "+6282175707023";
            const message = "";
            const url = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(url, '_blank');
        }

        function saveContact() {
            alert("Menyimpan kontak ASU Group ke perangkat Anda.");
        }

        function sendEmail() {
            window.location.href = "mailto:PTAsuGroup@gmail.com";
        }

        function subscribeNewsletter() {
            alert("Terima kasih! Anda telah berlangganan newsletter ASU Group.");
        }

        function showContactForm() {
            alert("Menampilkan formulir kontak ASU Group.");
        }

        function downloadBrochure() {
            alert("Mengunduh brosur ASU Group.");
        }

        function showFAQ() {
            alert("Menampilkan Frequently Asked Questions (FAQ) ASU Group.");
        }

        function showPrivacyPolicy() {
            alert("Menampilkan Kebijakan Privasi ASU Group.");
        }

        function showTerms() {
            alert("Menampilkan Syarat & Ketentuan ASU Group.");
        }

        function showSitemap() {
            alert("Menampilkan Peta Situs ASU Group.");
        }

        // Menambahkan event listener untuk kartu divisi
        document.querySelectorAll('.division-card').forEach(card => {
            card.addEventListener('click', function() {
                const divisionId = this.getAttribute('data-division');
                showModal(divisionId);
            });
        });

        // Menambahkan event listener untuk tombol close
        document.querySelectorAll('.close-button').forEach(button => {
            button.addEventListener('click', function() {
                hideModal();
                hideAllCompaniesModal();
            });
        });

        // Menutup modal ketika klik di luar konten modal
        document.querySelectorAll('.modal').forEach(modal => {
            modal.addEventListener('click', function(e) {
                if (e.target === this) {
                    hideModal();
                    hideAllCompaniesModal();
                }
            });
        });

        // Menutup modal dengan tombol Escape
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                hideModal();
                hideAllCompaniesModal();
            }
        });
    </script>
</body>
</html>
