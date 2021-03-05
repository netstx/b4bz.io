<template>
  <a
    href="#"
    data-name="contact"
    data-domain="thinkpad"
    data-tld="io"
    onclick="window.location.href = 'mailto:' + this.dataset.name + '@' + this.dataset.domain + '.' + this.dataset.tld; return false;"
    aria-label="contact me!"
  >
    <slot />
  </a>
</template>


<script>
export default {
  name: "SafeEmail",
  props: {
    icon: Boolean
  }
};
</script>

<style lang="scss" scoped>
.text-link.chm-safe-email:after {
  content: attr(data-name) "@" attr(data-domain) "." attr(data-tld);
}
</style>
