从完整的图形分割成多个小图形
<div class="page">
    <hgroup class="triangle2rect">
        <div class="a"></div>
        <div class="b"></div>
        <div class="c"></div>
        <div class="d"></div>
    </hgroup>
</div>

<style>
    .page {
        height: 200px;
    }
    .triangle2rect {
        position: relative;
        width: 100px;
        height: 100px;
        transform: translate(-50%, -50%);
        animation: aniContainer 2s infinite alternate;
        margin-left: 200px;
        margin-top: 100px;
    }

    .triangle2rect div {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }

    .a {
        background: deeppink;
        clip-path: polygon(0% 0%, 0% 100%, 50% 50%);
        animation: a 2s infinite alternate;
    }
    .b {
        background: deeppink;
        clip-path: polygon(0% 0%, 100% 0%, 50% 50%);
        animation: b 2s infinite alternate;
    }
    .c {
        background: deeppink;
        clip-path: polygon(100% 0%, 100% 100%, 50% 50%);
        animation: c 2s infinite alternate;
    }
    .d {
        background: deeppink;
        clip-path: polygon(100% 100%, 0% 100%, 50% 50%);
        animation: d 2s infinite alternate;
    }

    @keyframes a {
        0%, 10% {
            background: deeppink;
            clip-path: polygon(0% 0%, 0% 100%, 50% 50%);
        }
        90%, 100% {
            background: #000;
            clip-path: polygon(0% 100%, 25% 100%, 12.5% 0%);
        }
    }
    @keyframes b {
        0%, 10% {
            background: deeppink;
            clip-path: polygon(0% 0%, 100% 0%, 50% 50%);
        }
        90%, 100% {
            background: #000;
            clip-path: polygon(25% 0%, 50% 0%, 37.5% 100%);
        }
    }
    @keyframes c {
        0%, 10% {
            background: deeppink;
            clip-path: polygon(100% 0%, 100% 100%, 50% 50%);
        }
        90%, 100% {
            background: #000;
            clip-path: polygon(62.5% 0%, 75% 100%, 50% 100%);
        }
    }
    @keyframes d {
        0%, 10% {
            background: deeppink;
            clip-path: polygon(100% 100%, 0% 100%, 50% 50%);
        }
        90%, 100% {
            background: #000;
            clip-path: polygon(100% 0%, 87.5% 100%, 75% 0%);
        }
    }
    @keyframes aniContainer {
        0%, 10% {
            width: 100px;
            height: 100px;
        }
        90%, 100% {
            width: 250px;
            height: 60px;
        }
    }
</style>