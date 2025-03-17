<script lang="ts">
  import '@fontsource/inter/400.css';
  import '@fontsource/inter/700.css';
  import '@fontsource/inter/400-italic.css';
  import '@fontsource/inter/700-italic.css';
  import '@fontsource/ibm-plex-mono/400.css';
  import '@fontsource/ibm-plex-mono/700.css';
  import '@fontsource/ibm-plex-mono/400-italic.css';
  import '@fontsource/ibm-plex-mono/700-italic.css';

  import '../app.css';

  let { children } = $props();
</script>

{@render children?.()}
