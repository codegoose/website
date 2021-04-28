<main>
	<script src="prism.js"></script>
	<link href="prism.css" rel="stylesheet" />

	<link rel="preconnect" href="https://fonts.gstatic.com" />
	<link
		href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,400;0,700;1,400&display=swap"
		rel="stylesheet"
	/>

	<div class="content">
		<header>
			<img
				class="header-icon"
				src="assets/goose-white.png"
				alt="A white goose."
			/>
			<p><b>Brandon White</b></p>
			<p>a.k.a <i>codegoose</i></p>
		</header>

		<!--
		<section>
			<pre>
				<code class="language-cpp">
					{`
void kane::timing::tick() {
	auto now = std::chrono::high_resolution_clock::now();
	auto elapsed = std::chrono::duration_cast<std::chrono::nanoseconds>(now - last_tick);
	last_tick = now;
	for (auto &F : subs_varying) F(std::chrono::duration<double>(elapsed).count());
	auto ns_per_step = std::chrono::duration_cast<std::chrono::nanoseconds>(std::chrono::seconds(1)).count() / ticks_per_sec;
	leftover_time += elapsed;
	int num_steps = 0;
	bool capped_steps = false;
	while (leftover_time.count() >= ns_per_step) {
		for (auto &F : subs) F(1.0 / static_cast<double>(ticks_per_sec));
		leftover_time -= std::chrono::nanoseconds(ns_per_step);
		num_steps++;
		if (num_steps >= 8) {
			capped_steps = true;
			break;
		}
	}
	if (num_steps > 1) sl::debug("Loss of time. {} fixed-steps taken that frame. {}ms leftover.", num_steps, std::chrono::duration_cast<std::chrono::milliseconds>(leftover_time).count());
	if (capped_steps) sl::debug("Per-frame fixed-step cap reached. Leftovers for the next frame.");
}
					`}
				</code>
			</pre>
		</section>
		<section>
			<pre>
				<code class="language-cpp">
					{`
void kane::timing::reset() {
	last_tick = std::chrono::high_resolution_clock::now();
	leftover_time.zero();
	sl::warn("Timing subsystem reset issued.");
}
					`}
				</code>
			</pre>
		</section>
		<section>
			<pre>
				<code class="language-cpp">
					{`
#include <kane/timing.h>
#include <kane/logging.h>

#include <vector>

namespace kane::timing {
	const int ticks_per_sec = 30;
	std::chrono::high_resolution_clock::time_point last_tick;
	std::chrono::nanoseconds leftover_time;
	std::vector<std::function<void(double secs)>> subs;
	std::vector<std::function<void(double secs)>> subs_varying;
}
					`}
				</code>
			</pre>
		</section>
		-->
		<section>
			<h2>about</h2>
			<p>
				I'm a backend software engineer who also likes to manage servers
				and create mobile apps.
			</p>
		</section>
		<section>
			<h2>environments & tools</h2>
			<br />
			<img
				src="https://img.shields.io/badge/Linux-00599C.svg?&style=for-the-badge&logo=linux&logoColor=white"
				alt="Linux"
			/><img
				src="https://img.shields.io/badge/Android-14354C.svg?&style=for-the-badge&logo=android&logoColor=white"
				alt="Android"
			/><img
				src="https://img.shields.io/badge/Windows-00599C.svg?&style=for-the-badge&logo=windows&logoColor=white"
				alt="Windows"
			/>
			<br />
			<img
				src="https://img.shields.io/badge/C++-00599C.svg?&style=flat-square&logo=c%2B%2B&ogoColor=white"
				alt="C++"
			/><img
				src="https://img.shields.io/badge/Python-14354C.svg?&style=flat-square&logo=python&logoColor=white"
				alt="Python"
			/><img
				src="https://img.shields.io/badge/Dart-00599C?style=flat-square&logo=dart&logoColor=white"
				alt="Dart"
			/><img
				src="https://img.shields.io/badge/Flutter-14354C?style=flat-square&logo=flutter&logoColor=white"
				alt="Flutter"
			/><img
				src="https://img.shields.io/badge/JavaScript-00599C?style=flat-square&logo=javascript&logoColor=white"
				alt="JavaScript"
			/>
			<br />
			<img
				src="https://img.shields.io/badge/Excel-00599C?style=flat-square&logo=Microsoft-Excel&logoColor=white"
				alt="Excel"
			/><img
				src="https://img.shields.io/badge/NGINX-14354C?style=flat-square&logo=nginx&logoColor=white"
				alt="NGINX"
			/><img
				src="https://img.shields.io/badge/MongoDB-00599C?style=flat-square&logo=mongodb&logoColor=white"
				alt="MongoDB"
			/><img
				src="https://img.shields.io/badge/Snapcraft-14354C?style=flat-square&logo=snapcraft&logoColor=white"
				alt="Snapcraft"
			/><img
				src="https://img.shields.io/badge/Docker-00599C?style=flat-square&logo=docker&logoColor=white"
				alt="Docker"
			/>
		</section>
	</div>
</main>

<style lang="sass">

	*
		margin: 0
		padding: 0

	.content
		padding: 4em
		max-width: 900px
		margin-right: auto
		margin-left: auto
		background: rgba(8, 8, 8, 0.9)
		border-radius: 0.3em
		font-size: .85em

	:global(body)
		color: #808080
		background: #111
		font-family: "Open Sans", sans-serif
		background: #50a3a2
		background: -webkit-linear-gradient(top left, #50a3a2 0%, #53e3a6 100%)
		background: -moz-linear-gradient(top left, #50a3a2 0%, #53e3a6 100%)
		background: -o-linear-gradient(top left, #50a3a2 0%, #53e3a6 100%)
		background: linear-gradient(to bottom right, #50a3a2 0%, #53e3a6 100%)
		background-attachment: fixed

	main
		padding: 3em 0em

	header
		margin-bottom: 1em

	.header-icon
		width: 100px

	section
		margin-bottom: 1em

	h2
		font-size: 1em
		line-height: 2em
		color: #fff
		font-weight: bold

</style>
