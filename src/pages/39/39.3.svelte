拓展

<div>Hover Me</div>

<div class="two">Hover Me</div>

<div class="three">Hover Me</div>

<style>
    div {
        position: relative;
        width: 200px;
        height: 60px;
        line-height: 60px;
        font-size: 32px;
        cursor: pointer;
        color: #333;
        text-align: center;
        transition: color 0.5s;
    }

    div::before {
        content: "";
        position: absolute;
        left: 0;
        width: 200px;
        height: 60px;
        background-color: deeppink;
        z-index: -1;
        transform: scale3d(0, 1, 1);
        transform-origin: 100% 50%;
        transition: transform 0.5s;
    }

    div:hover {
        color: #fff;
    }
    div:hover::before {
        transform: scale3d(1, 1, 1);
        transform-origin: 0 50%;
        transition-timing-function: ease-in;
    }

    .two::before {
        transform: scale3d(0, 0, 1);
        transform-origin: 100% 100%;
    }

    .two:hover::before {
        transform: scale3d(1, 1, 1);
        transform-origin: 0 0;
    }

    .three::before {
        transform: scale3d(0, 0, 1);
        transform-origin: 50% 100%;
    }
    .three:hover::before {
        transform: scale3d(1, 1, 1);
        transform-origin: 50% 0;
    }
</style>
