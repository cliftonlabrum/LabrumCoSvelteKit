<script lang="ts">
	export let name: string;
	export let title: string;
	export let details: string;
	export let url: string;
	export let link: string;
	export let platforms: string;
</script>

<div class="app">
	<a href={url} class={name} target="_blank">
		{#if name == 'avid'}
			<img src="/images/avid.png" width="90" height="90" alt="Avid.pro" />
		{:else if name == 'pilotpro'}
			<img src="/images/pilotpro.png" width="90" height="90" alt="PilotPro.com" />
		{:else}
			<img src="/images/wardhub.png" width="90" height="90" alt="WardHub.org" />
		{/if}

		<h2>{title}</h2>
		<p>{details}</p>
		<h3>{link}</h3>
		<small>{platforms}</small>
	</a>
</div>

<style>
	.app {
		text-align: center;
		margin: 20px;
	}
	/* a.pilotpro h2 {
		margin-top: 4px;
	} */
	a {
		display: block;
		font-size: 12px;
		text-decoration: none;
		background: rgba(0, 0, 0, 0.2);
		border-radius: 10px;
		padding: 20px 0px;
		width: 250px;
		transition: background-color 0.3s ease;
	}
	a:hover {
		background: rgba(0, 0, 0, 0.3);
	}

	h2 {
		color: #fff;
		font-size: 18px;
		margin: 0;
		font-weight: normal;
	}
	h3 {
		color: #3fa3f5;
		font-weight: normal;
		font-size: 14px;
		margin: 0;
	}
	p {
		font-size: 14px;
		color: #bebfc2;
		margin: 10px 15px;
		line-height: 1.3;
	}
	small {
		display: block;
		font-size: 10px;
		color: #777879;
		margin: 15px auto 5px;
		font-weight: 500;
	}

	@media screen and (max-width: 568px) {
		.app {
			margin: 20px auto;
		}
	}
</style>
