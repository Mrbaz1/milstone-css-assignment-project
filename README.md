# milstone-css-assignment-project
   --primary-color: #2c3e50;
    --accent-color: #e67e22;
    --light-bg: #f4f4f4;
    --text-color: #333;
    --white: #ffffff;
    --padding-std: 2rem;
}

/* Requirement: Spacing (Box Model reset) */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; /* Crucial for predictable sizing */
}

/* Requirement: Typography & Custom Fonts */
body {
    font-family: 'Montserrat', sans-serif;
    line-height: 1.6;
    color: var(--text-color);
    background-color: var(--white);
}

h1, h2, h3 {
    font-family: 'Playfair Display', serif;
    margin-bottom: 1rem;
}

/* --- Header & Flexbox --- */
.main-header {
    background-color: var(--white);
    /* Requirement: Flexbox */
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 5%;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    position: sticky;
    top: 0;
    z-index: 100;
}

.logo {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary-color);
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 2rem; /* Spacing between flex items */
}

.nav-links a {
    text-decoration: none;
    color: var(--primary-color);
    font-weight: 500;
    transition: color 0.3s ease;
}

.nav-links a:hover {
    color: var(--accent-color);
}

/* Requirement: Sizing and units (rem, vh, %) */
.hero {
    height: 80vh; /* Viewport Height */
    background-color: var(--primary-color);
    color: var(--white);
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 0 1rem;
}

.hero h1 {
    font-size: 3.5rem; /* Relative sizing */
}

/* Buttons */
.btn-primary {
    background-color: var(--accent-color);
    color: var(--white) !important;
    padding: 0.5rem 1.2rem;
    border-radius: 5px;
}

.btn-secondary {
    display: inline-block;
    margin-top: 1.5rem;
    padding: 0.8rem 2rem;
    border: 2px solid var(--white);
    color: var(--white);
    text-decoration: none;
    transition: background 0.3s ease;
}

.btn-secondary:hover {
    background: var(--white);
    color: var(--primary-color);
}

/* --- Main Layout & Grid --- */
.container {
    padding: 4rem 5%;
    background-color: var(--light-bg);
}

.section-title {
    text-align: center;
    margin-bottom: 3rem;
}

.underline {
    width: 60px;
    height: 4px;
    background-color: var(--accent-color);
    margin: 0 auto;
}

/* Requirement: Grid Layout */
.grid-layout {
    display: grid;
    /* Requirement: Responsive Web Design (Auto-fit grid) */
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

.card {
    background: var(--white);
    padding: 2.5rem;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    border-left: 5px solid var(--accent-color);
}

footer {
    text-align: center;
    padding: 2rem;
    background: var(--primary-color);
    color: var(--white);
}

/* Requirement: Responsive Web Design (Media Queries) */
@media (max-width: 768px) {
    .hero h1 {
        font-size: 2.5rem;
    }

    .nav-links {
        display: none; /* In a real scenario, this would become a hamburger menu */
    }
    
    .grid-layout {
        grid-template-columns: 1fr; /* Force single column on mobile */
    }
}
