<script lang="ts">
  export let target: string = '_blank';

  export let content: string;
  export let href: string;
</script>

<li><a {href} {target}>{content}</a></li>
