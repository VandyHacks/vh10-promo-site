<script>
    import TopRight from "./rectangle4.svelte";
    import MidRight from "./rectangle5.svelte";
    import BotRight from "./rectangle6.svelte";
    import HotPinkStrip from "./hotpinkStrip.svelte";
    import BlueStrip from "./blueStrip.svelte";
    import PurpleStrip from "./purpleStrip2.svelte";
</script>

<div class="all">
    <div class="top">
        <TopRight />
    </div>
    <div class="mid">
        <MidRight />
    </div>
    <div class="bot">
        <BotRight />
    </div>
</div>

<style>
    .all {
        display: flex;
        flex-direction: column;
    }
    .top {
        align-items: center;
    }
    .mid {
        align-items: left;
    }
    .bot {
        align-items: right;
    }
</style>
