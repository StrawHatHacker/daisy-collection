<script>
	import themes from "../utils/themes";
</script>

<nav class="navbar bg-base-300 justify-between">
	<!-- Left side -->
	<a href="/" class="btn btn-ghost flex gap-2">
		<img src="/logo.svg" class="w-4 sm:w-6" alt="Daisy Catalog" />

		<div class="flex font-bold text-lg sm:text-2xl">
			Daisy
			<span class="text-primary">Collection</span>
		</div>
	</a>

	<!-- Right side -->
	<div class="flex gap-0 sm:gap-2">
		<!-- GitHub -->
		<a target="_blank" href="https://github.com/willpinha/daisy-collection" class="btn btn-ghost">
			<i class="fa-brands fa-github text-lg"></i>
			<span class="hidden sm:flex">GitHub</span>
		</a>

		<!-- Themes -->
		<div class="dropdown dropdown-bottom dropdown-end">
			<div role="button" tabindex="0" class="btn btn-ghost">
				<i class="fa-solid fa-palette"></i>
				<span class="hidden sm:flex">Themes</span>

				<span class="hidden sm:flex">
					<i class="fa-solid fa-angle-down"></i>
				</span>
			</div>

			<!-- Themes -->
			<div class="flex flex-col dropdown-content gap-2 mt-2 z-10 p-4 shadow-2xl bg-base-200 rounded-box w-64 h-72 overflow-y-scroll">
				{#each themes as theme}
					<button
						data-theme={theme}
						data-set-theme={theme}
						class="btn btn-sm bg-base-100 flex justify-between"
					>
						<span>{theme}</span>

						<div class="flex items-center gap-2">
							{#each ["bg-primary", "bg-secondary", "bg-accent", "bg-neutral"] as bg}
								<span class="{bg} h-4 w-2 rounded-box"></span>
							{/each}
						</div>
					</button>
				{/each}
			</div>
		</div>
	</div>
</nav>
