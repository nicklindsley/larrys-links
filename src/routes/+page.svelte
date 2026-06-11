<script lang="ts">
	import type { ComponentProps } from 'svelte';
	import LinkSection from '$lib/components/LinkSection.svelte';
	import * as Videos from '$lib/assets/videos';

	const linkSections: ComponentProps<typeof LinkSection>[] = [
		{
			name: 'Nicolet',
			url: 'https://4securecorp.ufsdata.com/EBC_EBC1151/Login/075917937/1',
			faviconUrl: 'https://www.nicoletbank.com/',
			video: Videos.nicolet,
			instructions: [
				'Click the link above',
				'The password should populate automatically',
				'Click "Log In"',
			],
		},
		// {
		// 	name: 'Fidelity',
		// 	url: 'https://workplaceservices.fidelity.com/mybenefits/navstation/navigation#/',
		// 	video: Videos.fidelity,
		// 	instructions: [
		// 		'Click the link above',
		// 		'The password should populate automatically',
		// 		'Click "Log In"',
		// 	],
		// },
		{
			name: 'Emplify',
			url: 'https://mychart.emplifyhealth.org/MyChart/Home/',
			video: Videos.emplify,
			instructions: [
				'Click the link above',
				'The password will NOT automatically populate. Click inside the "username" box and click the popup that says "Bellin / Emplify"',
				'Click "Continue"',
				'The password box should now show up. Click the popup that says "Bellin / Emplify" again',
				'Click "Log in"',
			],
		},
		{
			name: 'Aurora',
			url: 'https://livewell.aah.org/Chart/Home/',
			video: Videos.aurora,
			instructions: [
				'Click the link above',
				'The password should populate automatically',
				'Click "Log In"',
				`If it looks like it logs you in here, you're done! Otherwise go to step 5`,
				'Click "Send to my email"',
				'Check your email for an email from "LiveWell"',
				'Open the email and find the code inside',
				'Type that code into the box that says "Enter code"',
				'Click "Verify"',
			],
		},
		{
			name: 'Green Bay Country Club',
			url: 'https://www.greenbaycountryclub.com/',
			video: Videos.greenBayCountryClub,
			instructions: [
				'Click the link above',
				'Click "LOGIN" in the top right',
				'The password should populate automatically',
				'Click "SIGN IN"',
				'To get to the tee sheet, click "FORETEES"',
				`Hover over "Tee Times" at the top and click "Today's Tee Sheet"`,
				'To get to your tee times, hover over "Tee Times" and click "My Tee Times / List"',
			],
		},
		{
			name: 'Horseshoe Bay Golf Club',
			url: 'https://www.horseshoebaygolfclub.net/login.aspx',
			video: Videos.horseshoeBay,
			instructions: [
				'Click the link above',
				'The password should populate automatically',
				'Click "Login"',
				'To get to the tee sheet, click "Tee Times" on the lower half of the screen (you may need to scroll down slightly)',
				'To got to your tee times, click "My Reservations" at the top of the screen',
			],
		},
	];
</script>

<div class="flex flex-col gap-5 rounded-2xl bg-white p-5 shadow md:min-w-150">
	<h1>Larry's Links</h1>
	<div class="grid grid-cols-[auto_auto] gap-5">
		{#each linkSections as linkSection, index (linkSection.name)}
			{#if index > 0}
				<div class="col-span-2 border border-solid"></div>
			{/if}
			<LinkSection {...linkSection} />
		{/each}
	</div>
</div>
