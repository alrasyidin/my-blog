<template>
  <div class="layout">
    <slot/>
    <div class="footer">
      <p>
        Built with
        <a class="link" href="//gridsome.org">Gridsome</a>
        & Made with ❤️ by
        <a class="link" href="//id.linkedin.com/in/hamstergeek" target="_blank">hamstergeek</a>
      </p>
    </div>
  </div>
</template>

<style>
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
  border: 15px solid #fecd43;
  min-height: 100vh;
}

img{
  max-width: 100%;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.footer {
  padding-top: calc(30em / 4);
  text-align: center;
  font-size: 1em;
}

.link {
  border: 2px dashed #fecd43;
  padding: 7px;
  color: #333;
  text-decoration: none;
}

.navi {
  list-style: none;
  padding: 0;
}

.navi__li {
  display: inline-block;
  margin: 0 .5em
}
</style>
