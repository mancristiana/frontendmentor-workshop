* Overlay effect using Grid

* Developer tools in Chrome
* Responsiveness using max-width, Flexbox

Media Queries
* Change picture based on media query
* Change styles based on media query

--overlayColor: hsla(277, 100%, 36%, 0.4);

picture {
  display: grid;
  grid-template: 1fr / 1fr;
}

picture * {
  grid-row: 1 / 2;
  grid-column: 1 / 2;
}

picture .overlay {
  background-color: var(--overlayColor);
}

<picture>
    <source
    media="(min-width: 1000px)"
    srcset="images/image-header-desktop.jpg"
    />
    <img
    src="images/image-header-mobile.jpg"
    alt="data analysts typing on computer"
    />
    <div class="overlay"></div>
</picture>


body {
    display: flex;
    flex-direction: column;
    align-items: center;
}

main {
    max-width: 45ch;
}

.stat {
    margin: 20px;
}

@media screen and (min-width: 500px) {
    dl {
      display: flex;
    }
  }

@media screen and (min-width: 1000px) {
    main {
        display: flex;
        flex-direction: row-reverse;
        max-width: 100ch;
    }

    .content {
        max-width: 45ch;
        align-items: flex-start;
        text-align: left;
        padding: 48px 64px;
    }

    .stat:first-child {
        margin-left: 0;
    }
}