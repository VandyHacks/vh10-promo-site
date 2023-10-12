<script>
  export let answer;
</script>

<div class="all">
  <!-- Answer -->
  <div class="answer">{answer}</div>

  <!-- Big Board -->
  <svg
    width="633"
    height="512"
    viewBox="0 0 633 512"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M54.8008 440.867H82.693V497.349C82.693 505.051 76.4491 511.295 68.7469 511.295C61.0447 511.295 54.8008 505.051 54.8008 497.349V440.867Z"
      fill="#201857"
    />
    <path
      d="M106.4 440.867H134.293V497.349C134.293 505.051 128.049 511.295 120.346 511.295C112.644 511.295 106.4 505.051 106.4 497.349V440.867Z"
      fill="#201857"
    />
    <path
      d="M490.615 445.051H518.507V497.349C518.507 505.051 512.264 511.295 504.561 511.295C496.859 511.295 490.615 505.051 490.615 497.349V445.051Z"
      fill="#201857"
    />
    <path
      d="M542.217 445.051H570.109V497.349C570.109 505.051 563.865 511.295 556.163 511.295C548.461 511.295 542.217 505.051 542.217 497.349V445.051Z"
      fill="#201857"
    />
    <g filter="url(#filter0_di_558_11190)">
      <rect
        x="40"
        y="40"
        width="553"
        height="392"
        rx="25"
        fill="#FF509F"
        fill-opacity="0.1"
        shape-rendering="crispEdges"
      />
    </g>
    <defs>
      <filter
        id="filter0_di_558_11190"
        x="0"
        y="0"
        width="633"
        height="472"
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
        <feGaussianBlur stdDeviation="20" />
        <feComposite in2="hardAlpha" operator="out" />
        <feColorMatrix
          type="matrix"
          values="0 0 0 0 0.996078 0 0 0 0 0.796078 0 0 0 0 0.0941176 0 0 0 1 0"
        />
        <feBlend
          mode="normal"
          in2="BackgroundImageFix"
          result="effect1_dropShadow_558_11190"
        />
        <feBlend
          mode="normal"
          in="SourceGraphic"
          in2="effect1_dropShadow_558_11190"
          result="shape"
        />
        <feColorMatrix
          in="SourceAlpha"
          type="matrix"
          values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
          result="hardAlpha"
        />
        <feOffset />
        <feGaussianBlur stdDeviation="7.5" />
        <feComposite in2="hardAlpha" operator="arithmetic" k2="-1" k3="1" />
        <feColorMatrix
          type="matrix"
          values="0 0 0 0 0.996078 0 0 0 0 0.796078 0 0 0 0 0.0941176 0 0 0 1 0"
        />
        <feBlend
          mode="normal"
          in2="shape"
          result="effect2_innerShadow_558_11190"
        />
      </filter>
    </defs>
  </svg>
</div>

<style>
  .all {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
  }

  .answer {
    position: absolute;
    width: 80%;
    overflow-y: scroll;
  }
</style>
