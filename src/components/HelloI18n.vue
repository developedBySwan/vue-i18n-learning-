<template>
  <div>
    <h1>{{ $t("lan") }}</h1>
    <p>{{ $t("message") }}</p>
    <span>
      {{ $t("friut.apple") }}
    </span>
    <span>
      {{ $t("fruid.kiwi") }}
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
  methods: {
    change(lang) {
      this.$i18n.locale = lang;
    },
  },
};
</script>
