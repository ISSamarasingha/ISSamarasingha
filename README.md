<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Professional GitHub README</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-color: #ffffff;
            --text-color: #24292e;
            --card-bg: #f6f8fa;
            --border-color: #e1e4e8;
            --accent-color: #0366d6;
            --secondary-text: #586069;
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        [data-theme="dark"] {
            --bg-color: #0d1117;
            --text-color: #c9d1d9;
            --card-bg: #161b22;
            --border-color: #30363d;
            --accent-color: #58a6ff;
            --secondary-text: #8b949e;
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            transition: background-color 0.3s, color 0.3s, border-color 0.3s;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid var(--border-color);
        }

        .theme-toggle {
            display: flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
            padding: 8px 16px;
            border-radius: 20px;
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            font-size: 14px;
        }

        .theme-toggle i {
            font-size: 18px;
        }

        .profile {
            display: flex;
            gap: 30px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 3px solid var(--accent-color);
            object-fit: cover;
        }

        .profile-info {
            flex: 1;
            min-width: 300px;
        }

        .name {
            font-size: 28px;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .username {
            font-size: 20px;
            color: var(--secondary-text);
            margin-bottom: 15px;
        }

        .bio {
            margin-bottom: 20px;
            font-size: 16px;
        }

        .stats {
            display: flex;
            gap: 20px;
            margin-bottom: 20px;
        }

        .stat {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 14px;
        }

        .links {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .link {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            padding: 8px 16px;
            background-color: var(--accent-color);
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-size: 14px;
            transition: opacity 0.2s;
        }

        .link:hover {
            opacity: 0.9;
        }

        .section {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: var(--shadow);
        }

        .section-title {
            font-size: 22px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill {
            background-color: var(--bg-color);
            border: 1px solid var(--border-color);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 14px;
        }

        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }

        .project {
            background-color: var(--bg-color);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 20px;
            transition: transform 0.2s;
        }

        .project:hover {
            transform: translateY(-5px);
        }

        .project-title {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .project-description {
            font-size: 14px;
            color: var(--secondary-text);
            margin-bottom: 15px;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }

        .tech {
            font-size: 12px;
            color: var(--accent-color);
            background-color: var(--card-bg);
            padding: 4px 10px;
            border-radius: 12px;
        }

        .project-links {
            display: flex;
            gap: 15px;
        }

        .project-link {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 14px;
            color: var(--accent-color);
            text-decoration: none;
        }

        .project-link:hover {
            text-decoration: underline;
        }

        footer {
            text-align: center;
            padding: 20px;
            margin-top: 30px;
            border-top: 1px solid var(--border-color);
            color: var(--secondary-text);
            font-size: 14px;
        }

        @media (max-width: 768px) {
            .profile {
                flex-direction: column;
                align-items: center;
                text-align: center;
            }
            
            .stats, .links {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>GitHub Profile</h1>
            <div class="theme-toggle" id="themeToggle">
                <i class="fas fa-moon"></i>
                <span>Dark Mode</span>
            </div>
        </header>

        <main>
            <section class="profile">
                <img src="https://avatars.githubusercontent.com/u/583231?v=4" alt="Profile Picture" class="avatar">
                <div class="profile-info">
                    <h1 class="name">Alex Johnson</h1>
                    <p class="username">alexjohnson-dev</p>
                    <p class="bio">Full Stack Developer | Open Source Enthusiast | Tech Blogger</p>
                    <div class="stats">
                        <div class="stat">
                            <i class="fas fa-map-marker-alt"></i>
                            <span>San Francisco, CA</span>
                        </div>
                        <div class="stat">
                            <i class="fas fa-users"></i>
                            <span>25 followers</span>
                        </div>
                        <div class="stat">
                            <i class="fas fa-heart"></i>
                            <span>12 following</span>
                        </div>
                    </div>
                    <div class="links">
                        <a href="#" class="link">
                            <i class="fas fa-envelope"></i>
                            <span>Email</span>
                        </a>
                        <a href="#" class="link">
                            <i class="fab fa-twitter"></i>
                            <span>Twitter</span>
                        </a>
                        <a href="#" class="link">
                            <i class="fab fa-linkedin"></i>
                            <span>LinkedIn</span>
                        </a>
                        <a href="#" class="link">
                            <i class="fas fa-link"></i>
                            <span>Portfolio</span>
                        </a>
                    </div>
                </div>
            </section>

            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-user"></i>
                    About Me
                </h2>
                <p>I'm a passionate software engineer with over 5 years of experience building scalable web applications. I love working with modern JavaScript frameworks and have a keen interest in cloud technologies and DevOps practices.</p>
                <p>When I'm not coding, I enjoy contributing to open source projects, writing technical articles, and mentoring aspiring developers.</p>
            </section>

            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-code"></i>
                    Skills & Technologies
                </h2>
                <div class="skills">
                    <span class="skill">JavaScript</span>
                    <span class="skill">TypeScript</span>
                    <span class="skill">React</span>
                    <span class="skill">Node.js</span>
                    <span class="skill">Python</span>
                    <span class="skill">AWS</span>
                    <span class="skill">Docker</span>
                    <span class="skill">Kubernetes</span>
                    <span class="skill">PostgreSQL</span>
                    <span class="skill">MongoDB</span>
                    <span class="skill">GraphQL</span>
                    <span class="skill">Git</span>
                </div>
            </section>

            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-star"></i>
                    Featured Projects
                </h2>
                <div class="projects">
                    <div class="project">
                        <h3 class="project-title">
                            <i class="fas fa-project-diagram"></i>
                            E-Commerce Platform
                        </h3>
                        <p class="project-description">A full-stack e-commerce solution with React frontend, Node.js backend, and PostgreSQL database.</p>
                        <div class="project-tech">
                            <span class="tech">React</span>
                            <span class="tech">Node.js</span>
                            <span class="tech">PostgreSQL</span>
                            <span class="tech">Stripe API</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link">
                                <i class="fab fa-github"></i>
                                <span>Code</span>
                            </a>
                            <a href="#" class="project-link">
                                <i class="fas fa-external-link-alt"></i>
                                <span>Live Demo</span>
                            </a>
                        </div>
                    </div>
                    <div class="project">
                        <h3 class="project-title">
                            <i class="fas fa-chart-line"></i>
                            Data Visualization Dashboard
                        </h3>
                        <p class="project-description">Interactive dashboard for visualizing complex datasets with real-time updates.</p>
                        <div class="project-tech">
                            <span class="tech">D3.js</span>
                            <span class="tech">Vue.js</span>
                            <span class="tech">Express</span>
                            <span class="tech">MongoDB</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link">
                                <i class="fab fa-github"></i>
                                <span>Code</span>
                            </a>
                            <a href="#" class="project-link">
                                <i class="fas fa-external-link-alt"></i>
                                <span>Live Demo</span>
                            </a>
                        </div>
                    </div>
                    <div class="project">
                        <h3 class="project-title">
                            <i class="fas fa-mobile-alt"></i>
                            Task Management App
                        </h3>
                        <p class="project-description">Cross-platform mobile application for task management with offline capabilities.</p>
                        <div class="project-tech">
                            <span class="tech">React Native</span>
                            <span class="tech">Firebase</span>
                            <span class="tech">Redux</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link">
                                <i class="fab fa-github"></i>
                                <span>Code</span>
                            </a>
                            <a href="#" class="project-link">
                                <i class="fas fa-external-link-alt"></i>
                                <span>Live Demo</span>
                            </a>
                        </div>
                    </div>
                </div>
            </section>

            <section class="section">
                <h2 class="section-title">
                    <i class="fas fa-graduation-cap"></i>
                    Education & Certifications
                </h2>
                <p><strong>Bachelor of Science in Computer Science</strong> - Stanford University (2014-2018)</p>
                <p><strong>AWS Certified Solutions Architect</strong> - Amazon Web Services (2020)</p>
                <p><strong>Google Cloud Professional Developer</strong> - Google Cloud (2021)</p>
            </section>
        </main>

        <footer>
            <p>© 2023 Alex Johnson. Made with <i class="fas fa-heart" style="color: #e25555;"></i> and GitHub Pages.</p>
            <p style="margin-top: 10px;">
                <i class="fas fa-eye"></i> 
                <span id="viewCount">0</span> profile views
            </p>
        </footer>
    </div>

    <script>
        // Theme toggle functionality
        const themeToggle = document.getElementById('themeToggle');
        const themeIcon = themeToggle.querySelector('i');
        const themeText = themeToggle.querySelector('span');
        
        // Check for saved theme preference or default to light
        const currentTheme = localStorage.getItem('theme') || 'light';
        document.documentElement.setAttribute('data-theme', currentTheme);
        updateThemeToggle(currentTheme);
        
        themeToggle.addEventListener('click', () => {
            const currentTheme = document.documentElement.getAttribute('data-theme');
            const newTheme = currentTheme === 'light' ? 'dark' : 'light';
            
            document.documentElement.setAttribute('data-theme', newTheme);
            localStorage.setItem('theme', newTheme);
            updateThemeToggle(newTheme);
        });
        
        function updateThemeToggle(theme) {
            if (theme === 'dark') {
                themeIcon.className = 'fas fa-sun';
                themeText.textContent = 'Light Mode';
            } else {
                themeIcon.className = 'fas fa-moon';
                themeText.textContent = 'Dark Mode';
            }
        }
        
        // Simple view counter (for demo purposes)
        let viewCount = localStorage.getItem('viewCount') || 0;
        viewCount = parseInt(viewCount) + 1;
        localStorage.setItem('viewCount', viewCount);
        document.getElementById('viewCount').textContent = viewCount;
    </script>
</body>
</html>
