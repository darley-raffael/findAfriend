<script lang="ts">
	export let onClick = () => {};
</script>

<button class="btn" on:click={onClick}>
	<img src="whatsapp.svg" alt="icon Whatsapp" />
	<span>Entrar em contato</span>
</button>

<style lang="sass">
.btn
  border: none
  border-radius: 2rem
  padding: 1.2rem 3.2rem
  font-size: 1.8rem
  font-weight: 600
  background-color: $color-green
  color: $color-white
  width: 100%
  display: flex
  align-items: center
  justify-content: center
  gap: 1.6rem
  // adicionar o mixin de animação que foi criado no variables.sass
  @include hover-btn

</style>
