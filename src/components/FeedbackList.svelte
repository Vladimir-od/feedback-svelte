<script>
import { FeedbackStore } from './../stores.js';
import { fade,scale } from "svelte/transition";
import FeedbaclItem from "./FeedbaclItem.svelte";
</script>   


{#each $FeedbackStore as fb (fb.id)}
<div in:scale='{{duration: 500}}' out:fade='{{duration : 500}}'>
    <FeedbaclItem item={fb} />
</div>

{/each}