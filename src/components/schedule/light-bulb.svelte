<script>
  import MediaQuery from "../../MediaQuery.svelte";

  export let currentPage;
  export let pageNum;
  export let date;
  let hovering = false;

  const handleMouseEnter = () => {
    hovering = true;
  };

  const handleMouseLeave = () => {
    hovering = false;
  };

  const handleMouseClick = () => {
    currentPage = pageNum;
  };
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  <div
    class="container"
    class:container-mobile={matches}
    class:hovering
    on:mouseenter={handleMouseEnter}
    on:mouseleave={handleMouseLeave}
    on:click={handleMouseClick}
    on:keydown={handleMouseClick}
  >
    <svg
      viewBox="-33.5 -34 182 192"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <rect
        x="30.3457"
        y="126.189"
        width="55.1084"
        height="10.3827"
        rx="4"
        fill="#D9D9D9"
      />
      <rect
        x="30.3457"
        y="138.968"
        width="55.1084"
        height="10.3827"
        rx="4"
        fill="#D9D9D9"
      />
      <rect
        x="30.3457"
        y="151.747"
        width="55.1084"
        height="10.3827"
        rx="4"
        fill="#D9D9D9"
      />

      {#if hovering || currentPage == pageNum}
        <svg
          width="282"
          height="292"
          viewBox="0 0 282 292"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g filter="url(#filter0_di_550_2584)">
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M84.6555 107.297C102.263 97.674 114.206 78.9835 114.206 57.5036C114.206 26.1859 88.8184 0.797852 57.5007 0.797852C26.183 0.797852 0.794922 26.1859 0.794922 57.5036C0.794922 78.6572 12.3778 97.1054 29.5471 106.852V119.793C29.5471 122.003 31.338 123.793 33.5471 123.793H80.6555C82.8647 123.793 84.6555 122.003 84.6555 119.793V107.297Z"
              fill="white"
            />
          </g>
          <defs>
            <filter
              id="filter0_di_550_2584"
              x="-33.5"
              y="-34"
              width="181.411"
              height="190.996"
              filterUnits="userSpaceOnUse"
              color-interpolation-filters="sRGB"
            >
              <feFlood flood-opacity="0" result="BackgroundImageFix" />
              <feColorMatrix
                in="SourceAlpha"
                type="matrix"
                values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                result="hardAlpha"
              />
              <feOffset />
              <feGaussianBlur stdDeviation="12.5" />
              <feComposite in2="hardAlpha" operator="out" />
              <feColorMatrix
                type="matrix"
                values="0 0 0 0 0.866667 0 0 0 0 0.578139 0 0 0 0 0.0180556 0 0 0 1 0"
              />
              <feBlend
                mode="normal"
                in2="BackgroundImageFix"
                result="effect1_dropShadow_550_2584"
              />
              <feBlend
                mode="normal"
                in="SourceGraphic"
                in2="effect1_dropShadow_550_2584"
                result="shape"
              />
              <feColorMatrix
                in="SourceAlpha"
                type="matrix"
                values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                result="hardAlpha"
              />
              <feOffset />
              <feGaussianBlur stdDeviation="12.5" />
              <feComposite
                in2="hardAlpha"
                operator="arithmetic"
                k2="-1"
                k3="1"
              />
              <feColorMatrix
                type="matrix"
                values="0 0 0 0 0.866667 0 0 0 0 0.578139 0 0 0 0 0.0180556 0 0 0 1 0"
              />
              <feBlend
                mode="normal"
                in2="shape"
                result="effect2_innerShadow_550_2584"
              />
            </filter>
          </defs>
        </svg>
      {:else}
        <svg
          width="282"
          height="292"
          viewBox="0 0 282 292"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g filter="url(#filter0_i_550_2592)">
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M84.6555 107.297C102.263 97.674 114.206 78.9835 114.206 57.5036C114.206 26.1859 88.8184 0.797852 57.5007 0.797852C26.183 0.797852 0.794922 26.1859 0.794922 57.5036C0.794922 78.6572 12.3778 97.1054 29.5471 106.852V119.793C29.5471 122.003 31.338 123.793 33.5471 123.793H80.6555C82.8647 123.793 84.6555 122.003 84.6555 119.793V107.297Z"
              fill="#B3B3B3"
            />
          </g>
          <defs>
            <filter
              id="filter0_i_550_2592"
              x="0.794922"
              y="0.797852"
              width="113.411"
              height="122.995"
              filterUnits="userSpaceOnUse"
              color-interpolation-filters="sRGB"
            >
              <feFlood flood-opacity="0" result="BackgroundImageFix" />
              <feBlend
                mode="normal"
                in="SourceGraphic"
                in2="BackgroundImageFix"
                result="shape"
              />
              <feColorMatrix
                in="SourceAlpha"
                type="matrix"
                values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                result="hardAlpha"
              />
              <feOffset />
              <feGaussianBlur stdDeviation="12.5" />
              <feComposite
                in2="hardAlpha"
                operator="arithmetic"
                k2="-1"
                k3="1"
              />
              <feColorMatrix
                type="matrix"
                values="0 0 0 0 0.301961 0 0 0 0 0.301961 0 0 0 0 0.301961 0 0 0 1 0"
              />
              <feBlend
                mode="normal"
                in2="shape"
                result="effect1_innerShadow_550_2592"
              />
            </filter>
          </defs>
        </svg>
      {/if}
    </svg>

    <div class="date-text">
      {date}
    </div>
  </div>
</MediaQuery>

<style>
  .container {
    position: relative;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .container-mobile {
    /* move up a bit */
    top: -1vh;
    /* background-color: blue; */
  }

  .hovering {
    cursor: pointer;
  }

  .date-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-family: Inter;
    text-align: center;
  }
</style>
