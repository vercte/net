<script lang="ts">
    const { padding, direction, children }: { padding?: string, direction?: string, children: any } = $props()
</script>

<div class="center" style="flex-direction: {direction || "column"}; padding: {padding || "0"};">
    {@render children()}
</div>

<style>
    div.center {
        display: flex;
        justify-content: center;
        text-align: center;
        flex-wrap: wrap;
        gap: 0.7em;

        width: 1fr;
    }
</style>