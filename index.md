<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CardVault | Home</title>
    <style>
        :root {
            --primary-color: #24292e;
            --accent-color: #0366d6;
            --text-muted: #586069;
            --bg-color: #ffffff;
            --section-bg: #f6f8fa;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            line-height: 1.6;
            color: var(--primary-color);
            margin: 0;
            padding: 0;
            background-color: var(--bg-color);
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 40px 20px;
            text-align: center;
        }

        header {
            padding: 60px 0;
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            font-weight: 600;
        }

        p.subtitle {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-bottom: 30px;
        }

        .links-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .btn {
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 6px;
            font-weight: 500;
            transition: background-color 0.2s;
        }

        .btn-outline {
            border: 1px solid #e1e4e8;
            color: var(--accent-color);
        }

        .btn-outline:hover {
            background-color: var(--section-bg);
            border-color: var(--accent-color);
        }

        .contact-section {
            margin-top: 80px;
            padding: 40px;
            background-color: var(--section-bg);
            border-radius: 8px;
        }

        .contact-section h2 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        .email-link {
            color: var(--accent-color);
            text-decoration: none;
            font-size: 1.1rem;
            font-weight: 500;
        }

        .email-link:hover {
            text-decoration: underline;
        }

        footer {
            margin-top: 100px;
            font-size: 0.9rem;
            color: var(--text-muted);
            border-top: 1px solid #e1e4e8;
            padding-top: 20px;
        }
    </style>
</head>
<body>

    <div class="container">
        <header>
            <h1>CardVault</h1>
            <p class="subtitle">Secure digital management for your essential information.</p>
            
            <div class="links-container">
                <a href="https://mukulmark42.github.io/cardvault-privacy/" class="btn btn-outline">Privacy Policy</a>
                <a href="https://mukulmark42.github.io/Terms-of-Service/" class="btn btn-outline">Terms of Service</a>
            </div>
        </header>

        <section class="contact-section">
            <h2>Contact Us</h2>
            <p>For support, inquiries, or feedback regarding our services, please reach out via email:</p>
            <a href="mailto:mukulrahaman1@gmail.com" class="email-link">mukulrahaman1@gmail.com</a>
        </section>

        <footer>
            <p>&copy; 2024 CardVault. All rights reserved.</p>
        </footer>
    </div>

</body>
</html>
