<script lang="ts">
	import '$lib/fonts.css';
	import '$lib/global.css';
	import Icons from '$lib/Icons.svelte';
	import AppCard from '$lib/AppCard.svelte';
	let year = new Date().getFullYear();
</script>

<svelte:head>
	<title>Labrum Co • App Design &amp; Development</title>
</svelte:head>

<div id="app">
	<h1 title="Labrum Co. LC">
		<Icons name="logo" width="191" height="56" />
	</h1>
	<h3 title="App Design & Development">
		<Icons name="appDesign" width="284" height="31" />
	</h3>

	<div class="apps">
		<AppCard
			name="avid"
			title="Avid"
			details="Notes, tasks, projects, workflows, subtasks, & more."
			url="https://avid.pro"
			link="avid.pro"
			platforms="Mac • iOS • Android • Windows"
		/>

		<AppCard
			name="pilotpro"
			title="Pilot Pro"
			details="A beautiful and powerful logbook for pilots."
			url="https://pilotpro.com"
			link="pilotpro.com"
			platforms="Mac • iOS • Android • Windows"
		/>
	</div>

	<div id="footer">
		<p>Copyright &copy; {year} &nbsp; Labrum Co.</p>
	</div>
</div>

<style>
	#app {
		text-align: center;
	}
	h1 {
		color: #fff;
		margin: 60px auto 0px;
		font-weight: normal;
		text-align: center;
	}
	h3 {
		margin: 0;
	}

	/* --- Apps --- */
	.apps {
		display: flex;
		margin: 0 auto;
		max-width: 600px;
		justify-content: center;
	}

	/* --- Footer --- */
	#footer {
		padding-bottom: 30px;
	}
	#footer p {
		font-size: 10px;
		color: #5f6061;
	}
	/* --- Responsive --- */
	@media screen and (max-width: 568px) {
		.apps {
			flex-direction: column;
			text-align: center;
		}
	}
</style>
