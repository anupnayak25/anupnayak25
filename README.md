<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anup Nayak - GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
            margin-bottom: 20px;
        }
        
        .header {
            text-align: center;
            padding: 40px 0;
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
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            animation: shimmer 3s infinite;
        }
        
        @keyframes shimmer {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }
        
        .profile-title {
            font-size: 3.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            animation: titleGlow 2s ease-in-out infinite alternate;
        }
        
        @keyframes titleGlow {
            from { filter: drop-shadow(0 0 10px rgba(102, 126, 234, 0.3)); }
            to { filter: drop-shadow(0 0 20px rgba(118, 75, 162, 0.5)); }
        }
        
        .typing-animation {
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 30px;
            min-height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .wave {
            animation: wave 2s infinite;
            transform-origin: 70% 70%;
            display: inline-block;
            font-size: 2rem;
        }
        
        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-10deg); }
        }
        
        .section {
            margin: 40px 0;
            padding: 30px;
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0.6));
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }
        
        .section-title {
            font-size: 2rem;
            font-weight: 600;
            color: #333;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .emoji {
            font-size: 1.5em;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .about-content {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #555;
        }
        
        .about-content li {
            margin: 10px 0;
            padding-left: 20px;
            position: relative;
        }
        
        .about-content li::before {
            content: '🚀';
            position: absolute;
            left: 0;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .stat-card {
            background: linear-gradient(135deg, #667eea, #764ba2);
            padding: 20px;
            border-radius: 15px;
            color: white;
            text-align: center;
            transform: perspective(1000px) rotateY(0deg);
            transition: transform 0.6s ease;
        }
        
        .stat-card:hover {
            transform: perspective(1000px) rotateY(10deg) translateZ(20px);
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(80px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        
        .tech-item {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            color: white;
            font-weight: 500;
            transform: scale(1);
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .tech-item:hover {
            transform: scale(1.1) rotate(5deg);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        
        .connect-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin: 20px 0;
        }
        
        .connect-btn {
            padding: 12px 25px;
            border: none;
            border-radius: 25px;
            color: white;
            font-weight: 500;
            text-decoration: none;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .connect-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }
        
        .connect-btn:hover::before {
            left: 100%;
        }
        
        .linkedin { background: linear-gradient(135deg, #0077b5, #0066cc); }
        .gmail { background: linear-gradient(135deg, #ea4335, #fbbc05); }
        .github { background: linear-gradient(135deg, #333, #666); }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .project-card {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.9), rgba(255, 255, 255, 0.7));
            padding: 25px;
            border-radius: 15px;
            border: 2px solid transparent;
            background-clip: padding-box;
            position: relative;
            transition: all 0.3s ease;
        }
        
        .project-card::before {
            content: '';
            position: absolute;
            inset: 0;
            padding: 2px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 15px;
            mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
            mask-composite: exclude;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }
        
        .quote-section {
            text-align: center;
            padding: 40px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border-radius: 15px;
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }
        
        .quote-section::before {
            content: '"';
            font-size: 8rem;
            position: absolute;
            top: -20px;
            left: 20px;
            opacity: 0.1;
            font-family: serif;
        }
        
        .quote-text {
            font-size: 1.3rem;
            font-style: italic;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }
        
        .quote-author {
            font-size: 1rem;
            opacity: 0.8;
            position: relative;
            z-index: 1;
        }
        
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            font-size: 0.9rem;
        }
        
        .animated-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        
        .animated-bg::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="2" fill="rgba(255,255,255,0.1)"/></svg>');
            animation: float 20s infinite linear;
        }
        
        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); }
            100% { transform: translateY(-100vh) rotate(360deg); }
        }
        
        .current-typing {
            color: #667eea;
            font-weight: 500;
        }
        
        .cursor {
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }
        
        @media (max-width: 768px) {
            .profile-title {
                font-size: 2.5rem;
            }
            
            .section {
                padding: 20px;
                margin: 20px 0;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
            }
            
            .connect-buttons {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="animated-bg"></div>
    
    <div class="container">
        <div class="header">
            <h1 class="profile-title">Hi <span class="wave">👋</span>, I'm Anup Nayak!</h1>
            <div class="typing-animation">
                <span class="current-typing" id="typing-text">I'm a MCA Student</span>
                <span class="cursor">|</span>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">
                <span class="emoji">👨‍💻</span>
                About Me
            </h2>
            <div class="about-content">
                <ul>
                    <li><strong>🎓 MCA Student</strong> | Passionate Software Developer</li>
                    <li><strong>👨‍💻 Full Stack Developer</strong> | I enjoy working on Web Development & Database Solutions</li>
                    <li><strong>💡 Problem Solver</strong> | I love solving real-life problems using code</li>
                    <li><strong>🚀 Always Learning</strong> | Exploring the world of Computer Science</li>
                    <li><strong>💬 Ask me about:</strong> React, Node.js, Firebase, MySQL, Flutter</li>
                    <li><strong>📫 Reach me at:</strong> mrnayak27@gmail.com</li>
                </ul>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">
                <span class="emoji">📊</span>
                GitHub Stats
            </h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <h3>Profile Views</h3>
                    <p style="font-size: 2rem; font-weight: bold;">1,234+</p>
                </div>
                <div class="stat-card">
                    <h3>Repositories</h3>
                    <p style="font-size: 2rem; font-weight: bold;">25+</p>
                </div>
                <div class="stat-card">
                    <h3>Contributions</h3>
                    <p style="font-size: 2rem; font-weight: bold;">500+</p>
                </div>
                <div class="stat-card">
                    <h3>Current Streak</h3>
                    <p style="font-size: 2rem; font-weight: bold;">30 days</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">
                <span class="emoji">🔧</span>
                Tech Stack
            </h2>
            <div class="tech-grid">
                <div class="tech-item">C</div>
                <div class="tech-item">C++</div>
                <div class="tech-item">Java</div>
                <div class="tech-item">Python</div>
                <div class="tech-item">Flutter</div>
                <div class="tech-item">Dart</div>
                <div class="tech-item">HTML</div>
                <div class="tech-item">CSS</div>
                <div class="tech-item">JavaScript</div>
                <div class="tech-item">React</div>
                <div class="tech-item">Node.js</div>
                <div class="tech-item">Express</div>
                <div class="tech-item">MySQL</div>
                <div class="tech-item">MongoDB</div>
                <div class="tech-item">Firebase</div>
                <div class="tech-item">Git</div>
                <div class="tech-item">GitHub</div>
                <div class="tech-item">Figma</div>
                <div class="tech-item">Linux</div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">
                <span class="emoji">🔗</span>
                Connect with Me
            </h2>
            <div class="connect-buttons">
                <a href="https://www.linkedin.com/in/anup-nayak-05651b25b/" class="connect-btn linkedin">
                    LinkedIn
                </a>
                <a href="mailto:mrnayak27@gmail.com" class="connect-btn gmail">
                    Gmail
                </a>
                <a href="https://github.com/mrnayak25" class="connect-btn github">
                    GitHub
                </a>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">
                <span class="emoji">📌</span>
                Featured Projects
            </h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>🔍 JobHunt4U</h3>
                    <p>A comprehensive job search platform built with modern web technologies. Features include job listings, application tracking, and employer dashboard.</p>
                    <p><strong>Tech:</strong> React, Node.js, MongoDB, Express</p>
                </div>
                <div class="project-card">
                    <h3>🏢 Career Nest</h3>
                    <p>Career guidance and mentorship platform connecting students with industry professionals. Includes video calls, scheduling, and progress tracking.</p>
                    <p><strong>Tech:</strong> Flutter, Firebase, Node.js, MySQL</p>
                </div>
                <div class="project-card">
                    <h3>📱 Portfolio Website</h3>
                    <p>Personal portfolio showcasing projects and skills with modern animations and responsive design.</p>
                    <p><strong>Tech:</strong> React, CSS3, JavaScript</p>
                </div>
            </div>
        </div>

        <div class="quote-section">
            <p class="quote-text">"The most effective debugging tool is careful thought, coupled with judiciously placed print statements."</p>
            <p class="quote-author">– Brian Kernighan</p>
        </div>

        <div class="footer">
            <p>© 2025 Anup Nayak. All Rights Reserved.</p>
            <p>Made with ❤️ and lots of ☕</p>
        </div>
    </div>

    <script>
        // Typing animation
        const typingTexts = [
            "I'm a MCA Student",
            "Learning and Exploring Computer Science",
            "I love solving real-life problems using code",
            "Let's build something awesome together!",
            "Full Stack Web Developer",
            "Database Solutions Enthusiast"
        ];
        
        let currentTextIndex = 0;
        let currentCharIndex = 0;
        let isDeleting = false;
        const typingElement = document.getElementById('typing-text');
        
        function typeText() {
            const currentText = typingTexts[currentTextIndex];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, currentCharIndex - 1);
                currentCharIndex--;
                
                if (currentCharIndex === 0) {
                    isDeleting = false;
                    currentTextIndex = (currentTextIndex + 1) % typingTexts.length;
                    setTimeout(typeText, 500);
                    return;
                }
            } else {
                typingElement.textContent = currentText.substring(0, currentCharIndex + 1);
                currentCharIndex++;
                
                if (currentCharIndex === currentText.length) {
                    isDeleting = true;
                    setTimeout(typeText, 2000);
                    return;
                }
            }
            
            setTimeout(typeText, isDeleting ? 50 : 100);
        }
        
        // Start typing animation
        setTimeout(typeText, 1000);
        
        // Add hover effects to sections
        const sections = document.querySelectorAll('.section');
        sections.forEach(section => {
            section.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-5px) scale(1.02)';
            });
            
            section.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });
        
        // Animate tech items on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationDelay = Math.random() * 0.5 + 's';
                    entry.target.style.animation = 'bounce 0.6s ease-out forwards';
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('.tech-item').forEach(item => {
            observer.observe(item);
        });
        
        // Add floating animation to emoji
        document.querySelectorAll('.emoji').forEach(emoji => {
            emoji.addEventListener('mouseenter', function() {
                this.style.animation = 'bounce 0.5s ease-in-out';
            });
            
            emoji.addEventListener('animationend', function() {
                this.style.animation = 'bounce 2s infinite';
            });
        });
    </script>
</body>
</html>
