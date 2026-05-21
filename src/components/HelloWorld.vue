<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener" @click="trackLinkClick('vue-cli documentation', 'https://cli.vuejs.org', 'cli_plugins')">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener" @click="trackLinkClick('babel', 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel', 'cli_plugins')">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener" @click="trackLinkClick('eslint', 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint', 'cli_plugins')">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener" @click="trackLinkClick('Core Docs', 'https://vuejs.org', 'essential_links')">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener" @click="trackLinkClick('Forum', 'https://forum.vuejs.org', 'essential_links')">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener" @click="trackLinkClick('Community Chat', 'https://chat.vuejs.org', 'essential_links')">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener" @click="trackLinkClick('Twitter', 'https://twitter.com/vuejs', 'essential_links')">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener" @click="trackLinkClick('News', 'https://news.vuejs.org', 'essential_links')">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener" @click="trackLinkClick('vue-router', 'https://router.vuejs.org', 'ecosystem')">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener" @click="trackLinkClick('vuex', 'https://vuex.vuejs.org', 'ecosystem')">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener" @click="trackLinkClick('vue-devtools', 'https://github.com/vuejs/vue-devtools#vue-devtools', 'ecosystem')">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener" @click="trackLinkClick('vue-loader', 'https://vue-loader.vuejs.org', 'ecosystem')">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener" @click="trackLinkClick('awesome-vue', 'https://github.com/vuejs/awesome-vue', 'ecosystem')">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    trackLinkClick(linkName, linkUrl, category) {
      if (typeof pendo !== 'undefined') {
        pendo.track("External Link Clicked", {
          link_name: linkName,
          link_url: linkUrl,
          link_category: category,
          page_title: document.title
        });
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
