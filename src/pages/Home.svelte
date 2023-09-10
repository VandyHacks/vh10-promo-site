<script>
import VHlogo from "../components/VHlogo.svelte";
import FirstCloud from "../components/firstCloud.svelte";
import SecondCloud from "../components/secondCloud.svelte";
import ThirdCloud from "../components/thirdCloud.svelte";
import FourthCloud from "../components/fourthCloud.svelte";
import FifthCloud from "../components/fifthCloud.svelte";
</script>

<div style="position: relative; margin-bottom: 120px;">

    <a
        id="mlh-trust-badge"
        style="display:block;max-width:80px;min-width:40px;position:fixed;right:50px;top:0;width:10%;z-index:10000"
        href="https://mlh.io/seasons/2024/events?utm_source=na-hackathon&utm_medium=TrustBadge&utm_campaign=2024-season&utm_content=gray"
        target="_blank"
        ><img
            src="https://s3.amazonaws.com/logged-assets/trust-badge/2024/mlh-trust-badge-2024-gray.svg"
            alt="Major League Hacking 2023 Hackathon Season"
            style="width:100%"
            /></a
        >

        <div>
            <div
                style="display: flex;
                justify-content: center;  z-index: 4;"
                >
                <VHlogo />
            </div>
            <div
                style="display: flex;
                justify-content: center; text-shadow:
                0 0 7px #fff; color: white; font-size: 3em; font-weight: 700; position: relative; top: -2em; font: Inter;  z-index: 4;"
                >
                VANDYHACKS X
            </div>
            <div
                style="display: flex;
                justify-content: center; font-size: 1.4em; position: relative; top:-4em; color: #E0E1F5; font: Inter;  z-index: 4;"
                >
                October 28 - 29 | Nashville, TN
            </div>
            <div
                style="display: flex;
                justify-content: center; margin-top: 60px; position: relative; top: -6em"
                >
                <div
                    style=" display: flex;
                    justify-content: center;
                    align-items: center; width:160px; height:30px; border: 2px solid #FFFFFF; box-shadow:
                    0 0 7px #fff;  z-index: 2;"
                    >
                    <div
                        style="display: flex;
                        justify-content: center;
                        align-items: center; width:140px; height:20px; border: 2px solid #FFFFFF; box-shadow:
                        0 0 7px #fff; z-index: 2;"
                        >
                        <a href="https://apply.vandyhacks.org" target="_blank">
                            <div
                                style="
                                color:white;
                                font: Inter;
                                text-shadow:
                                0 0 4px #fff;  z-index: 2;"
                                >
                                Apply Now
                            </div>
                        </a>
                    </div>
                </div>
            </div>
        </div>

        <div style="position: absolute; left: -100px; top: 50px; z-index: 1;">
            <FirstCloud />
        </div>

        <div style="position: absolute; left: 50px; top: 650px; z-index: 1;">
            <SecondCloud />
        </div>

        <div style="position: absolute; left: 400px; top: 750px; z-index: 1;">
            <ThirdCloud />
        </div>

        <div style="position: absolute; right: 50px; top: 450px; z-index: 1;">
            <FourthCloud />
        </div>

        <div style="position: absolute; right: -100px; top: 50px; z-index: 1;">
            <FifthCloud />
        </div>


        </div>
