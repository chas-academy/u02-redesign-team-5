# Myh-grupp-5

html &amp; css uppgift nr2

## Introduction

This project makes the site myh.se responsive and possible to use when on a smaller device (i.e. phone or tablet). Hopefully the layout will make more sense to the user and make the experience on the site a bit less cluttered - with the perk of having the most used and wanted things easily available to the user.

## Product Backlog

- mobile responsiveness
- responsive layout
- repetitions on the site
  - repetitions we want
  - repetitions we don't want
  - common theme for repetitions
- make everything clickable that looks clickable
- make searchways correct (arrows instead of forward slash)
- set definition of userstory
- set basic structure
- better structure on the page

## Demands

#### Will work with

- Senaste Chrome
- Senaste Firefox
- Senaste Safari
- Microsoft Edge

#### Devices that will be tested

- PC desktop (upplösning 1920x1080p och uppåt)
- Laptop (upplösning 1280 x 900 och uppåt)
- Apple iPhone 8 (414x736)

#### Content demands

Innehåller ny design för samtliga landningssidor i MYH.se
huvudmeny:

- Start
- Om oss
- Verksamhetsområden
- Lagar, regler, tillsyn
- Statistik
- Publikationer
- Nyhetsrum
- Kontakt
- Är grundläggande tillgänglighetsanpassad

#### Layout demands

- Responsiv
- Parallax scrolling
- Rudimentära CSS animationer
- Inbäddad media såsom video och/eller ljud
- Statiskt kontaktformulär

---

## STYLING

#### Media querys

- @media screen and (max-width: 1280px)
- @media screen and (max-width: 720px)

#### Accordion in CSS

##### HTML

```html
<ul class="accordion4">
  <li class="accordion-item4">
    <p class="accordion-h6">Dela denna info 💻</p>
    <p class="accordion-h6">⬇</p>
    <div class="accordion-item-content4">
      <hr />
      <img
        class="thumbnail"
        src="assets/fb.png"
        alt="fb-icon"
        width="25"
        height="25"
      />
      <img
        class="thumbnail"
        src="assets/mail.png"
        alt="mail-icon"
        width="25"
        height="25"
      />
      <img
        class="thumbnail"
        src="assets/twitter.png"
        alt="twitter-icon"
        width="25"
        height="25"
      />
    </div>
  </li>
</ul>
```

##### CSS

```css
.accordion1 .accordion2 .accordion3 .accordion4 .accordion-item,
.accordion-item1,
.accordion-item2,
.accordion-item3,
.accordion-item4 {
  background-image: linear-gradient(90deg, #eee, #f5f5f5, #eee);
  border: 1px solid #666;
  padding: 1em;
  color: #eee;
  margin: 25px;
  width: 220px;
}

.accordion-h6 {
  font-size: 14px;
  font-weight: 400;
  text-align: center;
  text-decoration: none;
  color: black;
  font-family: "Roboto";
}

.accordion-p {
  font-family: "Open Sans";
  font-size: 12px;
  font-weight: 100;
  text-decoration: none;
  color: black;
  width: fit-content;
}

.accordion-p:hover {
  font-size: 16px;
  transition: 0.3s;
  width: fit-content;
}

.accordion-p-q {
  font-size: 12px;
  font-weight: 100;
  text-decoration: none;
  color: black;
  font-family: "Open Sans";
}

.accordion4 .accordion-item4 {
  background-color: hsl(80, 40%, 40%);
  background-image: linear-gradient(
    -90deg,
    hsl(80, 80%, 40%),
    hsl(80, 80%, 35%) 2em,
    hsl(80, 80%, 40%)
  );
}

.accordion-item4:hover .accordion-item-content4,
.accordion-item4--default {
  height: 7em;
}

.accordion-item-content4 {
  height: 0;
  overflow: hidden;
  transition: height 0.25s;
}
```

#### SELECT BUTTONS

##### HTML

```HTML

<div class="section">
          <label for="activity-type"> <h4>Verksamhetsområde</h4> </label>
          <select id="activity-type" name="activity-type">
            <option value="">Verksamhetsområde</option>
            <option value="yrkeshogskolan">Yrkeshögskolan</option>
            <option value="kulturutbildningar">
              Konst- och kulturutbildningar
            </option>
            <option value="tolkutbildningar">Tolkutbildningar</option>
            <option value="tillsyn">Utbildningar med endast tillsyn</option>
            <option value="validering">Validering</option>
            <option value="seqf">SeQF</option>
          </select>
        </div>
```

##### CSS

```CSS
select,
#searchPub {
  width: 170px;
  padding-left: 5px;
  font-size: 14px;
  border: 1px solid #000;
  height: 34px;
  background: whitesmoke;
}

select {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  background: url("images/arrow.png") 96% / 6% no-repeat whitesmoke;
}
```

#### PAGINATION

##### HTML

```HTML
<div class="center-number">
        <div class="pagination">
          <a href="#">&laquo;</a>
          <a href="#" class="active">1</a>
          <a href="#">2</a>
          <a href="#">3</a>
          <a href="#">4</a>
          <a href="#">5</a>
          <a href="#">&raquo;</a>
        </div>
      </div>
```

##### CSS

```CSS
.center-number {
  text-align: center;
}

.pagination {
  display: flex;
  justify-content: center;
}

.pagination > a {
  color: #000;
  padding: 8px 16px;
  text-decoration: none;
  transition: background-color 0.2s;
  border: 1px solid #000;
  margin: 0 4px;
}

.pagination > a.active {
  background-color: yellow;
  border: 2px solid #000;
}

.pagination > a:hover:not(.active) {
  background-color: whitesmoke;
}
```
