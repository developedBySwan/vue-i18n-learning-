<template>
  <div>
    <h1>{{ $t("lan") }}</h1>
    <p>{{ $t("message", { name }) }}</p>
    <span>
      {{ $t("friut.apple") }}
    </span>
    <span>
      {{ $t("fruid.kiwi") }}
    </span>
    <span>
      {{ $tc("car", 10) }}
    </span>
    <div>
      <button @click="change('en')">English</button>
      <button @click="change('mm')">Myanmar</button>
      <button @click="change('th')">Thailand</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloI18n",
  data() {
    return {
      name: "Vue.js",
    };
  },
  methods: {
    change(lang) {
      this.$i18n.locale = lang;
      localStorage.setItem("lang", lang);
    },
  },
};
</script>
