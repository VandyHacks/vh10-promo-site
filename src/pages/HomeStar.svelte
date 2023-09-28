<script>
	import Home from "../pages/Home.svelte";

	let numberOfDots = 50;
	let dots = [];

	// Generate random coordinates for each dot when the component is initialized
	for (let i = 0; i < numberOfDots; i++) {
	  dots.push({
		left: Math.random() * 100 + "%",
		top: Math.random() * 100 + "%",
	  });
	}
  </script>

  <style>
	.sparkling-container {
	  position: relative;
	  width: 100%;
	  height: 100%;
	  overflow: hidden;
	}

	.dot {
	  position: absolute;
	  width: 4px;
	  height: 4px;
	  background-color: #fff;
	  border-radius: 50%;
	  opacity: 0.8;
	  animation: sparkle 1.5s infinite alternate;
	}

	@keyframes sparkle {
	  0% {
		opacity: 0.5;
		transform: scale(0.9);
	  }
	  50% {
		opacity: 1;
	  }
	  100% {
		opacity: 0.5;
		transform: scale(1.1);
	  }
	}
  </style>

  <div class="sparkling-container">
	{#each dots as dot (dot.left + dot.top)}
	  <div class="dot" style="left: {dot.left}; top: {dot.top};"></div>
	{/each}

	<Home />

  </div>
