# mi-magic1
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MI-MAGIC | Opportunistic Salpingectomy (OBS) Education</title>
    <style>
        /* --- CSS VARIABLES & RESET --- */
        :root {
            --teal-primary: #008080;
            --teal-dark: #006666;
            --teal-light: #e6f2f2;
            --um-blue: #00274c;
            --text-color: #333;
            --text-light: #666;
            --white: #ffffff;
            --border-color: #ccc;
            --focus-outline: #ffcb05; /* U-M Maize for focus */
        }
        * { box-sizing: border-box; }
        body {
            font-family: sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            margin: 0;
            padding: 0;
            scroll-behavior: smooth;
        }
        /* --- ACCESSIBILITY --- */
        .skip-link {
            position: absolute;
            top: -40px;
            left: 0;
            background: var(--um-blue);
            color: white;
            padding: 8px;
            z-index: 1001;
            text-decoration: none;
        }
        .skip-link:focus { top: 0; }     
        :focus {
            outline: 3px solid var(--focus-outline);
            outline-offset: 2px;
        }
        /* --- LAYOUT --- */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }
        section {
            padding: 80px 0;
            border-bottom: 1px solid var(--teal-light);
        }
        /* --- HEADER & NAV --- */
        header {
            background: var(--white);
            border-bottom: 3px solid var(--teal-primary);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        .nav-wrapper {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
        }
        .logo-img { height: 50px; width: auto; }
        nav ul {
            display: flex;
            list-style: none;
            margin: 0;
            padding: 0;
        }
        nav ul li { margin-left: 15px; }
        nav ul li a {
            text-decoration: none;
            color: var(--um-blue);
            font-weight: bold;
            font-size: 0.9rem;
            padding: 5px 8px;
        }
        nav ul li a:hover, nav ul li a.active {
            color: var(--teal-primary);
        }
        .mobile-toggle {
            display: none;
            background: var(--teal-primary);
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
        }
        /* --- HERO --- */
        .hero {
            background-color: var(--teal-light);
            text-align: center;
            padding: 120px 20px 80px;
        }
        .hero h1 { font-size: 2.5rem; color: var(--um-blue); margin-bottom: 10px; }
        .hero p { font-size: 1.2rem; max-width: 700px; margin: 0 auto 30px; }
        .cta-group { display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; }
        .btn {
            padding: 15px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background 0.3s;
        }
        .btn-primary { background: var(--teal-primary); color: white; }
        .btn-primary:hover { background: var(--teal-dark); }
        .btn-secondary { background: var(--um-blue); color: white; }
        .btn-secondary:hover { opacity: 0.9; }
        /* --- COMPONENTS --- */
        .video-placeholder {
            background: #000;
            color: #fff;
            aspect-ratio: 16/9;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin: 20px 0;
            border: 4px solid var(--teal-primary);
        }
        .qr-placeholder { width: 120px; height: 120px; border: 1px solid var(--border-color); }
        .callout-box {
            background: var(--teal-light);
            border-left: 5px solid var(--teal-primary);
            padding: 20px;
            margin: 20px 0;
            display: flex;
            align-items: center;
            gap: 20px;
        }
        /* --- FAQ ACCORDION --- */
        .faq-item { border-bottom: 1px solid var(--border-color); }
        .faq-question {
            width: 100%;
            text-align: left;
            padding: 15px;
            background: none;
            border: none;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
        }
        .faq-answer {
            padding: 0 15px;
            display: none;
            color: var(--text-light);
        }
        .faq-answer.show { display: block; padding-bottom: 15px; }
        /* --- FORMS --- */
        .contact-form {
            display: grid;
            gap: 15px;
            max-width: 600px;
        }
        .contact-form input, .contact-form select, .contact-form textarea {
            padding: 10px;
            border: 1px solid var(--border-color);
            width: 100%;
        }
        /* --- FOOTER --- */
        footer {
            background: var(--um-blue);
            color: white;
            padding: 40px 0;
            text-align: center;
        }
        footer a { color: var(--teal-light); }
        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            .nav-wrapper { flex-direction: column; height: auto; padding: 10px; }
            .mobile-toggle { display: block; width: 100%; margin-top: 10px; }
            nav ul {
                display: none;
                flex-direction: column;
                width: 100%;
                text-align: center;
            }
            nav ul.show { display: flex; }
            nav ul li { margin: 10px 0; }
            .hero h1 { font-size: 1.8rem; }
            .callout-box { flex-direction: column; text-align: center; }
        }
    </style>
</head>
<body>
    <a href="#main-content" class="skip-link">Skip to main content</a>
    <header role="banner">
        <div class="container nav-wrapper">
            <img src="assets/mi-magic-logo.png" alt="MI-MAGIC logo" class="logo-img">
            <button class="mobile-toggle" aria-expanded="false" aria-controls="main-nav">Menu</button>
            <nav id="main-nav" role="navigation">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#patients">Patients</a></li>
                    <li><a href="#providers">Providers</a></li>
                    <li><a href="#resources">Resources</a></li>
                    <li><a href="#faq">FAQ</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#legal">Terms & Privacy</a></li>
                </ul>
            </nav>
        </div>
    </header>
    <main id="main-content">
        <section id="home" class="hero">
            <div class="container">
                <h1>MI-MAGIC: Education on Opportunistic Salpingectomy (OBS)</h1>
                <p>An educational initiative providing patient-centered resources and clinician training for the removal of fallopian tubes to reduce cancer risk.</p>
                <div class="cta-group">
                    <a href="#patients" class="btn btn-primary">Patient resources</a>
                    <a href="#providers" class="btn btn-secondary">Clinician/Provider resources</a>
                </div>
            </div>
        </section>
        <section id="patients">
            <div class="container">
                <h2>Patient Education</h2>
                <div class="content-grid">
                    <div>
                        <h3>The Role of Ovaries and Fallopian Tubes</h3>
                        <p>Ovaries produce hormones and release eggs. Fallopian tubes are the pathways that connect the ovaries to the uterus. Recent research suggests that many "ovarian" cancers actually begin in the fallopian tubes.</p>                   
                        <h3>What is OBS?</h3>
                        <p><strong>Opportunistic Salpingectomy (OBS)</strong> is the surgical removal of the fallopian tubes during another planned pelvic surgery (like a hysterectomy or tubal ligation). This procedure is performed to potentially reduce the future risk of ovarian cancer while leaving the ovaries intact.</p>
                        <h3>Why keep the ovaries?</h3>
                        <ul>
                            <li><strong>Research-Driven:</strong> Removing tubes is currently the preferred prevention strategy while keeping healthy ovaries.</li>
                            <li><strong>Hormonal Health:</strong> Ovaries produce important hormones even after menopause; removing them can trigger or worsen menopausal symptoms.</li>
                            <li><strong>Surgical Safety:</strong> Removing ovaries increases the complexity of the surgery and potential for complications.</li>
                        </ul>
                        <h3>When OBS might not be possible</h3>
                        <p>Sometimes, a surgeon may find heavy scar tissue (adhesions) or other anatomical factors that make removing the tubes unsafe. In these cases, your surgeon will prioritize your safety over the tube removal.</p>
                    </div>
                    <div class="callout-box">
                        <div>
                            <strong>Prefer video? Watch instead.</strong>
                            <div class="video-placeholder">
                                <p>Video hosted on MI-MAGIC (placeholder)</p>
                            </div>
                        </div>
                        <div>
                            <img src="assets/qr-placeholder.png" alt="QR code to watch video on mobile" class="qr-placeholder">
                            <p><small>Scan to watch</small></p>
                        </div>
                    </div>
                    <p><strong>Download:</strong> <a href="assets/MI-MAGIC-Patient-Decision-Aid.pdf">MI-MAGIC Patient Decision Aid (PDF)</a></p>
                </div>
            </div>
        </section>
        <section id="providers">
            <div class="container">
                <h2>Clinician & Provider Resources</h2>
                <p>MI-MAGIC provides clinical guidance for incorporating OBS into surgical practice. This is an educational resource and does not constitute a formal certification.</p>            
                <div class="module-list">
                    <h3>Training Modules (Coming Soon)</h3>
                    <ul>
                        <li>Eligibility and Indications</li>
                        <li>Counseling and Shared Decision-Making</li>
                        <li>Surgical Technique and Considerations</li>
                        <li>Workflow and Implementation</li>
                    </ul>
                </div>
                <div class="callout-box">
                    <div>
                        <strong>Implementation Video</strong>
                        <div class="video-placeholder">
                            <p>Video hosted on MI-MAGIC (placeholder)</p>
                        </div>
                    </div>
                    <div>
                        <img src="assets/qr-placeholder.png" alt="QR code for provider video" class="qr-placeholder">
                        <p><small>Scan for mobile view</small></p>
                    </div>
                </div>
                <p><strong>Download:</strong> <a href="assets/MI-MAGIC-Provider-Summary.pdf">Provider Implementation Summary (PDF)</a></p>
            </div>
        </section>
        <section id="resources">
            <div class="container">
                <h2>Resource Library</h2>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px;">
                    <div style="border: 1px solid var(--border-color); padding: 20px;">
                        <h4>Patient Aid</h4>
                        <p>Printable guide for patient counseling.</p>
                        <a href="assets/MI-MAGIC-Patient-Decision-Aid.pdf">Download PDF</a>
                    </div>
                    <div style="border: 1px solid var(--border-color); padding: 20px;">
                        <h4>Provider Guide</h4>
                        <p>Clinical workflow and coding summary.</p>
                        <a href="assets/MI-MAGIC-Provider-Summary.pdf">Download PDF</a>
                    </div>
                    <div style="border: 1px solid var(--border-color); padding: 20px;">
                        <h4>Video Library</h4>
                        <p>All on-site educational videos.</p>
                        <a href="#home">View Gallery</a>
                    </div>
                </div>
                <p style="margin-top: 20px;"><small>Tip: Use your browser's <strong>Print</strong> function (Ctrl+P) to save any page as a PDF.</small></p>
            </div>
        </section>
        <section id="faq">
            <div class="container">
                <h2>Frequently Asked Questions</h2>              
                <h3>For Patients</h3>
                <div class="faq-item">
                    <button class="faq-question" aria-expanded="false">Is OBS the same as removing ovaries? <span>+</span></button>
                    <div class="faq-answer">No. OBS removes only the fallopian tubes, leaving the ovaries to continue producing hormones.</div>
                </div>
                <div class="faq-item">
                    <button class="faq-question" aria-expanded="false">Does OBS guarantee I won’t get ovarian cancer? <span>+</span></button>
                    <div class="faq-answer">No surgery can offer a 100% guarantee, but research shows that removing the tubes significantly reduces the most common types of ovarian cancer risk.</div>
                </div>
                <div class="faq-item">
                    <button class="faq-question" aria-expanded="false">What if my tubes can’t be removed? <span>+</span></button>
                    <div class="faq-answer">If surgical complications or adhesions prevent removal, your surgeon will leave the tubes to ensure your safety.</div>
                </div>
                <div class="faq-item">
                    <button class="faq-question" aria-expanded="false">Why keep ovaries? <span>+</span></button>
                    <div class="faq-answer">Ovaries are essential for bone, heart, and brain health due to the hormones they produce.</div>
                </div>
                <h3 style="margin-top: 30px;">For Providers</h3>
                <div class="faq-item">
                    <button class="faq-question" aria-expanded="false">Can providers use this nationally? <span>+</span></button>
                    <div class="faq-answer">Yes, MI-MAGIC is designed as a national educational resource, though it is headquartered at the University of Michigan.</div>
                </div>
                <div class="faq-item">
                    <button class="faq-question" aria-expanded="false">Is this medical advice? <span>+</span></button>
                    <div class="faq-answer">No. This content is for educational purposes. Clinical judgment must always be applied to individual patient cases.</div>
                </div>
            </div>
        </section>
        <section id="about">
            <div class="container">
                <h2>About MI-MAGIC</h2>
                <p>MI-MAGIC is a University of Michigan-affiliated initiative dedicated to improving ovarian cancer prevention through physician and patient education. We focus on Opportunistic Salpingectomy (OBS)—sometimes referred to internally as Bilateral Opportunistic Salpingectomy (BOS).</p>
                <p>Our mission is to provide high-quality, evidence-based tools that facilitate shared decision-making between patients and their surgical teams across the country.</p>
                <img src="assets/placeholder-diagram.png" alt="Anatomical diagram of the female reproductive system" style="max-width: 100%; height: auto;">
            </div>
        </section>
        <section id="contact">
            <div class="container">
                <h2>Contact Us</h2>
                <p><strong>Note: Do not include personal health information (PHI) in this form.</strong></p>
                <form class="contact-form">
                    <div>
                        <label for="name">Name</label>
                        <input type="text" id="name" required>
                    </div>
                    <div>
                        <label for="email">Email</label>
                        <input type="email" id="email" required>
                    </div>
                    <div>
                        <label for="role">I am a...</label>
                        <select id="role">
                            <option>Patient</option>
                            <option>Provider</option>
                            <option>Researcher</option>
                            <option>Other</option>
                        </select>
                    </div>
                    <div>
                        <label for="message">Message</label>
                        <textarea id="message" rows="5" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary" style="border:none; cursor:pointer;">Send Message</button>
                </form>
            </div>
        </section>
        <section id="legal">
            <div class="container">
                <h2>Terms of Use & Privacy</h2>
                <h3>Educational Disclaimer</h3>
                <p>The information provided on MI-MAGIC is for educational purposes only. It does not constitute medical advice and does not establish a clinician-patient relationship. Patients should consult their doctors for medical decisions. Clinicians must use their independent professional judgment. Content is subject to change as medical research evolves.</p>                
                <h3>Privacy Summary</h3>
                <p>This site collects only the data you provide via the contact form. We do not sell your data. We use basic, privacy-friendly analytics to understand site traffic. Do not submit Protected Health Information (PHI) through this website.</p>
            </div>
        </section>
    </main>
    <footer>
        <div class="container">
            <p>&copy; 2026 MI-MAGIC / University of Michigan Affiliated Initiative</p>
            <p><a href="#home">Back to top</a></p>
        </div>
    </footer>
    <script>
        // --- MOBILE NAV TOGGLE ---
        const navToggle = document.querySelector('.mobile-toggle');
        const navUl = document.querySelector('nav ul');
        navToggle.addEventListener('click', () => {
            const expanded = navToggle.getAttribute('aria-expanded') === 'true' || false;
            navToggle.setAttribute('aria-expanded', !expanded);
            navUl.classList.toggle('show');
        });
        // --- FAQ ACCORDION ---
        const faqButtons = document.querySelectorAll('.faq-question');
        faqButtons.forEach(button => {
            button.addEventListener('click', () => {
                const expanded = button.getAttribute('aria-expanded') === 'true' || false;
                button.setAttribute('aria-expanded', !expanded);              
                const answer = button.nextElementSibling;
                answer.classList.toggle('show'); 
                const icon = button.querySelector('span');
                icon.textContent = expanded ? '+' : '-';
            });
        });
        // --- ACTIVE NAV ON SCROLL ---
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('nav ul li a');
        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= (sectionTop - 100)) {
                    current = section.getAttribute('id');
                }
            });
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').includes(current)) {
                    link.classList.add('active');
                }
            });
        });
        // --- PREVENT FORM SUBMIT ---
        document.querySelector('.contact-form').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('This is a demo. In a live site, this would send your message to the MI-MAGIC team.');
        });
    </script>
</body>
</html>
