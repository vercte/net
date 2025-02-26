<script lang="ts">
    import { onMount } from "svelte";

    let time: Date = $state(new Date());

    let hours = $derived(time.getUTCHours() - 8);
    let formatHours = $derived(((hours + 11) % 12 + 1));
    let period = $derived(hours > 12 || hours < 0 ? "P.M." : "A.M.");

    let minutes = $derived(time.getMinutes());
    let seconds = $derived(time.getSeconds());

    let formatDigit = (d: number): string => {
        if(d < 10) return "0" + d.toString()
        return d.toString();
    }

    onMount(() => {
        const interval = setInterval(() => { time = new Date() }, 1000);
        return () => clearInterval(interval);
    });
</script>

<span class="time">
    LOCAL TIME: {formatHours}:{formatDigit(minutes)}:{formatDigit(seconds)} {period}
</span>
