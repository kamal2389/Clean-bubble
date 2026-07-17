<!DOCTYPE html>
<html lang="el">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clean Bubble | Καθαρισμός Αεραγωγών & Επαγγελματικών Κουζινών</title>
    <meta name="description" content="Επαγγελματικός καθαρισμός αεραγωγών, φούσκας, φίλτρων και εξαερισμού επαγγελματικών κουζινών σε όλη την Ελλάδα.">
    <meta name="keywords" content="καθαρισμός αεραγωγών, εξαερισμός, επαγγελματική κουζίνα, φούσκα, φίλτρα, clean bubble">
    <meta name="author" content="Clean Bubble">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css">

    <style>
        /*======================================================
          CLEAN BUBBLE - PREMIUM STYLE SHEET
        =======================================================*/

        :root {
            --primary: #0f1115;
            --secondary: #ff8c00;
            --secondary-dark: #d87300;
            --white: #ffffff;
            --gray: #bdbdbd;
            --light: #f5f5f5;
            --card: #1b1d22;
            --border: #2b2d33;
            --shadow: 0 20px 50px rgba(0, 0, 0, .35);
            --radius: 18px;
            --transition: .35s ease;
            --max-width: 1280px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: var(--primary);
            color: var(--white);
            overflow-x: hidden;
            line-height: 1.7;
        }

        img {
            width: 100%;
            display: block;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        ul {
            list-style: none;
        }

        .container {
            width: 90%;
            max-width: var(--max-width);
            margin: auto;
        }

        /*==========================
         ANIMATIONS
        ===========================*/

        @keyframes floatDown {
            0% {
                transform: translate(-50%, 0);
            }
            50% {
                transform: translate(-50%, 10px);
            }
            100% {
                transform: translate(-50%, 0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /*==========================
         HEADER
        ===========================*/

        .header {
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 9999;
            transition: .4s;
            padding: 22px 0;
        }

        .header.scrolled {
            background: rgba(15, 17, 21, .96);
            backdrop-filter: blur(12px);
            box-shadow: 0 5px 20px rgba(0, 0, 0, .4);
        }

        .header .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--secondary);
        }

        .logo i {
            font-size: 2rem;
        }

        .navbar ul {
            display: flex;
            gap: 35px;
        }

        .navbar a {
            font-weight: 500;
            position: relative;
            transition: var(--transition);
        }

        .navbar a::after {
            content: "";
            position: absolute;
            left: 0;
            bottom: -8px;
            width: 0;
            height: 2px;
            background: var(--secondary);
            transition: .3s;
        }

        .navbar a:hover {
            color: var(--secondary);
        }

        .navbar a:hover::after {
            width: 100%;
        }

        .header-buttons {
            display: flex;
            gap: 15px;
            align-items: center;
        }

        .call-btn {
            background: var(--secondary);
            color: #111;
            padding: 12px 24px;
            border-radius: 40px;
            font-weight: 600;
            transition: .3s;
            border: none;
            cursor: pointer;
        }

        .call-btn:hover {
            transform: translateY(-3px);
            background: var(--secondary-dark);
        }

        .menu-btn {
            display: none;
            background: none;
            border: none;
            color: #fff;
            font-size: 1.7rem;
            cursor: pointer;
            transition: .3s;
        }

        .menu-btn:hover {
            color: var(--secondary);
        }

        /*==========================
         HERO
        ===========================*/

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            margin-top: 70px;
        }

        .hero::before {
            content: "";
            position: absolute;
            inset: 0;
            background: linear-gradient(90deg, rgba(10, 10, 10, .85), rgba(10, 10, 10, .55));
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 720px;
            padding-top: 120px;
        }

        .hero-top-text {
            display: inline-block;
            color: var(--secondary);
            font-weight: 600;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 20px;
        }

        .hero h1 {
            font-size: 4.5rem;
            line-height: 1.1;
            font-weight: 800;
            margin-bottom: 25px;
        }

        .hero p {
            color: var(--gray);
            font-size: 1.15rem;
            margin-bottom: 40px;
            max-width: 620px;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            margin-bottom: 50px;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 16px 34px;
            border-radius: 50px;
            transition: var(--transition);
            font-weight: 600;
            cursor: pointer;
            border: none;
            font-size: 1rem;
        }

        .btn-primary {
            background: var(--secondary);
            color: #111;
        }

        .btn-primary:hover {
            background: var(--secondary-dark);
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(255, 140, 0, .35);
        }

        .btn-secondary {
            border: 2px solid var(--secondary);
            color: #fff;
            background: transparent;
        }

        .btn-secondary:hover {
            background: var(--secondary);
            color: #111;
        }

        .hero-features {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
        }

        .feature {
            display: flex;
            align-items: center;
            gap: 12px;
            color: #ddd;
        }

        .feature i {
            color: var(--secondary);
            font-size: 1.2rem;
        }

        .scroll-down {
            position: absolute;
            left: 50%;
            bottom: 35px;
            transform: translateX(-50%);
            z-index: 3;
            animation: floatDown 2s infinite;
        }

        .scroll-down a {
            width: 55px;
            height: 55px;
            border-radius: 50%;
            border: 2px solid rgba(255, 255, 255, .3);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            transition: .3s;
        }

        .scroll-down a:hover {
            background: var(--secondary);
            color: #111;
            border-color: var(--secondary);
        }

        /*==========================
         STATS
        ===========================*/

        .stats {
            padding: 90px 0;
            background: #14161b;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
        }

        .stat-card {
            background: var(--card);
            padding: 45px 25px;
            border-radius: var(--radius);
            text-align: center;
            transition: .35s;
            border: 1px solid var(--border);
        }

        .stat-card:hover {
            transform: translateY(-10px);
            border-color: var(--secondary);
            box-shadow: var(--shadow);
        }

        .stat-card h2 {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 10px;
            font-weight: 800;
        }

        .stat-card p {
            color: var(--gray);
        }

        /*==========================
         SERVICES
        ===========================*/

        .services {
            padding: 120px 0;
            background: var(--primary);
        }

        .section-title {
            text-align: center;
            max-width: 760px;
            margin: 0 auto 70px;
        }

        .section-title span {
            display: inline-block;
            color: var(--secondary);
            font-size: .95rem;
            font-weight: 700;
            letter-spacing: 3px;
            margin-bottom: 15px;
            text-transform: uppercase;
        }

        .section-title h2 {
            font-size: 3rem;
            margin-bottom: 20px;
            font-weight: 800;
        }

        .section-title p {
            color: var(--gray);
            font-size: 1.05rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 35px;
        }

        .service-card {
            background: var(--card);
            border-radius: 22px;
            overflow: hidden;
            transition: .4s;
            border: 1px solid var(--border);
            position: relative;
        }

        .service-card:hover {
            transform: translateY(-12px);
            border-color: var(--secondary);
            box-shadow: 0 25px 60px rgba(0, 0, 0, .45);
        }

        .service-image {
            height: 250px;
            overflow: hidden;
            background: linear-gradient(135deg, #ff8c00, #d87300);
        }

        .service-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: .6s;
        }

        .service-card:hover img {
            transform: scale(1.12);
        }

        .service-content {
            padding: 35px;
        }

        .service-icon {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            background: rgba(255, 140, 0, .12);
            color: var(--secondary);
            font-size: 1.7rem;
            margin-bottom: 25px;
        }

        .service-content h3 {
            font-size: 1.6rem;
            margin-bottom: 15px;
        }

        .service-content p {
            color: var(--gray);
            margin-bottom: 25px;
        }

        .service-content ul {
            display: flex;
            flex-direction: column;
            gap: 14px;
            margin-bottom: 30px;
        }

        .service-content li {
            display: flex;
            align-items: center;
            gap: 12px;
            color: #ddd;
        }

        .service-content li i {
            color: var(--secondary);
        }

        .service-btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            color: var(--secondary);
            font-weight: 700;
            transition: .3s;
        }

        .service-btn:hover {
            gap: 18px;
        }

        /*==========================
         ABOUT
        ===========================*/

        .about {
            padding: 120px 0;
            background: #14161b;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 70px;
            align-items: center;
        }

        .about-image {
            position: relative;
            background: linear-gradient(135deg, #ff8c00, #d87300);
            border-radius: 24px;
            padding: 3px;
        }

        .about-image img {
            border-radius: 21px;
            box-shadow: var(--shadow);
            display: block;
        }

        .about-image::after {
            content: "";
            position: absolute;
            width: 180px;
            height: 180px;
            border: 6px solid var(--secondary);
            right: -30px;
            bottom: -30px;
            border-radius: 24px;
            z-index: -1;
        }

        .section-subtitle {
            color: var(--secondary);
            font-weight: 700;
            letter-spacing: 2px;
            display: inline-block;
            margin-bottom: 18px;
        }

        .about-content h2 {
            font-size: 3rem;
            line-height: 1.2;
            margin-bottom: 25px;
        }

        .about-content p {
            color: var(--gray);
            margin-bottom: 22px;
        }

        .about-features {
            display: flex;
            flex-direction: column;
            gap: 25px;
            margin: 40px 0;
        }

        .about-item {
            display: flex;
            gap: 22px;
            align-items: flex-start;
        }

        .about-item i {
            width: 65px;
            height: 65px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            background: rgba(255, 140, 0, .15);
            color: var(--secondary);
            font-size: 1.5rem;
            flex-shrink: 0;
        }

        .about-item h4 {
            margin-bottom: 8px;
            font-size: 1.2rem;
        }

        .about-item p {
            margin: 0;
            color: var(--gray);
        }

        /*==========================
         GALLERY
        ===========================*/

        .gallery {
            padding: 120px 0;
            background: var(--primary);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 22px;
            cursor: pointer;
            background: #111;
            box-shadow: var(--shadow);
        }

        .gallery-item img {
            width: 100%;
            height: 320px;
            object-fit: cover;
            transition: .6s;
            background: linear-gradient(135deg, #ff8c00, #d87300);
        }

        .gallery-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(0, 0, 0, .92), rgba(0, 0, 0, .05));
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 30px;
            opacity: 0;
            transition: .4s;
        }

        .gallery-overlay h3 {
            font-size: 1.5rem;
            margin-bottom: 8px;
        }

        .gallery-overlay p {
            color: #d0d0d0;
            margin-bottom: 20px;
        }

        .gallery-btn {
            width: 55px;
            height: 55px;
            border-radius: 50%;
            background: var(--secondary);
            color: #111;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: .35s;
            cursor: pointer;
            border: none;
            font-size: 1.5rem;
        }

        .gallery-btn:hover {
            transform: rotate(90deg) scale(1.1);
        }

        .gallery-item:hover img {
            transform: scale(1.12);
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        /*==========================
         LIGHTBOX
        ===========================*/

        .lightbox {
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, .95);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10000;
            animation: fadeInUp .3s ease;
        }

        .lightbox-content {
            position: relative;
            max-width: 90%;
            max-height: 90vh;
        }

        .lightbox-content img {
            width: 100%;
            height: auto;
            border-radius: 12px;
        }

        .lightbox-close {
            position: absolute;
            top: -40px;
            right: 0;
            color: #fff;
            font-size: 3rem;
            cursor: pointer;
            transition: .3s;
        }

        .lightbox-close:hover {
            color: var(--secondary);
        }

        /*==========================
         WHY US
        ===========================*/

        .why-us {
            padding: 120px 0;
            background: #14161b;
        }

        .why-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 35px;
        }

        .why-card {
            background: var(--card);
            border-radius: 22px;
            padding: 45px;
            border: 1px solid var(--border);
            text-align: center;
            transition: .4s;
        }

        .why-card:hover {
            transform: translateY(-12px);
            border-color: var(--secondary);
            box-shadow: var(--shadow);
        }

        .why-card i {
            width: 90px;
            height: 90px;
            margin: auto;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            background: rgba(255, 140, 0, .12);
            color: var(--secondary);
            font-size: 2rem;
            margin-bottom: 30px;
        }

        .why-card h3 {
            margin-bottom: 18px;
            font-size: 1.5rem;
        }

        .why-card p {
            color: var(--gray);
            line-height: 1.8;
        }

        /*==========================
         BEFORE AFTER
        ===========================*/

        .before-after {
            padding: 120px 0;
            background: var(--primary);
        }

        .before-after-grid {
            display: grid;
            grid-template-columns: 1.2fr .8fr;
            gap: 60px;
            align-items: center;
        }

        .compare-card {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .compare-image {
            position: relative;
            overflow: hidden;
            border-radius: 20px;
            background: linear-gradient(135deg, #ff8c00, #d87300);
        }

        .compare-image img {
            height: 520px;
            object-fit: cover;
            width: 100%;
        }

        .compare-image span {
            position: absolute;
            top: 20px;
            left: 20px;
            background: var(--secondary);
            color: #111;
            padding: 10px 18px;
            border-radius: 30px;
            font-weight: 700;
        }

        .compare-content h3 {
            font-size: 2.4rem;
            margin-bottom: 25px;
        }

        .compare-content p {
            color: var(--gray);
            margin-bottom: 30px;
        }

        .compare-content ul {
            display: flex;
            flex-direction: column;
            gap: 18px;
        }

        .compare-content li {
            display: flex;
            gap: 14px;
            align-items: center;
        }

        .compare-content li i {
            color: var(--secondary);
        }

        /*==========================
         TESTIMONIALS
        ===========================*/

        .testimonials {
            padding: 120px 0;
            background: #14161b;
        }

        .testimonial-slider {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 35px;
        }

        .testimonial {
            background: var(--card);
            padding: 40px;
            border-radius: 22px;
            border: 1px solid var(--border);
            transition: .4s;
        }

        .testimonial:hover {
            transform: translateY(-10px);
            border-color: var(--secondary);
            box-shadow: var(--shadow);
        }

        .stars {
            display: flex;
            gap: 8px;
            margin-bottom: 20px;
        }

        .stars i {
            color: var(--secondary);
            font-size: 1.1rem;
        }

        .testimonial p {
            color: var(--gray);
            margin-bottom: 20px;
            line-height: 1.8;
        }

        .testimonial h4 {
            margin-bottom: 5px;
            font-size: 1.1rem;
        }

        .testimonial span {
            color: #888;
            font-size: .9rem;
        }

        /*==========================
         FAQ
        ===========================*/

        .faq {
            padding: 120px 0;
            background: var(--primary);
        }

        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }

        .faq-item {
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: var(--radius);
            margin-bottom: 20px;
            overflow: hidden;
            transition: .3s;
        }

        .faq-item:hover {
            border-color: var(--secondary);
        }

        .faq-question {
            padding: 25px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            transition: .3s;
        }

        .faq-question:hover {
            background: rgba(255, 140, 0, .05);
        }

        .faq-question h3 {
            font-size: 1.1rem;
            margin: 0;
        }

        .faq-question i {
            color: var(--secondary);
            transition: .3s;
        }

        .faq-item.active .faq-question i {
            transform: rotate(45deg);
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: .3s;
        }

        .faq-item.active .faq-answer {
            max-height: 500px;
            padding: 0 25px 25px;
        }

        .faq-answer p {
            color: var(--gray);
            line-height: 1.8;
        }

        /*==========================
         CTA SECTION
        ===========================*/

        .cta-section {
            padding: 120px 0;
            background: #14161b;
        }

        .cta-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        .cta-content h2 {
            font-size: 3rem;
            margin-bottom: 25px;
        }

        .cta-content p {
            color: var(--gray);
            font-size: 1.1rem;
            margin-bottom: 40px;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        /*==========================
         CONTACT
        ===========================*/

        .contact {
            padding: 120px 0;
            background: var(--primary);
        }

        .contact-wrapper {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            margin-top: 60px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .contact-box {
            display: flex;
            gap: 25px;
            align-items: flex-start;
        }

        .contact-box i {
            width: 65px;
            height: 65px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            background: rgba(255, 140, 0, .15);
            color: var(--secondary);
            font-size: 1.5rem;
            flex-shrink: 0;
        }

        .contact-box h3 {
            margin-bottom: 10px;
        }

        .contact-box p {
            color: var(--gray);
            margin: 0;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            padding: 15px 20px;
            border: 1px solid var(--border);
            background: var(--card);
            color: #fff;
            border-radius: var(--radius);
            font-family: 'Poppins', sans-serif;
            transition: .3s;
            font-size: 1rem;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 15px rgba(255, 140, 0, .2);
        }

        .form-group select {
            cursor: pointer;
        }

        .form-group select option {
            background: var(--primary);
            color: #fff;
        }

        .submit-btn {
            width: 100%;
        }

        /*==========================
         MAP
        ===========================*/

        .map {
            width: 100%;
            height: 500px;
        }

        .map iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        /*==========================
         FOOTER
        ===========================*/

        .footer {
            background: #0a0b0f;
            padding: 60px 0 20px;
            border-top: 1px solid var(--border);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-about h3 {
            margin-bottom: 15px;
            font-size: 1.5rem;
            color: var(--secondary);
        }

        .footer-about p {
            color: var(--gray);
            margin-bottom: 20px;
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-links a {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: rgba(255, 140, 0, .15);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--secondary);
            transition: .3s;
        }

        .social-links a:hover {
            background: var(--secondary);
            color: #111;
        }

        .footer-links h4,
        .footer-contact h4 {
            margin-bottom: 20px;
            color: var(--secondary);
        }

        .footer-links ul {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .footer-links a {
            color: var(--gray);
            transition: .3s;
        }

        .footer-links a:hover {
            color: var(--secondary);
        }

        .footer-contact p {
            color: var(--gray);
            margin-bottom: 15px;
            display: flex;
            gap: 12px;
            align-items: center;
        }

        .footer-contact i {
            color: var(--secondary);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid var(--border);
            color: var(--gray);
        }

        /*==========================
         FLOATING BUTTONS
        ===========================*/

        .floating-call,
        .floating-whatsapp {
            position: fixed;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            font-size: 1.5rem;
            z-index: 999;
            transition: .3s;
            bottom: 30px;
        }

        .floating-call {
            background: var(--secondary);
            right: 30px;
        }

        .floating-call:hover {
            background: var(--secondary-dark);
            transform: scale(1.1);
        }

        .floating-whatsapp {
            background: #25d366;
            right: 100px;
        }

        .floating-whatsapp:hover {
            background: #20ba5f;
            transform: scale(1.1);
        }

        /*==========================
         RESPONSIVE DESIGN
        ===========================*/

        @media (max-width: 1024px) {
            .navbar ul {
                gap: 20px;
            }

            .hero h1 {
                font-size: 3.5rem;
            }

            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .about-grid,
            .before-after-grid {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .about-image::after {
                display: none;
            }

            .compare-image img {
                height: 400px;
            }

            .contact-wrapper {
                grid-template-columns: 1fr;
            }

            .cta-buttons {
                flex-direction: column;
            }
        }

        @media (max-width: 768px) {
            .header .container {
                position: relative;
            }

            .navbar {
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: rgba(15, 17, 21, .98);
                backdrop-filter: blur(12px);
                flex-direction: column;
                max-height: 0;
                overflow: hidden;
                transition: .3s;
            }

            .navbar.active {
                max-height: 400px;
            }

            .navbar ul {
                flex-direction: column;
                gap: 0;
                padding: 20px 0;
            }

            .navbar li {
                padding: 0;
            }

            .navbar a {
                display: block;
                padding: 15px 20px;
            }

            .call-btn {
                display: none;
            }

            .menu-btn {
                display: block;
            }

            .hero {
                margin-top: 0;
                min-height: 80vh;
            }

            .hero-content {
                padding-top: 60px;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .hero-features {
                flex-direction: column;
                gap: 15px;
            }

            .section-title h2 {
                font-size: 2rem;
            }

            .stats-grid,
            .services-grid,
            .why-grid {
                grid-template-columns: 1fr;
            }

            .stat-card h2 {
                font-size: 2rem;
            }

            .compare-card {
                grid-template-columns: 1fr;
            }

            .compare-image img {
                height: 300px;
            }

            .compare-content h3 {
                font-size: 1.8rem;
            }

            .floating-call,
            .floating-whatsapp {
                width: 50px;
                height: 50px;
                font-size: 1.2rem;
                bottom: 20px;
            }

            .floating-whatsapp {
                right: 80px;
            }

            .map {
                height: 300px;
            }
        }

        @media (max-width: 480px) {
            .container {
                width: 95%;
            }

            .hero h1 {
                font-size: 1.8rem;
            }

            .hero p {
                font-size: .95rem;
            }

            .hero-buttons {
                flex-direction: column;
            }

            .btn {
                padding: 14px 28px;
            }

            .section-title h2 {
                font-size: 1.6rem;
            }

            .service-card,
            .why-card,
            .testimonial {
                padding: 25px;
            }

            .service-image {
                height: 200px;
            }

            .gallery-item img {
                height: 250px;
            }

            .before-after-grid {
                gap: 30px;
            }

            .compare-content h3 {
                font-size: 1.4rem;
            }

            .compare-content ul {
                gap: 12px;
            }

            .contact-form {
                gap: 15px;
            }

            .form-group input,
            .form-group select,
            .form-group textarea {
                padding: 12px 15px;
            }

            .floating-call,
            .floating-whatsapp {
                width: 45px;
                height: 45px;
                font-size: 1rem;
            }

            .floating-whatsapp {
                right: 65px;
            }

            footer .footer-grid {
                gap: 30px;
            }
        }
    </style>
</head>

<body>

    <!-- ================= NAVBAR ================= -->
    <header class="header">
        <div class="container">
            <a href="#" class="logo">
                <i class="fa-solid fa-fan"></i>
                <span>Clean Bubble</span>
            </a>

            <nav class="navbar">
                <ul>
                    <li><a href="#home">Αρχική</a></li>
                    <li><a href="#services">Υπηρεσίες</a></li>
                    <li><a href="#about">Η Εταιρεία</a></li>
                    <li><a href="#gallery">Έργα</a></li>
                    <li><a href="#contact">Επικοινωνία</a></li>
                </ul>
            </nav>

            <div class="header-buttons">
                <a href="tel:+306933237692" class="call-btn">
                    <i class="fa-solid fa-phone"></i>
                    693 3237692
                </a>
                <button class="menu-btn">
                    <i class="fa-solid fa-bars"></i>
                </button>
            </div>
        </div>
    </header>

    <!-- ================= HERO ================= -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <span class="hero-top-text">Κορυφαίες Υπηρεσίες Καθαρισμού</span>

            <h1>
                Καθαρισμός Αεραγωγών
                <br>
                & Επαγγελματικών Κουζινών
            </h1>

            <p>
                Εξειδικευόμαστε στον καθαρισμό συστημάτων εξαερισμού,
                φούσκας, φίλτρων και αεραγωγών με πιστοποιημένο εξοπλισμό
                και εγγυημένο αποτέλεσμα.
            </p>

            <div class="hero-buttons">
                <a href="#contact" class="btn btn-primary">
                    <i class="fa-solid fa-paper-plane"></i>
                    Ζητήστε Προσφορά
                </a>
                <a href="tel:+302101234567" class="btn btn-secondary">
                    <i class="fa-solid fa-phone"></i>
                    Καλέστε Τώρα
                </a>
            </div>

            <div class="hero-features">
                <div class="feature">
                    <i class="fa-solid fa-circle-check"></i>
                    <span>10+ Χρόνια Εμπειρίας</span>
                </div>
                <div class="feature">
                    <i class="fa-solid fa-circle-check"></i>
                    <span>24/7 Εξυπηρέτηση</span>
                </div>
                <div class="feature">
                    <i class="fa-solid fa-circle-check"></i>
                    <span>Πιστοποιημένος Εξοπλισμός</span>
                </div>
            </div>
        </div>

        <div class="scroll-down">
            <a href="#stats">
                <i class="fa-solid fa-chevron-down"></i>
            </a>
        </div>
    </section>

    <!-- ================= COMPANY STATS ================= -->
    <section id="stats" class="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-card">
                    <h2 class="counter" data-target="500">0</h2>
                    <p>Ολοκληρωμένα Έργα</p>
                </div>
                <div class="stat-card">
                    <h2 class="counter" data-target="10">0</h2>
                    <p>Χρόνια Εμπειρίας</p>
                </div>
                <div class="stat-card">
                    <h2 class="counter" data-target="300">0</h2>
                    <p>Ευχαριστημένοι Πελάτες</p>
                </div>
                <div class="stat-card">
                    <h2>24/7</h2>
                    <p>Τεχνική Υποστήριξη</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ================= SERVICES ================= -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-title">
                <span>ΥΠΗΡΕΣΙΕΣ</span>
                <h2>Τι Αναλαμβάνουμε</h2>
                <p>
                    Παρέχουμε ολοκληρωμένες υπηρεσίες καθαρισμού και
                    συντήρησης συστημάτων εξαερισμού επαγγελματικών κουζινών,
                    σύμφωνα με τα υψηλότερα πρότυπα ποιότητας.
                </p>
            </div>

            <div class="services-grid">
                <div class="service-card">
                    <div class="service-image">
                        <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 250'%3E%3Crect fill='%23ff8c00' width='300' height='250'/%3E%3Ctext x='50%' y='50%' font-size='48' fill='white' text-anchor='middle' dominant-baseline='middle'%3E🌪️%3C/text%3E%3C/svg%3E" alt="Καθαρισμός Αεραγωγών">
                    </div>
                    <div class="service-content">
                        <div class="service-icon">
                            <i class="fa-solid fa-wind"></i>
                        </div>
                        <h3>Καθαρισμός Αεραγωγών</h3>
                        <p>
                            Πλήρης καθαρισμός δικτύων εξαερισμού,
                            απομάκρυνση λιπών, σκόνης και μικροβίων
                            με εξειδικευμένο εξοπλισμό.
                        </p>
                        <ul>
                            <li>
                                <i class="fa-solid fa-check"></i>
                                Απομάκρυνση λιπών
                            </li>
                            <li>
                                <i class="fa-solid fa-check"></i>
                                Απολύμανση
                            </li>
                            <li>
                                <i class="fa-solid fa-check"></i>
                                Έλεγχος δικτύου
                            </li>
                        </ul>
                        <a href="#contact" class="service-btn">
                            Περισσότερα
                            <i class="fa-solid fa-arrow-right"></i>
                        </a>
                    </div>
                </div>

                <div class="service-card">
                    <div class="service-image">
                        <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 250'%3E%3Crect fill='%23ff8c00' width='300' height='250'/%3E%3Ctext x='50%' y='50%' font-size='48' fill='white' text-anchor='middle' dominant-baseline='middle'%3E🔥%3C/text%3E%3C/svg%3E" alt="Καθαρισμός Φούσκας">
                    </div>
                    <div class="service-content">
                        <div class="service-icon">
                            <i class="fa-solid fa-fire"></i>
                        </div>
                        <h3>Καθαρισμός Φούσκας</h3>
                        <p>
                            Επαγγελματικός καθαρισμός απορροφητήρων,
                            φούσκας και καναλιών με ασφαλείς τεχνικές
                            και πιστοποιημένα καθαριστικά.
                        </p>
                        <ul>
                            <li>
                                <i class="fa-solid fa-check"></i>
                                Απομάκρυνση καμένου λίπους
                            </li>
                            <li>
                                <i class="fa-solid fa-check"></i>
                                Μείωση κινδύνου πυρκαγιάς
                            </li>
                            <li>
                                <i class="fa-solid fa-check"></i>
                                Πιστοποιημένος καθαρισμός
                            </li>
                        </ul>
                        <a href="#contact" class="service-btn">
                            Περισσότερα
                            <i class="fa-solid fa-arrow-right"></i>
                        </a>
                    </div>
                </div>

                <div class="service-card">
                    <div class="service-image">
                        <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 250'%3E%3Crect fill='%23ff8c00' width='300' height='250'/%3E%3Ctext x='50%' y='50%' font-size='48' fill='white' text-anchor='middle' dominant-baseline='middle'%3E🔧%3C/text%3E%3C/svg%3E" alt="Αλλαγή Φίλτρων">
                    </div>
                    <div class="service-content">
                        <div class="service-icon">
                            <i class="fa-solid fa-filter"></i>
                        </div>
                        <h3>Αλλαγή & Συντήρηση Φίλτρων</h3>
                        <p>
                            Αντικατάσταση φίλτρων, συντήρηση
                            εξαερισμού και πλήρης τεχνικός έλεγχος
                            για μέγιστη απόδοση.
                        </p>
                        <ul>
                            <li>
                                <i class="fa-solid fa-check"></i>
                                Αντικατάσταση φίλτρων
                            </li>
                            <li>
                                <i class="fa-solid fa-check"></i>
                                Συντήρηση εξαερισμού
                            </li>
                            <li>
                                <i class="fa-solid fa-check"></i>
                                Έλεγχος απόδοσης
                            </li>
                        </ul>
                        <a href="#contact" class="service-btn">
                            Περισσότερα
                            <i class="fa-solid fa-arrow-right"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ================= ABOUT ================= -->
    <section id="about" class="about">
        <div class="container">
            <div class="about-grid">
                <div class="about-image">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 400'%3E%3Crect fill='%23d87300' width='400' height='400'/%3E%3Ctext x='50%' y='50%' font-size='120' fill='white' text-anchor='middle' dominant-baseline='middle'%3E✓%3C/text%3E%3C/svg%3E" alt="Clean Bubble">
                </div>

                <div class="about-content">
                    <span class="section-subtitle">ΣΧΕΤΙΚΑ ΜΕ ΕΜΑΣ</span>
                    <h2>
                        Εξειδικευμένες Υπηρεσίες
                        Καθαρισμού Επαγγελματικών
                        Κουζινών
                    </h2>

                    <p>
                        Η Clean Bubble δραστηριοποιείται
                        στον επαγγελματικό καθαρισμό
                        αεραγωγών, φούσκας, φίλτρων
                        και εξαερισμού επαγγελματικών
                        κουζινών.
                    </p>

                    <p>
                        Με σύγχρονο εξοπλισμό και
                        εξειδικευμένο προσωπικό,
                        προσφέρουμε υπηρεσίες υψηλών
                        προδιαγραφών σε ξενοδοχεία,
                        εστιατόρια, καφέ, catering,
                        νοσοκομεία και βιομηχανίες
                        τροφίμων.
                    </p>

                    <div class="about-features">
                        <div class="about-item">
                            <i class="fa-solid fa-award"></i>
                            <div>
                                <h4>Πιστοποιημένες Εργασίες</h4>
                                <p>
                                    Όλες οι εργασίες
                                    εκτελούνται σύμφωνα
                                    με τα ευρωπαϊκά πρότυπα.
                                </p>
                            </div>
                        </div>

                        <div class="about-item">
                            <i class="fa-solid fa-clock"></i>
                            <div>
                                <h4>Άμεση Εξυπηρέτηση</h4>
                                <p>
                                    Διαθέσιμοι
                                    όλο το 24ωρο
                                    για επείγοντα περιστατικά.
                                </p>
                            </div>
                        </div>

                        <div class="about-item">
                            <i class="fa-solid fa-shield-halved"></i>
                            <div>
                                <h4>Εγγύηση Ποιότητας</h4>
                                <p>
                                    Χρησιμοποιούμε
                                    μόνο επαγγελματικό
                                    εξοπλισμό τελευταίας
                                    τεχνολογίας.
                                </p>
                            </div>
                        </div>
                    </div>

                    <a href="#gallery" class="btn btn-primary">
                        Δείτε τα Έργα μας
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ================= GALLERY ================= -->
    <section id="gallery" class="gallery">
        <div class="container">
            <div class="section-title">
                <span>GALLERY</span>
                <h2>Πρόσφατα Έργα</h2>
                <p>
                    Μερικά από τα έργα καθαρισμού
                    που έχουμε ολοκληρώσει
                    σε όλη την Ελλάδα.
                </p>
            </div>

            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 300'%3E%3Crect fill='%23ff8c00' width='300' height='300'/%3E%3Ctext x='50%' y='50%' font-size='64' fill='white' text-anchor='middle' dominant-baseline='middle'%3E🌬️%3C/text%3E%3C/svg%3E" alt="Καθαρισμός Αεραγωγών">
                    <div class="gallery-overlay">
                        <h3>Καθαρισμός Αεραγωγών</h3>
                        <p>Εστιατόριο Αθήνας</p>
                        <button class="gallery-btn">
                            <i class="fa-solid fa-expand"></i>
                        </button>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 300'%3E%3Crect fill='%23ff8c00' width='300' height='300'/%3E%3Ctext x='50%' y='50%' font-size='64' fill='white' text-anchor='middle' dominant-baseline='middle'%3E🔥%3C/text%3E%3C/svg%3E" alt="Καθαρισμός Φούσκας">
                    <div class="gallery-overlay">
                        <h3>Καθαρισμός Φούσκας</h3>
                        <p>Ξενοδοχειακή Μονάδα</p>
                        <button class="gallery-btn">
                            <i class="fa-solid fa-expand"></i>
                        </button>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 300'%3E%3Crect fill='%23ff8c00' width='300' height='300'/%3E%3Ctext x='50%' y='50%' font-size='64' fill='white' text-anchor='middle' dominant-baseline='middle'%3E🔧%3C/text%3E%3C/svg%3E" alt="Αντικατάσταση Φίλτρων">
                    <div class="gallery-overlay">
                        <h3>Αλλαγή Φίλτρων</h3>
                        <p>Βιομηχανική Κουζίνα</p>
                        <button class="gallery-btn">
                            <i class="fa-solid fa-expand"></i>
                        </button>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 300'%3E%3Crect fill='%23ff8c00' width='300' height='300'/%3E%3Ctext x='50%' y='50%' font-size='64' fill='white' text-anchor='middle' dominant-baseline='middle'%3E✨%3C/text%3E%3C/svg%3E" alt="Επαγγελματικός Καθαρισμός">
                    <div class="gallery-overlay">
                        <h3>Επαγγελματικός Καθαρισμός</h3>
                        <p>Catering</p>
                        <button class="gallery-btn">
                            <i class="fa-solid fa-expand"></i>
                        </button>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 300'%3E%3Crect fill='%23ff8c00' width='300' height='300'/%3E%3Ctext x='50%' y='50%' font-size='64' fill='white' text-anchor='middle' dominant-baseline='middle'%3E🏨%3C/text%3E%3C/svg%3E" alt="Συντήρηση Εξαερισμού">
                    <div class="gallery-overlay">
                        <h3>Συντήρηση Εξαερισμού</h3>
                        <p>Ξενοδοχείο</p>
                        <button class="gallery-btn">
                            <i class="fa-solid fa-expand"></i>
                        </button>
                    </div>
                </div>

                <div class="gallery-item">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 300'%3E%3Crect fill='%23ff8c00' width='300' height='300'/%3E%3Ctext x='50%' y='50%' font-size='64' fill='white' text-anchor='middle' dominant-baseline='middle'%3E⭐%3C/text%3E%3C/svg%3E" alt="Ολοκληρωμένο Έργο">
                    <div class="gallery-overlay">
                        <h3>Ολοκληρωμένο Έργο</h3>
                        <p>Επαγγελματική Κουζίνα</p>
                        <button class="gallery-btn">
                            <i class="fa-solid fa-expand"></i>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ================= WHY CHOOSE US ================= -->
    <section class="why-us">
        <div class="container">
            <div class="section-title">
                <span>ΓΙΑΤΙ ΕΜΑΣ</span>
                <h2>Γιατί να Επιλέξετε την Clean Bubble</h2>
                <p>
                    Προσφέρουμε υπηρεσίες υψηλής ποιότητας
                    με σύγχρονο εξοπλισμό και έμπειρο προσωπικό.
                </p>
            </div>

            <div class="why-grid">
                <div class="why-card">
                    <i class="fa-solid fa-user-check"></i>
                    <h3>Έμπειρο Προσωπικό</h3>
                    <p>
                        Οι τεχνικοί μας διαθέτουν πολυετή εμπειρία
                        στον καθαρισμό επαγγελματικών εγκαταστάσεων.
                    </p>
                </div>

                <div class="why-card">
                    <i class="fa-solid fa-gears"></i>
                    <h3>Σύγχρονος Εξοπλισμός</h3>
                    <p>
                        Χρησιμοποιούμε επαγγελματικά μηχανήματα
                        τελευταίας τεχνολογίας.
                    </p>
                </div>

                <div class="why-card">
                    <i class="fa-solid fa-shield"></i>
                    <h3>Ασφάλεια</h3>
                    <p>
                        Όλες οι εργασίες εκτελούνται
                        σύμφωνα με τα πρότυπα ασφαλείας.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- ================= BEFORE / AFTER ================= -->
    <section class="before-after">
        <div class="container">
            <div class="section-title">
                <span>ΠΡΙΝ & ΜΕΤΑ</span>
                <h2>Η Διαφορά είναι Ορατή</h2>
                <p>
                    Δείτε πραγματικά αποτελέσματα από
                    καθαρισμούς αεραγωγών και φούσκας.
                </p>
            </div>

            <div class="before-after-grid">
                <div class="compare-card">
                    <div class="compare-image before">
                        <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 400'%3E%3Crect fill='%23333' width='300' height='400'/%3E%3Ctext x='50%' y='50%' font-size='80' fill='white' text-anchor='middle' dominant-baseline='middle'%3E❌%3C/text%3E%3C/svg%3E" alt="Πριν">
                        <span>ΠΡΙΝ</span>
                    </div>

                    <div class="compare-image after">
                        <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 300 400'%3E%3Crect fill='%23ff8c00' width='300' height='400'/%3E%3Ctext x='50%' y='50%' font-size='80' fill='white' text-anchor='middle' dominant-baseline='middle'%3E✓%3C/text%3E%3C/svg%3E" alt="Μετά">
                        <span>ΜΕΤΑ</span>
                    </div>
                </div>

                <div class="compare-content">
                    <h3>
                        Γιατί είναι απαραίτητος
                        ο τακτικός καθαρισμός;
                    </h3>

                    <p>
                        Η συσσώρευση λιπών στους
                        αεραγωγούς αυξάνει σημαντικά
                        τον κίνδυνο πυρκαγιάς,
                        μειώνει την απόδοση του
                        εξαερισμού και δημιουργεί
                        έντονες οσμές.
                    </p>

                    <ul>
                        <li>
                            <i class="fa-solid fa-check"></i>
                            Μείωση κινδύνου πυρκαγιάς
                        </li>
                        <li>
                            <i class="fa-solid fa-check"></i>
                            Καλύτερη ποιότητα αέρα
                        </li>
                        <li>
                            <i class="fa-solid fa-check"></i>
                            Μεγαλύτερη διάρκεια ζωής
                            εξοπλισμού
                        </li>
                        <li>
                            <i class="fa-solid fa-check"></i>
                            Συμμόρφωση με τους
                            κανόνες υγιεινής
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- ================= TESTIMONIALS ================= -->

    <section class="faq">
        <div class="container">
            <div class="section-title">
                <span>FAQ</span>
                <h2>Συχνές Ερωτήσεις</h2>
            </div>

            <div class="faq-container">
                <div class="faq-item active">
                    <div class="faq-question">
                        <h3>
                            Κάθε πότε πρέπει να γίνεται
                            καθαρισμός αεραγωγών;
                        </h3>
                        <i class="fa-solid fa-plus"></i>
                    </div>
                    <div class="faq-answer">
                        <p>
                            Συνιστάται τουλάχιστον μία φορά
                            τον χρόνο ή συχνότερα σε χώρους
                            με έντονη χρήση όπως εστιατόρια,
                            ξενοδοχεία και catering.
                        </p>
                    </div>
                </div>

                <div class="faq-item">
                    <div class="faq-question">
                        <h3>
                            Πόσο διαρκεί ένας καθαρισμός;
                        </h3>
                        <i class="fa-solid fa-plus"></i>
                    </div>
                    <div class="faq-answer">
                        <p>
                            Ανάλογα με το μέγεθος της
                            εγκατάστασης, από 2 έως 8 ώρες.
                        </p>
                    </div>
                </div>

                <div class="faq-item">
                    <div class="faq-question">
                        <h3>
                            Παρέχετε πιστοποιητικό εργασιών;
                        </h3>
                        <i class="fa-solid fa-plus"></i>
                    </div>
                    <div class="faq-answer">
                        <p>
                            Ναι. Μετά την ολοκλήρωση των
                            εργασιών παρέχεται σχετική
                            βεβαίωση καθαρισμού όπου
                            απαιτείται.
                        </p>
                    </div>
                </div>

                <div class="faq-item">
                    <div class="faq-question">
                        <h3>
                            Εργάζεστε σε όλη την Ελλάδα;
                        </h3>
                        <i class="fa-solid fa-plus"></i>
                    </div>
                    <div class="faq-answer">
                        <p>
                            Προς το παρόν, αναλαμβάνουμε έργα σε όλη την Αττική και τις γειτονικές περιοχές.

                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ================= CALL TO ACTION ================= -->
    <section class="cta-section">
        <div class="container">
            <div class="cta-content">
                <h2>
                    Χρειάζεστε Καθαρισμό
                    Αεραγωγών;
                </h2>

                <p>
                    Επικοινωνήστε μαζί μας σήμερα
                    και λάβετε δωρεάν εκτίμηση
                    για τον χώρο σας.
                </p>

                <div class="cta-buttons">
                    <a href="tel:+302101234567" class="btn btn-primary">
                        <i class="fa-solid fa-phone"></i>
                        Καλέστε Τώρα
                    </a>

                    <a href="#contact" class="btn btn-secondary">
                        <i class="fa-solid fa-envelope"></i>
                        Ζητήστε Προσφορά
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ================= CONTACT ================= -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <span>ΕΠΙΚΟΙΝΩΝΙΑ</span>
                <h2>
                    Επικοινωνήστε Μαζί μας
                </h2>

                <p>
                    Συμπληρώστε τη φόρμα και
                    θα επικοινωνήσουμε μαζί σας
                    το συντομότερο δυνατό.
                </p>
            </div>

            <div class="contact-wrapper">
                <div class="contact-info">
                    <div class="contact-box">
                        <i class="fa-solid fa-phone"></i>
                        <div>
                            <h3>Τηλέφωνο</h3>
                            <p>
                                +30 693 3237692
                            </p>
                        </div>
                    </div>

                    <div class="contact-box">
                        <i class="fa-solid fa-envelope"></i>
                        <div>
                            <h3>Email</h3>
                            <p>
                               martensaid22@gmail.com
                            </p>
                        </div>
                    </div>

                    <div class="contact-box">
                        <i class="fa-solid fa-location-dot"></i>
                        <div>
                            <h3>Έδρα</h3>
                            <p>
                                Αθήνα, Ελλάδα
                            </p>
                        </div>
                    </div>
                </div>

                <form class="contact-form">
                    <div class="form-group">
                        <input
                            type="text"
                            name="name"
                            placeholder="Ονοματεπώνυμο"
                            required>
                    </div>

                    <div class="form-group">
                        <input
                            type="email"
                            name="email"
                            placeholder="Email"
                            required>
                    </div>

                    <div class="form-group">
                        <input
                            type="tel"
                            name="phone"
                            placeholder="Τηλέφωνο">
                    </div>

                    <div class="form-group">
                        <input
                            type="text"
                            name="company"
                            placeholder="Επωνυμία Επιχείρησης">
                    </div>

                    <div class="form-group">
                        <select name="service">
                            <option value="">
                                Επιλέξτε Υπηρεσία
                            </option>
                            <option>
                                Καθαρισμός Αεραγωγών
                            </option>
                            <option>
                                Καθαρισμός Φούσκας
                            </option>
                            <option>
                                Αντικατάσταση Φίλτρων
                            </option>
                            <option>
                                Συντήρηση Εξαερισμού
                            </option>
                        </select>
                    </div>

                    <div class="form-group">
                        <textarea
                            rows="6"
                            name="message"
                            placeholder="Γράψτε το μήνυμά σας..."
                            required>
                        </textarea>
                    </div>

                    <button
                        type="submit"
                        class="btn btn-primary submit-btn">
                        <i class="fa-solid fa-paper-plane"></i>
                        Αποστολή Μηνύματος
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- ================= GOOGLE MAP ================= -->
    <section class="map">
        <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3022.1841562581303!2d23.7293!3d37.9838!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14a1a1a1a1a1a1a1%3A0x1a1a1a1a1a1a1a1a!2z0s-R0YDQu9C80YPRgtC40Y8!5e0!3m2!1sel!2sgr!4v1234567890"
            loading="lazy"
            allowfullscreen="">
        </iframe>
    </section>

    <!-- ================= FOOTER ================= -->
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-about">
                    <h3>
                        Clean Bubble
                    </h3>

                    <p>
                        Επαγγελματικός καθαρισμός
                        αεραγωγών, εξαερισμού,
                        φούσκας και φίλτρων
                        επαγγελματικών κουζινών.
                    </p>

                    <div class="social-links">
                        <a href="https://facebook.com" target="_blank">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="https://instagram.com" target="_blank">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="https://linkedin.com" target="_blank">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="https://youtube.com" target="_blank">
                            <i class="fab fa-youtube"></i>
                        </a>
                    </div>
                </div>

                <div class="footer-links">
                    <h4>
                        Γρήγορο Μενού
                    </h4>

                    <ul>
                        <li>
                            <a href="#home">
                                Αρχική
                            </a>
                        </li>
                        <li>
                            <a href="#services">
                                Υπηρεσίες
                            </a>
                        </li>
                        <li>
                            <a href="#gallery">
                                Έργα
                            </a>
                        </li>
                        <li>
                            <a href="#contact">
                                Επικοινωνία
                            </a>
                        </li>
                    </ul>
                </div>

                <div class="footer-contact">
                    <h4>
                        Στοιχεία
                    </h4>

                    <p>
                        <i class="fa-solid fa-phone"></i>
                        +30 6933237692
                    </p>

                    <p>
                        <i class="fa-solid fa-envelope"></i>
                        martensaid22@gmail.com
                    </p>

                    <p>
                        <i class="fa-solid fa-location-dot"></i>
                        Αθήνα, Ελλάδα
                    </p>
                </div>
            </div>

            <div class="footer-bottom">
                <p>
                    © 2026 Clean Bubble.
                    All Rights Reserved.
                </p>
            </div>
        </div>
    </footer>

    <!-- Floating Buttons -->
    <a href="tel:+302101234567" class="floating-call">
        <i class="fa-solid fa-phone"></i>
    </a>

    <a href="https://wa.me/302101234567" target="_blank" class="floating-whatsapp">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        /*======================================================
          CLEAN BUBBLE - JAVASCRIPT
        =======================================================*/

        document.addEventListener('DOMContentLoaded', function () {

            // ================= HEADER SCROLL ================= 
            const header = document.querySelector('.header');
            window.addEventListener('scroll', function () {
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }
            });

            // ================= MOBILE MENU ================= 
            const menuBtn = document.querySelector('.menu-btn');
            const navbar = document.querySelector('.navbar');

            if (menuBtn) {
                menuBtn.addEventListener('click', function () {
                    navbar.classList.toggle('active');
                    menuBtn.classList.toggle('active');
                });
            }

            // ================= SMOOTH SCROLL & CLOSE MENU ================= 
            const navLinks = document.querySelectorAll('.navbar a');
            navLinks.forEach(link => {
                link.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetSection = document.querySelector(targetId);

                    if (targetSection) {
                        targetSection.scrollIntoView({ behavior: 'smooth' });
                        navbar.classList.remove('active');
                        menuBtn.classList.remove('active');
                    }
                });
            });

            // ================= COUNTER ANIMATION ================= 
            const counters = document.querySelectorAll('.counter');
            const statsSection = document.querySelector('.stats');
            let hasAnimated = false;

            function animateCounters() {
                counters.forEach(counter => {
                    const target = parseInt(counter.getAttribute('data-target'));
                    let current = 0;
                    const increment = target / 50;

                    const updateCounter = () => {
                        current += increment;
                        if (current < target) {
                            counter.textContent = Math.ceil(current);
                            setTimeout(updateCounter, 40);
                        } else {
                            counter.textContent = target;
                        }
                    };
                    updateCounter();
                });
            }

            // Trigger animation when stats section is visible
            const observerOptions = {
                threshold: 0.5
            };

            const observer = new IntersectionObserver(function (entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting && !hasAnimated) {
                        animateCounters();
                        hasAnimated = true;
                        observer.unobserve(entry.target);
                    }
                });
            }, observerOptions);

            if (statsSection) {
                observer.observe(statsSection);
            }

            // ================= FAQ TOGGLE ================= 
            const faqItems = document.querySelectorAll('.faq-item');

            faqItems.forEach(item => {
                const question = item.querySelector('.faq-question');
                question.addEventListener('click', function () {
                    // Close other items
                    faqItems.forEach(otherItem => {
                        if (otherItem !== item) {
                            otherItem.classList.remove('active');
                        }
                    });
                    // Toggle current item
                    item.classList.toggle('active');
                });
            });

            // ================= FORM SUBMISSION ================= 
            const contactForm = document.querySelector('.contact-form');

            if (contactForm) {
                contactForm.addEventListener('submit', function (e) {
                    e.preventDefault();

                    const formData = new FormData(this);
                    const data = Object.fromEntries(formData);

                    // Validate form
                    if (!data.name || !data.email || !data.message) {
                        alert('Παρακαλώ συμπληρώστε τα υποχρεωτικά πεδία');
                        return;
                    }

                    // Email validation
                    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                    if (!emailRegex.test(data.email)) {
                        alert('Παρακαλώ εισάγετε έγκυρο email');
                        return;
                    }

                    // Log form data (σε πραγματική εφαρμογή θα στέλνατε σε server)
                    console.log('Form Data:', data);
                    alert('Ευχαριστούμε! Θα επικοινωνήσουμε σύντομα.');
                    this.reset();
                });
            }

            // ================= GALLERY LIGHTBOX ================= 
            const galleryBtns = document.querySelectorAll('.gallery-btn');

            galleryBtns.forEach((btn, index) => {
                btn.addEventListener('click', function (e) {
                    e.preventDefault();
                    const imgElement = this.closest('.gallery-item').querySelector('img');
                    const imgSrc = imgElement.src;
                    const imgAlt = imgElement.alt;
                    createLightbox(imgSrc, imgAlt);
                });
            });

            function createLightbox(imgSrc, imgAlt) {
                // Remove existing lightbox
                const existingLightbox = document.querySelector('.lightbox');
                if (existingLightbox) {
                    existingLightbox.remove();
                }

                const lightbox = document.createElement('div');
                lightbox.className = 'lightbox';
                lightbox.innerHTML = `
                    <div class="lightbox-content">
                        <span class="lightbox-close">&times;</span>
                        <img src="${imgSrc}" alt="${imgAlt}">
                    </div>
                `;

                document.body.appendChild(lightbox);

                // Close lightbox
                const closeBtn = lightbox.querySelector('.lightbox-close');
                closeBtn.addEventListener('click', function () {
                    lightbox.remove();
                });

                lightbox.addEventListener('click', function (e) {
                    if (e.target === this) {
                        lightbox.remove();
                    }
                });

                // Close on escape key
                document.addEventListener('keydown', function (e) {
                    if (e.key === 'Escape') {
                        lightbox.remove();
                    }
                });
            }

            // ================= SCROLL ANIMATIONS ================= 
            const scrollElements = document.querySelectorAll('.service-card, .gallery-item, .why-card, .testimonial');

            const scrollObserver = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = 'fadeInUp 0.6s ease forwards';
                        scrollObserver.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });

            scrollElements.forEach(el => scrollObserver.observe(el));

        });
    </script>

</body>

</html>
