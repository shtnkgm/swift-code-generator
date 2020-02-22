<template>
<div id="app" class="uk-container uk-container-small">
  <nav class="uk-navbar-container uk-navbar-transparent" uk-navbar>
    <div class="uk-navbar-left">
      <a class="uk-link-heading" href="https://shtnkgm.github.io/SwiftCodeGenerator/">Swift Code Generator</a>
    </div>
    <div class="uk-navbar-right">

      <ul class="uk-navbar-nav">
        <li><a href="https://github.com/shtnkgm/SwiftCodeGenerator">GitHub</a></li>
      </ul>

    </div>
  </nav>

  <h1><a class="uk-link-heading" href="https://shtnkgm.github.io/SwiftCodeGenerator/">Swift Code Generator</a></h1>
  <button class="uk-button uk-button-primary uk-button-small uk-margin" @click="demo1OnClick">Try it</button>
  <!-- <button class="uk-button uk-button-secondary uk-button-small uk-margin" @click="demo2OnClick">Demo 2</button> -->
  <button class="uk-button uk-button-default uk-button-small uk-margin" @click="clearOnClick">Clear</button>
  <textarea :placeholder="[[ placeholder ]]" @="text" class="uk-textarea"></textarea>
  <template v-if="alert.length > 0">
    <div class="uk-alert-danger" uk-alert>
      <a class="uk-alert-close" uk-close></a>
      <p>{{alert}}</p>
    </div>
  </template>
  <template v-if="text.length > 0">
    <h2>Generated Code</h2>
    <h3>Memberwise Initializer</h3>
    <p style="white-space: pre-line">
      <pre class="hljs lang-swift"><code>{{ memberwiseInitializer }}</code></pre>
    </p>
    <h3>Factory Method</h3>
    <p style="white-space: pre-line">
      <pre class="hljs lang-swift"><code>{{ factoryMethod }}</code></pre>
    </p>
    <h3>Codable Implementation</h3>
    <p style="white-space: pre-line">
      <pre class="hljs lang-swift"><code>{{ codableImplementation }}</code></pre>
    </p>
    <h3>Equatable Implementation</h3>
    <p style="white-space: pre-line">
      <pre class="hljs lang-swift"><code>{{ equatableImplementation }}</code></pre>
    </p>
    <h3>Matchable Implementation for <a href="https://github.com/Brightify/Cuckoo" target="_blank"
        rel="noopener noreferrer">Cuckoo</a></h3>
    <p style="white-space: pre-line">
      <pre class="hljs lang-swift"><code>{{ matchableImplementation }}</code></pre>
    </p>
  </template>
  <hr>
  <article class="uk-comment uk-comment-primary">
    <div class="uk-comment-body uk-text-small">
      <p>Code generator for the following methods.</p>
      <ul>
        <li>Memberwise Initializer</li>
        <li>Factory Method</li>
        <li>Codable Implementation</li>
        <li>Equatable Implementation</li>
        <li>Matchable Implementation for <a href="https://github.com/Brightify/Cuckoo" target="_blank"
            rel="noopener noreferrer">Cuckoo</a></li>
      </ul>
      <p>Currently in β version.</p>
    </div>
  </article>
  <hr>
  <div class="uk-margin-auto">
    <p>Copyright 2020 @shtnkgm. All Rights Reserved.</p>
  </div>
</div>
</template>

<script>
export default {
  name: "App",
  components: {}
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
