<script lang="ts">
    import { onMount } from "svelte";
    import { getAssetsUrl } from "../../proxy";

    const img = getAssetsUrl("galaxy.jpg");

    onMount(() => {
        const style = document.createElement("style");
        style.id = "style_61_7";
        document.head.appendChild(style);

        const loopArr = [];
        for (let i = 20; i <= 30; i++) {
            const height = 20 + Math.floor(Math.random() * 40);
            const top = Math.floor(Math.random() * (150 - 60));
            const bottom = 150 - top - height;
            const left = -100 + Math.floor(Math.random() * 200);
            loopArr.push(`
            ${(i / 2).toFixed(1)}% {
                clip-path: inset(${top}px 0 ${bottom}px);
                left: ${left}px;
            }
            `);
        }
        const loop = loopArr.join("\n");
        const glitchOne = `
        ${loop}
        15.5% {
        clip-path: inset(10px 0 320px);
        left: -20px;
    }
    16% {
        clip-path: inset(10px 0 320px);
        left: -10px;
        opacity: 0;
    }
    45% {
        opacity: 0.5;
        left: -20px;
        filter: hue-rotate(90deg) saturate(1.3);
    }
    45.5% {
        left: 0px;
        filter: invert(1);
    }

    46% {
        clip-path: inset(150px 0 160px);
        left: 15%;
    }
    46.5% {
        clip-path: inset(20px 0 200px);
        left: -10%;
        transform: scale(1.1);
    }
    47% {
        clip-path: inset(240px 0 20px);
        left: -11%;
        transform: scale(1.2);
    }
    47.5% {
        clip-path: inset(20 0 20px);
        left: 13%;
        transform: scale(1.3);
        filter: invert(0);
    }
    48% {
        clip-path: inset(120 0 120px);
        left: 15%;
        transform: scale(1.1);
    }
    48.5% {
        clip-path: inset(260px 0 10px);
        left: -11%;
        transform: scale(1.2);
        filter: none;
    }
    49% {
        clip-path: inset(5px 0 350px);
        left: 11%;
        transform: scale(1.3);
    }
    49.5% {
        clip-path: inset(105px 0 210px);
        left: 0%;
        transform: scale(1.1);
    }
    50% {
        clip-path: inset(175px 0 160px);
        left: -11%;
    }
    50.5% {
        clip-path: inset(95px 0 230px);
        left: -14%;
        transform: scale(1.2);
    }
    51% {
        clip-path: inset(235px 0 12px);
        left: -14%;
    }
    51.5% {
        clip-path: inset(350px 0 7px);
        left: -14%;
    }
    52% {
        clip-path: inset(320px 0 27px);
        left: -12%;
        transform: scale(1.1);
    }
    52.5% {
        clip-path: inset(190px 0 127px);
        left: -11%;
        transform: scale(1.3);
        filter: hue-rotate(90deg) saturate(1.3);
    }
    54% {
        clip-path: inset(20px 0 20px);
        left: 12%;
        transform: scale(1.1);
        filter: none;
    }
    54% {
        background-image: none;
    }
        `;
        style.appendChild(document.createTextNode(glitchOne));

        const loop1Arr = [];
        for (let i = 40; i <= 50; i++) {
            const height = 20 + Math.floor(Math.random() * 40);
            const top = Math.floor(Math.random() * (150 - 60));
            const bottom = 150 - top - height;
            const left = -100 + Math.floor(Math.random() * 200);
            loop1Arr.push(`
            ${(i / 2).toFixed(1)}% {
                clip-path: inset(${top}px 0 ${bottom}px);
                left: ${left}px;
            }
            `);
        }
        const loop1 = loop1Arr.join("\n");
        const glitchTwo = `
            ${loop1}

            25.5% {
        clip-path: inset(10px 0 320px);
        left: -20px;
    }
    26% {
        clip-path: inset(10px 0 320px);
        left: -10px;
        opacity: 0;
    }
    45% {
        opacity: 0.3;
        left: -20px;
        filter: hue-rotate(45deg) saturate(1.1);
    }
    45.5% {
        left: 0px;
        filter: invert(1.2);
    }

    46% {
        clip-path: inset(50px 0 260px);
        left: -12%;
    }
    46.5% {
        clip-path: inset(120px 0 100px);
        left: 8%;
        transform: scale(1.2);
    }
    47% {
        clip-path: inset(40px 0 300px);
        left: 8%;
        transform: scale(1.3);
    }
    47.5% {
        clip-path: inset(220 0 70px);
        left: -9%;
        transform: scale(1.1);
        filter: invert(1.1);
    }
    48% {
        clip-path: inset(240px 0 120px);
        left: 11%;
        transform: scale(1.2);
    }
    48.5% {
        clip-path: inset(0px 0 310px);
        left: -12%;
        transform: scale(1.2);
        filter: none;
    }
    49% {
        clip-path: inset(255px 0 50px);
        left: 11%;
        transform: scale(1.3);
    }
    49.5% {
        clip-path: inset(10px 0 240px);
        left: 6%;
        transform: scale(1.1);
    }
    50% {
        clip-path: inset(275px 0 90px);
        left: -12%;
    }
    50.5% {
        clip-path: inset(195px 0 90px);
        left: 14%;
        transform: scale(1.4);
    }
    51% {
        clip-path: inset(35px 0 282px);
        left: -14%;
    }
    51.5% {
        clip-path: inset(350px 0 7px);
        left: 14%;
    }
    52% {
        clip-path: inset(20px 0 270px);
        left: -12%;
        transform: scale(1.1);
    }
    52.5% {
        clip-path: inset(90px 0 227px);
        left: -11%;
        transform: scale(1.3);
        filter: hue-rotate(150deg) saturate(1.3);
    }
    54% {
        clip-path: inset(220px 0 100px);
        left: 12%;
        transform: scale(1.1);
        filter: none;
    }
    54% {
        background-image: none;
    }
        `;

        style.appendChild(
            document.createTextNode(`
        cc1::before,
        cc1::after {
            background: url(${img}) no-repeat;
        }
        `)
        );
        return () => {
            document.head.removeChild(style);
        };
    });
</script>

`clip-path` 的 Glitch Art

<div class="cc1" style={`background: url(${img}) no-repeat;`} />

<style>
    div {
        position: relative;
        width: 200px;
        height: 150px;
        margin: auto;
        animation: main-img-hide 16s infinite step-end;
    }

    div::before,
    div::after {
        position: absolute;
        width: 200px;
        height: 150px;
        top: 0;
        left: 0;
    }

    div::after {
        content: "";
        animation: glitch-one 16s infinite step-end;
        z-index: 2;
    }

    div::before {
        content: "";
        animation: glitch-two 16s infinite 1s step-end;
        z-index: 1;
    }

    @keyframes main-img-hide {
        5% {
            filter: invert(1);
        }
        5.2% {
            filter: none;
        }
        10% {
            opacity: 0.5;
            filter: grayscale(1);
        }
        11% {
            filter: none;
            opacity: 1;
        }
        45% {
            opacity: 0.5;
            filter: grayscale(1);
        }
        46% {
            filter: none;
            opacity: 1;
        }
        53.5% {
            opacity: 0.5;
            filter: grayscale(1);
        }
        54% {
            filter: none;
            opacity: 1;
        }
        54.5% {
            opacity: 0.5;
            filter: hue-rotate(30deg);
        }
        55% {
            filter: none;
        }
        55.5% {
            background-image: none;
            filter: none;
            opacity: 1;
        }
        56% {
            background-image: url($img);
            opacity: 0.5;
        }
        56.5% {
            background-image: none;
        }
        57% {
            background-image: url($img);
            opacity: 0.8;
        }
        57.5% {
            opacity: 0.3;
        }
        58% {
            background-image: none;
        }
    }
</style>
