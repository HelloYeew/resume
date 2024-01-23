<script lang="ts">
	export let name: string = 'Foo';
	export let nickname: string = '';
	export let phone: string = '';
	export let email: string = '';
	export let github: string = '';
	export let linkedin: string = '';
	export let location: string = '';
	export let website: string = '';
	export let imageUrl: string = '';
</script>

<div class="flex flex-wrap flex-col sm:flex-row print:flex-row text-sm sm:text-base">
	<div class="flex-1 text-left sm:py-4 w-48">
		<p><a href={`tel:${phone}`}>{phone}</a></p>
		<p><a href={`mailto:${email}`}>{email}</a></p>
		<p>{location}</p>
	</div>

	<h2
		class="flex flex-row gap-4 order-first sm:order-none print:order-none text-4xl sm:text-2xl md:text-3xl lg:text-6xl text-center p-4 print:pt-0"
	>
		{#if imageUrl}
		<div class="hidden sm:block">
			<img src="{imageUrl}" alt="Profile" class="w-32 h-32 rounded-full shadow-lg print:shadow-none" />
		</div>
		{/if}
		<div class="flex flex-col justify-center">
			{name}
			<span class="block -mt-1 text-base lg:text-lg">({nickname})</span>
		</div>
	</h2>

	<div class="flex-1 text-left sm:text-right print:text-right sm:py-4 w-48 text-sm sm:text-base">
		<p>
			<a href={`https://github.com/${github}`} target="_blank" rel="noreferrer"
			>github.com/{github}</a
			>
		</p>
		<p>
			<a href={`https://${website}`} target="_blank" rel="noreferrer">{website}</a>
		</p>
		<p>
			<a href={`https://linkedin.com/in/${linkedin}`} target="_blank" rel="noreferrer">Linkedin</a>
		</p>
	</div>
</div>

<style lang="postcss">
    a {
        text-decoration: underline;
    }
</style>
