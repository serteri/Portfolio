# Portfolio Web site

### This is a web site about Serter Iyigunlu who is a professional web designer. You can reach me throuh the web site and see my jobs.

## Portfolio web site about Serter Iyigunlu

### Font-color choosing

#### I choosed colored coolers font color because I wanted my site give an expression to cool view to the viewer. Mainly orange,red orangew,forest green and lime green colors used.

## Html tags

<br>

### Nav bar section for home page

```html
<section class="nav-bar">
  <nav>
    <div class="logo">
      <a href="./">
        <img src="./images/logo1.png" alt="company logo" />
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

## Footer section of the web site

```html
<footer>
  <div class="iconShow">
    <a
      href="https://www.linkedin.com/in/serter-iyigunlu-18897955/"
      class="icon-link"
    >
      <i class="fa-brands fa-linkedin  icons"></i>
    </a>
    <a href="https://twitter.com/home" class="icon-link">
      <i class="fa-brands fa-twitter icons"></i>
    </a>
    <a href="https://github.com/serteri" class="icon-link">
      <i class="fa-brands fa-github  icons"></i>
    </a>
  </div>
  <span class="copyRight">&copy Copyright 2022,Serter Iyigunlu</span>
</footer>
```

## Sass styling for home page mobile approach

### button scss

```css
@mixin button {
  padding: 0.5rem;
  border-radius: 85px;
  background-color: $color-backgroung;
  color: $color-btn;
  font-size: 0.6rem;

  &:hover {
    color: $color-general;
    transform: scale(1.3);
  }
}

@mixin button-about {
  padding: 0.5rem;
  border-radius: 85px;
  background-color: $color-ahover;
  color: $color-btn;
  font-size: 0.3rem;
}
```

### color scss

```css
$color-general: #e55b13;
$color-links: #f6a21e;
$color-ahover: #e55b13;
$color-btn: #41729f;
$color-backgroung: #e7f2f8;
$color-nav-logo-letter: #7a871e;
```

### default scss

```css
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

$nav: 1rem;
$width_general: 100%;

$padding-general: 1.5rem;
```

### flex box scss

```css
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
```

### fonst scss

```css
$fontsize-general: 0.5rem;
$font-size-firstletters: 1rem;
$font-size-middle: 1.2rem;
$fontsize-big: 1.3rem;
$font-size-bigger: 2rem;
$font-size-p: 0.9em;
$fontfamily-general: "Montserrat", sans-serif;
```

## Navigation Design

```css
.nav-bar {
  width: 100%;
  background-color: $color-backgroung;
  height: 2.5rem;

  nav {
    @include flex-box-center;

    img {
      width: 48px;
      margin: 0 1em;
    }
    .nav-lists {
      width: 60%;
      li {
        font-size: $fontsize-general;
      }
    }
    .nav-list {
      list-style-type: none;
      display: flex;
      justify-content: flex-end;
      li {
        padding-left: 1.2rem;
        a {
          text-decoration: none;
          color: $color-links;
          &:hover {
            color: $color-ahover;
          }
        }
      }
    }
  }
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

![Website third view](./screenshots/third.png)
<br>

#### Third view for mobile

![Website third view](./screenshots/third-mobile.png)

<br>

#### Fourth view for mobile

![Website fourth view](./screenshots/30%20october%20mobile%20screenshot.png)
