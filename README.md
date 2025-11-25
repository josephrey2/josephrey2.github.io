<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Universe Mechanical & Air Conditioning, Inc.</title>

    <style>
        :root {
            --blue: #0d47a1;
            --light-blue: #e8f3ff;
            --gray: #555;
            --white: #fff;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: var(--light-blue);
            color: var(--gray);
        }

        header {
            background: var(--white);
            padding: 10px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            border-bottom: 3px solid var(--blue);
        }

        header img {
            height: 90px;
            width: auto;
        }

        nav {
            display: flex;
            gap: 20px;
        }

        nav a {
            text-decoration: none;
            font-size: 1.1em;
            color: var(--blue);
            font-weight: bold;
        }

        nav a:hover {
            text-decoration: underline;
        }

        .hero {
            background: url('https://images.unsplash.com/photo-1581092795360-7c6c03f37c67?auto=format&fit=crop&w=1400&q=80') center/cover no-repeat;
            padding: 120px 20px;
            text-align: center;
            color: var(--white);
            font-weight: bold;
            text-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
        }

        .hero h1 {
            font-size: 3em;
            margin: 0;
        }

        .hero p {
            font-size: 1.4em;
        }

        .container {
            max-width: 1200px;
            margin: auto;
            padding: 40px 20px;
        }

        h2 {
            color: var(--blue);
            border-left: 6px solid var(--blue);
            padding-left: 12px;
        }

        footer {
            background: var(--blue);
            color: var(--white);
            text-align: center;
            padding: 20px;
            margin-top: 40px;
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                text-align: center;
            }
            nav {
                margin-top: 15px;
            }
            header img {
                height: 70px;
            }
            .hero h1 {
                font-size: 2.3em;
            }
        }
    </style>
</head>
<body>

<header>
    <img src="/mnt/data/f2dcdb57-0a81-43f4-aff1-3ff4764ccde4.png" alt="Universe Mechanical & Air Conditioning Logo" />

    <nav>
        <a href="index.html">Home</a>
        <a href="new-construction.html">New Construction</a>
        <a href="services.html">Services</a>
        <a href="contact.html">Contact</a>
    </nav>
</header>

<section class="hero">
    <h1>Miami's Premier Air Conditioning Experts</h1>
    <p>Professional • Reliable • Family‑Owned Since 1995</p>
</section>

<div class="container">
    <h2>Welcome to Universe Mechanical & Air Conditioning, Inc.</h2>
    <p>
        We provide industry-leading A/C installation, repair, maintenance, and complete HVAC solutions
        throughout South Florida. With nearly 30 years of expertise, Universe Mechanical is trusted by
        homeowners, builders, and commercial partners for quality craftsmanship and exceptional service.
    </p>

    <p>
        Explore our services, learn about our new construction HVAC capabilities, or contact us today
        for fast and reliable assistance.
    </p>
</div>

<footer>
    © 2025 Universe Mechanical & Air Conditioning, Inc. • All Rights Reserved
</footer>

</body>
</html>


