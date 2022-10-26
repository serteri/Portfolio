# Portfolio Web site

### This is a web site about Serter Iyigunlu who is a professional web designer. You can reach me throuh the web site and see my jobs.

## Portfolio web site about Serter Iyigunlu

## Html tags

<br>

### Nav bar section for home page

```html
<section class="nav-bar">
  <nav>
    <div class="logo">
      <a class="logo-name" href="./">
        <span class="firstLetter">S</span>
        erter
        <span class="firstLetter">I</span>
        yigunlu
      </a>
    </div>
    <div class="nav-lists">
      <ul class="nav-list">
        <li>
          <a href="./">Home</a>
        </li>
        <li>
          <a href="aboutMe.html" target="_blank"> About Me</a>
        </li>
        <li>
          <a href="myExperience.html" target="_blank">Portfolio</a>
        </li>
        <li>
          <a href="contactMe.html" target="_blank">Contact me</a>
        </li>
      </ul>
    </div>
  </nav>
</section>
```

<br>

### Main section for home page

```html
<!--Main Section-->
<main class="main-content">
  <div class="contactMe">
    <h3 id="salute">
      <span id="firstSalute">Hello,</span>
      <br />
      My Name is
      <i id="name">Serter Iyigunlu</i>
    </h3>
    <p id="info">To see My Portfolio please click below</p>
    <button
      class="btn"
      type="button"
      onclick="location.href ='./myExperience.html'"
    >
      Contact Me!
    </button>
  </div>
  <div class="signUp">
    <h2 class="join-list">Join our newsletter</h2>
    <form id="form-signUp">
      <div class="form-elements">
        <label for="first-name" class="select"> First Name: </label>
        <input
          type="text"
          name="fist-name"
          id="first-name"
          placeholder="First Name"
          class="select-input"
        />
      </div>
      <div class="form-elements">
        <label for="last-name" class="select"> Last Name: </label>
        <input
          type="text"
          name="last-name"
          id="last-name"
          placeholder="Last Name"
          class="select-input"
        />
      </div>
      <div class="form-elements">
        <label for="email" class="select"> Email address: </label>
        <input
          type="email"
          name="email"
          id="email"
          placeholder="Email address"
          class="select-input"
        />
      </div>
      <div class="form-elements">
        <button class="btn" type="submit" name="submit">Send</button>
      </div>
    </form>
  </div>
</main>
```

<br>

## Sass styling for home page mobile approach

```css
// Sass variables
$nav: 1rem;
$width_general: 100%;
@mixin flex-box-center {
  display: flex;
  justify-content: center;
  align-items: center;
}
@mixin flex-box-center-column {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
$fontsize-general: 0.5rem;
$font-size-firstletters: 1rem;
$font-size-middle: 1.2rem;
$fontsize-big: 1.3rem;
$font-size-p: 0.9em;
$fontfamily-general: "Montserrat", sans-serif;
$color-general: #104210;
$color-links: #f6a21e;
$color-ahover: #e55b13;
$color-btn: #41729f;
$color-backgroung: #f3f3f3;
$color-nav-logo-letter: #7a871e;
$padding-general: 1.5rem;

// General declarations

- {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

// Navigation Design
nav {
  @include flex-box-center;
}
.nav-bar {
  width: $width_general;
  background-color: $color-backgroung;
  height: 2rem;
}
.logo {
  margin-right: auto;
  margin-left: 1rem;
}
.logo-name {
  font-size: $fontsize-general;
  display: inline-block;
  font-family: "Montserrat", sans-serif;
  font-weight: 800;
  color: $color-nav-logo-letter;
}
.firstLetter {
  font-size: $font-size-firstletters;
  color: $color-general;
  font-weight: 600;
}
.nav-lists {
  width: 60%;
}
.nav-list li {
  font-size: $fontsize-general;
  margin: 0 1em;
}

.nav-list {
  list-style-type: none;
  display: flex;
  padding: 0.5em;
  margin: 0;
  justify-content: space-around;
  a {
    text-decoration: none;
    color: $color-links;
  }
  a:hover {
    color: $color-ahover;
  }
}

// Main section

.main-content {
  @include flex-box-center-column();
  background-image: url(./images/back.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  height: 80%;
}
.contactMe {
  @include flex-box-center-column();
  margin-top: 1rem;
}
#salute {
  font-size: $fontsize-general;
  color: black;
  font-family: $fontfamily-general;
  #firstSalute {
    font-size: $font-size-firstletters;
    display: inline-block;
    padding-bottom: 2rem;
  }
  #name {
    font-size: $font-size-firstletters;
  }
}

#info {
  color: $color-general;
  font-family: "Montserrat", sans-serif;
  margin-top: 2rem;
  font-weight: 600;
  margin-bottom: 1rem;
  font-size: $fontsize-general;
}
.btn {
  padding: 0.5rem;
  border-radius: 85px;
  background-color: $color-backgroung;
  color: $color-btn;
  font-size: 0.3rem;
  .btn:hover {
    color: $color-general;
  }
}

.signUp {
  @include flex-box-center-column();
  margin-bottom: 1.2rem;
}

.join-list {
  margin-top: 2rem;
  color: $color-general;

  font-family: $fontfamily-general;
  font-size: $fontsize-general;
  padding-bottom: 0.5rem;
}
#form-contact {
  text-align: center;
  padding-top: 2rem;
  padding-bottom: 4rem;
  legend {
    margin-bottom: 1.2rem;
  }
}
.form-contact {
  background-image: url(./images/contact.jpg);
  background-size: cover;
  width: 100%;
  height: 100%;
}

.form-elements {
  margin-top: 0.6rem;
  width: 80%;
}
.select {
  width: 80px;
  display: inline-block;
  color: $color-links;
  font-size: 0.6rem;
  font-weight: bolder;
}
.select-input {
  width: 30%;
}
input::placeholder {
  font-size: 0.4rem;
}
#message {
  width: 40%;
}
textarea::placeholder {
  font-size: 0.4rem;
}
.newsletter {
  list-style-type: none;
  font-family: $fontfamily-general;
  font-size: 0.6rem;
  li {
    color: darkgreen;
    font-weight: bolder;
  }
}
.checkbox {
  width: 9px;
  height: 9px;
}
.signings {
  @include flex-box-center();
}
// footer
.iconShow {
  @include flex-box-center();
  height: 20px;
  width: 100vw;
}
.icon-contact {
  margin-top: 9rem;
}
.icons {
  color: rgb(241, 240, 255);
  margin-left: 0.9rem;
  background-color: #000080;
  font-size: 0.6rem;
}
.copyRight {
  display: block;
  margin-left: 0.5rem;
  font-size: 0.4rem;
  margin-top: 0.9rem;
}
```

## Css for other devies

```css
// * Media Queries */

@media screen and (min-width: 600px) {
  .nav-bar {
    width: 100%;
    background-color: #e7f2f8;
    height: 2rem;
  }

  .logo-name {
    font-size: 0.6rem;
    display: inline-block;
    font-family: "Montserrat", sans-serif;
    font-weight: 800;
  }
  .nav-lists {
    width: 80%;
  }
  .nav-list li {
    font-size: $fontsize-general;
  }
  .firstLetter {
    font-size: 1.2em;

    font-weight: 800;
  }
  .main-content {
    @include flex-box-center();
    width: 100%;
    height: 80%;
  }
  .contactMe {
    margin-right: 5rem;
  }
  .form-contact {
    background-image: url(./images/contact.jpg);
    background-size: cover;

    width: 100%;
    height: 100%;
  }
  .btn {
    padding: 0.5rem;
    border-radius: 85px;
    background-color: #c3e0e5;
    color: $color-btn;
    font-size: 1rem;
  }
  .join-list {
    color: black;
    font-family: "Montserrat", sans-serif;
    font-size: 2rem;
    padding-bottom: 0.5rem;
  }
  #salute {
    color: black;
    font-family: "Montserrat", sans-serif;
    font-size: 1.6rem;
  }
  #firstSalute {
    font-size: 2rem;
    display: inline-block;
    padding-bottom: 2rem;
  }
  #info {
    color: rgb(238, 73, 8);
    font-family: "Montserrat", sans-serif;
    margin-top: 2rem;
    font-weight: 600;
    margin-bottom: 1.4rem;
    font-size: 1.6rem;
  }
  #name {
    font-size: $font-size-middle;
  }
  .form-elements {
    margin-top: 0.6rem;
    width: 100%;
  }

  .select {
    width: 140px;
    display: inline-block;
    font-size: 1rem;
  }
  .select-input {
    width: 50%;
  }
  input::placeholder {
    font-size: 0.8rem;
  }
}
@media screen and (min-width: 760px) {
  .nav-bar {
    width: 100%;
    background-color: #e7f2f8;
    height: 2rem;
  }

  .logo-name {
    font-size: 0.8rem;
    display: inline-block;
    font-family: "Montserrat", sans-serif;
    font-weight: 800;
  }
  .nav-lists {
    width: 80%;
  }
  .nav-list li {
    font-size: 0.9em;
  }
  .firstLetter {
    font-size: 1.2em;

    font-weight: 800;
  }
  .main-content {
    @include flex-box-center();
    width: 100%;
    height: 80%;
  }
  .contactMe {
    margin-right: 5rem;
  }
  .form-contact {
    background-image: url(./images/contact.jpg);
    background-size: cover;

    width: 100%;
    height: 100%;
  }
  .btn {
    padding: 0.5rem;
    border-radius: 85px;
    background-color: #c3e0e5;
    color: $color-btn;
    font-size: 1rem;
  }
  .join-list {
    color: black;
    font-family: "Montserrat", sans-serif;
    font-size: 2rem;
    padding-bottom: 0.5rem;
  }
  #salute {
    color: black;
    font-family: "Montserrat", sans-serif;
    font-size: 1.6rem;
  }
  #firstSalute {
    font-size: 2rem;
    display: inline-block;
    padding-bottom: 2rem;
  }
  #info {
    color: rgb(238, 73, 8);
    font-family: "Montserrat", sans-serif;
    margin-top: 2rem;
    font-weight: 600;
    margin-bottom: 1.4rem;
    font-size: 1.6rem;
  }
  #name {
    font-size: $font-size-middle;
  }
  .form-elements {
    margin-top: 0.6rem;
    width: 100%;
  }

  .select {
    width: 140px;
    display: inline-block;
    font-size: 1rem;
  }
  .select-input {
    width: 50%;
  }
  input::placeholder {
    font-size: 0.8rem;
  }
}
@media screen and (min-width: 960px) {
  .nav-bar {
    width: 100%;
    background-color: #e7f2f8;
    height: 2.3rem;
  }

  .logo-name {
    font-size: 1.2rem;
    display: inline-block;
    font-family: "Montserrat", sans-serif;
    font-weight: 800;
  }
  .nav-lists {
    width: 70%;
  }
  .nav-list li {
    font-size: $fontsize-big;
  }
  .firstLetter {
    font-size: 1.2em;

    font-weight: 800;
  }
  .main-content {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 80%;
  }
  .contactMe {
    margin-right: 5rem;
  }
  .form-contact {
    background-image: url(./images/contact.jpg);
    background-size: cover;

    width: 100%;
    height: 100%;
  }
  .btn {
    padding: 0.5rem;
    border-radius: 85px;
    background-color: #c3e0e5;
    color: $color-btn;
    font-size: 1rem;
  }
  .join-list {
    color: black;
    font-family: "Montserrat", sans-serif;
    font-size: 3rem;
    padding-bottom: 0.5rem;
  }
  #salute {
    color: black;
    font-family: "Montserrat", sans-serif;
    font-size: 1.6rem;
  }
  #firstSalute {
    font-size: 3rem;
    display: inline-block;
    padding-bottom: 2rem;
  }
  #info {
    color: rgb(238, 73, 8);
    font-family: "Montserrat", sans-serif;
    margin-top: 2rem;
    font-weight: 600;
    margin-bottom: 1.4rem;
    font-size: 1.6rem;
  }
  #name {
    font-size: $font-size-middle;
  }
  .form-elements {
    margin-top: 0.6rem;
    width: 100%;
  }

  .select {
    width: 140px;
    display: inline-block;
    font-size: 1rem;
  }
  .select-input {
    width: 50%;
  }
  input::placeholder {
    font-size: 0.8rem;
  }
}
```

### Web site progress as shown

#### First view

![Website progress](./screenshots/first.png)

<br>

#### Second view

![Website second view](./screenshots/second.png)

<br>

#### Third view

![Website thied view](./screenshots/third.png)
<br>

#### Third view for mobile

![Website thied view](./screenshots/third-mobile.png)
