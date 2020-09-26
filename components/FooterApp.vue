<template>
  <div class="footer">
  <section class="masthead" role="img" aria-label="Image Description">
  </section>
  <section class="logo-placement">
    <h1>
      Maktتb
      <div class="customs">CUSTOMS</div>
    </h1>
    <div>
      <Insta />
      <Face />
    </div>
  </section>
  </div>
</template>

<script>
import Insta from "@/components/Insta";
import Face from "@/components/Face";
export default {
  components: {
    Insta,
    Face
  }
};
</script>

<style lang="scss" scoped>
.v-main__wrap .container {
  padding: 0;
  max-width: 100%;
  margin: 0;
  padding: 0;
  background: linear-gradient(to right, #3b3333, black);
}
.footer {
  display: flex;
  width: 100vw;
  position: relative;
  bottom: 36px;
  left: 0;
  background-color: black; /* if you don't want it to take up the full screen, reduce this number */
}
.masthead {
  text-align: center;
  width: 55%;
  height: 300px; /* if you don't want it to take up the full screen, reduce this number */
  overflow: hidden;
  background-size: cover !important;
  background: linear-gradient(
      -45deg,
      rgba(0, 0, 0, 0) 0%,
      rgba(0, 0, 0, 0) 66%,
      rgba(92, 81, 81, 0.65) 100%
    ),
    url(~assets/coupe-1374450_1920.jpg) no-repeat center center scroll;
}
.logo-placement {
  display: flex;
  justify-content: flex-end;
  align-items: flex-end;
  padding: 10px;
  width: 40%;
  h1 {
    font-family: "Montez", cursive;
    font-style: normal;
    font-weight: bold;
    color: #eee;
    font-size: 8vmin;
    letter-spacing: 0.03em;
    line-height: 1;
    text-shadow: 1px 2px 4px rgba(0, 0, 0, 0.8);
    margin-bottom: 35px;
    width: 60%;
    .customs {
      font-family: 'Montserrat', sans-serif;
      font-weight: 300;
      font-size: medium;
      text-align: initial;
    }
  }
}

</style>

