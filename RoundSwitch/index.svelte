<script>
	export let id = ''
</script>

<label class="Switch Round_Switch">
	<input {id} type="checkbox" on:change>
	<span class="slider round"></span>
</label>

<style>
	.Switch {
		position: relative;
		display: inline-block;
		width: 60px;
		height: 34px;
	}
	.Switch input {
		display: none;
	}
	.Switch input:checked + .slider {
		background-color: #3EBBC0;
	}
	.Switch input:checked + .slider:before {
		-webkit-transform: translateX(26px);
		-ms-transform: translateX(26px);
		transform: translateX(26px);
	}
	.Switch input:focused + .slider {
		box-shadow: 0 0 1px #2196F3;
	}
	.Switch input + .slider.round {
		border-radius: 34px;
	}
	.Switch input + .slider.round:before {
		border-radius: 50%;
	}
	.Switch .slider {
		position: absolute;
		cursor: pointer;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background-color: #ccc;
		-webkit-transition: .4s;
		transition: .4s;
	}
	.Switch .slider:before {
		position: absolute;
		content: "";
		height: 26px;
		width: 26px;
		left: 4px;
		bottom: 4px;
		background-color: white;
		-webkit-transition: .4s;
		transition: .4s;
	}
</style>
