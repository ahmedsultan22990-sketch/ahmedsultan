<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>سيرتي الذاتية</title>
    <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --text-color: #333;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f7fa;
            color: var(--text-color);
            line-height: 1.6;
        }

        .resume-container {
            max-width: 1000px;
            margin: 30px auto;
            background: white;
            box-shadow: var(--shadow);
            border-radius: 10px;
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 40px;
            text-align: center;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid white;
            margin: 0 auto 20px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
        }

        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .header p {
            font-size: 1.2rem;
            opacity: 0.9;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .main-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 0;
        }

        .sidebar {
            background-color: var(--light-color);
            padding: 30px;
        }

        .content {
            padding: 30px;
        }

        .section {
            margin-bottom: 30px;
        }

        .section-title {
            color: var(--primary-color);
            border-bottom: 2px solid var(--secondary-color);
            padding-bottom: 10px;
            margin-bottom: 20px;
            font-size: 1.5rem;
        }

        .skill-item {
            margin-bottom: 15px;
        }

        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }

        .skill-bar {
            height: 8px;
            background-color: #ddd;
            border-radius: 4px;
            overflow: hidden;
        }

        .skill-level {
            height: 100%;
            background-color: var(--secondary-color);
        }

        .timeline-item {
            margin-bottom: 25px;
            position: relative;
            padding-left: 20px;
        }

        .timeline-item:before {
            content: '';
            position: absolute;
            left: 0;
            top: 5px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: var(--secondary-color);
        }

        .timeline-item:after {
            content: '';
            position: absolute;
            left: 5px;
            top: 17px;
            width: 2px;
            height: calc(100% - 12px);
            background-color: #ddd;
        }

        .timeline-item:last-child:after {
            display: none;
        }

        .timeline-date {
            color: var(--secondary-color);
            font-weight: bold;
            margin-bottom: 5px;
        }

        .timeline-title {
            font-weight: bold;
            margin-bottom: 5px;
        }

        .project-item {
            margin-bottom: 20px;
            padding: 15px;
            background-color: var(--light-color);
            border-radius: 5px;
        }

        .project-title {
            font-weight: bold;
            margin-bottom: 10px;
            color: var(--primary-color);
        }

        .project-links {
            display: flex;
            gap: 15px;
            margin-top: 10px;
        }

        .btn {
            display: inline-block;
            padding: 8px 15px;
            background-color: var(--secondary-color);
            color: white;
            text-decoration: none;
            border-radius: 4px;
            transition: background-color 0.3s;
            font-size: 0.9rem;
        }

        .btn:hover {
            background-color: var(--primary-color);
        }

        .language-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .language-level {
            color: var(--secondary-color);
            font-weight: bold;
        }

        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr;
            }
            
            .header {
                padding: 30px 20px;
            }
            
            .header h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div id="root"></div>

    <script type="text/babel">
        const { useState } = React;

        function Resume() {
            const [darkMode, setDarkMode] = useState(false);

            const toggleDarkMode = () => {
                setDarkMode(!darkMode);
                document.body.style.backgroundColor = darkMode ? '#f5f7fa' : '#1a1a2e';
                document.body.style.color = darkMode ? '#333' : '#fff';
            };

            return (
                <div className={`resume-container ${darkMode ? 'dark-mode' : ''}`}>
                    <div className="header">
                        <div className="profile-img">
                            <span>👤</span>
                        </div>
                        <h1>أحمد محمد</h1>
                        <p>مطور ويب ومصمم واجهات مستخدم</p>
                        <div className="contact-info">
                            <div className="contact-item">
                                <span>📧</span>
                                <span>ahmed@example.com</span>
                            </div>
                            <div className="contact-item">
                                <span>📱</span>
                                <span>+966 55 123 4567</span>
                            </div>
                            <div className="contact-item">
                                <span>📍</span>
                                <span>الرياض، المملكة العربية السعودية</span>
                            </div>
                        </div>
                        <button 
                            className="btn" 
                            style={{marginTop: '20px', background: 'transparent', border: '1px solid white'}}
                            onClick={toggleDarkMode}
                        >
                            {darkMode ? 'الوضع النهاري' : 'الوضع الليلي'}
                        </button>
                    </div>

                    <div className="main-content">
                        <div className="sidebar">
                            <div className="section">
                                <h2 className="section-title">المهارات التقنية</h2>
                                <div className="skill-item">
                                    <div className="skill-name">
                                        <span>HTML/CSS</span>
                                        <span>95%</span>
                                    </div>
                                    <div className="skill-bar">
                                        <div className="skill-level" style={{width: '95%'}}></div>
                                    </div>
                                </div>
                                <div className="skill-item">
                                    <div className="skill-name">
                                        <span>JavaScript</span>
                                        <span>90%</span>
                                    </div>
                                    <div className="skill-bar">
                                        <div className="skill-level" style={{width: '90%'}}></div>
                                    </div>
                                </div>
                                <div className="skill-item">
                                    <div className="skill-name">
                                        <span>React</span>
                                        <span>85%</span>
                                    </div>
                                    <div className="skill-bar">
                                        <div className="skill-level" style={{width: '85%'}}></div>
                                    </div>
                                </div>
                                <div className="skill-item">
                                    <div className="skill-name">
                                        <span>Node.js</span>
                                        <span>80%</span>
                                    </div>
                                    <div className="skill-bar">
                                        <div className="skill-level" style={{width: '80%'}}></div>
                                    </div>
                                </div>
                                <div className="skill-item">
                                    <div className="skill-name">
                                        <span>Git/GitHub</span>
                                        <span>90%</span>
                                    </div>
                                    <div className="skill-bar">
                                        <div className="skill-level" style={{width: '90%'}}></div>
                                    </div>
                                </div>
                            </div>

                            <div className="section">
                                <h2 className="section-title">اللغات</h2>
                                <div className="language-item">
                                    <span>العربية</span>
                                    <span className="language-level">اللغة الأم</span>
                                </div>
                                <div className="language-item">
                                    <span>الإنجليزية</span>
                                    <span className="language-level">متقدم</span>
                                </div>
                            </div>

                            <div className="section">
                                <h2 className="section-title">الهوايات</h2>
                                <ul style={{paddingRight: '20px'}}>
                                    <li>القراءة</li>
                                    <li>البرمجة الجانبية</li>
                                    <li>السفر</li>
                                    <li>التصوير الفوتوغرافي</li>
                                </ul>
                            </div>
                        </div>

                        <div className="content">
                            <div className="section">
                                <h2 className="section-title">نبذة عني</h2>
                                <p>
                                    مطور ويب شغوف بخبرة تزيد عن 3 سنوات في تطوير واجهات المستخدم وتجربة المستخدم. 
                                    أتمتع بمهارات قوية في HTML, CSS, JavaScript و React. أسعى دائمًا لتحسين مهاراتي 
                                    وتعلم التقنيات الجديدة. أحب العمل في بيئة جماعية وأستمتع بحل المشكلات المعقدة.
                                </p>
                            </div>

                            <div className="section">
                                <h2 className="section-title">الخبرات العملية</h2>
                                <div className="timeline-item">
                                    <div className="timeline-date">2022 - الحاضر</div>
                                    <div className="timeline-title">مطور ويب أول - شركة التقنية المتقدمة</div>
                                    <p>
                                        قمت بتطوير وتصميم واجهات مستخدم تفاعلية باستخدام React و Redux. 
                                        عملت على تحسين أداء التطبيقات وزيادة سرعة تحميل الصفحات بنسبة 40%.
                                    </p>
                                </div>
                                <div className="timeline-item">
                                    <div className="timeline-date">2020 - 2022</div>
                                    <div className="timeline-title">مطور ويب - شركة الحلول الرقمية</div>
                                    <p>
                                        طورت مواقع ويب متجاوبة باستخدام HTML5, CSS3 و JavaScript. 
                                        عملت مع فريق التصميم لتحويل التصاميم إلى كود تفاعلي.
                                    </p>
                                </div>
                            </div>

                            <div className="section">
                                <h2 className="section-title">المشاريع</h2>
                                <div className="project-item">
                                    <div className="project-title">منصة التعليم الإلكتروني</div>
                                    <p>
                                        منصة تعليمية تفاعلية تقدم دورات في البرمجة وتطوير الويب. 
                                        تم تطوير الواجهة الأمامية باستخدام React وتصميم متجاوب.
                                    </p>
                                    <div className="project-links">
                                        <a href="#" className="btn">عرض المشروع</a>
                                        <a href="#" className="btn">الكود المصدري</a>
                                    </div>
                                </div>
                                <div className="project-item">
                                    <div className="project-title">تطبيق إدارة المهام</div>
                                    <p>
                                        تطبيق ويب لإدارة المهام اليومية مع إمكانية المزامنة بين الأجهزة. 
                                        تم استخدام React Hooks و Local Storage لحفظ البيانات.
                                    </p>
                                    <div className="project-links">
                                        <a href="#" className="btn">عرض المشروع</a>
                                        <a href="#" className="btn">الكود المصدري</a>
                                    </div>
                                </div>
                            </div>

                            <div className="section">
                                <h2 className="section-title">التعليم</h2>
                                <div className="timeline-item">
                                    <div className="timeline-date">2016 - 2020</div>
                                    <div className="timeline-title">بكالوريوس علوم الحاسب - جامعة الملك سعود</div>
                                    <p>تخرجت بتقدير امتياز مع مرتبة الشرف. تخصصت في تطوير الويب وتصميم واجهات المستخدم.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            );
        }

        ReactDOM.render(<Resume />, document.getElementById('root'));
    </script>
</body>
</html>
