<div class="btn both">Both</div>
<div class="btn rectangle">Rectangle</div>
<div class="btn circle">Circle</div>

<style>
    .btn {
        position: relative;
        width: 200px;
        height: 64px;
        line-height: 64px;
        box-shadow: inset 0 0 0 3px #ddd;
        margin: 50px auto;
        text-align: center;
        color: #333;
        font-size: 16px;
        cursor: pointer;
        transition: color 1s;
        overflow: hidden;
    }

    .btn::before,
    .btn::after {
        content: "";
        position: absolute;
        width: 0;
        height: 0;
        top: 0;
        left: 0;
        box-sizing: border-box;
        border: 3px solid transparent;
    }
    .both:hover {
        color: #00e2ff;
    }
    .both:hover::before {
        transition: width 0.5s, height 0.5s, border-bottom-color 0s;
        transition-delay: 0.5s, 0s, 0.5s;
        width: 200px;
        height: 64px;
        border-left: 3px solid #00e2ff;
        border-bottom: 3px solid #00e2ff;
    }

    .both:hover::after {
        transition: width 0.5s, height 0.5s, border-right-color 0.5s;
        transition-delay: 0s, 0.5s, 0.5s;
        width: 200px;
        height: 64px;
        border-top: 3px solid #00e2ff;
        border-right: 3px solid #00e2ff;
    }

    .rectangle::after {
        top: unset;
        left: unset;
        right: 0;
        bottom: -6px;
    }

    .rectangle:hover {
        color: #00e2ff;
    }
    .rectangle:hover::before {
        transition: height 0.25s, width 0.25s, border-bottom-color 0.25s;
        transition-delay: 0s, 0.25s, 0.25s;
        width: 200px;
        height: 64px;
        border-left: 3px solid #00e2ff;
        border-bottom: 3px solid #00e2ff;
    }

    .rectangle:hover::after {
        transition: width 0.25s, height 0.25s, border-top-color 0.25s;
        transition-delay: 0.75s, 0.5s, 0.75s;
        width: 200px;
        height: 70px;
        border-top: 3px solid #00e2ff;
        border-right: 3px solid #00e2ff;
    }

    .circle {
        width: 120px;
        height: 120px;
        line-height: 120px;
        border-radius: 50%;
    }

    .circle::before,
    .circle::after {
        border-radius: 50%;
    }

    .circle:hover {
        color: #00e2ff;
    }
    .circle:hover::before {
        width: 120px;
        height: 120px;
        border-color: #00e2ff;
        transition: border-top-color 0.25s linear,
            border-right-color 0.25s linear, border-bottom-color 0.25s linear,
            border-left-color 0.25s linear;
        transition-delay: 0s, 0.25s, 0.5s, 0.75s;
    }

    .circle:hover::after {
        width: 120px;
        height: 120px;
        border-top: 3px solid #00e2ff;
        transform: rotate(270deg);
        transition: transform 0.75s linear;
        transition-delay: 0s;
    }
</style>
