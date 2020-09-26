<template>
  <div class="divider">
    <h2>
        <span>
          {{title}}
        </span>
    </h2>
  </div>
</template>

<script>
    export default {
      props: {
        title:{ default: () => "Serviços"}
      }
    }
</script>

<style lang="scss" scoped>
.divider {
  text-align: center;
  width: 90vw;
}
h2 {
  font-family: "Montserrat", Helvetica, sans-serif;
  font-weight: 300;
  display: inline-block;
  position: relative;
  text-align: center;
}

h2 span {
  color: #e28754;
}

h2 span:after,
h2 span:before {
  content: " ";
  display: block;
  height: 1px;
  width: 40vw;
  background: #e6baa4;
  position: absolute;
  top: 50%;
}

h2 span:before {
  left: -42vw;
}
h2 span:after {
  right: -42vw;
}

</style>