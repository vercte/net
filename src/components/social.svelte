<script lang="ts">
    interface SocialProps {
        name: string;
        social: string;
        link: string;
        color: string;
    }

    const props: SocialProps = $props();
</script>

<a id="social-{props.social}" class="social {props.social}" style="--social-color: {props.color};"
    href={props.link} aria-label={props.name} title={props.name} target="_blank">
    <div id="icon" style="mask: url('/social/{props.social}.png');"></div>
</a>