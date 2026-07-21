# wwe-tickets.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WWE LIVE EVENTS - 2026 Tour Tickets</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
            color: #e0e0e0;
            line-height: 1.6;
        }

        /* HEADER & NAVIGATION */
        header {
            background: linear-gradient(180deg, rgba(0,0,0,0.95) 0%, rgba(20,20,20,0.9) 100%);
            padding: 20px 0;
            border-bottom: 3px solid #d4af37;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(212, 175, 55, 0.3);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .logo {
            font-size: 28px;
            font-weight: bold;
            color: #d4af37;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
            letter-spacing: 2px;
        }

        /* HERO SECTION */
        .hero {
            background: linear-gradient(rgba(212, 175, 55, 0.15), rgba(220, 20, 60, 0.15)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 400"><defs><pattern id="pattern" x="0" y="0" width="100" height="100" patternUnits="userSpaceOnUse"><rect fill="%23dc143c" x="0" y="0" width="50" height="100"/><rect fill="%23d4af37" x="50" y="0" width="50" height="100"/></pattern></defs><rect fill="%23000" width="1200" height="400"/><rect fill="url(%23pattern)" opacity="0.05" width="1200" height="400"/></svg>');
            background-size: cover;
            background-position: center;
            padding: 100px 20px;
            text-align: center;
            border-bottom: 5px solid #dc143c;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 50% 50%, rgba(212, 175, 55, 0.1) 0%, transparent 100%);
            pointer-events: none;
        }

        .hero-content {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-size: 72px;
            font-weight: bold;
            color: #d4af37;
            text-shadow: 3px 3px 8px rgba(0,0,0,0.9), 0 0 20px rgba(212, 175, 55, 0.5);
            margin-bottom: 20px;
            letter-spacing: 3px;
            animation: pulse 2s infinite;
        }

        .hero p {
            font-size: 24px;
            color: #dc143c;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
            font-weight: bold;
            letter-spacing: 1px;
        }

        @keyframes pulse {
            0%, 100% { text-shadow: 3px 3px 8px rgba(0,0,0,0.9), 0 0 20px rgba(212, 175, 55, 0.5); }
            50% { text-shadow: 3px 3px 8px rgba(0,0,0,0.9), 0 0 40px rgba(212, 175, 55, 0.8); }
        }

        /* PACKAGES SECTION */
        .packages-section {
            max-width: 1200px;
            margin: 80px auto;
            padding: 0 20px;
        }

        .section-title {
            font-size: 48px;
            font-weight: bold;
            color: #d4af37;
            text-align: center;
            margin-bottom: 60px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
            letter-spacing: 2px;
        }

        .packages-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .package-card {
            background: linear-gradient(135deg, #1a1a1a 0%, #2a2a2a 100%);
            border: 2px solid #d4af37;
            border-radius: 10px;
            padding: 40px 30px;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .package-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #dc143c, #d4af37);
        }

        .package-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(212, 175, 55, 0.4), 0 0 40px rgba(220, 20, 60, 0.2);
            border-color: #dc143c;
        }

        .package-name {
            font-size: 36px;
            font-weight: bold;
            color: #d4af37;
            margin-bottom: 15px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.8);
        }

        .package-price {
            font-size: 48px;
            font-weight: bold;
            color: #dc143c;
            margin-bottom: 30px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.8);
        }

        .package-price-label {
            font-size: 12px;
            color: #b0b0b0;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .package-features {
            list-style: none;
            margin-bottom: 40px;
            text-align: left;
        }

        .package-features li {
            padding: 12px 0;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
            color: #d0d0d0;
            font-size: 14px;
        }

        .package-features li:before {
            content: '✓ ';
            color: #d4af37;
            font-weight: bold;
            margin-right: 10px;
        }

        .select-btn {
            background: linear-gradient(135deg, #d4af37 0%, #ffd700 100%);
            color: #000;
            border: none;
            padding: 18px 40px;
            font-size: 18px;
            font-weight: bold;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 2px;
            width: 100%;
            box-shadow: 0 8px 20px rgba(212, 175, 55, 0.4);
        }

        .select-btn:hover {
            background: linear-gradient(135deg, #ffd700 0%, #d4af37 100%);
            box-shadow: 0 12px 30px rgba(212, 175, 55, 0.6);
            transform: scale(1.02);
        }

        .select-btn:active {
            transform: scale(0.98);
        }

        /* FORM SECTION */
        .form-section {
            max-width: 800px;
            margin: 80px auto;
            padding: 50px 30px;
            background: linear-gradient(135deg, #1a1a1a 0%, #2a2a2a 100%);
            border: 2px solid #d4af37;
            border-radius: 10px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.6);
        }

        .form-title {
            font-size: 36px;
            font-weight: bold;
            color: #d4af37;
            margin-bottom: 40px;
            text-align: center;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.8);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .form-row-full {
            grid-column: 1 / -1;
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #d4af37;
            font-weight: bold;
            text-transform: uppercase;
            font-size: 12px;
            letter-spacing: 1px;
        }

        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="number"],
        select {
            width: 100%;
            padding: 15px;
            background: #0a0a0a;
            border: 2px solid #404040;
            color: #e0e0e0;
            border-radius: 5px;
            font-size: 14px;
            transition: all 0.3s ease;
            font-family: inherit;
        }

        input[type="text"]:focus,
        input[type="email"]:focus,
        input[type="tel"]:focus,
        input[type="number"]:focus,
        select:focus {
            outline: none;
            border-color: #d4af37;
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.3);
            background: #151515;
        }

        input::placeholder {
            color: #606060;
        }

        /* PRICE SUMMARY */
        .price-summary {
            background: linear-gradient(135deg, rgba(212, 175, 55, 0.1) 0%, rgba(220, 20, 60, 0.1) 100%);
            padding: 30px;
            border-radius: 5px;
            margin-top: 30px;
            border-left: 4px solid #d4af37;
        }

        .price-summary-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
            font-size: 16px;
            color: #d0d0d0;
        }

        .price-summary-row.total {
            border-top: 2px solid #d4af37;
            padding-top: 15px;
            font-size: 24px;
            font-weight: bold;
            color: #d4af37;
        }

        /* SUBMIT BUTTON */
        .submit-btn {
            width: 100%;
            background: linear-gradient(135deg, #dc143c 0%, #ff1744 100%);
            color: #fff;
            border: none;
            padding: 18px 40px;
            font-size: 18px;
            font-weight: bold;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-top: 30px;
            box-shadow: 0 8px 20px rgba(220, 20, 60, 0.4);
        }

        .submit-btn:hover {
            background: linear-gradient(135deg, #ff1744 0%, #dc143c 100%);
            box-shadow: 0 12px 30px rgba(220, 20, 60, 0.6);
            transform: scale(1.02);
        }

        .submit-btn:active {
            transform: scale(0.98);
        }

        /* SUCCESS MODAL */
        .modal {
            display: none;
            position: fixed;
            z-index: 2000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.9);
            animation: fadeIn 0.3s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .modal-content {
            background: linear-gradient(135deg, #1a1a1a 0%, #2a2a2a 100%);
            margin: 5% auto;
            padding: 50px;
            border: 3px solid #d4af37;
            border-radius: 10px;
            max-width: 600px;
            text-align: center;
            box-shadow: 0 0 60px rgba(212, 175, 55, 0.5);
            animation: slideDown 0.3s ease;
        }

        @keyframes slideDown {
            from {
                transform: translateY(-50px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .success-message {
            font-size: 32px;
            color: #d4af37;
            margin-bottom: 30px;
            font-weight: bold;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.8);
        }

        .success-icon {
            font-size: 80px;
            color: #d4af37;
            margin-bottom: 20px;
            animation: bounce 0.6s ease;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .order-details {
            background: rgba(212, 175, 55, 0.1);
            padding: 25px;
            border-radius: 5px;
            margin: 30px 0;
            text-align: left;
            border-left: 4px solid #d4af37;
        }

        .order-detail-item {
            display: flex;
            justify-content: space-between;
            padding: 10px 0;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
            color: #d0d0d0;
        }

        .order-detail-item:last-child {
            border-bottom: none;
        }

        .order-detail-label {
            color: #d4af37;
            font-weight: bold;
        }

        /* COPY MESSAGE SECTION */
        .message-section {
            margin: 30px 0;
        }

        .message-label {
            color: #d4af37;
            font-weight: bold;
            margin-bottom: 15px;
            text-transform: uppercase;
            font-size: 12px;
            letter-spacing: 1px;
        }

        .copy-box {
            background: #0a0a0a;
            border: 2px solid #d4af37;
            padding: 20px;
            border-radius: 5px;
            margin-bottom: 20px;
            color: #d0d0d0;
            max-height: 200px;
            overflow-y: auto;
            white-space: pre-wrap;
            word-break: break-word;
            font-size: 13px;
            font-family: 'Courier New', monospace;
            line-height: 1.6;
        }

        .copy-btn {
            background: linear-gradient(135deg, #d4af37 0%, #ffd700 100%);
            color: #000;
            border: none;
            padding: 12px 30px;
            font-size: 14px;
            font-weight: bold;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 6px 15px rgba(212, 175, 55, 0.4);
            margin-right: 10px;
            margin-bottom: 10px;
        }

        .copy-btn:hover {
            background: linear-gradient(135deg, #ffd700 0%, #d4af37 100%);
            box-shadow: 0 8px 20px rgba(212, 175, 55, 0.6);
            transform: scale(1.02);
        }

        .telegram-btn {
            background: linear-gradient(135deg, #0088cc 0%, #0099ff 100%);
            color: #fff;
            border: none;
            padding: 15px 40px;
            font-size: 16px;
            font-weight: bold;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 2px;
            box-shadow: 0 8px 20px rgba(0, 136, 204, 0.4);
            display: inline-block;
        }

        .telegram-btn:hover {
            background: linear-gradient(135deg, #0099ff 0%, #0088cc 100%);
            box-shadow: 0 12px 30px rgba(0, 136, 204, 0.6);
            transform: scale(1.02);
        }

        .close-modal {
            color: #d4af37;
            float: right;
            font-size: 32px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            line-height: 1;
        }

        .close-modal:hover {
            color: #dc143c;
            transform: scale(1.2);
        }

        /* FOOTER */
        footer {
            background: linear-gradient(180deg, rgba(0,0,0,0.95) 0%, rgba(20,20,20,0.9) 100%);
            border-top: 3px solid #d4af37;
            padding: 40px 20px;
            text-align: center;
            color: #808080;
            margin-top: 100px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-text {
            font-size: 14px;
            margin-bottom: 15px;
        }

        .footer-highlight {
            color: #d4af37;
            font-weight: bold;
        }

        .footer-note {
            font-size: 12px;
            color: #606060;
            margin-top: 15px;
            font-style: italic;
        }

        /* RESPONSIVE DESIGN */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 42px;
            }

            .hero p {
                font-size: 18px;
            }

            .section-title {
                font-size: 32px;
            }

            .packages-container {
                grid-template-columns: 1fr;
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .modal-content {
                margin: 10% auto;
                padding: 30px 20px;
                max-width: 90%;
            }

            .success-message {
                font-size: 24px;
            }

            .success-icon {
                font-size: 60px;
            }

            input[type="text"],
            input[type="email"],
            input[type="tel"],
            input[type="number"],
            select {
                padding: 12px;
                font-size: 16px;
            }
        }

        @media (max-width: 480px) {
            .hero {
                padding: 60px 15px;
            }

            .hero h1 {
                font-size: 32px;
                letter-spacing: 1px;
            }

            .logo {
                font-size: 20px;
            }

            .section-title {
                font-size: 24px;
                margin-bottom: 40px;
            }

            .package-name {
                font-size: 24px;
            }

            .package-price {
                font-size: 36px;
            }

            .form-section {
                padding: 25px 15px;
                margin: 40px 15px;
            }

            .form-title {
                font-size: 24px;
            }

            .modal-content {
                margin: 20% auto;
                padding: 20px 15px;
            }

            label, .footer-text {
                font-size: 12px;
            }
        }

        .copy-feedback {
            display: none;
            color: #d4af37;
            font-weight: bold;
            margin-top: 10px;
            animation: fadeIn 0.3s ease;
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">🎭 WWE LIVE EVENTS</div>
        </nav>
    </header>

    <section class="hero">
        <div class="hero-content">
            <h1>WWE LIVE EVENTS – 2026 TOUR TICKETS</h1>
            <p>EXPERIENCE THE ULTIMATE WRESTLING ENTERTAINMENT</p>
        </div>
    </section>

    <section class="packages-section">
        <h2 class="section-title">TICKET PACKAGES</h2>
        <div class="packages-container">
            <div class="package-card" onclick="selectPackage('Elite', 249)">
                <div class="package-name">ELITE</div>
                <div class="package-price">$249<div class="package-price-label">per ticket</div></div>
                <ul class="package-features">
                    <li>General Admission Seating</li>
                    <li>Access to Main Event</li>
                    <li>WWE Event Program</li>
                    <li>Parking Included</li>
                    <li>Merchandise Discount (10%)</li>
                    <li>Digital Event Guide</li>
                </ul>
                <button class="select-btn">SELECT ELITE</button>
            </div>

            <div class="package-card" onclick="selectPackage('VIP', 399)">
                <div class="package-name">VIP</div>
                <div class="package-price">$399<div class="package-price-label">per ticket</div></div>
                <ul class="package-features">
                    <li>Premium Seating (Close to Ring)</li>
                    <li>VIP Entry & Exit</li>
                    <li>Commemorative VIP Pass</li>
                    <li>Premium Parking</li>
                    <li>Merchandise Discount (20%)</li>
                    <li>Exclusive VIP Lounge Access</li>
                </ul>
                <button class="select-btn">SELECT VIP</button>
            </div>

            <div class="package-card" onclick="selectPackage('Premium', 599)">
                <div class="package-name">PREMIUM</div>
                <div class="package-price">$599<div class="package-price-label">per ticket</div></div>
                <ul class="package-features">
                    <li>Ringside Premium Seating</li>
                    <li>Meet & Greet Opportunity*</li>
                    <li>Premium VIP Pass</li>
                    <li>Valet Parking</li>
                    <li>Free Merchandise Item</li>
                    <li>Exclusive Backstage Tour Video</li>
                </ul>
                <button class="select-btn">SELECT PREMIUM</button>
            </div>
        </div>
    </section>

    <section class="form-section">
        <h2 class="form-title">COMPLETE YOUR ORDER</h2>
        <form id="orderForm" onsubmit="submitForm(event)">
            <div class="form-row">
                <div class="form-group">
                    <label for="fullName">Full Name *</label>
                    <input type="text" id="fullName" name="fullName" placeholder="John Doe" required>
                </div>
                <div class="form-group">
                    <label for="email">Email Address *</label>
                    <input type="email" id="email" name="email" placeholder="your@email.com" required>
                </div>
            </div>

            <div class="form-row">
                <div class="form-group">
                    <label for="phone">Phone Number *</label>
                    <input type="tel" id="phone" name="phone" placeholder="+1 (555) 123-4567" required>
                </div>
                <div class="form-group">
                    <label for="quantity">Number of Tickets *</label>
                    <input type="number" id="quantity" name="quantity" min="1" value="1" required onchange="updatePrice()">
                </div>
            </div>

            <div class="form-row">
                <div class="form-group form-row-full">
                    <label for="address">Full Address - Street *</label>
                    <input type="text" id="address" name="address" placeholder="123 Main Street" required>
                </div>
            </div>

            <div class="form-row">
                <div class="form-group">
                    <label for="city">City *</label>
                    <input type="text" id="city" name="city" placeholder="New York" required>
                </div>
                <div class="form-group">
                    <label for="state">State *</label>
                    <input type="text" id="state" name="state" placeholder="NY" required>
                </div>
            </div>

            <div class="form-row">
                <div class="form-group">
                    <label for="zip">ZIP Code *</label>
                    <input type="text" id="zip" name="zip" placeholder="10001"*

