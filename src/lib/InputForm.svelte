<script lang="ts">
	export let typeInput = 'password';
	export let labelName = 'Exemplo';
	export let placeholder = 'exemplo';
	let showPassword = false;

	function togglePassword() {
		showPassword = !showPassword;
	}
</script>

<div class="input-container">
	<label for={labelName}>{labelName}</label>
	<div class="input-item">
		{#if typeInput === 'password'}
			<input class="input" type={showPassword ? 'text' : 'password'} id={labelName} {placeholder} />
			<button on:click={togglePassword} class="btn-input">
				{#if showPassword}
					<img src="eye-on.svg" alt="icon eye open" />
				{:else}
					<img src="eye-off.svg" alt="icon eye closed" />
				{/if}
			</button>
		{:else}
			<input class="input" type={typeInput} id={labelName} {placeholder} />
		{/if}
	</div>
</div>

<style lang="sass">

.input-container
  width: 100%
  display: flex
  flex-direction: column
  gap: 0.8rem

  .input-item
    width: 100%
    position: relative

    .btn-input
      background: none
      border: none
      position: absolute
      right: 1.2rem
      top: 1.2rem
      cursor: pointer

      transition: all 0.3s ease-in-out

  .input
    width: 100%
    box-sizing: border-box
    border-radius: 1rem
    border: 0.1rem solid $color-line-white
    background-color: $color-white
    font-size: 1.8rem
    padding: 1rem
    outline-color: $color-blue


    &::placeholder
      color: $color-blue
    &:focus
      transition: all 0.3s ease-in-out
    

</style>
