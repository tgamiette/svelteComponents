<script>
  export let colorBtn = '#234db6'
  export let fontColor = '#f8f8f8'
  export let slideColor = '#f8f8f8'
  export let type = 'button'
  export let label = 'Ceci est un bouton'
  export let animation = "slide-right"
</script>

<button class="btn"
        class:btn-slide-right={ animation === 'slide-right'}
        class:btn-slide-left={ animation === 'slide-left'}
        class:btn-slide-blob={ animation === 'slide-blob'}
        type={type}
        style="background-color: {colorBtn} ;text-align:center ;color: {fontColor};">{label}
</button>


<style lang="scss">
  //$btn_color: #234db6;
  $color: #4992c2;
  $first_color: #FFF;

  .btn {
    font-family: 'Open Sans Condensed', sans-serif;
    position: relative;
    display: inline-block;
    padding: .75rem 1.25rem;
    margin: .75rem;
    border-radius: 10rem;
    color: $first_color;
    transition: all .3s;
    font-size: 2rem;
    overflow: hidden;
    z-index: 1;
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
      background-color: darken($color, 10%);
      z-index: -1;
    }

    &:hover {
      color: #646cff;

      &:before {
        width: 100%;
        border-radius: 0 25rem 25rem 0;
        transition: all 1s;
      }

      &:active {
        color: red;
        border-color: red;
        //color: $first_color;
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
      background-color: darken($color, 10%);
      z-index: -1;
    }

    &:hover {
      color: #646cff;

      &:before {
        width: 100%;
        transition: all 1s;
        border-radius: 25rem 0 0 25rem;
      }

      &:active {
        color: red;
        //color: $first_color;
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
      background-color: darken($color, 10%);
      z-index: -1;
    }

    &:hover {
      color: #646cff;

      &:before {
        width: 100%;
        transition: all 1s;
        border-radius: 25rem 0 0 25rem;
      }

      &:active {
        color: red;
        //color: $first_color;
      }

    }
  }

  // blob

  *, *:before, *:after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  $openSans: 'Open Sans', Helvetica, Arial, sans-serif;
  body {
    background: #333;
    font-family: $openSans;
  }

  $cyan: #0505A9;
  $dark: #FFFFFF;
  $borderW: 2px;

  *, *:before, *:after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  $openSans: 'Open Sans', Helvetica, Arial, sans-serif;
  body {
    background: #333;
    font-family: $openSans;
  }

  .buttons {
    margin-top: 50px;
    text-align: center;
    border-radius: 30px;
  }

  $cyan: #0505A9;
  $dark: #FFFFFF;
  $borderW: 2px;
</style>