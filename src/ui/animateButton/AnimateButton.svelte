<script>
  export let fontColor = '#2E2D2D'
  export let type = 'button'
  export let label = 'Ceci est un bouton'
  export let animation = "slide-right"
</script>

<button class="btn"
        class:btn-slide-right={ animation === 'slide-right'}
        class:btn-slide-left={ animation === 'slide-left'}
        type={type}
        style="text-align:center ;color: {fontColor};">{label}
</button>


<style lang="scss">
  $color: #ffb72a;

  .btn {
    position: relative;
    display: inline-block;
    padding: .75rem 1.25rem;
    margin: .75rem;
    transition: all .3s;
    overflow: hidden;
    z-index: 1;
    border: none;
  }

  .btn-slide-right {
    &:before {
      content: '';
      position: absolute;
      border-radius: 0 100% 100% 0;
      bottom: 0;
      left: 0;
      width: 10%;
      height: 100%;
      transition: all 1s;
      background-color: lighten($color, 20%);
      z-index: -1;
    }

    &:hover {
      color: #646cff;

      &:before {
        width: 100%;
        border-radius: 0 8px 8px 0;
        transition: all 1s;
      }
    }
  }

  .btn-slide-left {

    &:before {
      content: '';
      position: absolute;
      border-radius: 100% 0 0 100%;
      bottom: 0;
      right: 0;
      width: 10%;
      height: 100%;
      transition: all 1s;
      background-color: lighten($color, 20%);
      z-index: -1;
    }

    &:hover {
      color: #646cff;

      &:before {
        width: 100%;
        transition: all 1s;
        border-radius: 8px 0 0 8px;
      }


    }
  }

  *, *:before, *:after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
</style>
