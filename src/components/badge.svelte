<script lang="ts">
    const { name, badge, link }: { name: string, badge: string, link?: string } = $props();
</script>

<a id="badge-{badge}" class="badge" href={link || "#"}
    aria-label={name} title={name} target="_blank">
    <img src="/badges/{badge}" alt={name}/>
</a>