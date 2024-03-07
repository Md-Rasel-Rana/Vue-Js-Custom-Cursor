<template>
  <div>
    <div class="content">
      <h1>Cursor Follow on MouseMove</h1>
      <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Molestias aperiam fugiat a asperiores nulla eveniet nihil excepturi laudantium exercitationem, earum ullam quo minus atque eos praesentium eum ad perferendis quis possimus dignissimos itaque porro. Consectetur dolorum quas ut magni laborum! Reiciendis quae, maxime, officia saepe placeat vero voluptas fugit ea quas sed nihil, similique repellat consequatur. Odit minima provident similique.
      </p>
    </div>
    <div class="cursor" :style="{ left: cursorPosition.x + 'px', top: cursorPosition.y + 'px' }"></div>
    <div class="cursor2" :style="{ left: cursorPosition.x + 'px', top: cursorPosition.y + 'px' }"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cursorPosition: { x: 0, y: 0 }
    };
  },
  mounted() {
    document.addEventListener("mousemove", this.handleMouseMove);
  },
  beforeDestroy() {
    document.removeEventListener("mousemove", this.handleMouseMove);
  },
  methods: {
    handleMouseMove(e) {
      this.cursorPosition = { x: e.clientX, y: e.clientY };
    }
  }
};
</script>

<style scoped>
body {
  margin: 0;
  padding: 0;
  background: url(~@/bg.jpg) no-repeat center;
  background-color: #110e0e;
  background-size: cover;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  font-family: "Open Sans", sans-serif;
  color: #110e0e;
  cursor: pointer;
}

.content p {
  width: 700px;
  line-height: 26px;
  font-size: 18px;
  text-align: justify;
}

.cursor,
.cursor2 {
  position: fixed;
  pointer-events: none;
}

.cursor {
  width: 50px;
  height: 50px;
  border: 1px solid #da1e1e;
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: 0.1s;
}

.cursor2 {
  width: 8px;
  height: 8px;
  background-color: #0eb40e;
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: 0.15s;
}

.content:hover ~ .cursor {
  transform: translate(-50%, -50%) scale(1.5);
  background-color: #3b0baa;
  opacity: 0.5;
}

.content:hover ~ .cursor2 {
  opacity: 0;
}
</style>
