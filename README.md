# Portfolio Web site

### This is a web site about Serter Iyigunlu who is a professional web designer. You can reach me throuh the web site and see my jobs.

## Portfolio web site about Serter Iyigunlu

## Html tags

### Nav bar section

```html
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
```

## Css styling

### Mobile first approach

```css
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
body {
  background-image: url(./images/back.jpg);
  background-size: 100%;
  background-repeat: no-repeat;
}

/* Nav- bar */

nav {
  display: flex;
  margin-top: 1rem;
}
.nav-bar {
  width: 100%;
}
.logo {
  margin-right: auto;
  margin-left: 2rem;
}
.nav-lists {
  width: 70%;
}
.nav-list li {
  font-size: 0.5em;
  margin: 0 1em;
}

.logo-name {
  font-size: 0.6rem;
  display: inline-block;
  font-family: "Montserrat", sans-serif;
  font-weight: 800;
}
.firstLetter {
  font-size: 1.1em;
  color: #d31669;
  font-weight: 300;
}

.nav-lists {
  width: 60%;
}
.nav-list {
  list-style-type: none;
  display: flex;
  padding: 0.5em;
  margin: 0;
  justify-content: space-around;
}

a {
  text-decoration: none;
  color: #f4ba0d;
}
a:hover {
  color: #d31669;
}
```

### Web site progress as shown

![Website progress](./screenshots/first.png)

<br>

![Website second view](./screenshots/second.png)
