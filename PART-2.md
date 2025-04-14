## **Part 2: Prototype Development & Initial Submission** 

### **Objective:**  
Develop a **basic working prototype** of the website with placeholder content, navigation, and CSS styling.  

### **Deliverables:**  
- **Homepage (`index.html`) with placeholder content**  
- **Basic Navigation Bar** across all pages  
- **External CSS Stylesheet** applied to all pages  
- **Site Folder Structure:** Must include subfolders for images, scripts, media, and CSS.  
- **“Meet the Team” Page** with professional headshots and bios  
- **One JavaScript Feature:** Simple interactive element (e.g., button click effect, text animation)  
- **Mobile Responsiveness Check**: Test site display on different screen sizes.  

### **Grading Rubric (25 Points Total):**  
| Criteria | Points | Description |
|----------|--------|-------------|
| Working Homepage | 5 | The homepage exists and includes the navigation structure. |
| Navigation | 5 | All links function correctly and point to relevant pages. |
| CSS Styling | 5 | External stylesheet applied correctly to maintain consistency. |
| JavaScript Integration | 5 | Includes at least one interactive feature. |
| Site Structure | 5 | Files and folders are organized properly for submission. |

//main page//
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Homepage</title>
  <link rel="stylesheet" href="css/style.css" />
  <script defer src="scripts/script.js"></script>
</head>
<body>
  <nav>
    <ul class="navbar">
      <li><a href="index.html">Home</a></li>
      <li><a href="meet-the-team.html">Meet the Team</a></li>
    </ul>
  </nav>

  <header>
    <h1>Welcome to Our Project</h1>
    <p>This is a placeholder homepage with basic navigation and styling.</p>
    <button id="clickMeBtn">Click Me!</button>
    <p id="responseText"></p>
  </header>
</body>
</html>


// meet the team//

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Meet the Team</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  <nav>
    <ul class="navbar">
      <li><a href="index.html">Home</a></li>
      <li><a href="meet-the-team.html">Meet the Team</a></li>
    </ul>
  </nav>

  <section class="team">
    <h2>Meet the Creator</h2>
    <div class="member">
      <img src="images/angelo-headshot.jpg" alt="Angelo Henderson">
      <h3>Angelo Henderson</h3>
      <p>
        I'm a third-year Computer Engineering student with a strong passion for Artificial Intelligence. 
        I love staying active and pushing myself both physically and mentally. I’m constantly learning new coding languages to deepen my understanding of how technology works and how it can be used to solve real-world problems.
      </p>
    </div>
  </section>
</body>
</html>


//css stying//
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.6;
}

.navbar {
  list-style: none;
  background-color: #333;
  display: flex;
  justify-content: center;
  padding: 0;
}

.navbar li {
  margin: 0;
}

.navbar a {
  display: block;
  padding: 14px 20px;
  color: white;
  text-decoration: none;
}

.navbar a:hover {
  background-color: #555;
}

header, .team {
  text-align: center;
  padding: 2em;
}

.member {
  margin: 20px auto;
  max-width: 300px;
}

.member img {
  width: 100%;
  border-radius: 10px;
}

@media (max-width: 600px) {
  .navbar {
    flex-direction: column;
  }
}

//java//

document.addEventListener("DOMContentLoaded", function () {
  const btn = document.getElementById("clickMeBtn");
  const output = document.getElementById("responseText");

  btn.addEventListener("click", function () {
    output.textContent = "You clicked the button!";
    output.style.color = "#0077cc";
  });
});
