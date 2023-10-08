<script lang="ts">
	export let title = 'Button';
	type colorBtn = 'blue' | 'white';
	export let colorBtn: colorBtn = 'blue';

	export let onClick = () => {};
</script>

<button class="btn {colorBtn === 'blue' ? 'btn-blue' : 'btn-white'}" on:click={onClick}>
	{title}
</button>

<style lang="sass">
.btn
  padding: 1.2rem 3.2rem
  border: none
  width: 100%
  font-size: 1.8rem
  font-weight: 600
  border-radius: 2rem
  @include hover-btn
.btn-white
  background-color: $color-white
  color: $color-blue
  border: solid .1rem $color-line-white


.btn-blue
  background-color: $color-blue
  color: $color-white
</style>
