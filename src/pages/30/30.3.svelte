clip-path 动画
<div class="polygon-animate"></div>

<style>
    .polygon-animate {
        position: relative;
        width: 200px;
        height: 200px;
        margin-left: 100px;
        margin-top: 100px;
        transform: translate(-50%, -50%);
        background-color: crimson;
        transition: .3s;
        clip-path: polygon(
            50% 0%,
            0% 100%,
            100% 100%,
            100% 100%,
            100% 100%,
            100% 100%,
            100% 100%,
            100% 100%,
            100% 100%
        );
        animation: polygon-ani 5s linear infinite;
    }

    @keyframes polygon-ani {
        10% {
            background-color: darkorange;
            clip-path: polygon(
                50% 0%,
                100% 50%,
                50% 100%,
                0% 50%,
                0% 50%,
                0% 50%,
                0% 50%,
                0% 50%,
                0% 50%
            );
        }
        14% {
            clip-path: polygon(
                50% 0%,
                100% 50%,
                50% 100%,
                0% 50%,
                0% 50%,
                0% 50%,
                0% 50%,
                0% 50%,
                0% 50%
            );
        }
        24% {
            background-color: lemonchiffon;
            clip-path: polygon(
                100% 38%,
                82% 100%,
                82% 100%,
                18% 100%,
                0% 38%,
                0% 38%,
                0% 38%,
                0% 38%,
                50% 0%
            );
        }
        28% {
            clip-path: polygon(
                100% 38%,
                82% 100%,
                82% 100%,
                18% 100%,
                0% 38%,
                0% 38%,
                0% 38%,
                0% 38%,
                50% 0%
            );
        }
        38% {
            background-color: darkturquoise;
            clip-path: polygon(
                50% 0%,
                100% 25%,
                100% 75%,
                100% 75%,
                50% 100%,
                0% 75%,
                0% 75%,
                0% 25%,
                0% 25%
            );
        }
        42% {
            clip-path: polygon(
                50% 0%,
                100% 25%,
                100% 75%,
                100% 75%,
                50% 100%,
                0% 75%,
                0% 75%,
                0% 25%,
                0% 25%
            );
        }
        52% {
            background-color: darkcyan;
            clip-path: polygon(
                50% 0%,
                90% 20%,
                100% 60%,
                75% 100%,
                25% 100%,
                25% 100%,
                0% 60%,
                10% 20%,
                50% 0%
            );
        }
        56% {
            clip-path: polygon(
                50% 0%,
                90% 20%,
                100% 60%,
                75% 100%,
                25% 100%,
                25% 100%,
                0% 60%,
                10% 20%,
                50% 0%
            );
        }
        66% {
            background-color: deepskyblue;
            clip-path: polygon(
                30% 0%,
                70% 0%,
                70% 0%,
                100% 30%,
                100% 70%,
                70% 100%,
                30% 100%,
                0% 70%,
                0% 30%
            );
        }
        70% {
            clip-path: polygon(
                30% 0%,
                70% 0%,
                70% 0%,
                100% 30%,
                100% 70%,
                70% 100%,
                30% 100%,
                0% 70%,
                0% 30%
            );
        }
        80% {
            background-color: indigo;
            clip-path: polygon(
                83% 12%,
                100% 43%,
                94% 78%,
                68% 100%,
                32% 100%,
                6% 78%,
                0% 43%,
                17% 12%,
                50% 0%
            );
        }
        84% {
            clip-path: polygon(
                83% 12%,
                100% 43%,
                94% 78%,
                68% 100%,
                32% 100%,
                6% 78%,
                0% 43%,
                17% 12%,
                50% 0%
            );
        }
        94% {
            background-color: crimson;
            clip-path: polygon(
                50% 0%,
                0% 100%,
                100% 100%,
                100% 100%,
                100% 100%,
                100% 100%,
                100% 100%,
                100% 100%,
                100% 100%
            );
        }
    }
</style>