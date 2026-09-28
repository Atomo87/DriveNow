<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DriveNow | Aluguel de Carros Premium - Reserve em 2 Minutos</title>
  <meta name="description" content="Aluguel de carros premium com seguro incluso, entrega grátis e suporte 24h. Frota nova, preços imbatíveis e reserva em 2 minutos.">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }

    :root {
      --primary: #0066FF;
      --primary-dark: #0052CC;
      --primary-light: #E6F0FF;
      --accent: #00D9A3;
      --dark: #0A0E1A;
      --dark-2: #131824;
      --gray: #64748B;
      --gray-light: #F1F5F9;
      --white: #FFFFFF;
      --gold: #FFB800;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Plus Jakarta Sans', sans-serif;
      background: var(--white);
      color: var(--dark);
      overflow-x: hidden;
      line-height: 1.6;
    }

    /* ============ TOP BAR ============ */
    .topbar {
      background: var(--dark);
      color: white;
      padding: 0.6rem 5%;
      font-size: 0.82rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-weight: 500;
    }

    .topbar-left, .topbar-right {
      display: flex;
      align-items: center;
      gap: 1.8rem;
    }

    .topbar i { color: var(--accent); margin-right: 0.4rem; }
    .topbar span { opacity: 0.9; }

    /* ============ HEADER ============ */
    header {
      position: sticky;
      top: 0;
      background: rgba(255, 255, 255, 0.98);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid rgba(0, 0, 0, 0.06);
      z-index: 900;
      padding: 1rem 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: all 0.3s;
    }

    .logo {
      font-size: 1.6rem;
      font-weight: 800;
      color: var(--dark);
      display: flex;
      align-items: center;
      gap: 0.5rem;
      letter-spacing: -0.5px;
    }

    .logo-icon {
      width: 40px;
      height: 40px;
      background: linear-gradient(135deg, var(--primary) 0%, var(--accent) 100%);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 1.2rem;
      box-shadow: 0 8px 16px -4px rgba(0, 102, 255, 0.4);
    }

    .logo span { color: var(--primary); }

    nav ul {
      display: flex;
      gap: 2.2rem;
      list-style: none;
      align-items: center;
    }

    nav a {
      text-decoration: none;
      color: var(--dark);
      font-weight: 600;
      font-size: 0.95rem;
      transition: color 0.2s;
      position: relative;
    }

    nav a:hover { color: var(--primary); }

    .header-cta {
      display: flex;
      gap: 0.8rem;
      align-items: center;
    }

    .btn-ghost {
      background: transparent;
      border: 1.5px solid var(--gray-light);
      padding: 0.7rem 1.4rem;
      border-radius: 10px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      transition: all 0.2s;
      color: var(--dark);
      text-decoration: none;
    }

    .btn-ghost:hover { border-color: var(--primary); color: var(--primary); }

    .btn-solid {
      background: var(--primary);
      color: white;
      padding: 0.75rem 1.5rem;
      border-radius: 10px;
      font-weight: 700;
      font-size: 0.9rem;
      text-decoration: none;
      border: none;
      cursor: pointer;
      transition: all 0.3s;
      box-shadow: 0 8px 20px -6px rgba(0, 102, 255, 0.5);
    }

    .btn-solid:hover {
      background: var(--primary-dark);
      transform: translateY(-2px);
      box-shadow: 0 12px 24px -6px rgba(0, 102, 255, 0.6);
    }

    /* ============ HERO ============ */
    .hero {
      position: relative;
      padding: 5rem 5% 6rem;
      background: linear-gradient(180deg, #F8FAFF 0%, #FFFFFF 100%);
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: -200px;
      right: -200px;
      width: 600px;
      height: 600px;
      background: radial-gradient(circle, rgba(0, 102, 255, 0.1) 0%, transparent 70%);
      border-radius: 50%;
    }

    .hero::after {
      content: '';
      position: absolute;
      bottom: -300px;
      left: -200px;
      width: 700px;
      height: 700px;
      background: radial-gradient(circle, rgba(0, 217, 163, 0.08) 0%, transparent 70%);
      border-radius: 50%;
    }

    .hero-inner {
      max-width: 1300px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: 1.15fr 1fr;
      gap: 4rem;
      align-items: center;
      position: relative;
      z-index: 1;
    }

    .badge-hero {
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      background: white;
      border: 1px solid rgba(0, 102, 255, 0.15);
      padding: 0.5rem 1rem;
      border-radius: 50px;
      font-size: 0.85rem;
      font-weight: 600;
      color: var(--dark);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.04);
      margin-bottom: 1.5rem;
    }

    .badge-hero .stars { color: var(--gold); }
    .badge-hero strong { color: var(--primary); }

    .hero h1 {
      font-size: 3.6rem;
      font-weight: 800;
      line-height: 1.08;
      letter-spacing: -2px;
      color: var(--dark);
      margin-bottom: 1.5rem;
    }

    .hero h1 .highlight {
      background: linear-gradient(135deg, var(--primary) 0%, var(--accent) 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .hero p.lead {
      font-size: 1.2rem;
      color: var(--gray);
      margin-bottom: 2rem;
      max-width: 540px;
      line-height: 1.6;
    }

    .hero-features {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      margin-bottom: 2.5rem;
    }

    .feature-check {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      font-size: 0.95rem;
      font-weight: 600;
      color: var(--dark);
    }

    .feature-check i {
      width: 22px;
      height: 22px;
      background: var(--accent);
      color: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.7rem;
    }

    .hero-social {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      padding-top: 1.5rem;
      border-top: 1px solid var(--gray-light);
    }

    .avatars {
      display: flex;
    }

    .avatars img {
      width: 42px;
      height: 42px;
      border-radius: 50%;
      border: 3px solid white;
      object-fit: cover;
      margin-left: -12px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    .avatars img:first-child { margin-left: 0; }

    .hero-social-text {
      font-size: 0.9rem;
      color: var(--gray);
      line-height: 1.3;
    }

    .hero-social-text strong {
      display: block;
      color: var(--dark);
      font-size: 1rem;
    }

    /* ============ RESERVA CARD ============ */
    .reserva-card {
      background: white;
      border-radius: 24px;
      padding: 2rem;
      box-shadow: 0 30px 60px -20px rgba(10, 14, 26, 0.25);
      border: 1px solid rgba(0, 0, 0, 0.04);
      position: relative;
      overflow: hidden;
    }

    .reserva-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: linear-gradient(90deg, var(--primary), var(--accent));
    }

    .reserva-header {
      margin-bottom: 1.5rem;
    }

    .reserva-header h3 {
      font-size: 1.4rem;
      font-weight: 800;
      color: var(--dark);
      margin-bottom: 0.3rem;
      letter-spacing: -0.5px;
    }

    .reserva-header p {
      color: var(--gray);
      font-size: 0.88rem;
    }

    .input-group {
      margin-bottom: 1rem;
    }

    .input-group label {
      display: block;
      font-size: 0.82rem;
      font-weight: 700;
      color: var(--dark);
      margin-bottom: 0.5rem;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .input-wrapper {
      position: relative;
    }

    .input-wrapper i {
      position: absolute;
      left: 1rem;
      top: 50%;
      transform: translateY(-50%);
      color: var(--gray);
      font-size: 0.9rem;
    }

    .input-group input, .input-group select {
      width: 100%;
      padding: 0.95rem 1rem 0.95rem 2.8rem;
      border: 1.5px solid #E2E8F0;
      border-radius: 12px;
      font-size: 0.95rem;
      font-family: inherit;
      font-weight: 500;
      transition: all 0.2s;
      background: #FAFBFC;
      color: var(--dark);
    }

    .input-group input:focus, .input-group select:focus {
      outline: none;
      border-color: var(--primary);
      background: white;
      box-shadow: 0 0 0 4px rgba(0, 102, 255, 0.1);
    }

    .row-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 0.8rem;
    }

    .btn-reservar {
      width: 100%;
      padding: 1.1rem;
      background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
      color: white;
      border: none;
      border-radius: 12px;
      font-size: 1rem;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.3s;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.6rem;
      margin-top: 0.5rem;
      font-family: inherit;
      letter-spacing: 0.3px;
      box-shadow: 0 10px 24px -8px rgba(0, 102, 255, 0.6);
    }

    .btn-reservar:hover {
      transform: translateY(-2px);
      box-shadow: 0 15px 30px -8px rgba(0, 102, 255, 0.7);
    }

    .reserva-trust {
      display: flex;
      justify-content: center;
      gap: 1.2rem;
      margin-top: 1.2rem;
      padding-top: 1.2rem;
      border-top: 1px dashed #E2E8F0;
      font-size: 0.78rem;
      color: var(--gray);
      font-weight: 500;
    }

    .reserva-trust i { color: var(--accent); margin-right: 0.3rem; }

    /* ============ MARCAS ============ */
    .marcas {
      padding: 3rem 5%;
      background: white;
      border-top: 1px solid var(--gray-light);
      border-bottom: 1px solid var(--gray-light);
    }

    .marcas-inner {
      max-width: 1200px;
      margin: 0 auto;
      text-align: center;
    }

    .marcas p {
      font-size: 0.85rem;
      font-weight: 600;
      color: var(--gray);
      text-transform: uppercase;
      letter-spacing: 1.5px;
      margin-bottom: 1.5rem;
    }

    .marcas-logos {
      display: flex;
      justify-content: space-around;
      align-items: center;
      flex-wrap: wrap;
      gap: 2rem;
      opacity: 0.7;
    }

    .marcas-logos span {
      font-size: 1.6rem;
      font-weight: 800;
      color: var(--dark);
      letter-spacing: -0.5px;
      transition: all 0.3s;
      cursor: default;
    }

    .marcas-logos span:hover {
      opacity: 1;
      color: var(--primary);
      transform: scale(1.05);
    }

    /* ============ SEÇÕES ============ */
    section {
      padding: 6rem 5%;
    }

    .container {
      max-width: 1300px;
      margin: 0 auto;
    }

    .section-head {
      text-align: center;
      max-width: 700px;
      margin: 0 auto 4rem;
    }

    .section-tag {
      display: inline-block;
      background: var(--primary-light);
      color: var(--primary);
      padding: 0.4rem 1rem;
      border-radius: 50px;
      font-size: 0.8rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 1rem;
    }

    .section-head h2 {
      font-size: 2.8rem;
      font-weight: 800;
      letter-spacing: -1.5px;
      line-height: 1.15;
      margin-bottom: 1rem;
      color: var(--dark);
    }

    .section-head p {
      font-size: 1.1rem;
      color: var(--gray);
    }

    /* ============ FROTA ============ */
    #frota { background: #F8FAFF; }

    .frota-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1.8rem;
    }

    .car-card {
      background: white;
      border-radius: 20px;
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      border: 1px solid rgba(0, 0, 0, 0.05);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
      position: relative;
    }

    .car-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 30px 50px -15px rgba(10, 14, 26, 0.2);
    }

    .car-img {
      position: relative;
      height: 200px;
      overflow: hidden;
      background: #E2E8F0;
    }

    .car-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s;
    }

    .car-card:hover .car-img img {
      transform: scale(1.08);
    }

    .car-tag {
      position: absolute;
      top: 1rem;
      left: 1rem;
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(10px);
      color: var(--dark);
      padding: 0.35rem 0.8rem;
      border-radius: 50px;
      font-size: 0.75rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .car-tag.promo {
      background: var(--accent);
      color: white;
    }

    .car-fav {
      position: absolute;
      top: 1rem;
      right: 1rem;
      width: 36px;
      height: 36px;
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(10px);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--gray);
      cursor: pointer;
      transition: all 0.2s;
      border: none;
    }

    .car-fav:hover { color: #EF4444; transform: scale(1.1); }

    .car-body { padding: 1.5rem; }

    .car-title-row {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 0.8rem;
    }

    .car-title-row h3 {
      font-size: 1.25rem;
      font-weight: 800;
      color: var(--dark);
      letter-spacing: -0.3px;
    }

    .car-title-row .categoria {
      display: block;
      font-size: 0.82rem;
      color: var(--gray);
      font-weight: 500;
      margin-top: 0.2rem;
    }

    .rating {
      display: flex;
      align-items: center;
      gap: 0.3rem;
      font-size: 0.82rem;
      font-weight: 700;
      color: var(--dark);
      background: #FFFBEB;
      padding: 0.3rem 0.6rem;
      border-radius: 8px;
    }

    .rating i { color: var(--gold); font-size: 0.75rem; }

    .car-specs {
      display: flex;
      gap: 1.2rem;
      padding: 0.8rem 0;
      border-top: 1px solid var(--gray-light);
      border-bottom: 1px solid var(--gray-light);
      margin-bottom: 1rem;
    }

    .spec {
      display: flex;
      align-items: center;
      gap: 0.4rem;
      font-size: 0.8rem;
      color: var(--gray);
      font-weight: 600;
    }

    .spec i { color: var(--primary); }

    .car-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .price-box .old-price {
      font-size: 0.78rem;
      color: var(--gray);
      text-decoration: line-through;
      display: block;
    }

    .price-box .price {
      font-size: 1.6rem;
      font-weight: 800;
      color: var(--dark);
      letter-spacing: -1px;
      line-height: 1;
    }

    .price-box .price small {
      font-size: 0.75rem;
      color: var(--gray);
      font-weight: 500;
      letter-spacing: 0;
    }

    .btn-car {
      background: var(--dark);
      color: white;
      border: none;
      padding: 0.75rem 1.3rem;
      border-radius: 10px;
      font-weight: 700;
      font-size: 0.85rem;
      cursor: pointer;
      transition: all 0.2s;
      font-family: inherit;
    }

    .btn-car:hover {
      background: var(--primary);
      transform: translateY(-2px);
      box-shadow: 0 8px 16px -4px rgba(0, 102, 255, 0.4);
    }

    /* ============ BENEFÍCIOS ============ */
    .beneficios-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }

    .benefit-card {
      padding: 2rem;
      background: white;
      border: 1px solid var(--gray-light);
      border-radius: 20px;
      transition: all 0.3s;
      position: relative;
      overflow: hidden;
    }

    .benefit-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 3px;
      background: linear-gradient(90deg, var(--primary), var(--accent));
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.4s;
    }

    .benefit-card:hover::before { transform: scaleX(1); }

    .benefit-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 25px 40px -15px rgba(10, 14, 26, 0.12);
      border-color: transparent;
    }

    .benefit-icon {
      width: 56px;
      height: 56px;
      background: linear-gradient(135deg, var(--primary-light) 0%, #F0F9FF 100%);
      border-radius: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--primary);
      font-size: 1.5rem;
      margin-bottom: 1.2rem;
    }

    .benefit-card h4 {
      font-size: 1.15rem;
      font-weight: 800;
      margin-bottom: 0.5rem;
      color: var(--dark);
      letter-spacing: -0.3px;
    }

    .benefit-card p {
      color: var(--gray);
      font-size: 0.92rem;
      line-height: 1.6;
    }

    /* ============ COMO FUNCIONA ============ */
    #como-funciona { background: var(--dark); color: white; }
    #como-funciona .section-head h2 { color: white; }
    #como-funciona .section-head p { color: rgba(255,255,255,0.7); }
    #como-funciona .section-tag { background: rgba(0, 217, 163, 0.15); color: var(--accent); }

    .steps-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 2rem;
      position: relative;
    }

    .step-card {
      text-align: center;
      padding: 2rem 1rem;
      position: relative;
    }

    .step-num {
      width: 70px;
      height: 70px;
      margin: 0 auto 1.5rem;
      background: linear-gradient(135deg, var(--primary), var(--accent));
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.6rem;
      font-weight: 800;
      color: white;
      box-shadow: 0 15px 30px -8px rgba(0, 102, 255, 0.5);
      position: relative;
    }

    .step-card h4 {
      font-size: 1.15rem;
      font-weight: 700;
      margin-bottom: 0.6rem;
      color: white;
    }

    .step-card p {
      color: rgba(255, 255, 255, 0.7);
      font-size: 0.9rem;
    }

    /* ============ DEPOIMENTOS ============ */
    #depoimentos { background: #F8FAFF; }

    .testimonials-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1.5rem;
    }

    .testimonial {
      background: white;
      padding: 2rem;
      border-radius: 20px;
      border: 1px solid rgba(0, 0, 0, 0.05);
      transition: all 0.3s;
    }

    .testimonial:hover {
      transform: translateY(-5px);
      box-shadow: 0 20px 40px -15px rgba(10, 14, 26, 0.12);
    }

    .stars-row {
      color: var(--gold);
      margin-bottom: 1rem;
      font-size: 0.95rem;
    }

    .testimonial p {
      color: var(--dark);
      font-size: 0.98rem;
      line-height: 1.7;
      margin-bottom: 1.5rem;
      font-weight: 500;
    }

    .testimonial-author {
      display: flex;
      align-items: center;
      gap: 0.9rem;
      padding-top: 1.2rem;
      border-top: 1px solid var(--gray-light);
    }

    .testimonial-author img {
      width: 48px;
      height: 48px;
      border-radius: 50%;
      object-fit: cover;
    }

    .testimonial-author strong {
      display: block;
      color: var(--dark);
      font-size: 0.95rem;
    }

    .testimonial-author span {
      color: var(--gray);
      font-size: 0.82rem;
    }

    /* ============ CTA FINAL ============ */
    .cta-final {
      background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
      border-radius: 32px;
      padding: 4rem 3rem;
      text-align: center;
      color: white;
      position: relative;
      overflow: hidden;
      max-width: 1200px;
      margin: 0 auto;
    }

    .cta-final::before {
      content: '';
      position: absolute;
      top: -100px;
      right: -100px;
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, rgba(0, 217, 163, 0.3) 0%, transparent 70%);
      border-radius: 50%;
    }

    .cta-final::after {
      content: '';
      position: absolute;
      bottom: -150px;
      left: -100px;
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 0%, transparent 70%);
      border-radius: 50%;
    }

    .cta-final > * { position: relative; z-index: 1; }

    .cta-final h2 {
      font-size: 2.6rem;
      font-weight: 800;
      letter-spacing: -1.5px;
      margin-bottom: 1rem;
      line-height: 1.15;
    }

    .cta-final p {
      font-size: 1.15rem;
      opacity: 0.92;
      margin-bottom: 2rem;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
    }

    .cta-buttons {
      display: flex;
      gap: 1rem;
      justify-content: center;
      flex-wrap: wrap;
    }

    .btn-white {
      background: white;
      color: var(--primary);
      padding: 1.1rem 2.2rem;
      border-radius: 12px;
      font-weight: 700;
      font-size: 1rem;
      text-decoration: none;
      border: none;
      cursor: pointer;
      transition: all 0.3s;
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      font-family: inherit;
      box-shadow: 0 10px 30px -10px rgba(0, 0, 0, 0.3);
    }

    .btn-white:hover { transform: translateY(-3px); box-shadow: 0 15px 35px -10px rgba(0, 0, 0, 0.4); }

    .btn-outline-white {
      background: transparent;
      color: white;
      border: 2px solid rgba(255, 255, 255, 0.4);
      padding: 1.1rem 2.2rem;
      border-radius: 12px;
      font-weight: 700;
      font-size: 1rem;
      cursor: pointer;
      transition: all 0.3s;
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      font-family: inherit;
    }

    .btn-outline-white:hover {
      background: rgba(255, 255, 255, 0.1);
      border-color: white;
    }

    /* ============ FOOTER ============ */
    footer {
      background: var(--dark-2);
      color: #94A3B8;
      padding: 4rem 5% 2rem;
    }

    .footer-grid {
      max-width: 1300px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: 2fr 1fr 1fr 1fr;
      gap: 3rem;
      padding-bottom: 3rem;
      border-bottom: 1px solid rgba(255, 255, 255, 0.08);
    }

    .footer-brand .logo { color: white; margin-bottom: 1rem; }
    .footer-brand p { font-size: 0.9rem; line-height: 1.7; max-width: 320px; margin-bottom: 1.5rem; }

    .social-links { display: flex; gap: 0.7rem; }

    .social-links a {
      width: 40px;
      height: 40px;
      background: rgba(255, 255, 255, 0.06);
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      text-decoration: none;
      transition: all 0.2s;
    }

    .social-links a:hover {
      background: var(--primary);
      transform: translateY(-3px);
    }

    .footer-col h5 {
      color: white;
      font-size: 1rem;
      margin-bottom: 1.2rem;
      font-weight: 700;
    }

    .footer-col a, .footer-col p {
      display: block;
      color: #94A3B8;
      text-decoration: none;
      margin-bottom: 0.7rem;
      font-size: 0.9rem;
      transition: color 0.2s;
    }

    .footer-col a:hover { color: var(--accent); }

    .footer-bottom {
      max-width: 1300px;
      margin: 2rem auto 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 1rem;
      font-size: 0.85rem;
    }

    .payment-methods {
      display: flex;
      gap: 1rem;
      align-items: center;
    }

    .payment-methods i {
      font-size: 1.5rem;
      opacity: 0.6;
      transition: opacity 0.2s;
    }

    .payment-methods i:hover { opacity: 1; }

    /* ============ CHATBOT ============ */
    .chatbot-window {
      position: fixed;
      bottom: 100px;
      right: 25px;
      width: 380px;
      max-width: calc(100vw - 40px);
      height: 550px;
      max-height: calc(100vh - 140px);
      background: white;
      border-radius: 24px;
      box-shadow: 0 30px 70px -15px rgba(10, 14, 26, 0.4);
      display: none;
      flex-direction: column;
      overflow: hidden;
      z-index: 1100;
      animation: slideUp 0.3s ease-out;
    }

    @keyframes slideUp {
      from { opacity: 0; transform: translateY(20px) scale(0.95); }
      to { opacity: 1; transform: translateY(0) scale(1); }
    }

    .chatbot-window.open { display: flex; }

    .chat-header {
      background: linear-gradient(135deg, var(--dark) 0%, var(--dark-2) 100%);
      color: white;
      padding: 1.2rem 1.4rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .chat-header-info {
      display: flex;
      align-items: center;
      gap: 0.8rem;
    }

    .chat-avatar {
      width: 42px;
      height: 42px;
      background: linear-gradient(135deg, var(--primary), var(--accent));
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      position: relative;
    }

    .chat-avatar::after {
      content: '';
      position: absolute;
      bottom: 0;
      right: 0;
      width: 12px;
      height: 12px;
      background: var(--accent);
      border-radius: 50%;
      border: 2px solid var(--dark);
    }

    .chat-header-info h4 {
      font-size: 0.95rem;
      font-weight: 700;
      margin-bottom: 0.15rem;
    }

    .chat-header-info span {
      font-size: 0.75rem;
      color: var(--accent);
      display: flex;
      align-items: center;
      gap: 0.3rem;
    }

    .chat-header-info span::before {
      content: '';
      width: 6px;
      height: 6px;
      background: var(--accent);
      border-radius: 50%;
      animation: pulse 1.5s infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.4; }
    }

    .chat-close {
      background: rgba(255, 255, 255, 0.1);
      border: none;
      color: white;
      width: 32px;
      height: 32px;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.2s;
      font-size: 0.9rem;
    }

    .chat-close:hover { background: rgba(255, 255, 255, 0.2); }

    .chat-messages {
      flex: 1;
      padding: 1.2rem;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      background: #F8FAFF;
    }

    .msg {
      max-width: 82%;
      padding: 0.85rem 1.1rem;
      border-radius: 16px;
      font-size: 0.9rem;
      line-height: 1.5;
      animation: msgIn 0.3s ease-out;
      font-weight: 500;
    }

    @keyframes msgIn {
      from { opacity: 0; transform: translateY(8px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .msg.bot {
      background: white;
      align-self: flex-start;
      border-bottom-left-radius: 4px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
      color: var(--dark);
    }

    .msg.user {
      background: var(--primary);
      color: white;
      align-self: flex-end;
      border-bottom-right-radius: 4px;
      box-shadow: 0 4px 12px -2px rgba(0, 102, 255, 0.4);
    }

    .quick-replies {
      display: flex;
      gap: 0.4rem;
      flex-wrap: wrap;
      margin-top: 0.5rem;
    }

    .quick-reply {
      background: white;
      border: 1.5px solid var(--primary-light);
      color: var(--primary);
      padding: 0.4rem 0.8rem;
      border-radius: 50px;
      font-size: 0.78rem;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.2s;
      font-family: inherit;
    }

    .quick-reply:hover {
      background: var(--primary);
      color: white;
      border-color: var(--primary);
    }

    .chat-input-area {
      padding: 1rem;
      background: white;
      border-top: 1px solid var(--gray-light);
      display: flex;
      gap: 0.6rem;
    }

    .chat-input-area input {
      flex: 1;
      padding: 0.85rem 1.1rem;
      border: 1.5px solid var(--gray-light);
      border-radius: 50px;
      font-size: 0.9rem;
      outline: none;
      font-family: inherit;
      transition: all 0.2s;
      background: #F8FAFF;
    }

    .chat-input-area input:focus {
      border-color: var(--primary);
      background: white;
    }

    .chat-send {
      width: 46px;
      height: 46px;
      background: linear-gradient(135deg, var(--primary), var(--primary-dark));
      color: white;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      transition: all 0.2s;
      font-size: 0.95rem;
      flex-shrink: 0;
      box-shadow: 0 6px 15px -4px rgba(0, 102, 255, 0.5);
    }

    .chat-send:hover { transform: scale(1.08); }

    /* ============ FLOATING BUTTONS ============ */
    .floating-actions {
      position: fixed;
      bottom: 25px;
      right: 25px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      z-index: 1200;
    }

    .float-btn {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      border: none;
      color: white;
      font-size: 1.6rem;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.3s;
      position: relative;
      box-shadow: 0 12px 25px -5px rgba(0, 0, 0, 0.3);
    }

    .float-btn:hover { transform: scale(1.1); }

    .float-btn.whatsapp {
      background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);
      animation: whatsappPulse 2s infinite;
    }

    @keyframes whatsappPulse {
      0%, 100% { box-shadow: 0 12px 25px -5px rgba(37, 211, 102, 0.5); }
      50% { box-shadow: 0 12px 25px -5px rgba(37, 211, 102, 0.9), 0 0 0 10px rgba(37, 211, 102, 0.15); }
    }

    .float-btn.chat {
      background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
    }

    .float-btn .notif {
      position: absolute;
      top: -4px;
      right: -4px;
      background: #EF4444;
      color: white;
      width: 22px;
      height: 22px;
      border-radius: 50%;
      font-size: 0.7rem;
      font-weight: 700;
      display: flex;
      align-items: center;
      justify-content: center;
      border: 2px solid white;
    }

    /* ============ RESPONSIVE ============ */
    @media (max-width: 1024px) {
      .hero-inner { grid-template-columns: 1fr; gap: 3rem; }
      .hero h1 { font-size: 2.8rem; }
      .footer-grid { grid-template-columns: 1fr 1fr; }
      nav ul { display: none; }
    }

    @media (max-width: 640px) {
      .topbar { display: none; }
      .hero { padding: 3rem 5% 4rem; }
      .hero h1 { font-size: 2.1rem; letter-spacing: -1px; }
      .hero p.lead { font-size: 1rem; }
      section { padding: 4rem 5%; }
      .section-head h2 { font-size: 1.9rem; letter-spacing: -0.8px; }
      .cta-final { padding: 2.5rem 1.5rem; }
      .cta-final h2 { font-size: 1.7rem; }
      .footer-grid { grid-template-columns: 1fr; gap: 2rem; }
      .header-cta .btn-ghost { display: none; }
      .logo { font-size: 1.3rem; }
      .chatbot-window { bottom: 90px; right: 12px; width: calc(100vw - 24px); height: calc(100vh - 120px); }
      .row-2 { grid-template-columns: 1fr; }
      .footer-bottom { flex-direction: column; text-align: center; }
    }
  </style>
</head>
<body>

  <!-- TOPBAR -->
  <div class="topbar">
    <div class="topbar-left">
      <span><i class="fas fa-map-marker-alt"></i> Atendemos toda Grande São Paulo</span>
      <span><i class="fas fa-clock"></i> Suporte 24h</span>
    </div>
    <div class="topbar-right">
      <span><i class="fas fa-phone"></i> (11) 4000-1234</span>
      <span><i class="fas fa-shield-alt"></i> Pagamento 100% seguro</span>
    </div>
  </div>

  <!-- HEADER -->
  <header>
    <div class="logo">
      <div class="logo-icon"><i class="fas fa-car-side"></i></div>
      Drive<span>Now</span>
    </div>
    <nav>
      <ul>
        <li><a href="#frota">Frota</a></li>
        <li><a href="#beneficios">Vantagens</a></li>
        <li><a href="#como-funciona">Como funciona</a></li>
        <li><a href="#depoimentos">Avaliações</a></li>
      </ul>
    </nav>
    <div class="header-cta">
      <a href="tel:+551140001234" class="btn-ghost"><i class="fas fa-phone"></i> Ligar</a>
      <a href="#reserva" class="btn-solid">Reservar agora</a>
    </div>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-inner">
      <div class="hero-content">
        <div class="badge-hero">
          <span class="stars">
            <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
          </span>
          <strong>4.9/5</strong> · +2.500 clientes satisfeitos
        </div>
        <h1>
          Alugue o carro <span class="highlight">perfeito</span> em menos de 2 minutos
        </h1>
        <p class="lead">
          Frota premium, seguro completo incluso e entrega grátis em toda Grande São Paulo. Sem burocracia, sem taxas escondidas.
        </p>
        <div class="hero-features">
          <div class="feature-check"><i class="fas fa-check"></i> Sem caução</div>
          <div class="feature-check"><i class="fas fa-check"></i> Cancelamento grátis</div>
          <div class="feature-check"><i class="fas fa-check"></i> Entrega grátis</div>
        </div>
        <div class="hero-social">
          <div class="avatars">
            <img src="https://i.pravatar.cc/80?img=12" alt="Cliente">
            <img src="https://i.pravatar.cc/80?img=32" alt="Cliente">
            <img src="https://i.pravatar.cc/80?img=45" alt="Cliente">
            <img src="https://i.pravatar.cc/80?img=68" alt="Cliente">
          </div>
          <div class="hero-social-text">
            <strong>+2.500 clientes</strong>
            alugaram este mês
          </div>
        </div>
      </div>

      <!-- CARD RESERVA -->
      <div class="reserva-card" id="reserva">
        <div class="reserva-header">
          <h3>Faça sua reserva</h3>
          <p>Preencha e receba as melhores ofertas</p>
        </div>
        <div class="input-group">
          <label>Local de retirada</label>
          <div class="input-wrapper">
            <i class="fas fa-map-marker-alt"></i>
            <input type="text" placeholder="Aeroporto, hotel ou endereço" value="São Paulo - SP">
          </div>
        </div>
        <div class="row-2">
          <div class="input-group">
            <label>Retirada</label>
            <div class="input-wrapper">
              <i class="fas fa-calendar"></i>
              <input type="date" id="dataRetirada">
            </div>
          </div>
          <div class="input-group">
            <label>Devolução</label>
            <div class="input-wrapper">
              <i class="fas fa-calendar"></i>
              <input type="date" id="dataDevolucao">
            </div>
          </div>
        </div>
        <div class="input-group">
          <label>Categoria do veículo</label>
          <div class="input-wrapper">
            <i class="fas fa-car"></i>
            <select>
              <option>Escolha uma categoria</option>
              <option>Econômico — a partir de R$ 89/dia</option>
              <option>Sedan — a partir de R$ 159/dia</option>
              <option>SUV — a partir de R$ 189/dia</option>
              <option>Executivo — a partir de R$ 399/dia</option>
            </select>
          </div>
        </div>
        <button class="btn-reservar" onclick="abrirChat()">
          <i class="fas fa-search"></i> Ver carros disponíveis
        </button>
        <div class="reserva-trust">
          <span><i class="fas fa-lock"></i> Dados seguros</span>
          <span><i class="fas fa-check-circle"></i> Sem taxa</span>
          <span><i class="fas fa-bolt"></i> Resposta em 1min</span>
        </div>
      </div>
    </div>
  </section>

  <!-- MARCAS -->
  <div class="marcas">
    <div class="marcas-inner">
      <p>Trabalhamos com as melhores marcas do mercado</p>
      <div class="marcas-logos">
        <span>TOYOTA</span>
        <span>HONDA</span>
        <span>JEEP</span>
        <span>VOLKSWAGEN</span>
        <span>CHEVROLET</span>
        <span>BMW</span>
      </div>
    </div>
  </div>

  <!-- FROTA -->
  <section id="frota">
    <div class="container">
      <div class="section-head">
        <span class="section-tag">Nossa frota</span>
        <h2>Escolha o carro ideal para sua viagem</h2>
        <p>Todos os veículos com seguro completo, revisão em dia e menos de 2 anos de uso</p>
      </div>
      <div class="frota-grid">
        <!-- CAR 1 -->
        <div class="car-card">
          <div class="car-img">
            <img src="https://images.unsplash.com/photo-1549317661-bd32c8ce0db2?w=600&h=400&fit=crop" alt="Fiat Argo">
            <span class="car-tag promo">🔥 Mais alugado</span>
            <button class="car-fav"><i class="far fa-heart"></i></button>
          </div>
          <div class="car-body">
            <div class="car-title-row">
              <div>
                <h3>Fiat Argo</h3>
                <span class="categoria">Econômico · 5 lugares</span>
              </div>
              <div class="rating"><i class="fas fa-star"></i> 4.9</div>
            </div>
            <div class="car-specs">
              <span class="spec"><i class="fas fa-gas-pump"></i> Flex</span>
              <span class="spec"><i class="fas fa-cog"></i> Automático</span>
              <span class="spec"><i class="fas fa-snowflake"></i> Ar-cond.</span>
            </div>
            <div class="car-footer">
              <div class="price-box">
                <span class="old-price">R$ 129</span>
                <span class="price">R$ 89<small>/dia</small></span>
              </div>
              <button class="btn-car" onclick="abrirChat()">Reservar</button>
            </div>
          </div>
        </div>

        <!-- CAR 2 -->
        <div class="car-card">
          <div class="car-img">
            <img src="https://images.unsplash.com/photo-1552519507-da3b142c6e3d?w=600&h=400&fit=crop" alt="Jeep Compass">
            <span class="car-tag">SUV</span>
            <button class="car-fav"><i class="far fa-heart"></i></button>
          </div>
          <div class="car-body">
            <div class="car-title-row">
              <div>
                <h3>Jeep Compass</h3>
                <span class="categoria">SUV · 5 lugares</span>
              </div>
              <div class="rating"><i class="fas fa-star"></i> 4.8</div>
            </div>
            <div class="car-specs">
              <span class="spec"><i class="fas fa-gas-pump"></i> Diesel</span>
              <span class="spec"><i class="fas fa-cog"></i> Automático</span>
              <span class="spec"><i class="fas fa-snowflake"></i> Ar-cond.</span>
            </div>
            <div class="car-footer">
              <div class="price-box">
                <span class="old-price">R$ 249</span>
                <span class="price">R$ 189<small>/dia</small></span>
              </div>
              <button class="btn-car" onclick="abrirChat()">Reservar</button>
            </div>
          </div>
        </div>

        <!-- CAR 3 -->
        <div class="car-card">
          <div class="car-img">
            <img src="https://images.unsplash.com/photo-1580273916550-e323be2ae537?w=600&h=400&fit=crop" alt="Toyota Corolla">
            <span class="car-tag promo">🏆 Escolha dos clientes</span>
            <button class="car-fav"><i class="far fa-heart"></i></button>
          </div>
          <div class="car-body">
            <div class="car-title-row">
              <div>
                <h3>Toyota Corolla</h3>
                <span class="categoria">Sedan · 5 lugares</span>
              </div>
              <div class="rating"><i class="fas fa-star"></i> 5.0</div>
            </div>
            <div class="car-specs">
              <span class="spec"><i class="fas fa-gas-pump"></i> Flex</span>
              <span class="spec"><i class="fas fa-cog"></i> Automático</span>
              <span class="spec"><i class="fas fa-snowflake"></i> Ar-cond.</span>
            </div>
            <div class="car-footer">
              <div class="price-box">
                <span class="old-price">R$ 199</span>
                <span class="price">R$ 159<small>/dia</small></span>
              </div>
              <button class="btn-car" onclick="abrirChat()">Reservar</button>
            </div>
          </div>
        </div>

        <!-- CAR 4 -->
        <div class="car-card">
          <div class="car-img">
            <img src="https://images.unsplash.com/photo-1605559424843-9e4c228bf1c2?w=600&h=400&fit=crop" alt="BMW Série 3">
            <span class="car-tag promo">⭐ Premium</span>
            <button class="car-fav"><i class="far fa-heart"></i></button>
          </div>
          <div class="car-body">
            <div class="car-title-row">
              <div>
                <h3>BMW Série 3</h3>
                <span class="categoria">Executivo · 5 lugares</span>
              </div>
              <div class="rating"><i class="fas fa-star"></i> 5.0</div>
            </div>
            <div class="car-specs">
              <span class="spec"><i class="fas fa-gas-pump"></i> Gasolina</span>
              <span class="spec"><i class="fas fa-cog"></i> Automático</span>
              <span class="spec"><i class="fas fa-snowflake"></i> Ar-cond.</span>
            </div>
            <div class="car-footer">
              <div class="price-box">
                <span class="old-price">R$ 499</span>
                <span class="price">R$ 399<small>/dia</small></span>
              </div>
              <button class="btn-car" onclick="abrirChat()">Reservar</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- BENEFÍCIOS -->
  <section id="beneficios">
    <div class="container">
      <div class="section-head">
        <span class="section-tag">Por que a DriveNow</span>
        <h2>Vantagens que fazem a diferença</h2>
        <p>Tudo que você precisa para uma experiência tranquila, sem surpresas</p>
      </div>
      <div class="beneficios-grid">
        <div class="benefit-card">
          <div class="benefit-icon"><i class="fas fa-shield-alt"></i></div>
          <h4>Seguro completo incluso</h4>
          <p>Proteção total contra roubo, furto e colisão. Você só se preocupa em aproveitar a viagem.</p>
        </div>
        <div class="benefit-card">
          <div class="benefit-icon"><i class="fas fa-truck-fast"></i></div>
          <h4>Entrega e retirada grátis</h4>
          <p>Levamos o carro até você: aeroporto, hotel ou endereço. Sem custo adicional.</p>
        </div>
        <div class="benefit-card">
          <div class="benefit-icon"><i class="fas fa-headset"></i></div>
          <h4>Suporte 24h por dia</h4>
          <p>Assistência 24h em todo o território nacional. Qualquer imprevisto, estamos com você.</p>
        </div>
        <div class="benefit-card">
          <div class="benefit-icon"><i class="fas fa-credit-card"></i></div>
          <h4>Sem caução, sem burocracia</h4>
          <p>Reserva em 2 minutos, pagamento facilitado no cartão, Pix ou boleto. Sem taxas escondidas.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- COMO FUNCIONA -->
  <section id="como-funciona">
    <div class="container">
      <div class="section-head">
        <span class="section-tag">Simples assim</span>
        <h2>Alugue em 3 passos</h2>
        <p>Do clique à chave na mão em menos de 5 minutos</p>
      </div>
      <div class="steps-grid">
        <div class="step-card">
          <div class="step-num">1</div>
          <h4>Escolha o carro</h4>
          <p>Navegue pela nossa frota e selecione o modelo ideal para você.</p>
        </div>
        <div class="step-card">
          <div class="step-num">2</div>
          <h4>Faça a reserva</h4>
          <p>Preencha seus dados em menos de 2 minutos. Sem burocracia.</p>
        </div>
        <div class="step-card">
          <div class="step-num">3</div>
          <h4>Retire e aproveite</h4>
          <p>Entregamos o carro no local combinado. Pronto para sua viagem!</p>
        </div>
      </div>
    </div>
  </section>

  <!-- DEPOIMENTOS -->
  <section id="depoimentos">
    <div class="container">
      <div class="section-head">
        <span class="section-tag">Avaliações reais</span>
        <h2>Quem alugou, aprova</h2>
        <p>Mais de 2.500 clientes satisfeitos em todo o Brasil</p>
      </div>
      <div class="testimonials-grid">
        <div class="testimonial">
          <div class="stars-row">
            <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
          </div>
          <p>"Processo super rápido! Reservei pelo site em 2 minutos e o carro estava impecável. Recomendo demais a DriveNow."</p>
          <div class="testimonial-author">
            <img src="https://i.pravatar.cc/80?img=12" alt="Marina Silva">
            <div>
              <strong>Marina Silva</strong>
              <span>Alugou Fiat Argo · 5 dias</span>
            </div>
          </div>
        </div>
        <div class="testimonial">
          <div class="stars-row">
            <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
          </div>
          <p>"Entregaram o carro no aeroporto no horário combinado. Atendimento impecável e preço justo. Já é minha locadora fixa."</p>
          <div class="testimonial-author">
            <img src="https://i.pravatar.cc/80?img=32" alt="Carlos Mendes">
            <div>
              <strong>Carlos Mendes</strong>
              <span>Alugou Jeep Compass · 3 dias</span>
            </div>
          </div>
        </div>
        <div class="testimonial">
          <div class="stars-row">
            <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
          </div>
          <p>"Tive um imprevisto na estrada e o suporte 24h resolveu em 20 minutos. Serviço de primeira, sem dúvida."</p>
          <div class="testimonial-author">
            <img src="https://i.pravatar.cc/80?img=45" alt="Juliana Costa">
            <div>
              <strong>Juliana Costa</strong>
              <span>Alugou Toyota Corolla · 7 dias</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA FINAL -->
  <section>
    <div class="cta-final">
      <h2>Pronto para pegar a estrada?</h2>
      <p>Reserve agora e receba condições exclusivas. Atendimento em menos de 1 minuto pelo WhatsApp.</p>
      <div class="cta-buttons">
        <a href="https://wa.me/5511999999999?text=Olá! Quero alugar um carro." target="_blank" class="btn-white">
          <i class="fab fa-whatsapp"></i> Falar no WhatsApp
        </a>
        <a href="#reserva" class="btn-outline-white">
          <i class="fas fa-calendar-check"></i> Fazer reserva online
        </a>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="logo">
          <div class="logo-icon"><i class="fas fa-car-side"></i></div>
          Drive<span>Now</span>
        </div>
        <p>A locadora que entrega mais que carros: entrega tranquilidade, segurança e liberdade para você ir mais longe.</p>
        <div class="social-links">
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fab fa-facebook-f"></i></a>
          <a href="#"><i class="fab fa-linkedin-in"></i></a>
          <a href="#"><i class="fab fa-youtube"></i></a>
        </div>
      </div>
      <div class="footer-col">
        <h5>Navegação</h5>
        <a href="#frota">Nossa frota</a>
        <a href="#beneficios">Vantagens</a>
        <a href="#como-funciona">Como funciona</a>
        <a href="#depoimentos">Avaliações</a>
      </div>
      <div class="footer-col">
        <h5>Atendimento</h5>
        <a href="tel:+551140001234"><i class="fas fa-phone"></i> (11) 4000-1234</a>
        <a href="https://wa.me/5511999999999" target="_blank"><i class="fab fa-whatsapp"></i> (11) 99999-9999</a>
        <a href="mailto:contato@drivenow.com.br"><i class="fas fa-envelope"></i> contato@drivenow.com.br</a>
        <p><i class="fas fa-clock"></i> Seg-Sex 8h-20h · Sáb 8h-18h</p>
      </div>
      <div class="footer-col">
        <h5>Institucional</h5>
        <a href="#">Sobre a DriveNow</a>
        <a href="#">Termos de uso</a>
        <a href="#">Política de privacidade</a>
        <a href="#">Trabalhe conosco</a>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2025 DriveNow. Todos os direitos reservados. CNPJ 00.000.000/0001-00</span>
      <div class="payment-methods">
        <i class="fab fa-cc-visa"></i>
        <i class="fab fa-cc-mastercard"></i>
        <i class="fab fa-cc-amex"></i>
        <i class="fas fa-barcode"></i>
        <i class="fas fa-qrcode"></i>
      </div>
    </div>
  </footer>

  <!-- CHATBOT -->
  <div class="chatbot-window" id="chatbotWindow">
    <div class="chat-header">
      <div class="chat-header-info">
        <div class="chat-avatar"><i class="fas fa-headset"></i></div>
        <div>
          <h4>Atendimento DriveNow</h4>
          <span>Online agora</span>
        </div>
      </div>
      <button class="chat-close" onclick="fecharChat()"><i class="fas fa-times"></i></button>
    </div>
    <div class="chat-messages" id="chatMessages">
      <div class="msg bot">Olá! 👋 Sou o assistente virtual da DriveNow.</div>
      <div class="msg bot">Posso te ajudar a encontrar o carro ideal, tirar dúvidas sobre preços, reservas e documentos. Como posso ajudar?</div>
      <div class="quick-replies" id="quickReplies">
        <button class="quick-reply" onclick="enviarRapido('Quero ver os preços')">💰 Ver preços</button>
        <button class="quick-reply" onclick="enviarRapido('Como faço uma reserva?')">📅 Fazer reserva</button>
        <button class="quick-reply" onclick="enviarRapido('Quais documentos preciso?')">📄 Documentos</button>
        <button class="quick-reply" onclick="enviarRapido('Vocês entregam no aeroporto?')">✈️ Entrega</button>
      </div>
    </div>
    <div class="chat-input-area">
      <input type="text" id="chatInput" placeholder="Digite sua mensagem..." onkeypress="if(event.key==='Enter') enviarMensagem()">
      <button class="chat-send" onclick="enviarMensagem()"><i class="fas fa-paper-plane"></i></button>
    </div>
  </div>

  <!-- FLOATING BUTTONS -->
  <div class="floating-actions">
    <button class="float-btn whatsapp" onclick="window.open('https://wa.me/5511999999999?text=Olá! Gostaria de informações sobre aluguel de carros.', '_blank')" title="Falar no WhatsApp">
      <i class="fab fa-whatsapp"></i>
    </button>
    <button class="float-btn chat" id="chatFloatBtn" onclick="toggleChat()" title="Chat online">
      <i class="fas fa-comments"></i>
      <span class="notif">1</span>
    </button>
  </div>

  <script>
    // ============ DATAS ============
    const hoje = new Date().toISOString().split('T')[0];
    const amanha = new Date(Date.now() + 86400000).toISOString().split('T')[0];
    document.getElementById('dataRetirada').min = hoje;
    document.getElementById('dataRetirada').value = hoje;
    document.getElementById('dataDevolucao').min = amanha;
    document.getElementById('dataDevolucao').value = amanha;

    // ============ CHATBOT ============
    const chatbotWindow = document.getElementById('chatbotWindow');
    const chatMessages = document.getElementById('chatMessages');
    const chatInput = document.getElementById('chatInput');
    const chatFloatBtn = document.getElementById('chatFloatBtn');

    function toggleChat() {
      chatbotWindow.classList.toggle('open');
      if (chatbotWindow.classList.contains('open')) {
        chatInput.focus();
        chatFloatBtn.querySelector('.notif').style.display = 'none';
      }
    }

    function abrirChat() {
      chatbotWindow.classList.add('open');
      chatInput.focus();
      chatFloatBtn.querySelector('.notif').style.display = 'none';
    }

    function fecharChat() {
      chatbotWindow.classList.remove('open');
    }

    const respostas = {
      'preç': '💰 Nossos preços:\n• Econômico: R$ 89/dia\n• Sedan: R$ 159/dia\n• SUV: R$ 189/dia\n• Executivo: R$ 399/dia\n\nTodos com seguro incluso!',
      'valor': '💰 Nossos preços:\n• Econômico: R$ 89/dia\n• Sedan: R$ 159/dia\n• SUV: R$ 189/dia\n• Executivo: R$ 399/dia\n\nTodos com seguro incluso!',
      'reserva': '📅 Para reservar é fácil:\n1. Preencha o formulário no topo da página\n2. Escolha o carro ideal\n3. Receba a confirmação na hora\n\nPrecisa de ajuda com algo específico?',
      'document': '📄 Para alugar você precisa de:\n• CNH válida (categoria B ou superior)\n• RG ou CPF\n• Cartão de crédito para garantia\n\nÉ rápido e sem burocracia!',
      'cnh': '📄 Sim! É necessário ter CNH válida, com pelo menos 2 anos de habilitação.',
      'entreg': '🚗 Sim! Entregamos em qualquer endereço da Grande São Paulo — aeroporto, hotel ou residência. E o melhor: é grátis!',
      'aeroporto': '✈️ Sim! Entregamos no aeroporto de Guarulhos, Congonhas e Viracopos. Sem custo adicional.',
      'seguro': '🛡️ Todos os nossos veículos possuem seguro completo incluso na diária (roubo, furto e colisão).',
      'cancel': '✅ Cancelamento gratuito até 24h antes da retirada. Após esse prazo, cobramos 20% do valor.',
      'horario': '🕐 Nosso atendimento:\n• Seg-Sex: 8h às 20h\n• Sáb: 8h às 18h\n• Dom: 9h às 14h\n\nSuporte 24h pelo WhatsApp!',
      'whatsapp': '📱 Clique no botão verde do WhatsApp para falar com nossa equipe agora mesmo!',
      'default': 'Entendi! Para te ajudar melhor, posso falar sobre: preços, reservas, documentos, entrega, seguro ou cancelamento. Sobre qual você quer saber? Ou clique em uma das opções acima 👆'
    };

    function enviarMensagem() {
      const texto = chatInput.value.trim();
      if (!texto) return;
      addMsg(texto, 'user');
      chatInput.value = '';
      document.getElementById('quickReplies')?.remove();
      setTimeout(() => {
        const resposta = getResposta(texto);
        addMsg(resposta, 'bot');
      }, 700);
    }

    function enviarRapido(texto) {
      addMsg(texto, 'user');
      document.getElementById('quickReplies')?.remove();
      setTimeout(() => {
        const resposta = getResposta(texto);
        addMsg(resposta, 'bot');
      }, 600);
    }

    function addMsg(texto, tipo) {
      const div = document.createElement('div');
      div.classList.add('msg', tipo);
      div.innerHTML = texto.replace(/\n/g, '<br>');
      chatMessages.appendChild(div);
      chatMessages.scrollTop = chatMessages.scrollHeight;
    }

    function getResposta(texto) {
      const t = texto.toLowerCase();
      for (let key in respostas) {
        if (t.includes(key)) return respostas[key];
      }
      return respostas.default;
    }

    // ============ HEADER SCROLL ============
    let lastScroll = 0;
    window.addEventListener('scroll', () => {
      const header = document.querySelector('header');
      if (window.scrollY > 100) {
        header.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.08)';
      } else {
        header.style.boxShadow = 'none';
      }
    });

    // ============ ANIMAÇÃO SCROLL ============
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = '1';
          entry.target.style.transform = 'translateY(0)';
        }
      });
    }, { threshold: 0.1 });

    document.querySelectorAll('.car-card, .benefit-card, .testimonial, .step-card').forEach(el => {
      el.style.opacity = '0';
      el.style.transform = 'translateY(20px)';
      el.style.transition = 'opacity 0.6s ease-out, transform 0.6s ease-out';
      observer.observe(el);
    });
  </script>
</body>
</html>
