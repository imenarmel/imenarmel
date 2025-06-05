<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EmpowerYouth Rwanda - Find Jobs. Build Skills. Grow.</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            min-height: 100vh;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
        }

        /* Header */
        .header {
            background: linear-gradient(90deg, #2c5aa0 0%, #1a365d 100%);
            color: white;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-icon {
            width: 40px;
            height: 40px;
            background: #f39c12;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 18px;
        }

        .tagline {
            font-size: 14px;
            opacity: 0.9;
            margin-left: 10px;
        }

        /* Navigation */
        .nav {
            background: #f8f9fa;
            padding: 1rem 2rem;
            border-bottom: 1px solid #e9ecef;
        }

        .nav-items {
            display: flex;
            gap: 2rem;
            align-items: center;
        }

        .nav-item {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 8px 16px;
            border-radius: 20px;
            text-decoration: none;
            color: #495057;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .nav-item:hover {
            background: #e9ecef;
            transform: translateY(-2px);
        }

        .nav-item.active {
            background: #007bff;
            color: white;
        }

        /* Main Content */
        .main-content {
            padding: 2rem;
        }

        /* Courses Section */
        .section {
            margin-bottom: 3rem;
        }

        .section-title {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 1rem;
            color: #2c5aa0;
            border-left: 4px solid #f39c12;
            padding-left: 1rem;
        }

        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .course-card {
            background: white;
            border: 1px solid #e9ecef;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .course-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }

        .course-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .course-title {
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .enroll-btn {
            background: #28a745;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 1rem;
        }

        .enroll-btn:hover {
            background: #218838;
            transform: scale(1.05);
        }

        /* Progress Section */
        .progress-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 2rem;
            border-radius: 10px;
            margin-bottom: 2rem;
        }

        .progress-bar {
            background: rgba(255,255,255,0.3);
            height: 10px;
            border-radius: 10px;
            margin: 1rem 0;
            overflow: hidden;
        }

        .progress-fill {
            background: #f39c12;
            height: 100%;
            width: 65%;
            border-radius: 10px;
            animation: progressFill 2s ease-in-out;
        }

        @keyframes progressFill {
            from { width: 0%; }
            to { width: 65%; }
        }

        .certificate-badge {
            display: inline-block;
            background: #f39c12;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 12px;
            margin-left: 10px;
        }

        /* Mentor Section */
        .mentor-card {
            background: #f8f9fa;
            border-radius: 10px;
            padding: 1.5rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .mentor-avatar {
            width: 60px;
            height: 60px;
            background: #6c757d;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
        }

        .mentor-info {
            flex: 1;
        }

        .mentor-name {
            font-weight: bold;
            margin-bottom: 0.25rem;
        }

        .meeting-info {
            display: flex;
            gap: 1rem;
            margin-top: 0.5rem;
            font-size: 14px;
        }

        .join-btn {
            background: #007bff;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .join-btn:hover {
            background: #0056b3;
            transform: scale(1.05);
        }

        /* Jobs Section */
        .jobs-grid {
            display: grid;
            gap: 1rem;
        }

        .job-card {
            background: white;
            border: 1px solid #e9ecef;
            border-radius: 8px;
            padding: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s ease;
        }

        .job-card:hover {
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            transform: translateX(5px);
        }

        .job-info {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .job-icon {
            font-size: 1.5rem;
        }

        .apply-btn {
            background: #17a2b8;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .apply-btn:hover {
            background: #138496;
            transform: scale(1.05);
        }

        /* Filters */
        .filters {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
            flex-wrap: wrap;
        }

        .filter-btn {
            background: #e9ecef;
            border: none;
            padding: 8px 16px;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .filter-btn:hover, .filter-btn.active {
            background: #007bff;
            color: white;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header {
                flex-direction: column;
                gap: 1rem;
            }

            .nav-items {
                flex-wrap: wrap;
                justify-content: center;
            }

            .main-content {
                padding: 1rem;
            }

            .mentor-card {
                flex-direction: column;
                text-align: center;
            }

            .meeting-info {
                justify-content: center;
            }
        }

        .notification-badge {
            background: #dc3545;
            color: white;
            border-radius: 50%;
            padding: 2px 6px;
            font-size: 10px;
            position: relative;
            top: -8px;
            left: -8px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header class="header">
            <div class="logo">
                <div class="logo-icon">EY</div>
                <div>
                    <strong>EmpowerYouth Rwanda</strong>
                    <div class="tagline">"Find Jobs. Build Skills. Grow."</div>
                </div>
            </div>
        </header>

        <!-- Navigation -->
        <nav class="nav">
            <div class="nav-items">
                <a href="#" class="nav-item active">
                    🔍 Search
                </a>
                <a href="#" class="nav-item">
                    🧑‍🏫 Courses
                </a>
                <a href="#" class="nav-item">
                    💼 Jobs
                </a>
                <a href="#" class="nav-item">
                    🔔 Notifications
                    <span class="notification-badge">3</span>
                </a>
                <a href="#" class="nav-item">
                    📩 Messages
                    <span class="notification-badge">2</span>
                </a>
            </div>
        </nav>

        <!-- Main Content -->
        <main class="main-content">
            <!-- Progress Section -->
            <div class="progress-section">
                <h3>Your Learning Progress</h3>
                <div class="progress-bar">
                    <div class="progress-fill"></div>
                </div>
                <p>65% Complete - Digital Marketing Course
                    <span class="certificate-badge">🏆 Certificate Ready</span>
                </p>
            </div>

            <!-- Courses Section -->
            <section class="section">
                <h2 class="section-title">Courses Available</h2>
                <div class="courses-grid">
                    <div class="course-card">
                        <div class="course-icon">💻</div>
                        <div class="course-title">Digital Marketing</div>
                        <p>Learn modern digital marketing strategies, social media management, and online advertising.</p>
                        <button class="enroll-btn">Enroll ▶</button>
                    </div>
                    <div class="course-card">
                        <div class="course-icon">🛠️</div>
                        <div class="course-title">Vocational Skills</div>
                        <p>Hands-on training in technical skills including carpentry, plumbing, and electrical work.</p>
                        <button class="enroll-btn">Enroll ▶</button>
                    </div>
                    <div class="course-card">
                        <div class="course-icon">📊</div>
                        <div class="course-title">Entrepreneurship</div>
                        <p>Build your business from the ground up with practical entrepreneurship skills.</p>
                        <button class="enroll-btn">Enroll ▶</button>
                    </div>
                </div>
            </section>

            <!-- Mentor Section -->
            <section class="section">
                <h2 class="section-title">Your Mentor</h2>
                <div class="mentor-card">
                    <div class="mentor-avatar">🧑🏿‍💼</div>
                    <div class="mentor-info">
                        <div class="mentor-name">Alice N.</div>
                        <div>Topic: Starting a business</div>
                        <div class="meeting-info">
                            <span>📅 June 10, 2PM</span>
                        </div>
                    </div>
                    <button class="join-btn">Join Meeting</button>
                </div>
                <a href="#" style="color: #007bff; text-decoration: none;">Browse More Mentors ▶</a>
            </section>

            <!-- Jobs Section -->
            <section class="section">
                <h2 class="section-title">Recommended Jobs</h2>
                <div class="jobs-grid">
                    <div class="job-card">
                        <div class="job-info">
                            <div class="job-icon">🌍</div>
                            <div>
                                <strong>Kigali Tech Intern</strong>
                                <div style="font-size: 14px; color: #6c757d;">Tech Company • Kigali</div>
                            </div>
                        </div>
                        <button class="apply-btn">Apply ▶</button>
                    </div>
                    <div class="job-card">
                        <div class="job-info">
                            <div class="job-icon">🛍️</div>
                            <div>
                                <strong>Retail Assistant</strong>
                                <div style="font-size: 14px; color: #6c757d;">Retail Store • Kigali</div>
                            </div>
                        </div>
                        <button class="apply-btn">Apply ▶</button>
                    </div>
                    <div class="job-card">
                        <div class="job-info">
                            <div class="job-icon">🧰</div>
                            <div>
                                <strong>Field Agent</strong>
                                <div style="font-size: 14px; color: #6c757d;">NGO • Various Locations</div>
                            </div>
                        </div>
                        <button class="apply-btn">Apply ▶</button>
                    </div>
                </div>
                
                <div class="filters">
                    <button class="filter-btn active">Location</button>
                    <button class="filter-btn">Skill Match</button>
                    <button class="filter-btn">Type</button>
                </div>
            </section>
        </main>
    </div>

    <script>
        // Add interactive functionality
        document.addEventListener('DOMContentLoaded', function() {
            // Navigation item clicks
            const navItems = document.querySelectorAll('.nav-item');
            navItems.forEach(item => {
                item.addEventListener('click', function(e) {
                    e.preventDefault();
                    navItems.forEach(nav => nav.classList.remove('active'));
                    this.classList.add('active');
                });
            });

            // Filter button clicks
            const filterBtns = document.querySelectorAll('.filter-btn');
            filterBtns.forEach(btn => {
                btn.addEventListener('click', function() {
                    filterBtns.forEach(filter => filter.classList.remove('active'));
                    this.classList.add('active');
                });
            });

            // Button animations
            const buttons = document.querySelectorAll('button');
            buttons.forEach(btn => {
                btn.addEventListener('click', function(e) {
                    // Create ripple effect
                    const ripple = document.createElement('span');
                    const rect = this.getBoundingClientRect();
                    const size = Math.max(rect.width, rect.height);
                    const x = e.clientX - rect.left - size / 2;
                    const y = e.clientY - rect.top - size / 2;
                    
                    ripple.style.cssText = `
                        position: absolute;
                        width: ${size}px;
                        height: ${size}px;
                        left: ${x}px;
                        top: ${y}px;
                        background: rgba(255,255,255,0.3);
                        border-radius: 50%;
                        transform: scale(0);
                        animation: ripple 0.6s linear;
                        pointer-events: none;
                    `;
                    
                    this.style.position = 'relative';
                    this.style.overflow = 'hidden';
                    this.appendChild(ripple);
                    
                    setTimeout(() => ripple.remove(), 600);
                });
            });

            // Course card hover effects
            const courseCards = document.querySelectorAll('.course-card');
            courseCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.borderColor = '#007bff';
                });
                card.addEventListener('mouseleave', function() {
                    this.style.borderColor = '#e9ecef';
                });
            });
        });

        // Add CSS for ripple animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes ripple {
                to {
                    transform: scale(4);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
