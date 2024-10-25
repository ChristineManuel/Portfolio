<template>
    <div class="drawing-container">
      <h1>Explore your creativity ₍^ >ヮ<^₎ .ᐟ.ᐟ</h1>
      <div class="toolbar">
        <input type="color" v-model="color" />
        <button @click="clearCanvas">Clear</button>
      </div>
      <canvas
        ref="canvas"
        :width="width"
        :height="height"
        @mousedown="startDrawing"
        @mousemove="draw"
        @mouseup="stopDrawing"
        @mouseleave="stopDrawing"
      ></canvas>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        color: '#000000', // Default brush color
        isDrawing: false,
        width: 800,
        height: 400,
        lastX: 0,
        lastY: 0,
      };
    },
    methods: {
      startDrawing(event) {
        this.isDrawing = true;
        const rect = this.$refs.canvas.getBoundingClientRect();
        this.lastX = event.clientX - rect.left;
        this.lastY = event.clientY - rect.top;
      },
      draw(event) {
        if (!this.isDrawing) return;
        const ctx = this.$refs.canvas.getContext('2d');
        const rect = this.$refs.canvas.getBoundingClientRect();
        const currentX = event.clientX - rect.left;
        const currentY = event.clientY - rect.top;
  
        ctx.strokeStyle = this.color;
        ctx.lineWidth = 2; // Brush thickness
        ctx.beginPath();
        ctx.moveTo(this.lastX, this.lastY);
        ctx.lineTo(currentX, currentY);
        ctx.stroke();
        ctx.closePath();
  
        this.lastX = currentX;
        this.lastY = currentY;
      },
      stopDrawing() {
        this.isDrawing = false;
      },
      clearCanvas() {
        const ctx = this.$refs.canvas.getContext('2d');
        ctx.clearRect(0, 0, this.width, this.height);
      },
    },
  };
  </script>
  
  <style scoped>
  .drawing-container {
    text-align: center;
    margin-top: 20px;
  }
  canvas {
    border: 1px solid #000;
  }
  .toolbar {
    margin-bottom: 10px;
  }
  </style>
  