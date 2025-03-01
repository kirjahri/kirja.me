<script lang="ts">
  export let target: string = '_blank';

  export let content: string;
  export let href: string;
</script>

<li class="m-4"><a {href} {target} class="block w-64">{content}</a></li>
