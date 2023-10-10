<script>
    import TopLeft from "./rectangle1.svelte";
    import MidLeft from "./rectangle2.svelte";
    import BotLeft from "./rectangle3.svelte";
    import PinkStrip from "./pinkStrip.svelte";
    import PurpleStrip from "./purpleStrip.svelte";
    import YellowStrip from "./yellowStrip.svelte";
</script>

<div class="all">
    <div class="top">
        <TopLeft />
    </div>
    <div class="mid">
        <MidLeft />
    </div>
    <div class="bot">
        <BotLeft />
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
