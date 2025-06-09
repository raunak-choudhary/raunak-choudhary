<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Raunak Choudhary - Dynamic Portfolio README</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #000000 0%, #1a0a2e 25%, #16213e 50%, #0f3460 75%, #533483 100%);
            color: white;
            font-family: 'Segoe UI', 'Fira Code', 'Courier New', monospace;
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
        }

        /* Animated Background Effects */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 80%, rgba(0, 245, 255, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255, 0, 255, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(255, 255, 0, 0.1) 0%, transparent 50%);
            animation: backgroundFloat 20s ease-in-out infinite;
            pointer-events: none;
            z-index: -1;
        }

        @keyframes backgroundFloat {
            0%, 100% { transform: translate(0, 0) scale(1); }
            25% { transform: translate(-20px, -20px) scale(1.05); }
            50% { transform: translate(20px, -10px) scale(0.95); }
            75% { transform: translate(-10px, 20px) scale(1.02); }
        }

        /* Floating Particles */
        .particle {
            position: fixed;
            width: 4px;
            height: 4px;
            background: rgba(0, 245, 255, 0.8);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
            z-index: -1;
        }

        .particle:nth-child(2) { 
            left: 20%; 
            animation-delay: -2s; 
            background: rgba(255, 0, 255, 0.8);
        }
        .particle:nth-child(3) { 
            left: 40%; 
            animation-delay: -4s; 
            background: rgba(255, 255, 0, 0.8);
        }
        .particle:nth-child(4) { 
            left: 60%; 
            animation-delay: -1s; 
            background: rgba(0, 255, 100, 0.8);
        }
        .particle:nth-child(5) { 
            left: 80%; 
            animation-delay: -3s; 
            background: rgba(255, 100, 0, 0.8);
        }

        @keyframes float {
            0%, 100% { transform: translateY(100vh) scale(0); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100px) scale(1); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        /* Header Section */
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 40px 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 30px;
            backdrop-filter: blur(20px);
            border: 2px solid rgba(0, 245, 255, 0.3);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(0, 245, 255, 0.1), transparent);
            animation: shimmer 3s ease-in-out infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }

        .main-title {
            font-size: 3.5rem;
            font-weight: 900;
            background: linear-gradient(45deg, #00f5ff, #ff00ff, #ffff00, #00ff88);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradientShift 4s ease-in-out infinite;
            text-shadow: 0 0 30px rgba(0, 245, 255, 0.5);
            margin-bottom: 20px;
            position: relative;
            z-index: 2;
        }

        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .typing-animation {
            font-size: 1.5rem;
            color: #00f5ff;
            text-shadow: 0 0 20px rgba(0, 245, 255, 0.8);
            position: relative;
            z-index: 2;
        }

        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .social-btn {
            padding: 12px 25px;
            border-radius: 50px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
            border: 2px solid;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }

        .social-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }

        .social-btn:hover::before {
            left: 100%;
        }

        .social-btn:hover {
            transform: translateY(-5px) scale(1.05);
            filter: brightness(1.3);
        }

        .btn-linkedin {
            background: linear-gradient(45deg, #0077B5, #00A0DC);
            border-color: #0077B5;
            box-shadow: 0 0 20px rgba(0, 119, 181, 0.5);
        }

        .btn-email {
            background: linear-gradient(45deg, #D14836, #FF6B6B);
            border-color: #D14836;
            box-shadow: 0 0 20px rgba(209, 72, 54, 0.5);
        }

        .btn-github {
            background: linear-gradient(45deg, #333, #666);
            border-color: #333;
            box-shadow: 0 0 20px rgba(51, 51, 51, 0.5);
        }

        .btn-portfolio {
            background: linear-gradient(45deg, #FF9900, #FF7700);
            border-color: #FF9900;
            box-shadow: 0 0 20px rgba(255, 153, 0, 0.5);
            color: #232f3e;
            font-weight: 700;
        }

        .btn-portfolio:hover {
            color: white;
            box-shadow: 0 0 30px rgba(255, 153, 0, 0.8);
        }

        .btn-phone {
            background: linear-gradient(45deg, #4285F4, #34A853);
            border-color: #4285F4;
            box-shadow: 0 0 20px rgba(66, 133, 244, 0.5);
        }

        /* Content Sections */
        .section {
            margin: 40px 0;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
        }

        .section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #00f5ff, #ff00ff, #ffff00, #00ff88);
            background-size: 300% 300%;
            animation: gradientShift 3s ease-in-out infinite;
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 700;
            color: #00f5ff;
            text-shadow: 0 0 15px rgba(0, 245, 255, 0.8);
            margin-bottom: 25px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, #00f5ff, #ff00ff);
            border-radius: 3px;
        }

        /* Code Block Styling */
        .code-block {
            background: rgba(0, 0, 0, 0.7);
            border-radius: 15px;
            padding: 25px;
            margin: 20px 0;
            border: 1px solid rgba(0, 245, 255, 0.3);
            position: relative;
            overflow: hidden;
        }

        .code-block::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, #00f5ff, transparent);
            animation: scanline 2s ease-in-out infinite;
        }

        @keyframes scanline {
            0%, 100% { opacity: 0; }
            50% { opacity: 1; }
        }

        .code-block pre {
            color: #00ff88;
            font-family: 'Fira Code', 'Courier New', monospace;
            overflow-x: auto;
            text-shadow: 0 0 5px rgba(0, 255, 136, 0.5);
        }

        /* Education Table */
        .education-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .education-table td {
            padding: 20px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            vertical-align: top;
        }

        .edu-badge {
            text-align: center;
            width: 150px;
        }

        .edu-badge img {
            background: linear-gradient(45deg, #5B2C6F, #E74C3C);
            color: white;
            padding: 8px 16px;
            border-radius: 25px;
            font-weight: 600;
            box-shadow: 0 0 15px rgba(91, 44, 111, 0.5);
            border: none;
            display: inline-block;
            text-decoration: none;
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .skill-badge {
            display: inline-block;
            transition: all 0.3s ease;
            filter: drop-shadow(0 0 10px rgba(0, 245, 255, 0.3));
        }

        .skill-badge:hover {
            transform: scale(1.1) translateY(-5px);
            filter: drop-shadow(0 0 20px rgba(0, 245, 255, 0.8));
        }

        .skill-badge img {
            width: 100%;
            height: auto;
            border-radius: 8px;
        }

        /* Projects Section */
        .project-card {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 15px;
            padding: 25px;
            margin: 20px 0;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 245, 255, 0.1), transparent);
            transition: left 0.8s;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: rgba(0, 245, 255, 0.5);
            box-shadow: 0 20px 40px rgba(0, 245, 255, 0.2);
        }

        .project-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: #ff00ff;
            text-shadow: 0 0 10px rgba(255, 0, 255, 0.5);
            margin-bottom: 15px;
        }

        .project-links {
            display: flex;
            gap: 15px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .project-btn {
            padding: 8px 20px;
            border-radius: 25px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: 2px solid;
            backdrop-filter: blur(10px);
        }

        .btn-repo {
            background: linear-gradient(45deg, #2563eb, #1d4ed8);
            border-color: #2563eb;
            box-shadow: 0 0 15px rgba(37, 99, 235, 0.5);
        }

        .btn-frontend {
            background: linear-gradient(45deg, #059669, #047857);
            border-color: #059669;
            box-shadow: 0 0 15px rgba(5, 150, 105, 0.5);
        }

        .btn-backend {
            background: linear-gradient(45deg, #7c3aed, #6d28d9);
            border-color: #7c3aed;
            box-shadow: 0 0 15px rgba(124, 58, 237, 0.5);
        }

        .btn-ml {
            background: linear-gradient(45deg, #dc2626, #b91c1c);
            border-color: #dc2626;
            box-shadow: 0 0 15px rgba(220, 38, 38, 0.5);
        }

        .btn-nlp {
            background: linear-gradient(45deg, #eab308, #ca8a04);
            border-color: #eab308;
            box-shadow: 0 0 15px rgba(234, 179, 8, 0.5);
        }

        .btn-orange {
            background: linear-gradient(45deg, #f97316, #ea580c);
            border-color: #f97316;
            box-shadow: 0 0 15px rgba(249, 115, 22, 0.5);
        }

        .project-btn:hover {
            transform: translateY(-3px) scale(1.05);
            filter: brightness(1.3);
        }

        /* Achievements Grid */
        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin: 25px 0;
        }

        .achievement-card {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            border: 1px solid rgba(255, 215, 0, 0.3);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .achievement-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 215, 0, 0.1) 0%, transparent 70%);
            animation: rotate 10s linear infinite;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .achievement-card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 215, 0, 0.8);
            box-shadow: 0 20px 40px rgba(255, 215, 0, 0.3);
        }

        .achievement-badge {
            font-size: 3rem;
            margin-bottom: 15px;
            position: relative;
            z-index: 2;
        }

        .achievement-title {
            font-size: 1.3rem;
            font-weight: 700;
            color: #ffd700;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.8);
            margin-bottom: 10px;
            position: relative;
            z-index: 2;
        }

        /* Certifications Grid */
        .cert-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin: 25px 0;
        }

        .cert-card {
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border: 1px solid rgba(255, 153, 0, 0.3);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .cert-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 153, 0, 0.1), transparent);
            transition: left 0.6s;
        }

        .cert-card:hover::before {
            left: 100%;
        }

        .cert-card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 153, 0, 0.8);
            box-shadow: 0 15px 35px rgba(255, 153, 0, 0.3);
        }

        .cert-image {
            width: 150px;
            height: 150px;
            margin: 0 auto 15px;
            border-radius: 10px;
            overflow: hidden;
            border: 2px solid rgba(255, 153, 0, 0.5);
            position: relative;
            z-index: 2;
        }

        .cert-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .cert-btn {
            background: linear-gradient(45deg, #FF9900, #FF7700);
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            display: inline-block;
            margin-top: 10px;
            border: 2px solid #FF9900;
            transition: all 0.3s ease;
            position: relative;
            z-index: 2;
        }

        .cert-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(255, 153, 0, 0.5);
        }

        /* GitHub Stats */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 25px 0;
        }

        .stat-card {
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border: 1px solid rgba(139, 92, 246, 0.3);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            border-color: rgba(139, 92, 246, 0.8);
            box-shadow: 0 15px 35px rgba(139, 92, 246, 0.3);
        }

        .stat-card img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .stat-card:hover img {
            transform: scale(1.05);
            filter: brightness(1.1);
        }

        /* Goals Grid */
        .goals-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 25px 0;
        }

        .goal-card {
            padding: 25px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .goal-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #5B2C6F, #E74C3C, #2ECC71, #3498DB);
            background-size: 300% 300%;
            animation: gradientShift 4s ease-in-out infinite;
        }

        .goal-card:hover {
            transform: translateY(-8px);
            border-color: rgba(255, 255, 255, 0.3);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }

        .goal-badge {
            background: linear-gradient(45deg, #5B2C6F, #E74C3C);
            color: white;
            padding: 8px 16px;
            border-radius: 25px;
            font-weight: 600;
            display: inline-block;
            margin-bottom: 15px;
            box-shadow: 0 0 15px rgba(91, 44, 111, 0.5);
        }

        .goal-badge.technical { background: linear-gradient(45deg, #E74C3C, #C0392B); }
        .goal-badge.community { background: linear-gradient(45deg, #2ECC71, #27AE60); }
        .goal-badge.career { background: linear-gradient(45deg, #3498DB, #2980B9); }

        .goal-list {
            list-style: none;
            padding: 0;
        }

        .goal-list li {
            padding: 8px 0;
            padding-left: 20px;
            position: relative;
            color: rgba(255, 255, 255, 0.9);
        }

        .goal-list li::before {
            content: '⚡';
            position: absolute;
            left: 0;
            color: #00f5ff;
            text-shadow: 0 0 10px rgba(0, 245, 255, 0.8);
        }

        /* Connect Section */
        .connect-section {
            text-align: center;
            padding: 40px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 25px;
            border: 2px solid rgba(0, 245, 255, 0.3);
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }

        .connect-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(0, 245, 255, 0.05), transparent);
            animation: shimmer 4s ease-in-out infinite;
        }

        .connect-title {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, #00f5ff, #ff00ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            position: relative;
            z-index: 2;
        }

        .connect-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .connect-btn {
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
            border: 2px solid;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
            z-index: 2;
        }

        .connect-btn:hover {
            transform: translateY(-5px) scale(1.05);
            filter: brightness(1.3);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .visitor-counter {
            background: linear-gradient(45deg, #8b5cf6, #ec4899);
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            display: inline-block;
            box-shadow: 0 0 20px rgba(139, 92, 246, 0.5);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .main-title {
                font-size: 2.5rem;
            }
            
            .typing-animation {
                font-size: 1.2rem;
            }
            
            .social-links {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            }
            
            .skills-grid {
                grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .achievements-grid {
                grid-template-columns: 1fr;
            }
            
            .goals-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Special animations */
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .pulse-animation {
            animation: pulse 2s ease-in-out infinite;
        }

        /* Glow effect for important elements */
        .glow {
            filter: drop-shadow(0 0 10px rgba(0, 245, 255, 0.8));
        }

        .glow:hover {
            filter: drop-shadow(0 0 20px rgba(0, 245, 255, 1));
        }
    </style>
</head>
<body>
    <!-- Floating Particles -->
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>

    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <h1 class="main-title">👋 Hi, I'm Raunak Choudhary!</h1>
            <div class="typing-animation">
                <img src="https://readme-typing-svg.herokuapp.com/?lines=AWS+Developer;Machine+Learning+Engineer;Full+Stack+Developer;Deep+Learning+Researcher&font=Fira%20Code&center=true&width=440&height=45&color=f75c7e&vCenter=true&size=22" alt="Typing Animation">
            </div>
            
            <div class="social-links">
                <a href="https://www.linkedin.com/in/raunak-choudhary" class="social-btn btn-linkedin">LinkedIn</a>
                <a href="mailto:raunakchoudhary17@gmail.com" class="social-btn btn-email">Email</a>
                <a href="https://github.com/raunak-choudhary" class="social-btn btn-github">GitHub</a>
                <a href="https://www.raunakchoudhary.com" class="social-btn btn-portfolio">Portfolio</a>
                <a href="tel:+19292894648" class="social-btn btn-phone">Phone</a>
            </div>
        </div>

        <!-- About Me Section -->
        <div class="section">
            <h2 class="section-title">🚀 About Me</h2>
            <div class="code-block">
                <pre><code>const raunak = {
  location: "New York, USA",
  education: {
    masters: "MS in Computer Science - NYU Tandon (GPA: 3.889/4.0)",
    bachelors: "B.E. in Computer Science - VTU (GPA: 8.47/10.0)"
  },
  workExperience: ["AWS Developer at TCS (3 years)", "Data Science & ML Intern"],
  certifications: ["AWS Certified Cloud Practitioner", "AWS Certified Data Analytics - Specialty"],
  interests: ["Cloud Computing", "Machine Learning", "Deep Learning", "Computer Vision", "NLP"],
  currentFocus: "Developing robust ML models and cloud-native applications"
};</code></pre>
            </div>
        </div>

        <!-- Education Section -->
        <div class="section">
            <h2 class="section-title">🎓 Education</h2>
            <table class="education-table">
                <tr>
                    <td class="edu-badge">
                        <div style="background: linear-gradient(45deg, #5B2C6F, #7B3F98); color: white; padding: 8px 16px; border-radius: 25px; font-weight: 600; box-shadow: 0 0 15px rgba(91, 44, 111, 0.5);">NYU</div>
                    </td>
                    <td>
                        <strong>Master's in Computer Science</strong><br>
                        New York University - Tandon School of Engineering<br>
                        GPA: 3.889/4.0 • Expected Graduation: May 2026<br>
                        <i>Relevant Coursework: Design and Analysis of Algorithms, Software Engineering, Machine Learning, Deep Learning</i>
                    </td>
                </tr>
                <tr>
                    <td class="edu-badge">
                        <div style="background: linear-gradient(45deg, #E74C3C, #C0392B); color: white; padding: 8px 16px; border-radius: 25px; font-weight: 600; box-shadow: 0 0 15px rgba(231, 76, 60, 0.5);">VTU</div>
                    </td>
                    <td>
                        <strong>B.E. in Computer Science and Engineering</strong><br>
                        Visvesvaraya Technological University - Shri Madhwa Vadiraja Institute of Technology and Management<br>
                        GPA: 8.47/10.0 • August 2017 - August 2021<br>
                        <i>Relevant Coursework: Data Structures, Advanced JAVA and J2EE, Web Technology and its Applications, Operating Systems</i>
                    </td>
                </tr>
            </table>
        </div>

        <!-- Current Focus Section -->
        <div class="section">
            <h2 class="section-title">🔄 Current Focus</h2>
            <p>I'm currently focusing on enhancing my skills in:</p>
            <ul style="list-style: none; padding: 0;">
                <li style="padding: 8px 0; padding-left: 30px; position: relative; color: rgba(255, 255, 255, 0.9);">
                    <span style="position: absolute; left: 0; color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.8);">🎓</span>
                    <strong>Master's in Computer Science</strong>: Completing my MS in Computer Science at NYU with a high GPA score and comprehensive knowledge collection across various domains
                </li>
                <li style="padding: 8px 0; padding-left: 30px; position: relative; color: rgba(255, 255, 255, 0.9);">
                    <span style="position: absolute; left: 0; color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.8);">🧠</span>
                    <strong>Adversarial Machine Learning</strong>: Developing robust models that can withstand various attack vectors
                </li>
                <li style="padding: 8px 0; padding-left: 30px; position: relative; color: rgba(255, 255, 255, 0.9);">
                    <span style="position: absolute; left: 0; color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.8);">☁️</span>
                    <strong>Multi-Cloud Expertise & DevOps</strong>: Exploring and earning more certifications in Azure and GCP along with AWS, building cloud-native projects integrated with DevOps practices
                </li>
                <li style="padding: 8px 0; padding-left: 30px; position: relative; color: rgba(255, 255, 255, 0.9);">
                    <span style="position: absolute; left: 0; color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.8);">🤖</span>
                    <strong>AI Applications Development</strong>: Building diverse AI applications and exploring the AI field in depth to create innovative solutions across various domains
                </li>
                <li style="padding: 8px 0; padding-left: 30px; position: relative; color: rgba(255, 255, 255, 0.9);">
                    <span style="position: absolute; left: 0; color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.8);">🔍</span>
                    <strong>Parameter-Efficient Fine-Tuning</strong>: Exploring techniques like LoRA for efficient adaptation of large language models
                </li>
                <li style="padding: 8px 0; padding-left: 30px; position: relative; color: rgba(255, 255, 255, 0.9);">
                    <span style="position: absolute; left: 0; color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.8);">🌐</span>
                    <strong>Full-Stack Development</strong>: Building end-to-end applications with trending technologies including React.js, Next.js, TypeScript frontend and Node.js, Express.js, FastAPI backend with modern databases like MongoDB, PostgreSQL
                </li>
            </ul>
        </div>

        <!-- Work Experience Section -->
        <div class="section">
            <h2 class="section-title">💼 Work Experience</h2>
            
            <div class="project-card">
                <div class="project-title">AWS Developer - Tata Consultancy Services (TCS) Ltd. [August 2021 - July 2024]</div>
                <ul style="list-style: none; padding: 0;">
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Led an 8-member Infrastructure team, achieving 100% on-time project delivery and reducing downtime by 20%
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Enhanced deployment efficiency by 25% through expertise in AWS Cloud Development and Infrastructure as Code
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Reduced system and network issues by 50% by supporting application and database teams with AWS infrastructure integration
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Executed impactful solutions for global clients in the UK, US, and Brazil, improving client satisfaction by 15%
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Played a key role in the migration of 15+ applications, reducing time by 40% with no data loss
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Collaborated with lead AWS architect to design architecture diagrams for 10+ applications, improving system scalability by 30%
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Obtained AWS Certifications, boosting technical proficiency and accelerating project delivery timelines by 15% across teams
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Trained 15+ team members, reducing onboarding time by 50% and ensuring consistent client support
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Rated in the top 10% of professionals at my level, reflecting consistent high performance and reliability
                    </li>
                </ul>
            </div>

            <div class="project-card">
                <div class="project-title">Data Science Intern - Great Learning Pvt. Ltd. [June 2020 - August 2020]</div>
                <ul style="list-style: none; padding: 0;">
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Worked on Data Science, Statistical Learning, and Applied Statistics projects with Amazon E-commerce, Insurance, and LaLiga datasets
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Analyzed over 1 million data points to uncover actionable insights using advanced statistical techniques
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Leveraged Python libraries like NumPy and Pandas for Data Visualization and EDA, resulting in 20% reduction in analysis time
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Improved data accuracy by 30% through rigorous preprocessing and feature engineering
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Employed advanced visualization techniques (Violin Plots, Network Graphs, Heatmaps), enhancing insights by 35%
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Presented analytical findings to stakeholders, resulting in implementation of data-driven recommendations
                    </li>
                </ul>
            </div>

            <div class="project-card">
                <div class="project-title">CCNA Networking Intern - Hewlett Packard Enterprise [July 2020 - August 2020]</div>
                <ul style="list-style: none; padding: 0;">
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Completed comprehensive virtual internship focusing on CISCO networking fundamentals and network infrastructure design
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Mastered CISCO Packet Tracer software, designing and simulating 15+ complex network topologies with 95% accuracy
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Gained expertise in routing protocols (OSPF, EIGRP), switching concepts, and VLAN configuration achieving 93% proficiency
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Implemented network security measures including ACLs, firewall configurations, and network troubleshooting with 90% success rate
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Studied TCP/IP protocol suite, subnetting, and network address translation, demonstrating 96% conceptual understanding
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Successfully cleared MTA: Networking Fundamentals (98-366) examination, validating networking knowledge and skills
                    </li>
                </ul>
            </div>

            <div class="project-card">
                <div class="project-title">Web Development Intern - Inmovidu Technologies [July 2020 - August 2020]</div>
                <ul style="list-style: none; padding: 0;">
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Developed full-stack web applications using HTML5, CSS3, JavaScript, and backend technologies
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Built 3 responsive web projects with modern UI/UX design principles, achieving 95% client satisfaction
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Implemented RESTful APIs and database integration, improving data retrieval efficiency by 40%
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Mastered frontend frameworks and backend development, delivering projects with 98% code quality standards
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Enhanced web performance optimization techniques, reducing page load times by 35% across all projects
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Successfully cleared MTA: HTML5 Application Development Fundamentals examination, demonstrating technical proficiency
                    </li>
                </ul>
            </div>

            <div class="project-card">
                <div class="project-title">Android App Development Intern - Azure Skynet Solutions Pvt. Ltd. [March 2020]</div>
                <ul style="list-style: none; padding: 0;">
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Developed 5 fully functional Android applications using Java and Android Studio with diverse feature implementations
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Mastered Android lifecycle management, UI/UX design patterns, and database integration achieving 92% app performance
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Implemented key Android components including Activities, Fragments, Services, and Broadcast Receivers with 96% accuracy
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Built applications featuring GPS integration, camera functionality, and local storage, demonstrating 90% technical proficiency
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Gained expertise in Material Design principles and responsive layouts, delivering apps with 94% user experience ratings
                    </li>
                </ul>
            </div>

            <div class="project-card">
                <div class="project-title">Machine Learning Intern - Verzeo Edutech Ltd. [July 2019 - August 2019]</div>
                <ul style="list-style: none; padding: 0;">
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Gained proficiency in Python for Machine Learning, mastering foundational concepts and algorithms
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Applied ML algorithms in over 3 practical projects, demonstrating versatility across different problem domains
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Developed an ML application focused on Autism Spectrum Disorder (ASD) prediction, achieving 88% accuracy
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Implemented K-Nearest Neighbors and Random Forest algorithms to create robust prediction models
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Explored Natural Language Processing techniques, improving prediction accuracy by 10% for text-based inputs
                    </li>
                    <li style="padding: 5px 0; padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: #00ff88;">•</span>
                        Collaborated with a team of 5 interns to deliver end-to-end machine learning solutions
                    </li>
                </ul>
            </div>
        </div>

        <!-- Skills Section -->
        <div class="section">
            <h2 class="section-title">🛠️ Skills & Competencies</h2>
            
            <h3 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5); margin: 25px 0 15px 0;">Programming Languages</h3>
            <div class="skills-grid">
                <div class="skill-badge"><img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white" alt="Java"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white" alt="C"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white" alt="R"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Scala-DC322F?style=for-the-badge&logo=scala&logoColor=white" alt="Scala"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="SQL"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white" alt="Shell Script"></div>
            </div>

            <h3 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5); margin: 25px 0 15px 0;">Machine Learning & Data Science</h3>
            <div class="skills-grid">
                <div class="skill-badge"><img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="scikit-learn"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white" alt="SciPy"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/NLTK-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="NLTK"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/LangChain-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="LangChain"></div>
            </div>

            <h3 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5); margin: 25px 0 15px 0;">Web Development</h3>
            <div class="skills-grid">
                <div class="skill-badge"><img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap"></div>
            </div>

            <h3 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5); margin: 25px 0 15px 0;">AWS & Cloud</h3>
            <div class="skills-grid">
                <div class="skill-badge"><img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="AWS"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/EC2-FF9900?style=for-the-badge&logo=amazon-ec2&logoColor=white" alt="EC2"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white" alt="S3"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Lambda-FF9900?style=for-the-badge&logo=aws-lambda&logoColor=white" alt="Lambda"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/RDS-527FFF?style=for-the-badge&logo=amazon-rds&logoColor=white" alt="RDS"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/DynamoDB-4053D6?style=for-the-badge&logo=amazon-dynamodb&logoColor=white" alt="DynamoDB"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/SageMaker-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="SageMaker"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/ECS-FF9900?style=for-the-badge&logo=amazon-ecs&logoColor=white" alt="ECS"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/EKS-FF9900?style=for-the-badge&logo=amazon-eks&logoColor=white" alt="EKS"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/CloudFormation-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="CloudFormation"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/IAM-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="IAM"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/API_Gateway-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="API Gateway"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white" alt="Azure"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white" alt="GCP"></div>
            </div>

            <h3 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5); margin: 25px 0 15px 0;">DevOps & Tools</h3>
            <div class="skills-grid">
                <div class="skill-badge"><img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white" alt="Jenkins"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/GitLab_CI/CD-FCA121?style=for-the-badge&logo=gitlab&logoColor=white" alt="GitLab CI/CD"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/ArgoCD-EF7B4D?style=for-the-badge&logo=argo&logoColor=white" alt="ArgoCD"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=helm&logoColor=white" alt="Helm"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" alt="Terraform"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white" alt="Ansible"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" alt="Prometheus"></div>
                <div class="skill-badge"><img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Grafana"></div>
            </div>
        </div>

        <!-- Featured Projects Section -->
        <div class="section">
            <h2 class="section-title">🚀 Featured Projects</h2>
            
            <div class="project-card">
                <div class="project-title">CareVault Healthcare App</div>
                <div class="project-links">
                    <a href="https://github.com/raunak-choudhary/CareVault_Frontend_Repo" class="project-btn btn-frontend">Frontend Repo</a>
                    <a href="https://github.com/raunak-choudhary/CareVault_Backend_Repo" class="project-btn btn-backend">Backend Repo</a>
                </div>
                <p>An AI-powered healthcare management platform designed to centralize and simplify access to personal medical data. The application enables users to upload, organize, and query medical documents through an intuitive interface, while receiving intelligent support from a Retrieval-Augmented Generation (RAG) system for document understanding and assistance. Features include document storage, appointment tracking, and AI-powered health query responses.</p>
                <p><strong>Tech Stack:</strong> React.js, Python, Supabase, PostgreSQL, RAG System, File Storage Buckets</p>
            </div>

            <div class="project-card">
                <div class="project-title">Adversarial Attacks on ResNet and DenseNet</div>
                <div class="project-links">
                    <a href="https://github.com/raunak-choudhary/DeepModel-AdversarialAttacks-ResNet-DenseNet" class="project-btn btn-ml">Adversarial Attacks</a>
                </div>
                <p>A comprehensive research project evaluating and enhancing adversarial attacks on deep neural network image classifiers. Implements multiple attack strategies including FGSM, PGD, MI-FGSM, and Patch attacks against pre-trained ResNet-34 and DenseNet-121 models on ImageNet subset. Achieved significant performance degradation (ResNet-34 accuracy dropped from 77.40% to 0.00% with PGD) and analyzed attack transferability across different architectures.</p>
                <p><strong>Tech Stack:</strong> PyTorch, TorchVision, NumPy, Matplotlib, Pillow, Jupyter Notebook, ImageNet Dataset</p>
            </div>

            <div class="project-card">
                <div class="project-title">RoBERTa-LoRA News Classification</div>
                <div class="project-links">
                    <a href="https://github.com/raunak-choudhary/RoBERTa-LoRA-News-Classification" class="project-btn btn-nlp">RoBERTa LoRA</a>
                </div>
                <p>An advanced NLP project implementing Parameter-Efficient Fine-Tuning (PEFT) with Low-Rank Adaptation (LoRA) to optimize RoBERTa for AG News classification. Achieved 94.59% test accuracy using only 925,444 trainable parameters (0.737% of total model parameters), demonstrating efficient adaptation of large language models for text classification across four news categories: World, Sports, Business, and Sci/Tech.</p>
                <p><strong>Tech Stack:</strong> Hugging Face Transformers, PyTorch, PEFT, LoRA, AG News Dataset, Python</p>
            </div>

            <div class="project-card">
                <div class="project-title">Shark Tank US Investment Prediction</div>
                <div class="project-links">
                    <a href="https://github.com/raunak-choudhary/Shark-Tank-US-Investment-Prediction-ML" class="project-btn btn-ml">Shark Tank ML</a>
                </div>
                <p>A comprehensive machine learning project analyzing 1,365 startup pitches from all 16 seasons of Shark Tank US to predict investment likelihood and amounts. Utilizes advanced techniques including text embeddings via OpenAI models, SMOTE for class imbalance, and ensemble methods. Features shark-specific prediction models, industry preference analysis, and achieves superior performance with XGBoost for both classification and regression tasks.</p>
                <p><strong>Tech Stack:</strong> Python, XGBoost, Random Forest, SVM, OpenAI Embeddings, SMOTE, PCA, t-SNE, Pandas, scikit-learn</p>
            </div>

            <div class="project-card">
                <div class="project-title">SynergyPro - Productivity Platform</div>
                <div class="project-links">
                    <a href="https://github.com/raunak-choudhary/SynergyPro_NYU_SE_Project" class="project-btn btn-repo">SynergyPro</a>
                </div>
                <p>A hybrid productivity platform designed for task management and personalized study scheduling for professionals and students. Features include individual and team dashboards, calendar integration, real-time collaboration, file upload with version control, analytics with visual insights, and a help center with task management guides. Supports both individual workflow optimization and team project coordination.</p>
                <p><strong>Tech Stack:</strong> React.js, JavaScript, HTML, CSS, SQL, Bootstrap, Django, Python</p>
            </div>

            <div class="project-card">
                <div class="project-title">TapShip - Agricultural E-Marketplace</div>
                <div class="project-links">
                    <a href="https://github.com/raunak-choudhary/Tapship_Undergrad_Final_Project" class="project-btn btn-orange">TapShip</a>
                </div>
                <p>A full-stack web-based agricultural e-marketplace platform connecting farmers, customers, and transport drivers to eliminate middlemen and ensure fair crop pricing. Features include crop listing and bidding system, real-time price analytics, weather forecasts, OTP verification, SQL injection protection, and location-based recommendations using machine learning. Won first place at the I2CONECCT-2021 Project Competition.</p>
                <p><strong>Tech Stack:</strong> HTML, CSS, JavaScript, Bootstrap, PHP, Python, MySQL, XAMPP, Bing Maps API, OpenWeatherMap API, Twilio OTP</p>
            </div>
        </div>

        <!-- Achievements Section -->
        <div class="section">
            <h2 class="section-title">🏆 Achievements & Awards</h2>
            <div class="achievements-grid">
                <div class="achievement-card">
                    <div class="achievement-badge">🏆</div>
                    <div class="achievement-title">'I2CONECCT-2021' Project Competition</div>
                    <p><strong>Project:</strong> "TapShip - Tap to Ship"</p>
                    <p>An innovative shipping solution that won first place at the I2CONECCT-2021 Project Competition and Exhibition. The application streamlined shipping processes with a user-friendly mobile interface and real-time tracking capabilities.</p>
                </div>
                
                <div class="achievement-card">
                    <div class="achievement-badge">🥈</div>
                    <div class="achievement-title">IIoT (Industrial Internet of Things) - 2019</div>
                    <p><strong>Project:</strong> "Smart Energy Meter"</p>
                    <p>Developed an IoT-enabled smart energy monitoring system that provides real-time electricity consumption data and analytics, helping users optimize their energy usage and reduce costs.</p>
                </div>
                
                <div class="achievement-card">
                    <div class="achievement-badge">⭐</div>
                    <div class="achievement-title">TCS Star of the Quarter (July-September 2023)</div>
                    <p>Recognized for exceptional contributions to a critical project, meeting stringent licensing requirements, and delivering a 30% improvement in project compliance and efficiency.</p>
                </div>
                
                <div class="achievement-card">
                    <div class="achievement-badge">📊</div>
                    <div class="achievement-title">TCS Performance Recognition</div>
                    <p>Rated in the top 10% of professionals at my level by the manager and supervisor, reflecting consistent high performance and reliability in AWS infrastructure development and management.</p>
                </div>
            </div>
        </div>

        <!-- Certifications Section -->
        <div class="section">
            <h2 class="section-title">📜 Certifications & Badges</h2>
            
            <h3 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5); margin: 25px 0 15px 0; text-align: center;">AWS Certifications</h3>
            <div class="cert-grid">
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #FF9900, #FF7700); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 12px;">AWS Cloud Practitioner Badge</div>
                    </div>
                    <h4 style="color: #FF9900; margin: 10px 0;">AWS Certified Cloud Practitioner</h4>
                    <a href="#" class="cert-btn">View Certificate</a>
                </div>
                
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #FF9900, #FF7700); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 12px;">AWS Data Analytics Badge</div>
                    </div>
                    <h4 style="color: #FF9900; margin: 10px 0;">AWS Certified Data Analytics Specialty</h4>
                    <a href="#" class="cert-btn">View Certificate</a>
                </div>
            </div>

            <h3 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5); margin: 25px 0 15px 0; text-align: center;">Microsoft Technology Associate (MTA) Certifications</h3>
            <div class="cert-grid">
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #0078D4, #106EBE); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 10px;">MTA HTML5 Badge</div>
                    </div>
                    <h4 style="color: #0078D4; margin: 10px 0;">MTA: HTML5 Application Development Fundamentals</h4>
                    <a href="#" class="cert-btn" style="background: linear-gradient(45deg, #0078D4, #106EBE); border-color: #0078D4;">View Certificate</a>
                </div>
                
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #0078D4, #106EBE); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 12px;">MTA Networking</div>
                    </div>
                    <h4 style="color: #0078D4; margin: 10px 0;">MTA: Networking Fundamentals (98-366)</h4>
                    <a href="#" class="cert-btn" style="background: linear-gradient(45deg, #0078D4, #106EBE); border-color: #0078D4;">View Certificate</a>
                </div>
                
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #0078D4, #106EBE); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 12px;">MTA Python</div>
                    </div>
                    <h4 style="color: #0078D4; margin: 10px 0;">MTA: Python Programming (98-381)</h4>
                    <a href="#" class="cert-btn" style="background: linear-gradient(45deg, #0078D4, #106EBE); border-color: #0078D4;">View Certificate</a>
                </div>
            </div>

            <h3 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5); margin: 25px 0 15px 0; text-align: center;">NYU Tandon LeetCode Bootcamp</h3>
            <div style="text-align: center; margin: 20px 0;">
                <div class="cert-image" style="display: inline-block; width: 180px; height: 180px; margin: 0 auto;">
                    <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #5B2C6F, #7B3F98); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 12px; border-radius: 10px;">NYU LeetCode Bootcamp Badge</div>
                </div>
                <h4 style="color: #5B2C6F; margin: 10px 0;">Competitive Programming & DSA Excellence</h4>
            </div>

            <h3 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5); margin: 25px 0 15px 0; text-align: center;">Professional Recognition</h3>
            <div style="text-align: center; margin: 20px 0;">
                <div class="cert-image" style="display: inline-block; width: 250px; height: 180px; margin: 0 auto;">
                    <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #FFD700, #FFA500); display: flex; align-items: center; justify-content: center; color: #000; font-weight: bold; text-align: center; font-size: 12px; border-radius: 10px;">TCS Star Award Certificate</div>
                </div>
                <h4 style="color: #FFD700; margin: 10px 0;">TCS Star of the Quarter (Q3 2023)</h4>
                <p style="font-style: italic; margin: 0;">For exceptional contributions to a critical project, meeting stringent licensing requirements, and delivering a 30% improvement in project compliance and efficiency.</p>
            </div>
        </div>

        <!-- Professional Internships Section -->
        <div class="section">
            <h2 class="section-title">🎓 Professional Internships</h2>
            <div class="cert-grid">
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #8B5CF6, #EC4899); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 10px;">Verzeo ML Internship</div>
                    </div>
                    <h4 style="color: #8B5CF6; margin: 10px 0;">Machine Learning Internship</h4>
                    <p style="font-style: italic; margin: 5px 0;">Verzeo Edutech Ltd.</p>
                </div>
                
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #10B981, #059669); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 10px;">Great Learning Data Science</div>
                    </div>
                    <h4 style="color: #10B981; margin: 10px 0;">Data Science Internship</h4>
                    <p style="font-style: italic; margin: 5px 0;">Great Learning Pvt. Ltd.</p>
                </div>
                
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45d, #3B82F6, #1D4ED8); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 10px;">HPE CCNA Internship</div>
                    </div>
                    <h4 style="color: #3B82F6; margin: 10px 0;">CCNA Networking Internship</h4>
                    <p style="font-style: italic; margin: 5px 0;">Hewlett Packard Enterprise</p>
                </div>
                
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #F59E0B, #D97706); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 10px;">Android App Development</div>
                    </div>
                    <h4 style="color: #F59E0B; margin: 10px 0;">Android App Development Internship</h4>
                    <p style="font-style: italic; margin: 5px 0;">Azure Skynet Solutions Pvt. Ltd.</p>
                </div>
                
                <div class="cert-card">
                    <div class="cert-image">
                        <div style="width: 100%; height: 100%; background: linear-gradient(45deg, #EF4444, #DC2626); display: flex; align-items: center; justify-content: center; color: white; font-weight: bold; text-align: center; font-size: 10px;">Web Development Inmovidu</div>
                    </div>
                    <h4 style="color: #EF4444; margin: 10px 0;">Web Development Internship</h4>
                    <p style="font-style: italic; margin: 5px 0;">Inmovidu Technologies</p>
                </div>
            </div>
        </div>

        <!-- GitHub Statistics Section -->
        <div class="section">
            <h2 class="section-title">📊 GitHub Statistics & Activity</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <img src="https://github-readme-stats-git-masterrstaa-rickstaa.vercel.app/api?username=raunak-choudhary&show_icons=true&count_private=true&theme=radical&include_all_commits=true&hide_border=true" alt="Raunak's GitHub Stats" />
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-stats-git-masterrstaa-rickstaa.vercel.app/api/top-langs/?username=raunak-choudhary&layout=compact&theme=radical&hide=jupyter%20notebook&langs_count=8&hide_border=true" alt="Most Used Languages" />
                </div>
            </div>
            
            <div style="text-align: center; margin: 25px 0;">
                <div class="stat-card" style="display: inline-block;">
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=raunak-choudhary&theme=radical&hide_border=true" alt="GitHub Streak Stats" />
                </div>
            </div>

            <div style="text-align: center; margin: 25px 0;">
                <h4 style="color: #00f5ff; text-shadow: 0 0 10px rgba(0, 245, 255, 0.5);">View My Contributions</h4>
                <div class="stat-card" style="display: inline-block; width: 100%;">
                    <img src="https://github-readme-activity-graph.vercel.app/graph?username=raunak-choudhary&theme=redical&hide_border=true" alt="Raunak's GitHub Activity Graph" style="width: 100%;" />
                </div>
                
                <div style="margin: 20px 0;">
                    <p style="margin-bottom: 15px;">View contributions by time period:</p>
                    <div style="display: flex; justify-content: center; gap: 15px; flex-wrap: wrap;">
                        <a href="https://github.com/raunak-choudhary?tab=overview&from=2025-01-01&to=2025-12-31" class="social-btn" style="background: linear-gradient(45deg, #8b5cf6, #ec4899); border-color: #8b5cf6;">2025</a>
                        <a href="https://github.com/raunak-choudhary?tab=overview&from=2024-01-01&to=2024-12-31" class="social-btn" style="background: linear-gradient(45deg, #ff69b4, #ff1493); border-color: #ff69b4;">2024</a>
                        <a href="https://github.com/raunak-choudhary?tab=overview&from=2023-01-01&to=2023-12-31" class="social-btn" style="background: linear-gradient(45deg, #87ceeb, #4169e1); border-color: #87ceeb;">2023</a>
                        <a href="https://github.com/raunak-choudhary?tab=overview&from=2022-01-01&to=2022-12-31" class="social-btn" style="background: linear-gradient(45deg, #ff6347, #dc143c); border-color: #ff6347;">2022</a>
                    </div>
                </div>
            </div>

            <div style="text-align: center; margin: 25px 0;">
                <div class="stat-card" style="display: inline-block;">
                    <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical" alt="Random Dev Quote" />
                </div>
            </div>
        </div>

        <!-- Professional Goals Section -->
        <div class="section">
            <h2 class="section-title">🎯 Professional Goals</h2>
            <div class="goals-grid">
                <div class="goal-card">
                    <div class="goal-badge">🎓 Academic Goals</div>
                    <ul class="goal-list">
                        <li>Complete MS in Computer Science at NYU with distinction</li>
                        <li>Publish research papers in adversarial machine learning</li>
                        <li>Participate in academic conferences in AI/ML</li>
                        <li>Collaborate with professors on cutting-edge research</li>
                    </ul>
                </div>
                
                <div class="goal-card">
                    <div class="goal-badge technical">💻 Technical Goals</div>
                    <ul class="goal-list">
                        <li>Develop expertise in robust ML model development</li>
                        <li>Master parameter-efficient fine-tuning methods for LLMs</li>
                        <li>Create cloud-native ML deployment frameworks</li>
                        <li>Build healthcare AI applications with practical impact</li>
                    </ul>
                </div>
                
                <div class="goal-card">
                    <div class="goal-badge community">🌐 Community Goals</div>
                    <ul class="goal-list">
                        <li>Contribute to open-source ML and cloud projects</li>
                        <li>Mentor junior developers and data scientists</li>
                        <li>Participate in hackathons and coding competitions</li>
                        <li>Share knowledge through blog posts and tutorials</li>
                    </ul>
                </div>

                <div class="goal-card">
                    <div class="goal-badge career">🚀 Career Goals</div>
                    <ul class="goal-list">
                        <li>Secure a position as ML Engineer or AWS Cloud Developer</li>
                        <li>Earn additional AWS certifications (Solutions Architect)</li>
                        <li>Build a portfolio of impactful ML projects</li>
                        <li>Work on projects with measurable real-world impact</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Let's Connect Section -->
        <div class="connect-section">
            <h2 class="connect-title">🤝 Let's Connect</h2>
            <div class="connect-links">
                <a href="https://www.linkedin.com/in/raunak-choudhary" class="connect-btn btn-linkedin">
                    LinkedIn - Connect
                </a>
                <a href="mailto:raunak.choudhary@nyu.edu" class="connect-btn btn-email">
                    NYU Email - Contact
                </a>
                <a href="mailto:raunakchoudhary17@gmail.com" class="connect-btn btn-email">
                    Personal Email - Contact
                </a>
                <a href="tel:+19292894648" class="connect-btn btn-phone">
                    Phone - +1 (929) 289 4648
                </a>
                <a href="https://github.com/raunak-choudhary" class="connect-btn btn-github">
                    GitHub - Follow
                </a>
            </div>
            <p style="position: relative; z-index: 2; margin-top: 20px; font-size: 1.1rem; line-height: 1.6;">
                I'm always open to collaborating on interesting projects, research opportunities, or just discussing ideas in ML, cloud computing, and software development.
            </p>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div class="visitor-counter">
                <img src="https://komarev.com/ghpvc/?username=raunak-choudhary&color=blueviolet&style=flat-square&label=Profile+Views" alt="Profile Views">
            </div>
        </div>
    </div>

    <!-- Additional JavaScript for Enhanced Interactivity -->
    <script>
        // Enhanced particle system
        function createParticles() {
            const particleContainer = document.body;
            
            // Create more particles
            for (let i = 0; i < 15; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 6 + 's';
                particle.style.animationDuration = (Math.random() * 3 + 4) + 's';
                
                // Random colors
                const colors = [
                    'rgba(0, 245, 255, 0.8)',
                    'rgba(255, 0, 255, 0.8)',
                    'rgba(255, 255, 0, 0.8)',
                    'rgba(0, 255, 100, 0.8)',
                    'rgba(255, 100, 0, 0.8)'
                ];
                particle.style.background = colors[Math.floor(Math.random() * colors.length)];
                
                particleContainer.appendChild(particle);
            }
        }

        // Smooth scrolling for internal links
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            
            // Add hover effects to project cards
            const projectCards = document.querySelectorAll('.project-card');
            projectCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-10px) scale(1.02)';
                });
                
                card.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0) scale(1)';
                });
            });

            // Add pulse effect to social buttons
            const socialBtns = document.querySelectorAll('.social-btn, .connect-btn');
            socialBtns.forEach(btn => {
                btn.addEventListener('mouseenter', function() {
                    this.style.animation = 'pulse 0.6s ease-in-out infinite';
                });
                
                btn.addEventListener('mouseleave', function() {
                    this.style.animation = 'none';
                });
            });

            // Interactive skill badges
            const skillBadges = document.querySelectorAll('.skill-badge');
            skillBadges.forEach(badge => {
                badge.addEventListener('click', function() {
                    // Create ripple effect
                    const ripple = document.createElement('div');
                    ripple.style.position = 'absolute';
                    ripple.style.borderRadius = '50%';
                    ripple.style.background = 'rgba(0, 245, 255, 0.6)';
                    ripple.style.transform = 'scale(0)';
                    ripple.style.animation = 'ripple 0.6s linear';
                    ripple.style.left = '50%';
                    ripple.style.top = '50%';
                    ripple.style.width = '20px';
                    ripple.style.height = '20px';
                    ripple.style.marginLeft = '-10px';
                    ripple.style.marginTop = '-10px';
                    
                    this.style.position = 'relative';
                    this.appendChild(ripple);
                    
                    setTimeout(() => {
                        ripple.remove();
                    }, 600);
                });
            });

            // Typing effect for main title
            const mainTitle = document.querySelector('.main-title');
            if (mainTitle) {
                const text = mainTitle.textContent;
                mainTitle.textContent = '';
                let i = 0;
                
                function typeWriter() {
                    if (i < text.length) {
                        mainTitle.textContent += text.charAt(i);
                        i++;
                        setTimeout(typeWriter, 100);
                    }
                }
                
                setTimeout(typeWriter, 1000);
            }

            // Intersection Observer for animations
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                        
                        // Add special effects for different sections
                        if (entry.target.classList.contains('project-card')) {
                            entry.target.style.animation = 'slideInUp 0.8s ease-out';
                        } else if (entry.target.classList.contains('achievement-card')) {
                            entry.target.style.animation = 'bounceIn 0.8s ease-out';
                        } else if (entry.target.classList.contains('cert-card')) {
                            entry.target.style.animation = 'fadeInScale 0.8s ease-out';
                        }
                    }
                });
            }, observerOptions);

            // Observe all cards
            document.querySelectorAll('.project-card, .achievement-card, .cert-card, .goal-card, .stat-card').forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(30px)';
                card.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
                observer.observe(card);
            });

            // Enhanced background animation
            let mouseX = 0;
            let mouseY = 0;
            
            document.addEventListener('mousemove', (e) => {
                mouseX = e.clientX / window.innerWidth;
                mouseY = e.clientY / window.innerHeight;
                
                const bgElement = document.body;
                bgElement.style.background = `
                    linear-gradient(135deg, 
                        hsl(${240 + mouseX * 60}, 50%, ${5 + mouseY * 10}%) 0%, 
                        hsl(${260 + mouseX * 40}, 60%, ${8 + mouseY * 12}%) 25%, 
                        hsl(${220 + mouseX * 50}, 55%, ${10 + mouseY * 15}%) 50%, 
                        hsl(${200 + mouseX * 60}, 50%, ${12 + mouseY * 18}%) 75%, 
                        hsl(${280 + mouseX * 30}, 45%, ${15 + mouseY * 20}%) 100%)
                `;
            });

            // Portfolio button special animation
            const portfolioBtn = document.querySelector('.btn-portfolio');
            if (portfolioBtn) {
                setInterval(() => {
                    portfolioBtn.style.boxShadow = '0 0 30px rgba(255, 153, 0, 0.8), 0 0 60px rgba(255, 119, 0, 0.5)';
                    setTimeout(() => {
                        portfolioBtn.style.boxShadow = '0 0 20px rgba(255, 153, 0, 0.5)';
                    }, 1000);
                }, 3000);
            }
        });

        // Additional CSS animations via JavaScript
        const style = document.createElement('style');
        style.textContent = `
            @keyframes ripple {
                to {
                    transform: scale(4);
                    opacity: 0;
                }
            }
            
            @keyframes slideInUp {
                from {
                    opacity: 0;
                    transform: translateY(60px);
                }
                to {
                    opacity: 1;
                    transform: translateY(0);
                }
            }
            
            @keyframes bounceIn {
                0% {
                    opacity: 0;
                    transform: scale(0.3);
                }
                50% {
                    transform: scale(1.05);
                }
                70% {
                    transform: scale(0.9);
                }
                100% {
                    opacity: 1;
                    transform: scale(1);
                }
            }
            
            @keyframes fadeInScale {
                from {
                    opacity: 0;
                    transform: scale(0.8);
                }
                to {
                    opacity: 1;
                    transform: scale(1);
                }
            }
            
            @keyframes glow {
                0%, 100% {
                    text-shadow: 0 0 5px rgba(0, 245, 255, 0.5);
                }
                50% {
                    text-shadow: 0 0 20px rgba(0, 245, 255, 1), 0 0 30px rgba(0, 245, 255, 0.8);
                }
            }
            
            .section-title {
                animation: glow 3s ease-in-out infinite;
            }
            
            /* Enhanced hover effects */
            .achievement-card:hover {
                animation: bounceIn 0.6s ease-out;
            }
            
            .cert-card:hover .cert-image {
                transform: rotateY(15deg) scale(1.1);
                transition: transform 0.4s ease;
            }
            
            .goal-card:hover .goal-badge {
                transform: scale(1.1);
                transition: transform 0.3s ease;
            }
            
            /* Responsive enhancements */
            @media (max-width: 768px) {
                .particle {
                    display: none;
                }
                
                .main-title {
                    font-size: 2rem;
                }
                
                .connect-links {
                    flex-direction: column;
                    align-items: center;
                }
                
                .connect-btn {
                    width: 80%;
                    max-width: 300px;
                    margin: 5px 0;
                }
                
                .social-links {
                    flex-direction: column;
                    align-items: center;
                }
                
                .social-btn {
                    width: 80%;
                    max-width: 250px;
                    margin: 5px 0;
                }
            }
            
            /* Special effects for portfolio button */
            .btn-portfolio::after {
                content: '⚡';
                margin-left: 8px;
                animation: pulse 1.5s ease-in-out infinite;
            }
            
            /* Enhanced glassmorphism for connect section */
            .connect-section {
                background: 
                    linear-gradient(135deg, rgba(255, 255, 255, 0.1) 0%, rgba(255, 255, 255, 0.05) 100%),
                    radial-gradient(circle at 30% 30%, rgba(0, 245, 255, 0.1) 0%, transparent 50%),
                    radial-gradient(circle at 70% 70%, rgba(255, 0, 255, 0.1) 0%, transparent 50%);
                backdrop-filter: blur(20px);
                border: 2px solid rgba(255, 255, 255, 0.2);
                box-shadow: 
                    0 25px 50px rgba(0, 0, 0, 0.4),
                    inset 0 1px 0 rgba(255, 255, 255, 0.2);
            }
            
            /* Footer enhancements */
            .footer {
                background: rgba(0, 0, 0, 0.5);
                backdrop-filter: blur(10px);
                border-top: 1px solid rgba(0, 245, 255, 0.3);
                position: relative;
            }
            
            .footer::before {
                content: '';
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                height: 1px;
                background: linear-gradient(90deg, transparent, #00f5ff, transparent);
                animation: scanline 3s ease-in-out infinite;
            }
            
            .visitor-counter {
                transition: all 0.3s ease;
            }
            
            .visitor-counter:hover {
                transform: scale(1.1);
                box-shadow: 0 0 25px rgba(139, 92, 246, 0.8);
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
                

                
