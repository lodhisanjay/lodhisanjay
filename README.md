<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="icon" href="./assets/img/h1.png" />
  <link rel="stylesheet" href="assets/css/styles.css" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

  <!-- =====BOX ICONS===== -->
  <link href="https://cdn.jsdelivr.net/npm/boxicons@2.0.5/css/boxicons.min.css" rel="stylesheet" />
  <!--===== SCROLL REVEAL =====-->
  <script src="https://unpkg.com/scrollreveal"></script>
  <title>Sanjay Lodhi</title>
  <style>
    /*===== GOOGLE FONTS =====*/
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap");
/*===== VARIABLES CSS =====*/
:root {
  --header-height: 3rem;
  --font-semi: 600;
}

/*===== Colores =====*/
:root {
  --first-color: #4070f4;
  --second-color: #0e2431;
  --third-color: #ffffff;
}

/*===== Fuente y tipografia =====*/
:root {
  --body-font: "Poppins", sans-serif;
  --big-font-size: 2rem;
  --h2-font-size: 1.25rem;
  --normal-font-size: 0.938rem;
}
@media screen and (min-width: 768px) {
  :root {
    --big-font-size: 3.5rem;
    --h2-font-size: 2rem;
    --normal-font-size: 1rem;
  }
}

/*===== Margenes =====*/
:root {
  --mb-1: 0.5rem;
  --mb-2: 1rem;
  --mb-3: 1.5rem;
  --mb-4: 2rem;
  --mb-5: 2.5rem;
  --mb-6: 3rem;
}

/*===== z index =====*/
:root {
  --z-back: -10;
  --z-normal: 1;
  --z-tooltip: 10;
  --z-fixed: 100;
}

/*===== BASE =====*/
*,
::before,
::after {
  box-sizing: border-box;
}
html {
  scroll-behavior: smooth;
}
body {
  background-color: white;
  margin: var(--header-height) 0 0 0;
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
  color: var(--second-color);
}
.dark-mode{
  background-color: black;
  color: var(--third-color);

}

#jobTitle{
  animation: blinker 6s linear infinite;
}

@keyframes blinker {
  70%{
    opacity: .2;
  }
}

h1,
h2,
p {
  margin: 0;
}
ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
a {
  text-decoration: none;
}
img {
  max-width: 100%;
  height: auto;
  display: block;
}



/*===== CLASS CSS ===== */
.section-title {
  position: relative;
  font-size: var(--h2-font-size);
  color: var(--first-color);
  margin-top: var(--mb-2);
  margin-bottom: var(--mb-4);
  text-align: center;
}
.section-title::after {
  position: absolute;
  content: "";
  width: 64px;
  height: 0.18rem;
  left: 0;
  right: 0;
  margin: auto;
  top: 2rem;
  background-color: var(--first-color);
}
.section {
  padding-top: 3rem;
  padding-bottom: 2rem;
}

/*===== LAYOUT =====*/
.bd-grid {
  max-width: 1024px;
  display: grid;
  grid-template-columns: 100%;
  grid-column-gap: 2rem;
  width: calc(100% - 2rem);
  margin-left: var(--mb-2);
  margin-right: var(--mb-2);
}
.l-header {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: var(--z-fixed);
  background-color: #fff;
  box-shadow: 0 1px 4px rgba(146, 161, 176, 0.15);
}

/*===== NAV =====*/
.nav {
  height: var(--header-height);
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-weight: var(--font-semi);
}
@media screen and (max-width: 768px) {
  .nav-menu {
    position: fixed;
    top: var(--header-height);
    right: -100%;
    width: 80%;
    height: 100%;
    padding: 2rem;
    background-color: var(--second-color);
    transition: 0.5s;
  }
}
.nav-item {
  margin-bottom: var(--mb-4);
}
.nav-link {
  position: relative;
  color: #fff;
}
.nav-link:hover {
  position: relative;
}
.nav-link:hover::after {
  position: absolute;
  content: "";
  width: 100%;
  height: 0.18rem;
  left: 0;
  top: 2rem;
  background-color: var(--first-color);
}
.nav-logo img {
  color: var(--second-color);
  font-weight: var(--font-semi);
  width: 3rem;
  border-radius: 50%;
}
.nav-toggle {
  color: var(--second-color);
  font-size: 1.5rem;
  cursor: pointer;
}

/*Active menu*/
.active::after {
  position: absolute;
  content: "";
  width: 100%;
  height: 0.18rem;
  left: 0;
  top: 2rem;
  background-color: var(--first-color);
}

/*=== Show menu ===*/
.show {
  right: 0;
}

/*===== HOME =====*/
.home {
  height: calc(100vh - 3rem);
  row-gap: 1rem;
}
.home-data {
  align-self: center;
}
.home-title {
  font-size: var(--big-font-size);
  margin-bottom: var(--mb-5);
}
.home-title-color {
  color: var(--first-color);
}
.home-social {
  display: flex;
  flex-direction: column;
}
.home-social-icon {
  width: max-content;
  margin-bottom: var(--mb-2);
  font-size: 1.5rem;
  color: var(--second-color);
}
.home-social-icon:hover,
.footer-icon:hover {
  color: var(--first-color);
}
.home-img {
  position: absolute;
  right: 0;
  bottom: 0;
  width: 65%;
  
}

/*BUTTONS*/
.button {
  display: inline-block;
  background-color: var(--first-color);
  border: 1px solid var(--first-color);
  color: #fff;
  padding: 0.75rem 2.5rem;
  font-weight: var(--font-semi);
  border-radius: 0.5rem;
}
.button:hover {
  background-color: #fff;
  color: var(--first-color);
  box-shadow: 0 10px 36px rgba(0, 0, 0, 0.15);
}

/* ===== ABOUT =====*/
section.about {
  padding: 20vh 15px;
}
.about-container {
  row-gap: 2rem;
  text-align: center;
}
.about-subtitle {
  margin-bottom: var(--mb-2);
}
.about-img {
  justify-self: center;
}
.about-img img {
  width: 200px;
  border-radius: 0.5rem;
  cursor: pointer;
}

.about-img img:hover {
  -webkit-transform: scale(1.2);
  -ms-transform: scale(1.2);
  transform: scale(1.2);
  transition: 1s ease;
}


/* ===== EDUCATION =====*/

.education-data{
  /* border:1px solid red; */
  
  /* justify-content: space-between;
  align-items: center; */
  position: relative;
  font-weight: var(--font-semi);
  padding: 0.5rem 1rem;
  border-radius: 0.5rem;
  margin-bottom: var(--mb-4);
  box-shadow: 0 4px 25px rgba(14, 36, 49, 0.15);
  transition: 1s ease;
}


.education-name{
  margin: 6px;
  display: flex;
  justify-content: center;
  align-items: center;
   font-size: 20px;
   cursor: pointer;
  }
  .education-platform{
    margin: 6px;
    display: flex;
    justify-content: center;
    align-items: center;
     font-size: 16px;
     cursor: pointer;
    }

    .education-duration{
      margin: 6px;
      display: flex;
      justify-content: center;
      align-items: center;
       font-size: 12px;
       cursor: pointer;
      }
  
  .education-data:hover {
    -webkit-transform: scale(1.1);
    -ms-transform: scale(1.1);
    transform: scale(1.1);
    transition: 1s ease;
  }




/* ===== SKILLS =====*/
.skills-container {
  row-gap: 2rem;
  text-align: center;
}



.skills-subtitle {
  margin-bottom: var(--mb-2);
}
.skills-text {
  margin-bottom: var(--mb-4);
}
.skills-data {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
  font-weight: var(--font-semi);
  padding: 0.5rem 1rem;
  margin-bottom: var(--mb-4);
  border-radius: 0.5rem;
  box-shadow: 0 4px 25px rgba(14, 36, 49, 0.15);
  transition: 1s ease;
  cursor: pointer;
}

.skills-icon {
  width: 2rem;
  font-size: 2rem;
  margin-right: var(--mb-2);
  color: var(--first-color);
}
img.man-icons {
  font-size: 2rem;
  margin-right: var(--mb-2);
  color: var(--first-color);
}
.skills-names {
  display: flex;
  align-items: center;
}


.skills-names:hover {
  -webkit-transform: scale(1.1);
  -ms-transform: scale(1.1);
  transform: scale(1.1);
  transition: 1s ease;
}

.skills-bar {
  position: absolute;
  left: 0;
  bottom: 0;
  background-color: var(--first-color);
  height: 0.25rem;
  border-radius: 0.5rem;
  z-index: var(--z-back);
}
.skills-html {
  width: 75%;
}
.skills-css {
  width: 70%;
}
.skills-js {
  width: 85%;
}
.skills-react,
.skills-mongo {
  width: 80%;
}
.skills-redux {
  width: 90%;
}
.skills-mui,
.skills-sql {
  width: 65%;
}
.skills-ts {
  width: 70%;
}
.skills-express,
.skills-node {
  width: 85%;
}
.skills-img {
  border-radius: 0.5rem;
}

/* ===== Projects =====*/
.project-container {
  gap: 2rem;
  max-width: 1024px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  /* column-gap: 2rem; */
  width: calc(100% - 2rem);
  margin: auto;
}
.project-img {
  box-shadow: 0 4px 25px rgba(14, 36, 49, 0.15);
  border-radius: 0.5rem;
  overflow: hidden;
}
.project-img img {
  transition: 1s;
  cursor: pointer;
  margin-bottom: 0.5rem;
}
.project-img img:hover {
  transform: scale(1.1);
}
.project-container p {
  margin: auto 1rem 1rem;
}
.project-title {
  margin-bottom: var(--mb-2);
  margin-top: var(--mb-3);
  font-size: var(--h2-font-size);
}
.project-subtitle {
  margin-bottom: var(--mb-4);
  padding-bottom: 3.5rem;
}
.small-btn {
  padding: 0.3rem 1.3rem;
  font-weight: 400;
  margin: 1rem;
}
.project-btns {
  position: absolute;
  bottom: 0;
}

/* ===== CONTACT =====*/
.contact-input {
  width: 100%;
  font-size: var(--normal-font-size);
  font-weight: var(--font-semi);
  padding: 1rem;
  border-radius: 0.5rem;
  border: 1.5px solid var(--second-color);
  outline: none;
  margin-bottom: var(--mb-4);
}
.contact-button {
  display: block;
  border: none;
  outline: none;
  font-size: var(--normal-font-size);
  cursor: pointer;
  margin-left: auto;
}

/* ===== FOOTER =====*/
.footer {
  background-color: var(--second-color);
  color: #fff;
  text-align: center;
  font-weight: var(--font-semi);
  padding: 3.5rem 0;
}
.footer-title {
  font-size: 2rem;
  margin-bottom: var(--mb-4);
}
.footer-social {
  margin-bottom: var(--mb-4);
}
.footer-icon {
  font-size: 1rem;
  color: #fff;
  margin: 0 var(--mb-2);
}

/* ===== MEDIA QUERIES=====*/
@media screen and (min-width: 768px) {
  body {
    margin: 0;
  }
  .section {
    padding-top: 4rem;
    padding-bottom: 3rem;
  }
  .section-title {
    margin-bottom: var(--mb-6);
  }
  .section-title::after {
    width: 80px;
    top: 3rem;
  }

  .nav {
    height: calc(var(--header-height) + 1rem);
  }
  .nav-list {
    display: flex;
    padding-top: 0;
  }
  .nav-item {
    margin-left: var(--mb-6);
    margin-bottom: 0;
  }
  .nav-toggle {
    display: none;
  }
  .nav-link {
    color: var(--second-color);
  }

  .home {
    height: 100vh;
  }
  .home-data {
    align-self: flex-end;
  }
  .home-social {
    padding-top: 0;
    padding-bottom: 2.5rem;
    flex-direction: row;
    align-self: flex-end;
  }
  .home-social-icon {
    margin-bottom: 0;
    margin-right: var(--mb-4);
  }
  .home-img {
    width: 39%;
    max-width: 420px;
    bottom: 15%;
    
  }
  .home-img img{
    border-radius: 50%;
    
  }
  .about-container {
    align-items: center;
    margin: auto;
    width: 50%;
    transition: 0.5s;
  }
  /* .about-container {
    width: 50%;
  } */
  .skills-container {
    grid-template-columns: repeat(2, 1fr);
    text-align: initial;
  }
  .about-img img {
    width: 300px;
  }
  .project-container {
    grid-template-columns: repeat(2, 1fr);
    /* grid-template-rows: repeat(2, 1fr); */
    column-gap: 3rem;
  }
  .contact-form {
    width: 360px;
  }
  .contact-container {
    justify-items: center;
  }
}

@media screen and (min-width: 1024px) {
  .bd-grid {
    margin-left: auto;
    margin-right: auto;
  }
  .home-img {
    right: 10%;
  }
}

  </style>
</head>

<body>
  <!--===== HEADER =====-->
  <header class="l-header">
    <nav class="nav bd-grid">
      <div>
        <!-- &#60;&#62; -->
        <a href="#home" class="nav-logo"><img src="sanjay.jpeg" height="70px" alt="H" /></a>
      </div>

      <div class="nav-menu" id="nav-menu">
        <ul class="nav-list">
          <li class="nav-item">
            <a href="#home" class="nav-link home active">Home</a>
          </li>
          <li class="nav-item">
            <a href="#experience" class="nav-link experience">Experience</a>
          </li>
          <li class="nav-item">
            <a href="#about" class="nav-link about">About</a>
          </li>
          <li class="nav-item">
            <a href="#skills" class="nav-link skills">Skills</a>
          </li>
          <li class="nav-item">
            <a href="#projects" class="nav-link projects">Projects</a>
          </li>
          <li class="nav-item">
            <a href="#contact" class="nav-link contact">Contact</a>
          </li>
          <li class="nav-item">
          <a href = "#" onclick="myFunction()"> <img src="sanjay.jpeg" alt="" height="20px" width="20px" style="background-color: transparent; border-radius: 50%;"> </a>
          </li>
        </ul>
      </div>

      <div class="nav-toggle" id="nav-toggle">
        <i class="bx bx-menu"></i>
      </div>
    </nav>
  </header>

  <main class="l-main">
    <!--===== HOME =====-->
    <section class="home bd-grid section" id="home">
      <div class="home-data">
        <h2 class="home-title">
          Hi 👋,<br />I'am <span class="home-title-color">Sanjay Lodhi</span><br />
         <span id="jobTitle" >Java Developer</span> 
        </h2>

        <a href="sanjay_lodhi.pdf"  target="_blank"
          class="button">Resume</a>

      </div>

      <div class="home-social">
        <a href="https://www.linkedin.com/in/sanjay-lodhi-298387200/" target="_blank" class="home-social-icon"><i
            class="bx bxl-linkedin"></i></a>
        <a href="https://github.com/lodhisanjay" target="_blank" class="home-social-icon"><i
            class="bx bxl-github"></i></a>
      </div>

      <div class="home-img">
        <img src="sanjay.jpeg" alt="" />
      </div>
    </section>
      <!--===== ABOUT =====-->
      <section class="about section" id="experience">
        <h2 class="section-title">Experience</h2>
  
        <div class="about-container bd-grid">
          
          <div style="text-align: center">
            <h2 class="about-subtitle">I'am Sanjay Lodhi</h2>
            <h1 class="about-subtitle">I have 1 year of experience as a java developer</h1>
  
            <p class="about-text">
              Results-driven Java Developer with one years of hands-on experience in designing, developing, and maintaining robust software solutions. Proficient in Java, Spring Framework. Adept at collaborating with cross-functional teams to deliver high-quality, scalable applications. Seeking to leverage technical expertise and passion for innovation in a challenging development role.
            </p>
            <br />
            
            <p>
              <b>Drop a mail :</b> lodhisanjay67@gmail.com
              <i style="color: #4070f4; font-size: 1.2rem; cursor: pointer" class="bx bx-copy" id="copy"></i>
            </p>
          </div>
        </div>
      </section>
  

    <!--===== ABOUT =====-->
    <section class="about section" id="about">
      <h2 class="section-title">About</h2>

      <div class="about-container bd-grid">
        <div class="about-img">
          <img src="assets/img/profile_1.jpeg" alt="" />
        </div>

        <div style="text-align: center">
          <h2 class="about-subtitle">I'am Sanjay Lodhi</h2>
          <p class="about-text">
            Quick learner and an aspiring java developer with java and spring boot framework
            knowledge of other technology. Looking forward to applying
            and enhancing my skills and knowledge as a java developer.
          </p>
          <br />
          
          <p>
            <b>Drop a mail :</b> lodhisanjay67@gmail.com
            <i style="color: #4070f4; font-size: 1.2rem; cursor: pointer" class="bx bx-copy" id="copy"></i>
          </p>
        </div>
      </div>
    </section>


    <!---========Education ======--->
    <section class="education section" id="education">
      <h2 class="section-title">Education</h2>
      <div class="education-container bd-grid">
    
        <div class="education-data">
          <div class="education-names">
            <!-- <i class="bx bxl-html5 skills-icon"></i> -->
            <span class="education-name">Marticulation</span> 
            <p class="education-platform ">Raja Bhoj Higher Secondary School, Bhopal</p>
            <p class="education-duration ">2014 - 2015</p>

          </div>
          <div class="education-names">
            <!-- <i class="bx bxl-html5 skills-icon"></i> -->
            <span class="education-name">Intermediate</span> 
            <p class="education-platform ">Raja Bhoj Higher Secondary School, Bhopal</p>
            <p class="education-duration ">2012 - 2013</p>

          </div>
        </div>
        </div>
      <div class="education-container bd-grid">
    
    <div class="education-data">
      <div class="education-names">
        <!-- <i class="bx bxl-html5 skills-icon"></i> -->
        <span class="education-name">BCA</span>
        <p class="education-platform ">Sect College of Professional Education(SCOPE), Bhopal</p>
        <p class="education-duration ">2015 - 2018</p>

      </div>
    </div>
    </div>

    <!--===== SKILLS =====-->
    <section class="skills section" id="skills">
      <h2 class="section-title">Skills</h2>

      <div class="skills-container bd-grid">
        <div>
          <!-- <h2 class="skills-subtitle">Front-end Skills</h2> -->
          <div class="skills-data">
            <div class="skills-names">
           
              <iconify-icon class="skills-icon" icon="devicon:java-wordmark" style="font-size:40px;"></iconify-icon>
              
              <span class="skills-name">Java(SE) Java(EE)</span>
            </div>
            <!-- <div class="skills-bar skills-html"></div> 
             <div>
                <span class="skills-percentage">75%</span>
              </div>  -->
          </div>
          <div class="skills-data">
            <div class="skills-names">
            
              <iconify-icon class="skills-icon" style="font-size: 40px; color: green;" icon="bxl:spring-boot"></iconify-icon>
              <span class="skills-name">Spring Boot</span>
            </div>
             <!-- <div class="skills-bar skills-css"></div>  -->
            <!-- <div>
                <span class="skills-percentage">70%</span>
              </div>  -->
          </div>
          <div class="skills-data">
            <div class="skills-names">
              <iconify-icon class="skills-icon" style="font-size: 40px; color: green;"  icon="devicon:spring-wordmark"></iconify-icon>
              <span class="skills-name">Spring MVC</span>
            </div>
            <!-- <div class="skills-bar skills-css"></div>  -->
            <div>
                <!-- <span class="skills-percentage">70%</span> -->
              </div> 

          </div>
          <div class="skills-data">
            <div class="skills-names">
              <iconify-icon class="skills-icon" style="font-size: 40px; color: green;" icon="simple-icons:springsecurity"></iconify-icon>
              <span class="skills-name">Spring Security</span>
            
            </div>
            <!-- <div class="skills-bar skills-react"></div> -->
            <div>
                <!-- <span class="skills-percentage">50%</span> -->
              </div>
          </div>
          <div class="skills-data">
            <div class="skills-names">
              <iconify-icon class="skills-icon" style="font-size: 40px;" icon="devicon:hibernate-wordmark"></iconify-icon>
              <span class="skills-name">Hibernate</span>
            </div>
            <!-- <div class="skills-bar skills-redux"></div>  -->
            <!-- <div class="skills-bar skills-css"></div>  -->
            <div>
                <!-- <span class="skills-percentage">50%</span> -->
              </div> 

          </div>
          <div class="skills-data">
            <div class="skills-names">
              <iconify-icon class="skills-icon" style="font-size: 40px;"  icon="devicon:react-wordmark"></iconify-icon>
              <span class="skills-name">React(Basic)</span>
            
            </div>
            <!-- <div class="skills-bar skills-css"></div>  -->
            <div>
                <!-- <span class="skills-percentage">70%</span> -->
              </div> 
          </div>
         
        </div>
        <div>
          <!-- <h2 class="skills-subtitle">Back-end Skills</h2> -->
          <div class="skills-data">
            <div class="skills-names">
              <iconify-icon class="skills-icon" style="font-size: 40px; color: green;" icon="logos:jwt-icon"></iconify-icon>
              <span class="skills-name">JWT Token</span>
            
            </div>
            <!-- <div class="skills-bar skills-css"></div>  -->
            <div>
                <!-- <span class="skills-percentage">70%</span> -->
              </div> 
          </div>

          <div class="skills-data">
            <div class="skills-names">
              <iconify-icon class="skills-icon" style="font-size: 40px;" icon="devicon:mysql-wordmark"></iconify-icon>
              <span class="skills-name">MySQL</span>
            
            </div>
            <!-- <div class="skills-bar skills-css"></div>  -->
            <div>
                <!-- <span class="skills-percentage">70%</span> -->
              </div> 
          </div>
          <div class="skills-data">
            <div class="skills-names">
              <iconify-icon class="skills-icon" style="font-size: 40px;" icon="logos:html-5"></iconify-icon>
              <span class="skills-name">HTML</span>
            
            </div>
            <!-- <div class="skills-bar skills-css"></div> -->
            <div>
                <!-- <span class="skills-percentage">70%</span> -->
              </div> 
          </div>

          <div class="skills-data">
            <div class="skills-names">
              <iconify-icon class="skills-icon" style="font-size: 40px; color: coral;"  icon="vaadin:css"></iconify-icon>
              <span class="skills-name">CSS</span>
            
            </div>
            <!-- <div class="skills-bar skills-css"></div>  -->
            <div>
                <!-- <span class="skills-percentage">70%</span> -->
              </div> 
          </div>
          <div>
             <!-- <h2 class="skills-subtitle">TOOLS</h2> --> 
             <div class="skills-data">
              <div class="skills-names">
                <iconify-icon class="skills-icon" style="font-size: 40px;"  icon="skill-icons:javascript"></iconify-icon>
                <span class="skills-name">HTML</span>
              
              </div>
            </div>

            <div class="skills-data">
              <div class="skills-names">
                <iconify-icon class="skills-icon" style="font-size: 40px;"   icon="devicon:bootstrap-wordmark"></iconify-icon>
                <span class="skills-name">Bootstrap</span>
              
              </div>
            </div>
            
            

          </div>
        </div>
    </section>

    <!--===== Projects =====-->
    <section class="projects section" id="projects">
      <h2 class="section-title">Projects</h2>

      <div class="project-container">
        <div class="project-img">
          
          <p class="project-title">Edutech</p>
          <p class="project-subtitle">
            Educational Technology, or EdTech, refers to the use of technology to enhance and support the learning and teaching process.
            <br> <b>Features:</b>
            Development and utilization of online platforms, learning management systems (LMS), and virtual classrooms for educational purposes.<br>
            Customized learning experiences tailored to individual student needs, often leveraging data and algorithms to adjust content and pace.
            User upload new posts. <br />
            
            <br />
            A collaborative project, built in our self
            . <br />
            <br />Java | Jsp | Servlet | Sessions | MySQL | HTML | CSS | JavaScript | Bootstrap.
          </p>
          
        </div>
        <div class="project-img">
          
          <p class="project-title">Tech-Blog Application</p>
          <p class="project-subtitle">
            A web application to upload blogs and view other users blogs & user can do messages and Likes.Allow users to create profiles, customize preferences, and build a personalized feed based on their interests.
           <br> <b>Features:</b>
            User authentication & authorization
            User view all posts and filter by category
            User upload new posts. <br />
            <br />
            A collaborative project, built in our self
            . <br />
            <br />Java | Spring Boot | Spring Security | JWT Token | Web Development | JPA | MySQL.
          </p>
          
        </div>


        <div class="project-img">
          
          <p class="project-title">Smart Contact Manager</p>
          <p class="project-subtitle">
            Consolidate emails, messages, and calls in one place Automatically categorize and organize contacts based on relationships and interactions. <br />
           <b>Features:</b>
            Implement robust security measures to protect sensitive contact information, prioritizing user privacy.
            <br />
            <br>
            A collaborative project, built in our self.
            <br>
            <br /> Java | Spring Boot | Spring Security | JWT Token | Web Development | JPA | MySQL | Thymeleaf.
          </p>
          
        </div>

        <div class="project-img">
          
          <p class="project-title">Student Web Portal</p>
          <p class="project-subtitle">
            Provide students with a customized dashboard displaying relevant information such as class schedules, announcements, and upcoming deadlines.
          <br>
            Enroll in courses, view syllabi, and access course materials and resources from a centralized location.
            <br />
            <b>Features:</b>
            Explore career development resources, job postings, and internship opportunities integrated into the portal.
            <br/><br>
            A collaborative project, built in our self.
            <br>
            <br />Java | Jsp | Servlet | Sessions | MySQL | HTML | CSS | JavaScript | Bootstrap.
          </p>
          
        </div>
        
        

       
      </div>
    </section>
  </main>

  <!--===== FOOTER + CONTACT=====-->
  
  <footer class="footer section" id="contact">
    <h2 class="section-title">Get in Touch</h2>
    <p class="footer-title">Sanjay Lodhi</p>
    <div class="footer-social">
      <a href="https://www.linkedin.com/in/sanjay-lodhi-298387200/" target="_blank" class="footer-icon"><i
          class="bx bxl-linkedin">
          <br />
          LinkedIn</i></a>
      <a href="mailto:lodhisanjay67@gmail.com" target="_blank" class="footer-icon"><i class="bx bxl-twitter">
          <br />
          E-mail</i></a>
      <a href="tel:+91 8878856131" target="_blank" class="footer-icon"><i class="bx bx-phone">
          <br />
          Phone</i></a>
      <a href="https://github.com/lodhisanjay" target="_blank" class="footer-icon"><i
            class="bx bxl-github">
          <br />
          GitHub
          </i></a>
    </div>
    <p>&#169; 2020 copyright all right reserved</p>
  </footer>
  <script src="https://unpkg.com/scrollreveal"></script>
  <script src="https://code.iconify.design/iconify-icon/1.0.7/iconify-icon.min.js"></script>
<script>
    /*===== MENU SHOW =====*/
const showMenu = (toggleId, navId) => {
  const toggle = document.getElementById(toggleId),
    nav = document.getElementById(navId);

  if (toggle && nav) {
    toggle.addEventListener("click", () => {
      nav.classList.toggle("show");
    });
  }
};
showMenu("nav-toggle", "nav-menu");

/*===== ACTIVE AND REMOVE MENU =====*/
const navLinks = document.querySelectorAll(".nav-link");
const sections = document.querySelectorAll(".section");

window.addEventListener("scroll", () => {
  let current = '';
  sections.forEach(section => {
    const sectionTop = section.offsetTop;
    const sectionHeight = section.clientHeight;
    if (scrollY >= sectionTop - 390) {
      current = section.getAttribute('id');
    }
  })

  navLinks.forEach(link => {
    link.classList.remove('active');
    if (link.classList.contains(current)) {
      link.classList.add('active');
    }
  })
})

// function linkAction() {
//   /*Active link*/
//   navLinks.forEach((n) => n.classList.remove("active"));
//   this.classList.add("active");

//   /*Remove menu mobile*/
const navMenu = document.getElementById("nav-menu");
//   navMenu.classList.remove("show");
// }
navLinks.forEach((n) => n.addEventListener("click", () => { navMenu.classList.remove("show") }));

/*===== COPY Email =====*/
const copy = document.getElementById("copy");
copy.addEventListener("click", () => {
  navigator.clipboard.writeText("lodhisanjay67@gmail.com");
  copy.innerHTML = "copied";
  setTimeout(() => {
    copy.innerHTML = null;
  }, 1000);
});

/*===== SCROLL REVEAL ANIMATION =====*/
const sr = ScrollReveal({
  origin: "top",
  distance: "80px",
  duration: 2000,
  reset: true,
});

/*SCROLL HOME*/
sr.reveal(".home-title", {});
sr.reveal(".button", { delay: 200 });
sr.reveal(".home-img", { delay: 400 });
sr.reveal(".home-social-icon", { interval: 200 });

/*SCROLL ABOUT*/
sr.reveal(".about-img", {});
sr.reveal(".about-subtitle", { delay: 400 });
sr.reveal(".about-text", { delay: 400 });

/*SCROLL SKILLS*/
sr.reveal(".skills-subtitle", {});
sr.reveal(".skills-text", {});
sr.reveal(".skills-data", { interval: 100 });
// sr.reveal(".skills-img", { delay: 600 });

/*SCROLL projects*/
sr.reveal(".project-img", { interval: 200 });

/*SCROLL CONTACT*/
  // sr.reveal(".contact-input", { interval: 200 });

  function myFunction(){
    var element = document.body;
    element.classList.toggle("dark-mode")
  }


  var messageArr = [];
  var textPosition = 0;
  var speed = 200;

  typewriter = () => {
    // for(let i = 0; i < messageArr.length; i++) {
    document.querySelector("#jobTitle").innerHTML = messageArr[0].substring(0, textPosition)  ;
    if(textPosition ++  != messageArr[0].length)
        setTimeout(typewriter, speed)
  }


  window.addEventListener("load" , typewriter);
</script>
</body>

</html>
