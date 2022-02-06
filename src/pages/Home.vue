<template>
  <main>
    <div class="text-top">Videos novos toda <b>quinta</b> às <b>20h</b></div>
    <a href="https//:www.google.com.br" target="blank">
      <img
        src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg
"
        alt="Inscreva-se"
        id="subscribe"
      />
    </a>
    <div class="text-botton">youtube.com/wdevoficial</div>
  </main>
</template>

<script>
export default {
  nome: "Home",
};
</script>

<style scoped>
main {
  background-color: var(--color-background-home);
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.text-top {
  color: var(--color-text-light);
  font-size: 22px;
  margin-bottom: 20px;
}

.text-botton {
  color: var(--color-text-light);
  font-size: 18px;
  margin-bottom: 20px;
}

#subscribe{
    width: 340px;
    margin-bottom: 20px;

}
</style>