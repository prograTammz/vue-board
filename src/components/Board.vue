<template>
  <canvas ref="canvas" id= "canvas" width="600" height="400" @mousedown = "mouseDown" @mousemove = "mouseMove" @mouseup = "mouseUp" @mouseleave = "mouseLeave"></canvas>

</template>

<script>
  export default {
    name: "Board",
    data: () => ({
      isMouseDown: false,
      color: "black",
      currentEvent : "",
    }),
    watch:{
        draw: function(){
            let ctx =this.$refs.canvas.getContext('2d');
            ctx.canvas.width  = window.innerWidth;
            ctx.canvas.height = window.innerHeight;
        }
    },
    methods:{
        mouseDown: function(e){
            this.currentEvent = e;
            this.isMouseDown = true;
        },
        mouseMove: function(e){
            
            if(this.isMouseDown){
                let context = this.$refs.canvas.getContext('2d');
                context.beginPath();
                context.lineWidth = 5;
                context.lineCap = 'round';
                context.lineJoin = "round";
                context.moveTo(this.currentEvent.offsetX, this.currentEvent.offsetY+32);
                context.lineTo(e.offsetX, e.offsetY+32)
                context.strokeStyle = this.color;
                context.stroke();
                this.currentEvent = e;

            }
        },
        mouseUp: function(){
            this.isMouseDown = false;
        },
        mouseLeave: function(){
            this.isMouseDown = false;
        }
    }
  }
</script>

<style scoped>
  #canvas{
    margin-top: 10px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
    transition: all 0.3s cubic-bezier(.25,.8,.25,1);
    cursor: url("../assets/cursors/pencil.png"),crosshair;
  }
</style>