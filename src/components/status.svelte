<script lang="ts">
    import { browser } from '$app/environment'
    import { get, readable } from 'svelte/store'
    import { useLanyard } from 'svelte-lanyard'
  import { fade } from 'svelte/transition';

    const getLanyard = (): ReturnType<typeof useLanyard> => {
        if(browser) {
            return useLanyard("829853860289970236");
        }
        return readable();
    }

    const data = getLanyard();
    const getStatus = () => {
        const status = get(data).discord_status;
        if(["online", "dnd"].indexOf(status) != -1) return "online";
        if(status == "idle") return "idle";
        return "offline";
    }
</script>

{#if $data}
    {#key $data}
        <span class="status {getStatus()}">
            I am currently <span class="display">{getStatus()}</span>.
        </span>
    {/key}
{:else}
    <span class="status loading">
        I am currently <span class="display">???</span>.
    </span>
{/if}