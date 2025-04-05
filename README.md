# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout</title>
  <style>
    /* Reset */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
    }

    /* Navigation Bar */
    nav {
      background-color: #333;
      color: white;
      padding: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1rem;
    }

    nav ul li {
      cursor: pointer;
    }

    /* Grid Layout */
    .container {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 20px;
      padding: 20px;
    }

    .sidebar {
      background-color: #f4f4f4;
      padding: 15px;
    }

    .main {
      background-color: #e2e2e2;
      padding: 15px;
    }

    /* Media Queries */
    @media (max-width: 768px) {
      .container {
        grid-template-columns: 1fr;
      }

      nav ul {
        flex-direction: column;
        gap: 0.5rem;
      }
    }

    @media (min-width: 1024px) {
      .container {
        grid-template-columns: 1fr 3fr;
      }
    }
  </style>
</head>
<body>

  <nav>
    <div class="logo">MySite</div>
    <ul>
      <li>Home</li>
      <li>About</li>
      <li>Services</li>
      <li>Contact</li>
    </ul>
  </nav>

  <div class="container">
    <div class="sidebar">
      <h3>Sidebar</h3>
      <p>Some sidebar content goes here.</p>
    </div>
    <div class="main">
      <h2>Main Content</h2>
      <p>This is the main section of the page. It expands depending on the screen size.</p>
    </div>
  </div>

</body>
</html>
Happy Coding! 💻✨
