<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ayobami's Portfolio</title>
    <link rel="stylesheet" href="responsive.css" />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
    <script src="https://unpkg.com/scrollreveal"></script>
    
  </head>
  <style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

:root {
  /*=======Main theme colors=======*/
  --first-color: #0e2431;
  --second-color: blue;
  --third-color: #777;

  /*=======Hover colors=======*/
  --hover-color: #1e0e85;

  /*=======Background colors=======*/
  --body-bg-color: #fefefe;
  --card-bg-color: #fff;
  --modal-bg-color: #fff;
  --bg-transparent-color: rgba(0, 0, 0, 0.1);
  --transparent-color-01: rgba(0, 0, 0, 0.1);
  --transparent-color-02: rgba(106, 89, 209, 0.1);
  --line-color: #d7d7d7;

  /*=======Colors filters=======*/
  --color-filter: invert(1);

  /*=======Box shadow=======*/
  --box-shadow: 0px 0px 20px rgba(0 0 0 / 10%);

  /*=======Font size=======*/
  --small-font-size: 0.9em;
  --normal-font-size: 1em;

  /*=======Scroll bar colors=======*/
  --scroll-bar-color: #c5cadf;
  --scroll-thumb-color: #70768a;
  --scroll-thumb-hover-color: #454f6b;
}

.dark-theme {
  /*=======Main theme colors=======*/
  --first-color: #fff;
  --second-color: blue;
  --third-color: #a9afc3;

  /*=======Background colors=======*/
  --body-bg-color: #07090e;
  --card-bg-color: #0a1735;
  --modal-bg-color: #102048;
  --bg-transparent-color: rgba(255, 255, 255, 0.1);
  --transparent-color-01: rgba(255, 255, 255, 0.1);
  --line-color: #454f6b;

  /*=======Colors filters=======*/
  --color-filter: invert(0);

  /*=======Scroll bar colors=======*/
  --scroll-bar-color: #c1ceff;
  --scroll-thumb-color: #282f4e;
  --scroll-thumb-hover-color: #454f6b;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

html {
  scroll-behavior: smooth;
}

body {
  color: var(--first-color);
  background: var(--body-bg-color);
  margin: 2rem 0 0 0;
  transition: 0.5s ease;
}

a {
  text-decoration: none;
}

li {
  list-style: none;
}

/*=======Scroll to top button=======*/
.scrollToTop-btn {
  z-index: 99999;
  position: fixed;
  right: 0;
  bottom: 20px;
  width: 45px;
  height: 45px;
  background: var(--second-color);
  color: #fff;
  font-size: var(--small-font-size);
  border-radius: 3px;
  cursor: pointer;
  opacity: 0;
  transition: 0.5s ease;
}

.scrollToTop-btn.active {
  right: 20px;
  pointer-events: all;
  opacity: 1;
}

/*=======Light/Dark theme button=======*/
.theme-btn {
  z-index: 999999;
  position: fixed;
  right: 0;
  top: 100px;
  background: var(--transparent-color-01);
  backdrop-filter: blur(20px);
  width: 50px;
  height: 50px;
  font-size: 1.2em;
  border-radius: 5px 0 0 5px;
  box-shadow: var(--box-shadow);
  cursor: pointer;
}

.theme-btn .fa-sun,
.theme-btn.sun .fa-moon {
  display: none;
}

.theme-btn.sun .fa-sun {
  display: block;
}

/*=======Scroll bar=======*/
::-webkit-scrollbar {
  width: 10px;
  background: var(--scroll-bar-color);
}

::-webkit-scrollbar-thumb {
  background: var(--scroll-thumb-color);
  border-radius: 2em;
}

::-webkit-scrollbar-thumb:hover {
  background: var(--scroll-thumb-hover-color);
}

/*=======Header=======*/
header {
  z-index: 99999;
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  backdrop-filter: blur(20px);
  transition: 0.6s ease;
}

header.sticky {
  background: rgba(255, 255, 255, 0.1);
  box-shadow: var(--box-shadow);
}
.nav-bar {
  position: relative;
  height: calc(4rem + 1rem);
  max-width: 1250px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-left: auto;
  margin-right: auto;
  padding: 0 20px;
  transition: 0.6s ease;
}

header.sticky .nav-bar {
  height: calc(2.5rem + 1rem);
}

.nav-bar .logo {
  color: var(--first-color);
  font-size: 1.3em;
  font-weight: 600;
}

.nav-items a {
  color: var(--first-color);
  font-size: var(--normal-font-size);
  font-weight: 500;
}

.nav-items a.active {
  color: var(--second-color);
}

.nav-items a:not(:last-child) {
  margin-right: 50px;
}

.nav-items a:hover {
  color: var(--second-color);
}

.nav-menu-btn {
  display: none;
}

/*=======Home section=======*/
.home {
  position: relative;
  max-width: 1250px;
  min-height: 100vh;
  margin-left: auto;
  margin-right: auto;
  padding: 4rem 2rem;
  flex-direction: column;
}

.home .home-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.home-container .media-icons {
  display: flex;
  flex-direction: column;
  margin-right: 40px;
}

.home-container .media-icons a {
  color: var(--second-color);
  font-size: 1.5em;
  margin: 10px 0;
}

.home-container .media-icons a:hover {
  color: var(--hover-color);
}

.home-container .info h2 {
  font-size: 4em;
  font-weight: 600;
  line-height: 70px;
}

.home-container .info h3 {
  color: var(--third-color);
  font-weight: 600;
  font-feature-settings: 1.3em;
  line-height: 50px;
}

.home-container .info p {
  color: var(--third-color);
  font-size: var(--normal-font-size);
  max-width: 350px;
}

.btn {
  background: var(--second-color);
  color: #fff;
  font-size: var(--normal-font-size);
  font-weight: 500;
  display: inline-block;
  margin-top: 25px;
  padding: 20px 30px;
  letter-spacing: 1px;
  border-radius: 10px;
}

.btn:hover {
  background: var(--hover-color);
}

.home-container .home-img {
  position: relative;
  width: 250px;
  height: 300px;
  margin-top: none;
}

.home-container .home-img img {
  width: 90%;
  transform: translate(0, 0);
}

.home .scroll-down {
  color: var(--first-color);
  font-size: var(--normal-font-size);
  font-weight: 500;
  margin-top: 20px;
}

.home .scroll-down i {
  color: var(--second-color);
  font-size: 1.2em;
  animation: arrow-down ease 2s infinite;
}

@keyframes arrow-down {
  0% {
    transform: translateY(0);
  }
  30% {
    transform: translateY(10px);
  }
}

/*=======Common style for all sections=======*/
.flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.section {
  position: relative;
  max-width: 1150px;
  margin-left: auto;
  margin-right: auto;
  padding: 6rem 2rem 2rem;
}

.sub-section {
  position: relative;
  max-width: 1150px;
  margin-left: auto;
  margin-right: auto;
  padding: 6rem 0;
}

.section-title-01 {
  font-size: 4.5em;
  font-weight: 800;
  margin-bottom: 2rem;
  background: linear-gradient(to top, transparent 0%, var(--first-color) 70%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  opacity: 0.1;
}

.section-title-02 {
  font-size: 2.5em;
  font-weight: 700;
  transform: translateY(-80px);
}

.section-title-02::before {
  content: "";
  position: absolute;
  width: 70px;
  height: 5px;
  right: 0;
  bottom: 0;
  background: var(--second-color);
}
.container {
  position: relative;
  flex-direction: column;
}

/*=======About section=======*/
.about .container .content {
  column-gap: 40px;
  width: 100%;
}

.about-img {
  position: relative;
}

.about-img img {
  height: 400px;
  max-width: 100%;
  min-width: 500px;
  border-radius: 10px;
}

.about-info .description {
  max-width: 600px;
}

.about-info .description h3 {
  font-size: 1.3em;
  font-weight: 600;
  margin-bottom: 10px;
}

.about-info .description h4 {
  font-size: 1.3em;
  font-weight: 600;
  margin-bottom: 10px;
}

.about-info .description h4 span {
  color: var(--second-color);
}

.about-info .description p {
  color: var(--third-color);
  font-size: var(--normal-font-size);
  margin-bottom: 15px;
  padding-bottom: 25px;
  border-bottom: 2px solid var(--line-color);
}

.about-info .professional-list {
  display: flex;
  column-gap: 30px;
}

.about-info .professional-list .list-item {
  display: flex;
  justify-content: center;
  align-items: center;
  column-gap: 15px;
  margin-bottom: 20px;
}

.about-info .professional-list .list-item h3 {
  font-size: 2.5em;
  font-weight: 700;
}

.about-info .professional-list .list-item span {
  color: var(--third-color);
  font-size: var(--small-font-size);
}

/*=======Skills sections=======*/
.skills .container .content {
  width: 100%;
}

.skills-description {
  max-width: 700px;
  margin-bottom: 50px;
}

.skills-description h3 {
  font-size: 2em;
  margin-bottom: 5px;
}

.skills-info {
  max-width: 100%;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  margin: 0 auto;
}

.skills-info h4 {
  margin-bottom: 20px;
  margin-top: 20px;
}

.skills-info h4 label {
  background: var(--second-color);
  color: #fff;
  font-size: var(--normal-font-size);
  font-weight: 400;
  padding: 5px 15px;
  border-radius: 5px;
}

.education-all {
  margin-bottom: 80px;
}
.edu-list .item {
  background: var(--card-bg-color);
  box-shadow: var(--box-shadow);
  border-bottom: 3px solid var(--second-color);
  padding: 20px;
  margin-top: 15px;
  border-radius: 6px;
  transition: 0.3s ease;
}

.edu-list .item .year {
  font-size: var(--small-font-size);
  margin-bottom: 5px;
}

.edu-list .item p {
  color: var(--third-color);
  font-size: var(--small-font-size);
}

.edu-list .item p span {
  color: var(--first-color);
  font-size: var(--normal-font-size);
  font-weight: 500;
}

.bar {
  background: var(--card-bg-color);
  box-shadow: var(--box-shadow);
  margin-bottom: 10px;
  padding: 20px;
  border-radius: 6px;
  transition: 0.3s ease;
}

.bar .info {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 5px;
  font-size: var(--small-font-size);
}

.bar .info span {
  font-weight: 500;
}

.bar .line {
  position: relative;
  width: 100%;
  height: 7px;
  background: #c5cadf;
  border-radius: 2px;
}

.bar .line:before {
  content: "";
  position: absolute;
  height: 100%;
  top: 0;
  left: 0;
  background: var(--second-color);
  border-radius: 2px;
}

.bar .html:before {
  width: 95%;
}

.bar .css:before {
  width: 80%;
}

.bar .javascript:before {
  width: 65%;
}

.edu-list .item:hover,
.bar:hover {
  transform: scale(1.03);
}

/*=======Services section=======*/
.services .container .content {
  width: 100%;
}

.services-description h3 {
  font-size: 2em;
  margin-bottom: 50px;
}

.service-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(225px, 1fr));
  max-width: 100%;
  margin: 0 auto;
  gap: 20px;
}

.service-card {
  background: var(--card-bg-color);
  border-bottom: 3px solid var(--second-color);
  padding: 50px;
  border-radius: 6px;
  box-shadow: var(--box-shadow);
}

.service-card > i {
  color: var(--second-color);
  font-size: 3em;
  margin-bottom: 30px;
}

.service-card h3 {
  font-size: 1.5em;
  font-weight: 700;
  line-height: 30px;
  margin-bottom: 20px;
}

.service-card .learn-more-btn {
  color: var(--third-color);
  cursor: pointer;
  transition: 0.3s ease;
}

.service-card .learn-more-btn i {
  transition: 0.3s ease;
}

.service-card:hover .learn-more-btn i {
  transform: translateX(10px);
}

.service-modal {
  z-index: 999999;
  position: fixed;
  width: 100%;
  height: 100vh;
  top: 0;
  left: 0;
  background: var(--bg-transparent-color);
  backdrop-filter: blur(10px);
  visibility: hidden;
  opacity: 0;
  transition: 0.3s ease;
}

.service-modal.active {
  visibility: visible;
  opacity: 1;
}

.service-modal-body {
  position: relative;
  background: var(--modal-bg-color);
  max-width: 600px;
  margin: 20px;
  padding: 40px;
  border-radius: 10px;
  box-shadow: var(--box-shadow);
  transform: translateY(-50px);
  transition: 0.5s ease;
}

.service-modal.active .service-modal-body {
  transform: translateY(0px);
}

.service-modal-body .modal-close-btn {
  position: absolute;
  top: 0;
  right: 0;
  margin: 20px;
  cursor: pointer;
}

.service-modal-body h3 {
  font-size: 2em;
}

.service-modal-body h4 {
  font-size: 1.3em;
  font-weight: 600;
  margin: 15px 0 10px;
}

.service-modal-body ul li {
  margin-top: 15px;
}

.service-modal-body ul li i {
  color: var(--second-color);
}

/*=======Portfolio section=======*/
.portfolio .container .content {
  width: 100%;
}

.portfolio-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  max-width: 100%;
  gap: 35px;
  margin: 0 auto;
}

.portfolio-list .img-card {
  position: relative;
  max-width: 100%;
  height: 360px;
  border-radius: 10px;
  box-shadow: var(--box-shadow);
  overflow: hidden;
  cursor: pointer;
}

.portfolio-list .img-card .overlay {
  transition: 1s ease;
}

.portfolio-list .img-card:hover .overlay {
  z-index: 777;
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}

.portfolio-list .img-card .info {
  z-index: 777;
  position: absolute;
  bottom: 0;
  left: 0;
  margin: 20px;
  color: #fff;
  transform: translateY(20px);
  opacity: 0;
  transition: 0.5s ease;
}

.portfolio-list .img-card:hover .info {
  transform: translateY(0);
  opacity: 1;
}

.portfolio-list .img-card .info h3 {
  font-size: 1.5em;
}

.portfolio-list .img-card .info span {
  font-size: 1.2em;
}

.portfolio-list .img-card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.portfolio-model {
  z-index: 999999;
  position: fixed;
  width: 100%;
  height: 100vh;
  top: 0;
  left: 0;
  background: var(--transparent-color-01);
  backdrop-filter: blur(20px);
  visibility: hidden;
  opacity: 0;
  transition: 0.3s ease;
}

.portfolio-model.active {
  visibility: visible;
  opacity: 1;
}

.portfolio-model-body {
  position: relative;
  background: var(--modal-bg-color);
  max-width: 600px;
  margin: 20px;
  padding: 40px;
  border-radius: 10px;
  box-shadow: var(--box-shadow);
  transform: translateY(-50px);
  transition: 0.5s ease;
}

.portfolio-model.active .portfolio-model-body {
  transform: translateY(0);
}

.portfolio-close-btn {
  position: absolute;
  top: 0;
  right: 0;
  margin: 20px;
  cursor: pointer;
}

.portfolio-model-body h3 {
  font-size: 1.5em;
}

.portfolio-model-body img {
  width: 100%;
  margin: 20px 0;
  border-radius: 10px;
}

/*=======Get-in-touch=======*/
.get-in-touch {
  margin-top: 70px;
}

.get-in-touch .container .content {
  width: 100%;
}

.get-in-touch .contact-card {
  position: relative;
  width: 90%;
  background: var(--card-bg-color);
  box-shadow: var(--box-shadow);
  padding: 50px;
  border-radius: 10px;
  column-gap: 50px;
}

.contact-card .title {
  text-transform: uppercase;
  line-height: 60px;
}
.contact-card .title h4 {
  font-size: 1.2em;
  font-weight: 300;
  line-height: 20px;
}

.contact-card .title h3 {
  font-size: 2.3em;
  font-weight: 400;
}
.contact-card .title h2 {
  font-size: 4.2em;
  font-weight: 700;
  background: linear-gradient(to top, transparent 0%, var(--first-color) 30%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  opacity: 0.9;
}

/*=======Contact section=======*/
.contact .container .content {
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.contact-left h2 {
  font-size: 2.1em;
  font-weight: 800;
  margin-bottom: 40px;
}

.contact-list li {
  margin-bottom: 40px;
}

.contact-list li h3 {
  font-size: 1.3em;
  font-weight: 600;
  margin-bottom: 10px;
}

.contact-list li h3 i {
  color: var(--second-color);
  font-size: 1.3em;
  margin-right: 10px;
}

.contact-list li span {
  color: var(--third-color);
  margin-left: 40px;
}

.contact-list li span a {
  color: var(--third-color);
}

.contact-right p {
  color: var(--third-color);
  font-size: 1.6em;
  margin-bottom: 30px;
}

.contact-right p span {
  color: var(--first-color);
  font-weight: 700;
}

.contact-form input,
.contact-form textarea {
  border: none;
  color: var(--first-color);
  background: var(--transparent-color-02);
  font-size: var(--normal-font-size);
  margin-bottom: 20px;
  padding: 15px 40px 40px 20px;
  border-radius: 5px;
}

.contact-form textarea {
  width: 100%;
  resize: none;
}

::placeholder {
  color: var(--first-color);
}

.contact-form .first-row input {
  width: 100%;
}

.contact-form .second-row {
  display: flex;
  justify-content: space-between;
}

.contact-form .second-row input {
  width: 48%;
}

.contact-form .btn {
  border: none;
  margin-top: 0;
  border-radius: 5px;
  cursor: pointer;
}

/*=======Footer=======*/
footer {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background: var(--second-color);
  width: 100%;
  margin-top: 50px;
  padding: 3rem 2rem;
  color: #fff;
}

footer a {
  color: #fff;
}

.footer-container {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 1150px;
}

.footer-container .about h2 {
  font-size: 3em;
  background: linear-gradient(to top, transparent 0%, #fff 50%);
  font-weight: 600;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  opacity: 0.8;
}

.footer-container .about p {
  font-size: var(--normal-font-size);
  font-weight: 300;
  margin-bottom: 30px;
}

.footer-container .info,
.footer-container .follow {
  display: flex;
  align-items: center;
  flex-direction: column;
}

.footer-container .info h3,
.footer-container .follow h3 {
  font-size: 1.1em;
  font-weight: 500;
  margin-bottom: 30px;
}

.footer-container .info ul,
.footer-container .follow ul {
  display: flex;
}

.footer-container .info a {
  margin: 20px;
}

.footer-container .follow a {
  font-size: 1.5em;
  margin: 20px;
}

.footer-copyright p {
  font-size: var(--normal-font-size);
  font-weight: 300;
  margin-top: 50px;
}

/*=======Media query max-width 1070px=======*/
@media screen and (max-width: 1070px) {
  /*=======Header navigation menu=======*/
  .navigation {
    position: fixed;
    width: 100%;
    height: 100vh;
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background: var(--transparent-color-01);
    visibility: hidden;
    opacity: 0;
    transition: 0.3s ease;
  }

  .navigation.active {
    visibility: visible;
    opacity: 1;
  }

  .nav-items {
    position: relative;
    background: var(--modal-bg-color);
    width: 600px;
    max-width: 600px;
    display: flex;
    align-items: center;
    flex-direction: column;
    margin: 20px;
    padding: 40px;
    border-radius: 10px;
    box-shadow: var(--box-shadow);
    transform: translateY(-50px);
    transition: 0.3s ease;
  }

  .navigation.active .nav-items {
    transform: translateY(0);
  }

  .nav-items a {
    margin: 15px 50px;
  }

  .nav-close-btn {
    position: absolute;
    background: url(images/close.png) no-repeat;
    filter: var(--color-filter);
    background-size: 12px;
    background-position: center;
    width: 40px;
    height: 40px;
    top: 0;
    right: 0;
    margin: 10px;
    cursor: pointer;
  }

  .nav-menu-btn {
    background: url(images/open.png) no-repeat;
    background-size: 30px;
    filter: var(--color-filter);
    background-position: center;
    width: 40px;
    height: 40px;
    cursor: pointer;
    display: block;
  }

  /*=======Home section=======*/
  .home .home-container .info {
    font-size: 0.85rem;
  }

  /*=======About section=======*/
  .about .container .content {
    display: grid;
    width: 100%;
    row-gap: 20px;
  }

  .about-img img {
    min-width: 0;
    width: 100%;
  }

  .about-info {
    min-width: 0;
    width: 100%;
  }

  .about-info .professional-list {
    flex-direction: column;
  }

  .about-info .professional-list .list-item {
    justify-content: start;
  }

  /*=======Get-in-touch=======*/
  .get-in-touch .contact-card {
    display: grid;
    width: 100%;
  }

  .contact-card .title {
    font-size: 0.8rem;
    line-height: 50px;
  }

  /*=======Contact section=======*/
  .contact .content {
    flex-direction: column;
    font-size: 0.9rem;
  }

  .contact .contact-left {
    margin-bottom: 40px;
  }

  .contact-form .second-row {
    flex-direction: column;
  }

  .contact-form .second-row input {
    width: 100%;
  }

  /*=======Footer=======*/
  footer .footer-container {
    flex-direction: column;
  }

  .footer-container .about,
  .footer-container .info {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin-bottom: 50px;
  }

  .footer-container .info ul {
    align-items: center;
    flex-direction: column;
  }

  .footer-container .info ul li {
    margin: 5px 0;
  }

  .footer-container .hr {
    width: 100%;
    height: 2px;
    background: rgba(255, 255, 255, 0.1);
    margin: 10px 0 22px;
  }
}

/*=======Media query max-width 730px=======*/
@media screen and (max-width: 730px) {
  /*=======Common styles for all sections=======*/
  body {
    margin: 5rem 0 0 0;
  }

  .section-title-01 {
    font-size: 3em;
  }

  .section-title-02 {
    font-size: 2em;
    transform: translateY(-65px);
  }
  /*=======Home section=======*/
  .home .home-container {
    display: grid;
  }

  .home-container .home-img {
    position: absolute;
  }

  .home-container .home-img img {
    width: 65%;
    transform: translateY(80px, -180px);
  }

  .home .home-container .info {
    font-size: 0.8rem;
  }

  .media-icons {
    margin-bottom: 80px;
  }

  /*=======Get-in-touch section=======*/
  .get-in-touch .contact-card {
    display: grid;
  }

  .contact-card .title {
    font-size: 0.6rem;
    line-height: 40px;
  }

  .contact-card .contact-btn .btn {
    font-size: 0.8rem;
  }
}

  </style>

  <body>

    <!--=======Scroll to top button=======-->
    <div class="scrollToTop-btn flex-center active">
      <i class="fas fa-arrow-up"></i>
    </div>

    <!--=======Light/Dark theme button=======-->
    <div class="theme-btn flex-center">
      <i class="fas fa-moon"></i>
      <i class="fas fa-sun"></i>
    </div>

    <!--=======Header=======-->
    <header>
      <div class="nav-bar">
        <a href="#" class="logo">Ayobami</a>
        <div class="navigation">
          <div class="nav-items">
            <div class="nav-close-btn"></div>
            <a class="active" href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#skills">Skills</a>
            <a href="#services">Services</a>
            <a href="#portfolio">Portfolio</a>
            <a href="#contact">Contact</a>
          </div>
        </div>
        <div class="nav-menu-btn"></div>
      </div>
    </header>

    <!--=======Home section=======-->
    <section class="home flex-center" id="home">
      <div class="home-container">
        <div class="media-icons">
          <a href="#"><i class="fab fa-facebook-f"></i></a>
          <a href="#"><i class="fab fa-twitter"></i></a>
          <a href="#"><i class="fab fa-linkedin"></i></a>
        </div>
        <div class="info">
          <h2>Hi, I am Efuwape Ayobami</h2>
          <h3>Front-end Developer</h3>
          <p>
            I create stunning websites for your business, Highly experienced in
            web design and development.
          </p>
          <a href="" class="btn"
            >Contact Me <i class="fas fa-arrow-circle-right"></i
          ></a>
        </div>
        <div class="home-img">
          <img src="images/era.png" alt="Ayobami's image" />
        </div>
      </div>
      <a href="#about" class="scroll-down"
        >Scroll Down <i class="fas fa-arrow-down"></i
      ></a>
    </section>

    <!--=======About section=======-->
    <section class="about section" id="about">
      <div class="container flex-center">
        <h1 class="section-title-01">About Me</h1>
        <h2 class="section-title-02">About Me</h2>
        <div class="content flex-center"></div>
        <div class="about-img">
          <img src="images/wesley.png.jpg" alt="Ayobami's image" />
        </div>
        <div class="about-info">
          <div class="description">
            <h3>I'm Ayobami</h3>
            <h4>A Lead <span>Front-end Developer</span> based in <span>Nigeria</span></h4>
            <p>
              I design and develop services for customers specializing creating
              stylish, modern websites, web services and online stores. My
              passion is to design digital user experiences through meaningful
              interactions. Check out my portfolio
            </p>
          </div>
          <ul class="professional-list">
            <li class="list-item">
              <h3>2+</h3>
              <span>Years of<br />Experience</span>
            </li>
            <li class="list-item">
              <h3>1+</h3>
              <span>Happy <br />Customers</span>
            </li>
            <li class="list-item">
              <h3>1+</h3>
              <span>Successful <br />Projects</span>
            </li>
          </ul>
          <a href="" class="btn">Download CV <i class="fas fa-dowload"></i></a>
        </div>
      </div>
    </section>
    <!--=======Skill section=======-->
    <section class="skills section" id="skills">
      <div class="container flex-center">
        <h1 class="section-title-01">Skills</h1>
        <h2 class="section-title-02">Skills</h2>
        <div class="content">
          <div class="skills-description">
            <h3>Education & Skills</h3>
            <p>
              For more than 2 year our experts have been accomplishing enough
              with modern Web Development, new generation web programming
              language.
            </p>
          </div>
          <div class="skills-info education-all">
            <div class="education">
              <h4><label>Education</label></h4>
              <ul class="edu-list">
                <li class="item">
                  <span class="year">2021-till date</span>
                  <p>
                    <span>Degree in Computer Science</span> - Olabisi Onabanjo
                    University, Ago-Iwoye, Nigeria
                  </p>
                </li>
                <li class="item">
                  <span class="year">2013-2019</span>
                  <p>
                    <span>O-level</span> - Nigerian Navy Secondary School,
                    Abeokuta, Nigeria
                  </p>
                </li>
              </ul>
              <div class="education">
                <h4><label>Skills</label></h4>
                <ul class="bars">
                  <li class="bar">
                    <div class="info">
                      <span>HTML</span>
                      <span>95%</span>
                    </div>
                    <div class="line html"></div>
                  </li>
                  <li class="bar">
                    <div class="info">
                      <span>CSS</span>
                      <span>80%</span>
                    </div>
                    <div class="line css"></div>
                  </li>
                  <li class="bar">
                    <div class="info">
                      <span>JAVASCRIPT</span>
                      <span>65%</span>
                    </div>
                    <div class="line javascript"></div>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!--=======Services section=======-->
    <section class="services section" id="services">
      <div class="container flex-center">
        <h1 class="section-title-01">Services</h1>
        <h2 class="section-title-02">Services</h2>
        <div class="content">
          <div class="services-description">
            <h3>What I provide</h3>
          </div>
          <ul class="service-list">
            <li class="service-container">
              <div class="service-card">
                <i class="fas fa-file-code"></i>
                <h3>Web Development</h3>
                <div class="learn-more-btn">
                  Learn More <i class="fas fa-long-arrow-alt-right"></i>
                </div>
              </div>
              <div class="service-modal flex-center">
                <div class="service-modal-body">
                  <i class="fas fa-times modal-close-btn"></i>
                  <h3>Web Development</h3>
                  <h4>What is Web Development?</h4>
                  <p>
                    Web development are used to design, build, support, and
                    evolve all types of web-based software.
                  </p>
                  <h4>What I provide</h4>
                  <ul>
                    <li><i class="fas fa-check-circle"></i> Web Development</li>
                    <li><i class="fas fa-check-circle"></i> Testing</li>
                    <li><i class="fas fa-check-circle"></i> Maintenance</li>
                  </ul>
                </div>
              </div>
            </li>
            <li class="service-container">
              <div class="service-card">
                <i class="fas fa-align-left"></i>
                <h3>Content Writing</h3>
                <div class="learn-more-btn">
                  Learn More <i class="fas fa-long-arrow-alt-right"></i>
                </div>
              </div>
              <div class="service-modal flex-center">
                <div class="service-modal-body">
                  <i class="fas fa-times modal-close-btn"></i>
                  <h3>Content Writing</h3>
                  <h4>What is Content Writing?</h4>
                  <p>
                    Content writing is the process of planning, writing and
                    editing web content, typically for digital marketing
                    purposes.
                  </p>
                  <h4>What I provide</h4>
                  <ul>
                    <li>
                      <i class="fas fa-check-circle"></i> Web content writing
                    </li>
                    <li>
                      <i class="fas fa-check-circle"></i> Blog writing for
                      websites
                    </li>
                    <li>
                      <i class="fas fa-check-circle"></i> Social media content
                    </li>
                  </ul>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </section>

    <!--=======Portfolio section=======-->
    <section class="portfolio section" id="portfolio">
      <div class="container flex-center">
        <h1 class="section-title-01">Portfolio</h1>
        <h2 class="section-title-02">Portfolio</h2>
        <div class="content">
          <div class="portfolio-list">
            <div class="img-card-container">
              <div class="img-card">
                <div class="overlay">
                  <div class="info">
                    <h3>Web Development</h3>
                    <span>Youtube</span>
                  </div>
                  <img src="images/cont.jpg" alt="youtube image" />
                </div>
                <div class="portfolio-model flex-center">
                  <div class="portfolio-model-body">
                    <i class="fas fa-times portfolio-close-btn"></i>
                    <h3>Web Developer</h3>
                    <img src="images/cont.jpg" alt="youtube image" />
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipisicing elit,
                      sed do elusmod tempor incididunt ut labore et dolore magna
                      aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                      ullamco laboris nisi ut aliquip ex ea commodo consequat.
                    </p>
                  </div>
                </div>
              </div>
              <div class="img-card-container">
                <div class="img-card">
                  <div class="overlay">
                    <div class="info">
                      <h3>Content Writing</h3>
                      <span>Youtube</span>
                    </div>
                    <img src="images/cont.jpg" alt="Content writing image" />
                  </div>
                  <div class="portfolio-model flex-center">
                    <div class="portfolio-model-body">
                      <i class="fas fa-times portfolio-close-btn"></i>
                      <h3>Content Writing
                      </h3>
                      <img src="images/cont.jpg" alt="content writing image" />
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit,
                        sed do elusmod tempor incididunt ut labore et dolore magna
                        aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                        ullamco laboris nisi ut aliquip ex ea commodo consequat
                      </p>
                    </div>
                  </div>
                </div>
  
            </div>
          </div>
        </div>
      </div>
      <!--=======Get-in-touch=======-->
      <div class="get-in-touch sub-section">
        <div class="container">
          <div class="content flex-center">
            <div class="contact-card flex-center">
              <div class="title">
                <h4>Let's Talk
                </h4>
                <h3>About Your</h3>
                <h2>Next Project</h2>
              </div>
              <div class="contact-btn">
                <a href="" class="btn">Get In Touch <i class="fas fa-paper-plane"></i></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!--=======Contact section=======-->
    <section class="contact section" id="contact">
      <div class="container flex-center">
        <h1 class="section-title-01">Contact Me</h1>
        <h2 class="section-title-02">Contact Me</h2>
        <div class="content">
          <div class="contact-left">
          <h2>Let's discuss your project</h2>
          <ul class="contact-list">
            <li>
              <h3 class="item-title"><i class="fas fa-phone"></i>Phone</h3>
              <span>09037678263</span>
            </li>
            <li>
              <h3 class="item-title"><i class="fas fa-envelope"></i>Email Address</h3>
              <span><a href="mailto:ayobamiefuwape@gmail.com">ayobamiefuwape@gmail.com</a></span>
            </li>
            <li>
              <h3 class="item-title"><i class="fas fa-map-marker-alt"></i>Official Address</h3>
              <span>28, Amororo Str, Iperu Remo, Ogun State, Nigeria.</span>
            </li>
          </ul>
        </div>
        </div>
        <div class="contact-right">
          <p>I'm always open to discussing <br><span>web development work or partnerships</p></span>
          <form action="" class="contact-form">
            <div class="first-row">
              <input type="text" placeholder="Name">
            </div>
            <div class="second-row">
              <input type="email" placeholder="Email">
              <input type="text" placeholder="Subject">
            </div>
            <div class="third-row">
              <textarea name="message" id="" rows="7" placeholder="Message"></textarea>
            </div>
            <button class="btn" type="submit">Send Message <i class="fas fa-paper-plane"></i></button>
          </form>
        </div>
      </div>
    </section>
    <!--=======Footer=======-->
    <footer>
      <div class="footer-container">
        <div class="about group">
          <h2>Ayobami</h2>
          <p>Front-end Developer</p>
          <a href="#about">About Me</a>
        </div>
        <div class="hr"></div>
        <div class="info group">
          <h3>More</h3>
          <ul>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#portfolio">Portfolio</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>
        <div class="hr"></div>
        <div class="follow group">
          <h3>Follow</h3>
          <ul>
          <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
          <li><a href="#"><i class="fab fa-twitter"></i></a></li>
          <li><a href="#"><i class="fab fa-linkedin"></i></a></li>
          </ul>
      </div>
    </div>
    <div class="footer-copyright group">
      <p>&copy; 2023 by Efuwape Ayobami. All rights reserved.</p>
    </div>
    </footer>

    <!--=======External scripts=======-->
    <script src="responsive.js"></script>
  </body>
</html>


