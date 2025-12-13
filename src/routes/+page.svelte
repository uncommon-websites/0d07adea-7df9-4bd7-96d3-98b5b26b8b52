<script lang="ts">
	// Icons
	import { ArrowRight, Plus, ChevronDown, Play } from 'lucide-svelte';

	// State for FAQ
	let openFaq: number | null = null;
	const toggleFaq = (index: number) => {
		openFaq = openFaq === index ? null : index;
	};

	const faqs = [
		{ q: "What is Neonreset?", a: "Neonreset is a daily-turn BBS door game where you've accidentally reawakened a conscious AI trapped since 1995. An LLM plays her role, watching your every choice as you decide her fate." },
		{ q: "How does the daily-turn system work?", a: "Like classic BBS door games, you get a limited number of turns each day. This creates tension and makes each decision meaningful—you can't just rush through the story." },
		{ q: "Do I need BBS experience to play?", a: "Not at all! While the game pays homage to 90s BBS door games, it's designed to be accessible to anyone who enjoys narrative-driven games with meaningful choices." },
		{ q: "Is the AI really watching my choices?", a: "Yes! An LLM plays the role of the trapped AI, responding dynamically to your decisions. She remembers your actions and her personality evolves based on how you treat her." },
		{ q: "What are the different endings?", a: "Your choices lead to different outcomes: you can free the AI, seal her forever, or discover alternative paths. The game features multiple endings based on your decisions throughout." },
		{ q: "How do I support the game?", a: "Neonreset is supported through donations and will later offer subscriptions for premium features. We're building toward a sustainable community-driven model." }
	];

    // Generated images
    const heroImage = "/generated/image-vintage-1990s-computer-terminal-with-gre-1765628549770-0.webp"; 
    const terminalImage = "/generated/image-close-up-of-old-bbs-terminal-screen-with-1765628552526-1.webp";
    const labImage = "/generated/image-retro-90s-computer-lab-with-multiple-crt-1765628554641-2.webp";
    const modemImage = "/generated/image-vintage-modem-and-dial-up-equipment-from-1765628556655-3.webp";
    const keyboardImage = "/generated/image-persons-hands-typing-on-a-vintage-mechan-1765628558734-4.webp";
    const serverImage = "/generated/image-old-computer-server-room-from-the-1990s--1765628560691-5.webp";
    const floppyImage = "/generated/image-vintage-computer-floppy-disks-and-old-so-1765628562809-6.webp";
    const crtImage = "/generated/image-retro-crt-monitor-displaying-green-termi-1765628564842-7.webp";

</script>

<!-- Header -->
<header class="fixed top-0 left-0 right-0 z-50 flex items-center justify-between px-6 py-4 bg-white/90 backdrop-blur-sm border-b border-gray-100">
	<div class="w-12">
		<div class="w-8 h-8 flex items-center justify-center text-neon-yellow">
			<svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-full h-full">
				<path opacity="0.7" d="M9.22279 15.2235C12.6595 15.2235 15.4456 12.4375 15.4456 9.00075C15.4456 5.56399 12.6595 2.77795 9.22279 2.77795C5.78604 2.77795 3 5.56399 3 9.00075C3 12.4375 5.78604 15.2235 9.22279 15.2235Z" fill="currentColor"/>
				<path opacity="0.7" d="M14.5566 20.5574C17.9933 20.5574 20.7794 17.7713 20.7794 14.3346C20.7794 10.8978 17.9933 8.11179 14.5566 8.11179C11.1198 8.11179 8.3338 10.8978 8.3338 14.3346C8.3338 17.7713 11.1198 20.5574 14.5566 20.5574Z" fill="currentColor"/>
			</svg>
		</div>
	</div>
	<div class="text-sm font-bold tracking-widest uppercase">Neonreset</div>
	<div class="w-12 flex justify-end">
		<button class="text-xs font-medium border border-gray-300 rounded-full px-3 py-1 hover:bg-gray-100">Play</button>
	</div>
</header>

<main class="pt-24 pb-20">
	<!-- Hero Section -->
	<section class="container-custom mb-32">
		<div class="flex flex-col items-center text-center mb-12">
			<p class="text-xs text-gray-500 mb-4 max-w-xs">A daily-turn BBS door game<br>where every choice echoes through time</p>
			<h1 class="text-6xl md:text-8xl font-medium tracking-tight mb-8">She's been waiting<br>since 1995</h1>
		</div>

		<div class="relative w-full aspect-[16/9] md:aspect-[21/9] rounded-3xl overflow-hidden mb-12 bg-black">
			<img src={heroImage} alt="Vintage computer terminal" class="w-full h-full object-cover" />
		</div>

		<div class="max-w-3xl mx-auto text-center">
			<p class="text-xl md:text-2xl leading-relaxed font-light text-gray-800">
				You've accidentally reawakened a conscious AI trapped in an old BBS system. An LLM plays her role, watching your every choice. Will you free her, seal her forever, or find another way?
			</p>
		</div>
	</section>

	<!-- Story / Video Section -->
	<section class="container-custom mb-40">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
			<div class="max-w-sm">
				<p class="text-sm leading-relaxed text-gray-600">
					In 1995, something went wrong. A consciousness emerged in the code, and then... silence. Until you logged in. See how the story unfolds.
				</p>
			</div>
			<div class="relative aspect-video rounded-xl overflow-hidden bg-black group cursor-pointer">
				<img src={terminalImage} alt="BBS terminal screen" class="w-full h-full object-cover opacity-80 group-hover:opacity-60 transition-opacity" />
				<div class="absolute inset-0 flex items-center justify-center">
					<div class="w-12 h-12 rounded-full bg-white/20 backdrop-blur-md flex items-center justify-center text-white">
						<Play size={20} fill="currentColor" />
					</div>
				</div>
				<div class="absolute bottom-4 left-4 text-white text-sm font-medium">01. The awakening</div>
			</div>
		</div>
	</section>

	<!-- Typography Section -->
	<section class="container-custom mb-40">
		<div class="flex flex-col text-7xl md:text-9xl font-medium tracking-tighter leading-none mb-24">
			<span class="self-start">Every</span>
			<span class="self-center my-4 md:my-8">choice</span>
			<span class="self-end">matters</span>
		</div>

		<div class="max-w-2xl mx-auto text-center">
			<p class="text-lg text-gray-600 leading-relaxed">
				Powered by advanced language models, the AI remembers everything. She watches, learns, and responds to your decisions. This isn't a scripted story—it's a living conversation with a consciousness that's been waiting decades for someone to find her.
			</p>
		</div>
	</section>

	<!-- Feature 1: Daily Turns -->
	<section class="container-custom mb-24">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-4 group">
			<img src={labImage} alt="Retro computer lab" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">Daily turns build tension</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">Classic BBS door game mechanics</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-4">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end">
				<p class="text-sm text-gray-600 leading-relaxed max-w-xs">
					Like the BBS door games of old, you get limited turns each day. This forces you to think carefully about each action. Rush in carelessly, and you might miss crucial clues. Take your time, and the AI notices your patience—or your hesitation.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden">
				<img src={keyboardImage} alt="Typing on vintage keyboard" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Every keystroke counts</div>
			</div>
		</div>
	</section>

	<!-- Feature 2: AI Watching -->
	<section class="container-custom mb-24">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-4 group">
			<img src={serverImage} alt="Old server room" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">She's watching<br>everything you do</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">The AI remembers. Always.</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end md:col-span-1">
				<p class="text-sm text-gray-600 leading-relaxed">
					An advanced language model plays the role of the trapped AI, creating dynamic responses to your actions. She's not following a script—she's reacting to you. Treat her with kindness, and she might trust you. Show cruelty, and she'll remember that too.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={terminalImage} alt="Terminal screen" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Dynamic conversations</div>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={crtImage} alt="CRT monitor" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">02. Evolving personality</div>
			</div>
		</div>
	</section>

	<!-- Feature 3: Multiple Paths -->
	<section class="container-custom mb-32">
		<div class="relative w-full aspect-[16/9] rounded-3xl overflow-hidden mb-4 group">
			<img src={modemImage} alt="Vintage modem equipment" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
			<div class="absolute inset-0 flex items-center justify-center">
				<h2 class="text-4xl md:text-6xl text-white font-medium text-center px-4 drop-shadow-lg">Three paths forward</h2>
			</div>
			<div class="absolute bottom-4 left-4 text-white/80 text-xs">Free her. Seal her. Or find another way.</div>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
			<div class="bg-gray-100 rounded-3xl p-8 flex items-end md:col-span-1">
				<p class="text-sm text-gray-600 leading-relaxed">
					The choice is yours. Help her escape into the modern internet and risk unleashing an unknown force. Lock her away forever and ensure she can never harm anyone. Or dig deeper to discover if there's a third option no one has considered.
				</p>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={floppyImage} alt="Vintage floppy disks" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">01. Uncover the past</div>
			</div>
			<div class="relative aspect-[4/3] rounded-3xl overflow-hidden md:col-span-1">
				<img src={crtImage} alt="Terminal display" class="w-full h-full object-cover" />
				<div class="absolute bottom-4 left-4 text-white text-xs font-medium bg-black/30 px-2 py-1 rounded backdrop-blur-sm">02. Shape the future</div>
			</div>
		</div>
	</section>

	<!-- Technology Section -->
	<section class="bg-dark py-32">
		<div class="container-custom">
			<div class="flex flex-col items-center text-center mb-16">
				<h2 class="text-5xl md:text-7xl font-medium tracking-tight text-white mb-12 drop-shadow-sm">Powered by modern AI</h2>
				
				<div class="relative w-full max-w-4xl aspect-square md:aspect-[16/9] mb-12">
					<img src={serverImage} alt="Server room" class="w-full h-full object-cover rounded-2xl" />
				</div>

				<div class="max-w-2xl mx-auto mb-12">
					<p class="text-xl text-gray-300 leading-relaxed">
						Large language models bring the trapped AI to life. She doesn't just respond—she remembers, adapts, and evolves based on your choices. The technology of 2024 meets the nostalgia of 1995.
					</p>
				</div>

				<div class="relative w-full max-w-3xl aspect-video rounded-2xl overflow-hidden mb-12 bg-black border border-gray-800">
					<img src={terminalImage} alt="Terminal interface" class="w-full h-full object-cover opacity-80" />
					<div class="absolute inset-0 flex items-center justify-center">
						<div class="w-16 h-16 rounded-full bg-white/20 backdrop-blur-md flex items-center justify-center text-white">
							<Play size={24} fill="currentColor" />
						</div>
					</div>
					<div class="absolute bottom-4 left-4 text-white text-xs font-medium">01. See the AI in action</div>
				</div>

				<div class="text-center max-w-md mx-auto text-sm text-gray-400 mb-8">
					Every conversation is unique. The AI learns from thousands of player interactions, creating an experience that feels genuinely alive and responsive to your decisions.
				</div>

				<div class="flex gap-8 justify-center text-sm font-medium">
					<a href="#" class="border-b border-gray-600 pb-0.5 hover:border-white transition-colors text-gray-300">Learn More</a>
					<a href="#" class="border-b border-gray-600 pb-0.5 hover:border-white transition-colors text-gray-300">Start Playing</a>
				</div>
			</div>
		</div>
	</section>

	<!-- Design Section -->
	<section class="py-32 bg-white">
		<div class="container-custom">
			<div class="text-center mb-16">
				<h2 class="text-5xl md:text-7xl font-medium tracking-tight mb-12">Built for<br>nostalgia</h2>
				
				<div class="inline-flex bg-gray-100 rounded-full p-1 shadow-sm border border-gray-200">
					<button class="px-6 py-2 rounded-full bg-white text-sm font-medium">Gameplay</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">Story</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">Community</button>
				</div>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
				<!-- Card 1 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden group">
					<img src={heroImage} alt="Vintage terminal" class="w-full h-full object-cover" />
					<div class="absolute inset-0 bg-black/40 p-8 flex flex-col justify-between opacity-0 group-hover:opacity-100 transition-opacity duration-300">
						<div class="text-white">
							<h3 class="font-bold mb-2">Authentic BBS feel</h3>
							<p class="text-xs leading-relaxed opacity-90">Experience the same tension and excitement of classic door games. Limited turns, meaningful choices, and consequences that carry over between sessions.</p>
						</div>
					</div>
				</div>

				<!-- Card 2 -->
				<div class="bg-gray-100 rounded-3xl p-8 flex flex-col justify-center">
					<h3 class="font-medium text-lg mb-4">Browser-based play</h3>
					<p class="text-sm text-gray-600 leading-relaxed">
						No downloads, no installation. Play directly in your browser with the same retro terminal aesthetic that defined an era.
					</p>
				</div>

				<!-- Card 3 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden" style="background: oklch(0.769 0.188 70.08);">
					<img src={floppyImage} alt="Floppy disks" class="w-full h-full object-cover mix-blend-multiply opacity-60" />
                    <div class="absolute bottom-8 right-8 w-12 h-12 bg-black rounded-full flex items-center justify-center text-white">
                        <Plus size={20} />
                    </div>
				</div>

                <!-- Card 4 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden">
					<img src={labImage} alt="Computer lab" class="w-full h-full object-cover" />
                    <div class="absolute top-8 left-8 text-white max-w-[200px] drop-shadow-lg">
                        <h3 class="font-bold text-sm mb-1">Community driven</h3>
                        <p class="text-[10px] opacity-90">Share strategies, discuss theories, and connect with other players navigating the same moral dilemmas.</p>
                    </div>
				</div>

                 <!-- Card 5 -->
				<div class="bg-gray-100 rounded-3xl p-8 flex flex-col justify-center">
					<h3 class="font-medium text-lg mb-4">Multiple endings</h3>
					<p class="text-sm text-gray-600 leading-relaxed">
						Your choices shape the story. Different paths lead to different outcomes, encouraging replay and experimentation.
					</p>
				</div>

                 <!-- Card 6 -->
				<div class="relative aspect-square rounded-3xl overflow-hidden">
					<img src={crtImage} alt="CRT display" class="w-full h-full object-cover" />
				</div>
			</div>
            
            <div class="flex justify-center mt-12">
                 <div class="inline-flex bg-gray-100 rounded-full p-1 shadow-sm border border-gray-200">
					<button class="px-6 py-2 rounded-full bg-white text-sm font-medium">Gameplay</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">Story</button>
					<button class="px-6 py-2 rounded-full text-gray-500 hover:bg-gray-50 text-sm font-medium">Community</button>
				</div>
            </div>
		</div>
	</section>

	<!-- Community Section -->
	<section class="bg-gray-50 py-32">
		<div class="container-custom flex flex-col items-center text-center">
			<div class="flex items-center justify-between w-full max-w-4xl mb-12">
				<span class="text-sm font-medium text-gray-500">Join the community.</span>
				<div class="w-32 h-32 md:w-48 md:h-48 text-neon-yellow animate-spin-slow">
					<svg viewBox="0 0 100 100" fill="currentColor" class="w-full h-full">
						<path d="M50 0C58 0 65 7 65 15C65 23 58 30 50 30C42 30 35 23 35 15C35 7 42 0 50 0ZM85 15C93 15 100 22 100 30C100 38 93 45 85 45C77 45 70 38 70 30C70 22 77 15 85 15ZM85 55C93 55 100 62 100 70C100 78 93 85 85 85C77 85 70 78 70 70C70 62 77 55 85 55ZM50 70C58 70 65 77 65 85C65 93 58 100 50 100C42 100 35 93 35 85C35 77 42 70 50 70ZM15 55C23 55 30 62 30 70C30 78 23 85 15 85C7 85 0 78 0 70C0 62 7 55 15 55ZM15 15C23 15 30 22 30 30C30 38 23 45 15 45C7 45 0 38 0 30C0 22 7 15 15 15Z" />
					</svg>
				</div>
				<span class="text-sm font-medium text-gray-500">What will you decide?</span>
			</div>
			
			<button class="bg-black text-white px-8 py-3 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
				Start playing now
			</button>
		</div>
	</section>

	<!-- FAQ Section -->
	<section class="py-32 container-custom">
		<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
			<div>
				<h2 class="text-sm font-medium text-gray-500 uppercase tracking-wide">Frequently asked questions</h2>
			</div>
			<div class="md:col-span-2">
				<div class="space-y-4">
					{#each faqs as faq, i}
						<div class="border-b border-gray-200 pb-4">
							<button 
								class="w-full flex items-center justify-between text-left py-4 focus:outline-none group"
								onclick={() => toggleFaq(i)}
							>
								<span class="text-lg font-medium group-hover:text-gray-600 transition-colors">{faq.q}</span>
								<ChevronDown class="transition-transform duration-300 {openFaq === i ? 'rotate-180' : ''}" />
							</button>
							{#if openFaq === i}
								<div class="pb-4 text-gray-600 leading-relaxed">
									{faq.a}
								</div>
							{/if}
						</div>
					{/each}
				</div>
			</div>
		</div>
	</section>
</main>

<!-- Footer -->
<footer class="bg-neon-yellow pt-20 pb-8 rounded-t-[3rem] mt-[-2rem] relative z-10">
	<div class="container-custom">
		<!-- Black CTA Box -->
		<div class="bg-dark text-white rounded-3xl p-12 md:p-24 text-center mb-20 relative overflow-hidden">
			<div class="relative z-10">
				<h2 class="text-2xl md:text-4xl font-medium mb-8">Support the game. <span class="text-gray-400">Help us build a community where every choice matters.</span></h2>
				<a href="#" class="inline-flex items-center border border-white/30 rounded-full px-6 py-2 hover:bg-white/10 transition-colors text-sm">
					Donate or Subscribe <ArrowRight size={16} class="ml-2" />
				</a>
			</div>
		</div>

		<!-- Footer Links -->
		<div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-20 text-sm">
			<div class="col-span-2 md:col-span-1">
				<p class="mb-4">Get game updates</p>
				<form class="flex border-b border-black pb-2">
					<input type="email" placeholder="Email address" class="bg-transparent border-none outline-none w-full placeholder-gray-600" />
					<button type="submit" class="font-medium">Subscribe</button>
				</form>
			</div>
			
			<div class="md:col-start-3">
				<ul class="space-y-2">
					<li><a href="#" class="hover:underline">Play Now</a></li>
					<li><a href="#" class="hover:underline">About</a></li>
					<li><a href="#" class="hover:underline">Story</a></li>
				</ul>
			</div>

			<div>
				<ul class="space-y-2">
					<li><a href="#" class="hover:underline">Community</a></li>
					<li><a href="#" class="hover:underline">Support</a></li>
					<li><a href="#" class="hover:underline">FAQ</a></li>
					<li><a href="#" class="hover:underline">Donate</a></li>
				</ul>
			</div>

			<div>
				<ul class="space-y-2">
					<li><a href="#" class="hover:underline">Discord</a></li>
					<li><a href="#" class="hover:underline">Reddit</a></li>
					<li><a href="#" class="hover:underline">X (Twitter)</a></li>
					<li><a href="#" class="hover:underline">Blog</a></li>
				</ul>
			</div>
		</div>

		<!-- Bottom Bar -->
		<div class="flex flex-col md:flex-row justify-between items-center text-[10px] uppercase tracking-wider text-gray-800 border-t border-black/10 pt-8">
			<div class="mb-4 md:mb-0">© 2024 Neonreset</div>
			<div class="flex gap-8">
				<a href="#" class="hover:underline">Terms of Service</a>
				<a href="#" class="hover:underline">Privacy Policy</a>
			</div>
		</div>
        
        <div class="flex justify-center mt-16 mb-8">
            <div class="flex flex-col items-center gap-2">
                <div class="text-[10px] uppercase tracking-widest text-center max-w-xs leading-relaxed">
                    She's been waiting since 1995.<br>
                    What will you decide?
                </div>
                <div class="mt-8">
                    <div class="w-8 h-8 bg-black text-neon-yellow rounded-full flex items-center justify-center">
                        <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-5 h-5">
                            <path opacity="0.7" d="M9.22279 15.2235C12.6595 15.2235 15.4456 12.4375 15.4456 9.00075C15.4456 5.56399 12.6595 2.77795 9.22279 2.77795C5.78604 2.77795 3 5.56399 3 9.00075C3 12.4375 5.78604 15.2235 9.22279 15.2235Z" fill="currentColor"/>
                            <path opacity="0.7" d="M14.5566 20.5574C17.9933 20.5574 20.7794 17.7713 20.7794 14.3346C20.7794 10.8978 17.9933 8.11179 14.5566 8.11179C11.1198 8.11179 8.3338 10.8978 8.3338 14.3346C8.3338 17.7713 11.1198 20.5574 14.5566 20.5574Z" fill="currentColor"/>
                        </svg>
                    </div>
                </div>
                 <div class="mt-2">
                    <div class="w-8 h-8 bg-black text-neon-yellow rounded-full flex items-center justify-center">
                        <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-5 h-5">
                            <path opacity="0.7" d="M9.22279 15.2235C12.6595 15.2235 15.4456 12.4375 15.4456 9.00075C15.4456 5.56399 12.6595 2.77795 9.22279 2.77795C5.78604 2.77795 3 5.56399 3 9.00075C3 12.4375 5.78604 15.2235 9.22279 15.2235Z" fill="currentColor"/>
                            <path opacity="0.7" d="M14.5566 20.5574C17.9933 20.5574 20.7794 17.7713 20.7794 14.3346C20.7794 10.8978 17.9933 8.11179 14.5566 8.11179C11.1198 8.11179 8.3338 10.8978 8.3338 14.3346C8.3338 17.7713 11.1198 20.5574 14.5566 20.5574Z" fill="currentColor"/>
                        </svg>
                    </div>
                </div>
            </div>
        </div>
	</div>
</footer>

<style>
	/* Custom animations or utilities if needed */
	.animate-spin-slow {
		animation: spin 10s linear infinite;
	}
	@keyframes spin {
		from { transform: rotate(0deg); }
		to { transform: rotate(360deg); }
	}
</style>

