背景渐变动画 & 文字裁剪
<div>背景渐变动画</div>

<style>
    div {
        font-size: 80px;
        background:  linear-gradient(90deg, red 0, orange 15%, yellow 30%, green 45%, teal 60%, blue 75%, purple 90% ,purple 100%);
        -webkit-background-clip: text;
        color: transparent;
        animation: changeColor .5s linear infinite alternate;
    }

    @keyframes changeColor {
        0% {
            background-image: linear-gradient(90deg, red 0, orange 15%, yellow 30%, green 45%, teal 60%, blue 75%, purple 90% ,purple 100%);
        }
        50% {
            background-image: linear-gradient(90deg, deeppink 0, yellowgreen 15%, fuchsia 30%, lime 45%, olive 60%, aqua 75%, coral 90% ,brown 100%);
        }
        100% {
            background-image: linear-gradient(-90deg, red 0, orange 15%, yellow 30%, green 45%, teal 60%, blue 75%, purple 90% ,purple 100%);
        }
    }
</style>