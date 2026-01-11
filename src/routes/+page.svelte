<script lang="ts">
	import LinkSection from '$lib/components/LinkSection.svelte';
	import type { ComponentProps } from 'svelte';

	const linkSections: ComponentProps<typeof LinkSection>[] = [
		{
			title: 'Finance',
			links: [
				{
					name: 'Nicolet',
					url: 'https://4securecorp.ufsdata.com/EBC_EBC1151/Login/075917937/1',
					faviconUrl: 'https://www.nicoletbank.com/',
				},
				{ name: 'Schwab', url: 'https://client.schwab.com/Areas/Access/Login' },
				{
					name: 'Fidelity',
					url: 'https://workplaceservices.fidelity.com/mybenefits/navstation/navigation#/',
				},
				{ name: 'American Express', url: 'https://global.americanexpress.com/overview' },
				{ name: 'Capital One', url: 'https://www.capitalone.com/' },
				{ name: 'FNBO', url: 'https://www.fnbo.com/' },
				{ name: 'CLA', url: 'https://www.clientaxcess.com/#/login' },
				{ name: 'Wi DOR Tax', url: 'https://tap.revenue.wi.gov/mta/_/' },
			],
		},
		{
			title: 'Insurance',
			links: [
				{
					name: 'Acuity',
					url: 'https://www.acuity.com/sso/editProfile',
				},
			],
		},
		{
			title: 'Utilities',
			links: [
				{
					name: 'Spectrum',
					url: 'https://www.spectrum.net/account-summary',
				},
				{
					name: 'Verizon',
					url: 'https://secure.verizon.com/signin',
				},
				{
					name: 'WPS',
					url: 'https://www.wisconsinpublicservice.com/secure/auth/l/acct/summary_accounts',
				},
				{
					name: 'SiriusXM',
					url: 'https://care.siriusxm.com/accountcenter/home',
				},
			],
		},
		{
			title: 'Health',
			links: [
				{
					name: 'Kemper Patient Portal',
					url: 'https://kempercogwell.md-hq.com/',
					faviconUrl: 'https://kemperwellness.com/',
				},
				{
					name: 'Aurora',
					url: 'https://livewell.aah.org/Chart/Home/',
				},
				{
					name: 'Emplify',
					url: 'https://mychart.emplifyhealth.org/MyChart/Home/',
				},
				{
					name: 'Mayo Clinic',
					url: 'https://www.mayoclinic.org/',
				},
			],
		},
		{
			title: 'Golf',
			links: [
				{
					name: 'Green Bay Country Club',
					url: 'https://www.greenbaycountryclub.com/',
				},
				{
					name: 'Horseshoe Bay Golf Club',
					url: 'https://www.horseshoebaygolfclub.net/Home.aspx',
				},
				{
					name: 'WSGA',
					url: 'http://www.wsga.org/',
				},
			],
		},
		{
			title: 'Other',
			links: [
				{
					name: 'Amazon',
					url: 'https://www.amazon.com/',
				},
				{
					name: 'Microsoft',
					url: 'https://www.microsoft.com/en-us/',
				},
				{
					name: 'BMW',
					url: 'https://mybmw.bmwusa.com/home',
				},
				{
					name: 'Passwords',
					url: 'https://docs.google.com/spreadsheets/d/1JesaEZphkBE6fHhjZ711EsEjC-QDkUrNml-KmeJI0pw/edit?gid=0#gid=0',
				},
			],
		},
	];
</script>

<div class="flex min-w-150 flex-col gap-5 rounded-2xl bg-white p-5 shadow">
	<h1>Larry's Links</h1>
	{#each linkSections as linkSection (linkSection.title)}
		<LinkSection {...linkSection} />
	{/each}
</div>
