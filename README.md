
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sherif Malik Yussif</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            text-align: center;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            transform: translateY(0);
            transition: all 0.3s ease;
        }

        header:hover {
            transform: translateY(-5px);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.15);
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(45deg, #667eea, #764ba2);
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
            color: white;
            font-weight: bold;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subtitle {
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 20px;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .contact-item {
            background: rgba(102, 126, 234, 0.1);
            padding: 10px 20px;
            border-radius: 25px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            background: rgba(102, 126, 234, 0.2);
            transform: translateY(-2px);
        }

        .section {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .section:hover {
            transform: translateY(-3px);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
        }

        .section h2 {
            font-size: 2rem;
            margin-bottom: 25px;
            color: #333;
            position: relative;
            padding-bottom: 10px;
        }

        .section h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        .education-item, .position-item {
            background: rgba(102, 126, 234, 0.05);
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 20px;
            border-left: 4px solid #667eea;
            transition: all 0.3s ease;
        }

        .education-item:hover, .position-item:hover {
            background: rgba(102, 126, 234, 0.1);
            transform: translateX(10px);
        }

        .education-item h3, .position-item h3 {
            color: #667eea;
            margin-bottom: 10px;
            font-size: 1.3rem;
        }

        .institution {
            font-weight: 600;
            color: #333;
            margin-bottom: 5px;
        }

        .positions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .position-category {
            background: rgba(118, 75, 162, 0.05);
            padding: 20px;
            border-radius: 15px;
            border-left: 4px solid #764ba2;
        }

        .position-category h4 {
            color: #764ba2;
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .position-list {
            list-style: none;
        }

        .position-list li {
            padding: 8px 0;
            padding-left: 20px;
            position: relative;
            transition: all 0.3s ease;
        }

        .position-list li::before {
            content: '▶';
            position: absolute;
            left: 0;
            color: #764ba2;
            font-size: 0.8rem;
        }

        .position-list li:hover {
            color: #667eea;
            transform: translateX(5px);
        }

        .cta-section {
            text-align: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 20px;
            padding: 40px;
        }

        .cta-section h2 {
            color: white;
            margin-bottom: 20px;
        }

        .cta-section h2::after {
            background: white;
        }

        .btn {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid rgba(255, 255, 255, 0.3);
            margin: 10px;
        }

        .btn:hover {
            background: white;
            color: #667eea;
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }
            
            header {
                padding: 30px 20px;
            }
            
            .section {
                padding: 30px 20px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .contact-info {
                flex-direction: column;
                align-items: center;
            }
            
            .positions-grid {
                grid-template-columns: 1fr;
            }
        }

        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .floating-circle {
            position: absolute;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            animation: float 6s ease-in-out infinite;
        }

        .floating-circle:nth-child(1) {
            width: 100px;
            height: 100px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .floating-circle:nth-child(2) {
            width: 60px;
            height: 60px;
            top: 60%;
            right: 10%;
            animation-delay: 2s;
        }

        .floating-circle:nth-child(3) {
            width: 80px;
            height: 80px;
            bottom: 20%;
            left: 20%;
            animation-delay: 4s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-circle"></div>
        <div class="floating-circle"></div>
        <div class="floating-circle"></div>
    </div>

    <div class="container">
        <header>
            <div class="profile-img">SM</div>
            <h1>Sherif Malik Yussif</h1>
            <p class="subtitle">Biomedical Engineering Student | Future Surgeon General | University of Ghana, Legon</p>
            <div class="contact-info">
                <div class="contact-item">📧 Maliksherif09@gmail.com</div>
                <div class="contact-item">🎓 University of Ghana, Legon</div>
                <div class="contact-item">🏫 Prempeh College Alumni</div>
                <div class="position-category">
                    <h4>Community Service</h4>
                    <ul class="position-list">
                        <li>Health Advocacy</li>
                        <li>Emergency Response (Red Cross)</li>
                        <li>Youth Development</li>
                        <li>Student Mentoring</li>
                    </ul>
                </div>
            </div>
        </header>

        <div class="section">
            <h2>Education</h2>
            <div class="education-item">
                <h3>Biomedical Engineering</h3>
                <div class="institution">University of Ghana, Legon</div>
                <p>Currently pursuing a degree in Biomedical Engineering with the aspiration to become a Surgeon General, combining engineering principles with medical applications.</p>
            </div>
            <div class="education-item">
                <h3>Junior High School</h3>
                <div class="institution">Martin Luther King Jr School</div>
                <p>Completed junior high education while actively participating in sports and leadership activities.</p>
            </div>
            <div class="education-item">
                <h3>High School</h3>
                <div class="institution">Prempeh College</div>
                <p>Completed secondary education at this renowned institution, known for academic excellence and leadership development.</p>
            </div>
        </div>

        <div class="section">
            <h2>Leadership Experience</h2>
            <div class="positions-grid">
                <div class="position-category">
                    <h4>High School Leadership (Prempeh College)</h4>
                    <ul class="position-list">
                        <li>Health Prefect</li>
                        <li>Dispensary Prefect</li>
                        <li>Advisor to the Health Club</li>
                        <li>Red Cross Society Member</li>
                        <li>School Cadet Member</li>
                        <li>House Athletics Representative - Ramseyer House (Running)</li>
                    </ul>
                </div>
                <div class="position-category">
                    <h4>Junior School Leadership (Martin Luther King Jr School)</h4>
                    <ul class="position-list">
                        <li>School Cadet Member</li>
                        <li>Sports Prefect</li>
                        <li>Athletics Team Member</li>
                        <li>Football Team Member</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>Professional Experience</h2>
            <div class="education-item">
                <h3>Education Consultant</h3>
                <div class="institution">Independent Consultant</div>
                <p>Assist students with university admission processes for both local and international institutions, providing guidance on applications, requirements, and opportunities for studying overseas.</p>
            </div>
            <div class="education-item">
                <h3>Dispatch Officer</h3>
                <div class="institution">Wordsworthy Press and Packaging Ltd</div>
                <p>Managed dispatch operations, coordinating deliveries and ensuring efficient logistics processes. Developed strong organizational skills and attention to detail in a fast-paced industrial environment.</p>
            </div>
        </div>

        <div class="section">
            <h2>Current Projects & Interests</h2>
            <div class="education-item">
                <h3>YouTube Content Creator</h3>
                <div class="institution">Digital Media</div>
                <p>Managing and creating content for my YouTube channel, developing skills in video production, audience engagement, and digital marketing.</p>
            </div>
            <div class="education-item">
                <h3>Cryptocurrency Research</h3>
                <div class="institution">Self-Directed Learning</div>
                <p>Actively studying cryptocurrency markets and blockchain technology, focusing on Bitcoin and Ethereum. Staying current with digital finance trends and investment strategies.</p>
            </div>
        </div>

        <div class="section">
            <h2>Career Aspirations</h2>
            <div class="education-item">
                <h3>Future Surgeon General</h3>
                <div class="institution">Long-term Goal</div>
                <p>My ultimate career aspiration is to become a Surgeon General, combining my biomedical engineering background with medical expertise to serve in the highest levels of healthcare leadership and public health policy.</p>
            </div>
        </div>

        <div class="section">
            <h2>Skills & Interests</h2>
            <div class="positions-grid">
                <div class="position-category">
                    <h4>Leadership & Management</h4>
                    <ul class="position-list">
                        <li>Team Leadership</li>
                        <li>Health & Safety Management</li>
                        <li>Student Mentoring</li>
                        <li>Event Organization</li>
                    </ul>
                </div>
                <div class="position-category">
                    <h4>Professional Skills</h4>
                    <ul class="position-list">
                        <li>Education Consulting & Admissions Guidance</li>
                        <li>International Student Advisory</li>
                        <li>Dispatch & Logistics Management</li>
                        <li>Content Creation & Video Production</li>
                        <li>Cryptocurrency & Blockchain Analysis</li>
                        <li>Digital Marketing</li>
                    </ul>
                </div>
                <div class="position-category">
                    <h4>Technical Skills</h4>
                    <ul class="position-list">
                        <li>Biomedical Engineering Principles</li>
                        <li>Healthcare Technology</li>
                        <li>Research & Analysis</li>
                        <li>Video Production</li>
                        <li>Cryptocurrency Trading</li>
                        <li>Public Health Understanding</li>
                    </ul>
                </div>
                <div class="position-category">
                    <h4>Athletics & Sports</h4>
                    <ul class="position-list">
                        <li>Track & Field (Running)</li>
                        <li>House Athletics Representative</li>
                        <li>Football Team Member (Junior High)</li>
                        <li>Sports Leadership & Coordination</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="section cta-section">
            <h2>Let's Connect</h2>
            <p>I'm always open to new opportunities, collaborations, and meaningful connections. Whether you're interested in discussing leadership, health advocacy, or academic pursuits, I'd love to hear from you.</p>
            <a href="mailto:Maliksherif09@gmail.com" class="btn">Send Email</a>
            <a href="#" class="btn">Download CV</a>
        </div>
    </div>

    <script>
        // Add smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(section);
        });

        // Add typing effect to the title
        function typeWriter(element, text, speed = 100) {
            let i = 0;
            element.innerHTML = '';
            function type() {
                if (i < text.length) {
                    element.innerHTML += text.charAt(i);
                    i++;
                    setTimeout(type, speed);
                }
            }
            type();
        }

        // Initialize typing effect
        window.addEventListener('load', () => {
            const title = document.querySelector('h1');
            const originalText = title.textContent;
            typeWriter(title, originalText, 150);
        });
    </script>
</body>
</html>
