<script lang="ts">
    let mode = "normal";
</script>

实例 ({mode})
<h1 class="title">
    Mix Blend Mode:
    <select id="select" bind:value={mode}>
        <option value="normal">normal -- 正常</option>
        <option value="multiply">multiply -- 正片叠底</option>
        <option value="screen">screen -- 滤色</option>
        <option value="overlay">overlay -- 叠加</option>
        <option value="darken">darken -- 变暗</option>
        <option value="lighten">lighten -- 变亮</option>
        <option value="color-dodge">color-dodge -- 颜色减淡</option>
        <option value="color-burn">color-burn -- 颜色加深</option>
        <option value="hard-light">hard-light -- 强光</option>
        <option value="soft-light">soft-light -- 柔光</option>
        <option value="difference">difference -- 差值</option>
        <option value="exclusion">exclusion -- 排除</option>
        <option value="hue">hue -- 色相</option>
        <option value="saturation">saturation -- 饱和度</option>
        <option value="color">color -- 颜色</option>
        <option value="luminosity">luminosity -- 亮度</option>
    </select>
</h1>

<div class="container">
    <div class="red" style="mix-blend-mode: {mode};" />
    <div class="blue" style="mix-blend-mode: {mode};" />
    <div class="white" style="mix-blend-mode: {mode};" />
</div>

<style>
    .title {
        color: #333;
        font-size: 24px;
        line-height: 32px;
        text-align: center;
    }

    .container {
        position: relative;
        width: 150px;
        height: 150px;
        margin: 100px auto;
    }

    .container > div {
        position: absolute;
        top: 0;
        left: 0;
        width: 150px;
        height: 150px;
        border-radius: 50%;
        mix-blend-mode: normal;
    }

    .container > .red {
        background-color: rgba(255, 0, 0, 0.8);
        transform: translateX(25%);
    }

    .blue {
        background-color: rgba(0, 255, 0, 0.8);
        transform: translateX(-25%);
    }

    .white {
        background-color: rgba(0, 0, 255, 0.8);
        transform: translateY(-25%);
    }
</style>
