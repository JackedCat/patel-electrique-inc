<script lang="ts">
	import heroInstallation from '$lib/assets/patel-hero-installation.jpg';
	import panelInspection from '$lib/assets/patel-panel-inspection.jpg';
	import logo from '$lib/assets/patel_electrique.png';

	const phoneDisplay = '(514) 684-3844';
	const phoneHref = 'tel:+15146843844';
	const address = '64 Rue Audubon, Dollard-des-Ormeaux, QC H9B 3E9';
	const currentYear = new Date().getFullYear();

	type Language = 'fr' | 'en';

	let language = $state<Language>('fr');

	const copy = {
		fr: {
			metaTitle: 'Patel Électrique Inc | Électriciens résidentiels et commerciaux',
			metaDescription:
				'Patel Électrique Inc offre des services électriques résidentiels et commerciaux à Dollard-des-Ormeaux. Appelez le (514) 684-3844 pour un travail propre, fiable et conforme au code.',
			nav: {
				services: 'Services',
				reviews: 'Avis',
				contact: 'Contact'
			},
			hero: {
				eyebrow: 'Électriciens résidentiels et commerciaux',
				title: 'Un travail électrique propre, ponctuel et conforme.',
				intro:
					'Patel Électrique Inc accompagne les propriétaires et les entreprises avec des conseils clairs, une exécution précise et une réputation bâtie sur la confiance.',
				estimate: 'Demander une estimation',
				call: `Appeler ${phoneDisplay}`,
				reviews: 'Voir les avis',
				media: 'Installation résidentielle'
			},
			rating: {
				label: 'Évaluation Google',
				reviews: '136 avis Google',
				clean: 'Travail bien fait et propre',
				punctual: "À l'heure prévue",
				call: `Appel direct ${phoneDisplay}`
			},
			statement: {
				kicker: 'Patel Électrique Inc',
				title: 'Des interventions sérieuses, sans raccourcis.',
				text: 'Chaque mandat est traité avec le même standard : comprendre le besoin, expliquer les options, protéger les lieux, exécuter avec précision et laisser une installation sécuritaire.'
			},
			servicesTitle: 'Pour propriétés privées et espaces de travail.',
			services: [
				{
					title: 'Résidentiel',
					text: 'Installation, rénovation, diagnostic et entretien électrique pour les maisons, condos et immeubles.'
				},
				{
					title: 'Commercial',
					text: 'Interventions fiables pour commerces, bureaux et propriétés locatives, avec un travail documenté et soigné.'
				},
				{
					title: 'Mise aux normes',
					text: 'Conseils clairs, exécution conforme au code et aucune solution rapide qui compromet la sécurité.'
				}
			],
			proof: {
				kicker: 'Méthode',
				title: 'Clair avant, propre pendant, conforme après.',
				text: "Les avis clients reviennent sur les mêmes points : ponctualité, professionnalisme, explications simples et travaux faits avec soin. C'est le standard appliqué sur chaque intervention.",
				media: 'Inspection et vérification',
				steps: [
					'Évaluation du besoin et conseils pratiques',
					'Exécution efficace avec respect des lieux',
					'Travail terminé selon le code et sans compromis'
				]
			},
			reviewsTitle: 'Une note parfaite, portée par la constance.',
			reviews: [
				{
					quote:
						'Absolument excellent. Très compétent, professionnel et humain. Tout était expliqué clairement et le travail a été fait efficacement.',
					name: 'Avis Google'
				},
				{
					quote:
						'Utilisé depuis plus de 10 ans pour des propriétés résidentielles et commerciales. Toujours professionnel, fiable et hautement qualifié.',
					name: 'Client résidentiel et commercial'
				},
				{
					quote:
						'Conseils professionnels, travail terminé à temps et confiance que le projet sera fait selon le code, sans raccourcis.',
					name: 'Avis Google'
				}
			],
			contact: {
				title: 'Parlez-nous de votre projet.',
				text: "Pour une demande rapide, appelez directement. Sinon, décrivez le travail à faire, l'adresse du projet et vos disponibilités.",
				detailsLabel: 'Coordonnées',
				phone: 'Téléphone',
				address: 'Adresse',
				hours: "Heures d'ouverture",
				holiday: 'Les horaires peuvent varier les jours fériés.',
				form: {
					name: 'Nom',
					email: 'Courriel',
					project: 'Type de projet',
					select: 'Sélectionner',
					message: 'Message',
					submit: 'Envoyer la demande'
				}
			},
			hours: [
				{ day: 'Lundi', time: '8h00-17h00' },
				{ day: 'Mardi', time: '8h00-17h00' },
				{ day: 'Mercredi', time: '8h00-17h00' },
				{ day: 'Jeudi', time: '8h00-17h00' },
				{ day: 'Vendredi', time: '8h00-17h00' },
				{ day: 'Samedi', time: 'Fermé' },
				{ day: 'Dimanche', time: 'Fermé' }
			],
			footer: {
				tagline: 'Électriciens résidentiels et commerciaux à Dollard-des-Ormeaux.',
				coordinates: 'Coordonnées',
				hours: 'Heures',
				navigation: 'Navigation',
				privacy: 'Politique de confidentialité',
				rights: `Tous droits réservés.`
			}
		},
		en: {
			metaTitle: 'Patel Electrique Inc | Residential and Commercial Electricians',
			metaDescription:
				'Patel Electrique Inc provides residential and commercial electrical services in Dollard-des-Ormeaux. Call (514) 684-3844 for clean, reliable, code-compliant work.',
			nav: {
				services: 'Services',
				reviews: 'Reviews',
				contact: 'Contact'
			},
			hero: {
				eyebrow: 'Residential and commercial electricians',
				title: 'Clean, punctual, code-compliant electrical work.',
				intro:
					'Patel Electrique Inc helps homeowners and businesses with clear advice, precise execution, and a reputation built on trust.',
				estimate: 'Request an estimate',
				call: `Call ${phoneDisplay}`,
				reviews: 'See reviews',
				media: 'Residential installation'
			},
			rating: {
				label: 'Google rating',
				reviews: '136 Google reviews',
				clean: 'Clean, well-done work',
				punctual: 'On time as scheduled',
				call: `Direct call ${phoneDisplay}`
			},
			statement: {
				kicker: 'Patel Electrique Inc',
				title: 'Serious electrical work, without shortcuts.',
				text: 'Every job follows the same standard: understand the need, explain the options, protect the space, execute with precision, and leave a safe installation behind.'
			},
			servicesTitle: 'For private properties and workspaces.',
			services: [
				{
					title: 'Residential',
					text: 'Installation, renovation, troubleshooting, and electrical maintenance for homes, condos, and buildings.'
				},
				{
					title: 'Commercial',
					text: 'Reliable service for businesses, offices, and rental properties, with careful and documented work.'
				},
				{
					title: 'Code compliance',
					text: 'Clear advice, code-compliant execution, and no quick fixes that compromise safety.'
				}
			],
			proof: {
				kicker: 'Method',
				title: 'Clear before, clean during, compliant after.',
				text: 'Customer reviews point to the same qualities: punctuality, professionalism, simple explanations, and careful workmanship. That is the standard applied to every service call.',
				media: 'Inspection and verification',
				steps: [
					'Needs assessment and practical advice',
					'Efficient execution with respect for the property',
					'Work completed to code without compromise'
				]
			},
			reviewsTitle: 'A perfect rating, earned through consistency.',
			reviews: [
				{
					quote:
						'Absolutely excellent. Very knowledgeable, professional, and personable. Everything was explained clearly and the work was completed efficiently.',
					name: 'Google review'
				},
				{
					quote:
						'Used for more than 10 years for residential and commercial properties. Always professional, reliable, and highly skilled.',
					name: 'Residential and commercial client'
				},
				{
					quote:
						'Professional advice, work completed on time, and confidence that the project will be done to code without shortcuts.',
					name: 'Google review'
				}
			],
			contact: {
				title: 'Tell us about your project.',
				text: 'For a quick request, call directly. Otherwise, describe the work needed, the project address, and your availability.',
				detailsLabel: 'Contact details',
				phone: 'Phone',
				address: 'Address',
				hours: 'Opening hours',
				holiday: 'Hours may vary on statutory holidays.',
				form: {
					name: 'Name',
					email: 'Email',
					project: 'Project type',
					select: 'Select',
					message: 'Message',
					submit: 'Send request'
				}
			},
			hours: [
				{ day: 'Monday', time: '8:00 AM-5:00 PM' },
				{ day: 'Tuesday', time: '8:00 AM-5:00 PM' },
				{ day: 'Wednesday', time: '8:00 AM-5:00 PM' },
				{ day: 'Thursday', time: '8:00 AM-5:00 PM' },
				{ day: 'Friday', time: '8:00 AM-5:00 PM' },
				{ day: 'Saturday', time: 'Closed' },
				{ day: 'Sunday', time: 'Closed' }
			],
			footer: {
				tagline: 'Residential and commercial electricians in Dollard-des-Ormeaux.',
				coordinates: 'Contact',
				hours: 'Hours',
				navigation: 'Navigation',
				privacy: 'Privacy Policy',
				rights: `All rights reserved.`
			}
		}
	} as const;

	const content = $derived(copy[language]);
</script>

<svelte:head>
	<title>{content.metaTitle}</title>
	<meta name="description" content={content.metaDescription} />
</svelte:head>

<main>
	<section class="hero" id="accueil">
		<header
			class="site-header"
			aria-label={language === 'fr' ? 'Navigation principale' : 'Main navigation'}
		>
			<a class="brand" href="#accueil" aria-label="Patel Electrique Inc">
				<img src={logo} alt="Patel Electrique Inc" />
			</a>

			<nav>
				<a href="#services">{content.nav.services}</a>
				<a href="#avis">{content.nav.reviews}</a>
				<a href="#contact">{content.nav.contact}</a>
				<a class="nav-phone" href={phoneHref}>{phoneDisplay}</a>
			</nav>

			<div
				class="language-switch"
				aria-label={language === 'fr' ? 'Choix de langue' : 'Language selector'}
			>
				<button type="button" class:active={language === 'fr'} onclick={() => (language = 'fr')}>
					FR
				</button>
				<button type="button" class:active={language === 'en'} onclick={() => (language = 'en')}>
					EN
				</button>
			</div>
		</header>

		<div class="hero-body">
			<div class="hero-inner">
				<p class="eyebrow">{content.hero.eyebrow}</p>
				<h1>{content.hero.title}</h1>
				<p class="intro">{content.hero.intro}</p>

				<div class="hero-actions">
					<a class="button primary" href="#contact">{content.hero.estimate}</a>
					<a class="button call" href={phoneHref}>{content.hero.call}</a>
					<a class="button secondary" href="#avis">{content.hero.reviews}</a>
				</div>
			</div>

			<figure class="hero-media" data-reveal>
				<img
					src={heroInstallation}
					alt={language === 'fr'
						? 'Installation électrique résidentielle propre dans un intérieur lumineux'
						: 'Clean residential electrical installation in a bright interior'}
					loading="eager"
					decoding="async"
				/>
				<figcaption>{content.hero.media}</figcaption>
			</figure>
		</div>

		<div class="rating-strip" aria-label={content.rating.label}>
			<strong>5,0</strong>
			<span>{content.rating.reviews}</span>
			<span>{content.rating.clean}</span>
			<span>{content.rating.punctual}</span>
			<a href={phoneHref}>{content.rating.call}</a>
		</div>
	</section>

	<section class="statement" data-reveal>
		<div>
			<p class="section-kicker">{content.statement.kicker}</p>
			<h2>{content.statement.title}</h2>
		</div>
		<p>{content.statement.text}</p>
	</section>

	<section class="services" id="services" aria-labelledby="services-title" data-reveal>
		<div class="section-heading">
			<p class="section-kicker">{content.nav.services}</p>
			<h2 id="services-title">{content.servicesTitle}</h2>
		</div>

		<div class="service-grid">
			{#each content.services as service}
				<article class="service-card">
					<span aria-hidden="true"></span>
					<h3>{service.title}</h3>
					<p>{service.text}</p>
				</article>
			{/each}
		</div>
	</section>

	<section class="proof" aria-labelledby="proof-title" data-reveal>
		<div class="proof-copy">
			<p class="section-kicker">{content.proof.kicker}</p>
			<h2 id="proof-title">{content.proof.title}</h2>
			<p>{content.proof.text}</p>
		</div>

		<div class="proof-stack">
			<figure class="proof-media">
				<img
					src={panelInspection}
					alt={language === 'fr'
						? 'Panneau électrique organisé avec outil de mesure et câblage soigné'
						: 'Organized electrical panel with measuring tool and careful wiring'}
					loading="lazy"
					decoding="async"
				/>
				<figcaption>{content.proof.media}</figcaption>
			</figure>

			<div class="proof-list">
				{#each content.proof.steps as step, index}
					<div>
						<strong>{String(index + 1).padStart(2, '0')}</strong>
						<span>{step}</span>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<section class="reviews" id="avis" aria-labelledby="reviews-title" data-reveal>
		<div class="section-heading">
			<p class="section-kicker">{content.nav.reviews}</p>
			<h2 id="reviews-title">{content.reviewsTitle}</h2>
		</div>

		<div class="review-grid">
			{#each content.reviews as review}
				<figure class="review-card">
					<blockquote>{review.quote}</blockquote>
					<figcaption>{review.name}</figcaption>
				</figure>
			{/each}
		</div>
	</section>

	<section class="contact" id="contact" aria-labelledby="contact-title" data-reveal>
		<div class="contact-info">
			<div class="contact-copy">
				<p class="section-kicker">{content.nav.contact}</p>
				<h2 id="contact-title">{content.contact.title}</h2>
				<p>{content.contact.text}</p>
			</div>

			<div class="contact-details" aria-label={content.contact.detailsLabel}>
				<a class="detail-card phone-card" href={phoneHref}>
					<span>{content.contact.phone}</span>
					<strong>{phoneDisplay}</strong>
				</a>

				<div class="detail-card">
					<span>{content.contact.address}</span>
					<strong>{address}</strong>
				</div>

				<div class="detail-card hours-card">
					<span>{content.contact.hours}</span>
					<ul>
						{#each content.hours as item}
							<li>
								<strong>{item.day}</strong>
								<time>{item.time}</time>
							</li>
						{/each}
					</ul>
					<p>{content.contact.holiday}</p>
				</div>
			</div>
		</div>

		<form name="contact" method="post">
			<label>
				{content.contact.form.name}
				<input name="name" type="text" autocomplete="name" required />
			</label>

			<label>
				{content.contact.form.email}
				<input name="email" type="email" autocomplete="email" required />
			</label>

			<label>
				{content.contact.form.project}
				<select name="project" required>
					<option value="">{content.contact.form.select}</option>
					{#each content.services as service}
						<option>{service.title}</option>
					{/each}
					<option>{language === 'fr' ? 'Autre demande' : 'Other request'}</option>
				</select>
			</label>

			<label>
				{content.contact.form.message}
				<textarea name="message" rows="5" required></textarea>
			</label>

			<button type="submit">{content.contact.form.submit}</button>
		</form>
	</section>

	<footer class="site-footer">
		<div>
			<a class="footer-brand" href="#accueil" aria-label="Patel Electrique Inc">
				<img src={logo} alt="Patel Electrique Inc" />
			</a>
			<p>{content.footer.tagline}</p>
		</div>

		<div>
			<h2>{content.footer.coordinates}</h2>
			<a class="footer-phone" href={phoneHref}>{phoneDisplay}</a>
			<p>{address}</p>
		</div>

		<div>
			<h2>{content.footer.hours}</h2>
			<ul class="footer-hours">
				{#each content.hours as item}
					<li>
						<span>{item.day}</span>
						<span>{item.time}</span>
					</li>
				{/each}
			</ul>
		</div>

		<div>
			<h2>{content.footer.navigation}</h2>
			<a href="#services">{content.nav.services}</a>
			<a href="#avis">{content.nav.reviews}</a>
			<a href="#contact">{content.nav.contact}</a>
			<a href="/confidentialite">{content.footer.privacy}</a>
		</div>

		<div class="footer-legal">
			<p>&copy; {currentYear} Patel Electrique Inc. {content.footer.rights}</p>
			<a href="/confidentialite">{content.footer.privacy}</a>
		</div>
	</footer>
</main>

<style>
	:global(*) {
		box-sizing: border-box;
	}

	:global(html) {
		scroll-behavior: smooth;
	}

	:global(body) {
		margin: 0;
		background: #f7f7f4;
		color: #161616;
		font-family:
			Inter,
			ui-sans-serif,
			system-ui,
			-apple-system,
			BlinkMacSystemFont,
			'Segoe UI',
			sans-serif;
		line-height: 1.5;
	}

	:global(a) {
		color: inherit;
		text-decoration: none;
	}

	main {
		overflow: hidden;
	}

	@keyframes rise-in {
		from {
			opacity: 0;
			transform: translateY(28px);
		}

		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	@keyframes hero-focus {
		from {
			opacity: 0;
			transform: translateX(32px) scale(0.97);
		}

		to {
			opacity: 1;
			transform: translateX(0) scale(1);
		}
	}

	@keyframes soft-float {
		0%,
		100% {
			transform: translateY(0);
		}

		50% {
			transform: translateY(-10px);
		}
	}

	.hero {
		position: relative;
		min-height: 96svh;
		display: grid;
		grid-template-rows: auto 1fr auto;
		padding: 24px clamp(20px, 4vw, 64px) 28px;
		background:
			linear-gradient(90deg, rgba(247, 247, 244, 0.95), rgba(247, 247, 244, 0.7)),
			linear-gradient(135deg, rgba(19, 97, 179, 0.12), rgba(26, 26, 26, 0) 45%), #f7f7f4;
	}

	.hero::after {
		position: absolute;
		inset: auto -10vw 14vh auto;
		width: min(58vw, 760px);
		height: 44vh;
		content: '';
		border: 1px solid rgba(22, 22, 22, 0.12);
		background:
			linear-gradient(
				90deg,
				transparent 0 23%,
				rgba(22, 22, 22, 0.08) 23% 23.5%,
				transparent 23.5%
			),
			linear-gradient(0deg, transparent 0 47%, rgba(22, 22, 22, 0.08) 47% 47.5%, transparent 47.5%),
			linear-gradient(135deg, rgba(255, 255, 255, 0.82), rgba(202, 214, 226, 0.34));
		opacity: 0.8;
		transform: rotate(-2deg);
	}

	.site-header,
	.hero-body,
	.rating-strip {
		position: relative;
		z-index: 1;
	}

	.site-header {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 24px;
	}

	.brand {
		display: block;
		width: clamp(190px, 24vw, 320px);
	}

	.brand img {
		display: block;
		width: 100%;
		height: auto;
	}

	nav {
		display: flex;
		align-items: center;
		gap: clamp(16px, 2vw, 32px);
		color: #2d2d2d;
		font-size: 0.74rem;
		font-weight: 800;
		letter-spacing: 0.08em;
		text-transform: uppercase;
	}

	nav a {
		border-bottom: 1px solid transparent;
		padding-block: 6px;
	}

	nav a:hover {
		border-color: currentColor;
	}

	.nav-phone {
		border: 1px solid #161616;
		padding: 10px 12px;
		background: #161616;
		color: #fff;
		white-space: nowrap;
	}

	nav .nav-phone:hover {
		border-color: #2f64b7;
		background: #2f64b7;
	}

	.language-switch {
		display: inline-grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 1px;
		border: 1px solid #161616;
		background: #161616;
	}

	.language-switch button {
		min-height: 38px;
		border: 0;
		padding: 8px 12px;
		background: #fff;
		color: #161616;
		font-size: 0.72rem;
	}

	.language-switch button.active {
		background: #161616;
		color: #fff;
	}

	.language-switch button:hover {
		background: #2f64b7;
		color: #fff;
		transform: none;
	}

	.hero-body {
		display: grid;
		grid-template-columns: minmax(0, 0.88fr) minmax(330px, 0.7fr);
		gap: clamp(32px, 6vw, 96px);
		align-items: center;
		padding-block: 70px;
	}

	.hero-inner {
		width: min(760px, 100%);
	}

	.eyebrow,
	.section-kicker {
		margin: 0 0 18px;
		color: #134f8b;
		font-size: 0.72rem;
		font-weight: 900;
		letter-spacing: 0.16em;
		text-transform: uppercase;
	}

	h1,
	h2,
	h3,
	p {
		margin-top: 0;
	}

	h1 {
		max-width: 780px;
		margin-bottom: 22px;
		font-size: clamp(3.2rem, 9vw, 8.4rem);
		font-weight: 850;
		letter-spacing: 0;
		line-height: 0.91;
	}

	h2 {
		margin-bottom: 0;
		font-size: clamp(2.2rem, 5vw, 5rem);
		font-weight: 820;
		letter-spacing: 0;
		line-height: 0.96;
	}

	h3 {
		margin-bottom: 14px;
		font-size: 1.1rem;
		letter-spacing: 0;
	}

	.intro {
		max-width: 600px;
		margin-bottom: 34px;
		color: #3b3b3b;
		font-size: clamp(1rem, 1.5vw, 1.18rem);
	}

	.hero-actions {
		display: flex;
		flex-wrap: wrap;
		gap: 12px;
	}

	.hero-media,
	.proof-media {
		position: relative;
		margin: 0;
		overflow: hidden;
		border: 1px solid rgba(22, 22, 22, 0.14);
		background: #e7e7e1;
	}

	.hero-media {
		aspect-ratio: 4 / 5;
		align-self: stretch;
	}

	.hero-media::before,
	.proof-media::before {
		position: absolute;
		inset: 0;
		z-index: 1;
		content: '';
		background: linear-gradient(180deg, transparent 54%, rgba(0, 0, 0, 0.42));
		pointer-events: none;
	}

	.hero-media img,
	.proof-media img {
		display: block;
		width: 100%;
		height: 100%;
		object-fit: cover;
		transition:
			transform 700ms ease,
			filter 700ms ease;
	}

	.hero-media:hover img,
	.proof-media:hover img {
		filter: saturate(1.06) contrast(1.03);
		transform: scale(1.045);
	}

	.hero-media figcaption,
	.proof-media figcaption {
		position: absolute;
		right: 18px;
		bottom: 16px;
		z-index: 2;
		color: #fff;
		font-size: 0.72rem;
		font-weight: 900;
		letter-spacing: 0.12em;
		text-transform: uppercase;
	}

	.button,
	button {
		min-height: 48px;
		border: 1px solid #161616;
		padding: 14px 20px;
		background: transparent;
		color: #161616;
		font: inherit;
		font-size: 0.74rem;
		font-weight: 900;
		letter-spacing: 0.1em;
		text-transform: uppercase;
		cursor: pointer;
		transition:
			background-color 180ms ease,
			border-color 180ms ease,
			color 180ms ease,
			transform 180ms ease;
	}

	.button.primary,
	button {
		background: #161616;
		color: #fff;
	}

	.button.call {
		border-color: #2f64b7;
		background: #2f64b7;
		color: #fff;
	}

	.button.secondary:hover,
	.button.call:hover,
	button:hover {
		background: #2f64b7;
		border-color: #2f64b7;
		color: #fff;
		transform: translateY(-2px);
	}

	.rating-strip {
		display: grid;
		grid-template-columns: auto repeat(4, minmax(0, 1fr));
		gap: 1px;
		background: rgba(22, 22, 22, 0.16);
		border: 1px solid rgba(22, 22, 22, 0.16);
	}

	.rating-strip > * {
		display: flex;
		align-items: center;
		min-height: 68px;
		padding: 14px 18px;
		background: rgba(255, 255, 255, 0.7);
		font-size: 0.84rem;
		font-weight: 800;
		text-transform: uppercase;
	}

	.rating-strip strong {
		justify-content: center;
		background: #161616;
		color: #fff;
		font-size: 1.6rem;
	}

	.statement,
	.services,
	.proof,
	.reviews,
	.contact,
	.site-footer {
		padding: clamp(72px, 10vw, 132px) clamp(20px, 4vw, 64px);
	}

	.statement {
		display: grid;
		grid-template-columns: minmax(0, 1.05fr) minmax(260px, 0.75fr);
		gap: clamp(30px, 8vw, 120px);
		background: #161616;
		color: #fff;
	}

	.statement p:last-child,
	.proof-copy p,
	.contact-copy p {
		align-self: end;
		margin-bottom: 0;
		color: rgba(255, 255, 255, 0.72);
		font-size: 1.02rem;
	}

	.statement .section-kicker,
	.proof .section-kicker {
		color: #86b7ef;
	}

	.section-heading {
		display: grid;
		grid-template-columns: 0.32fr 1fr;
		gap: clamp(24px, 6vw, 84px);
		max-width: 1220px;
		margin-bottom: 42px;
	}

	.service-grid,
	.review-grid {
		display: grid;
		grid-template-columns: repeat(3, minmax(0, 1fr));
		gap: 1px;
		background: rgba(22, 22, 22, 0.14);
		border: 1px solid rgba(22, 22, 22, 0.14);
	}

	.service-card,
	.review-card {
		margin: 0;
		background: #fff;
	}

	.service-card {
		min-height: 310px;
		padding: clamp(24px, 4vw, 44px);
		transition:
			background-color 220ms ease,
			box-shadow 220ms ease,
			transform 220ms ease;
	}

	.service-card:hover,
	.review-card:hover {
		position: relative;
		z-index: 1;
		box-shadow: 0 22px 50px rgba(22, 22, 22, 0.1);
		transform: translateY(-6px);
	}

	.service-card span {
		display: block;
		width: 42px;
		height: 6px;
		margin-bottom: 60px;
		background: linear-gradient(90deg, #0ab14b 0 33%, #ed1c24 33% 66%, #2f64b7 66%);
	}

	.service-card p,
	blockquote,
	.review-card figcaption {
		color: #4b4b4b;
	}

	.proof {
		display: grid;
		grid-template-columns: minmax(0, 0.85fr) minmax(320px, 0.7fr);
		gap: clamp(34px, 7vw, 96px);
		background: #1d1d1b;
		color: #fff;
	}

	.proof-stack {
		display: grid;
		gap: 18px;
	}

	.proof-media {
		aspect-ratio: 16 / 10;
		border-color: rgba(255, 255, 255, 0.16);
		background: #101010;
	}

	.proof-list {
		display: grid;
		align-content: center;
		gap: 1px;
		background: rgba(255, 255, 255, 0.16);
		border: 1px solid rgba(255, 255, 255, 0.16);
	}

	.proof-list div {
		display: grid;
		grid-template-columns: 64px 1fr;
		gap: 24px;
		align-items: center;
		min-height: 100px;
		padding: 20px 24px;
		background: #1d1d1b;
	}

	.proof-list strong {
		color: #86b7ef;
		font-size: 0.82rem;
	}

	.proof-list span {
		font-weight: 800;
	}

	.reviews {
		background: #f7f7f4;
	}

	figure {
		margin: 0;
	}

	.review-card {
		min-height: 280px;
		padding: clamp(24px, 4vw, 42px);
		transition:
			box-shadow 220ms ease,
			transform 220ms ease;
	}

	blockquote {
		margin: 0 0 32px;
		font-size: clamp(1.05rem, 1.7vw, 1.35rem);
		line-height: 1.35;
	}

	figcaption {
		font-size: 0.76rem;
		font-weight: 900;
		letter-spacing: 0.12em;
		text-transform: uppercase;
	}

	.contact {
		display: grid;
		grid-template-columns: minmax(0, 0.75fr) minmax(320px, 0.65fr);
		gap: clamp(34px, 7vw, 110px);
		background: #fff;
	}

	.contact-info {
		display: grid;
		align-content: start;
		gap: 34px;
	}

	.contact .section-kicker {
		color: #134f8b;
	}

	.contact-copy p {
		margin-top: 24px;
		color: #4b4b4b;
	}

	.contact-details {
		display: grid;
		gap: 1px;
		border: 1px solid rgba(22, 22, 22, 0.14);
		background: rgba(22, 22, 22, 0.14);
	}

	.detail-card {
		display: grid;
		gap: 10px;
		padding: 22px;
		background: #fbfbf8;
		transition:
			background-color 180ms ease,
			transform 180ms ease;
	}

	.detail-card:hover {
		background: #fff;
		transform: translateX(4px);
	}

	.detail-card > span {
		color: #134f8b;
		font-size: 0.72rem;
		font-weight: 900;
		letter-spacing: 0.12em;
		text-transform: uppercase;
	}

	.detail-card > strong {
		color: #161616;
		font-size: clamp(1.1rem, 2vw, 1.55rem);
		line-height: 1.2;
	}

	.phone-card {
		background: #161616;
		color: #fff;
	}

	.phone-card > span,
	.phone-card > strong {
		color: inherit;
	}

	.hours-card ul,
	.footer-hours {
		display: grid;
		gap: 8px;
		margin: 0;
		padding: 0;
		list-style: none;
	}

	.hours-card li,
	.footer-hours li {
		display: grid;
		grid-template-columns: minmax(92px, 0.45fr) 1fr;
		gap: 18px;
		align-items: baseline;
	}

	.hours-card li strong,
	.footer-hours li span:first-child {
		font-weight: 850;
	}

	.hours-card time {
		color: #363636;
		font-style: normal;
	}

	.hours-card p {
		margin: 8px 0 0;
		color: #666;
		font-size: 0.92rem;
	}

	form {
		display: grid;
		gap: 18px;
		align-self: start;
	}

	label {
		display: grid;
		gap: 8px;
		color: #363636;
		font-size: 0.76rem;
		font-weight: 850;
		letter-spacing: 0.08em;
		text-transform: uppercase;
	}

	input,
	select,
	textarea {
		width: 100%;
		border: 1px solid #c7c7c1;
		border-radius: 0;
		padding: 13px 14px;
		background: #fbfbf8;
		color: #161616;
		font: inherit;
		font-size: 1rem;
		letter-spacing: 0;
	}

	input:focus,
	select:focus,
	textarea:focus {
		border-color: #2f64b7;
		outline: 2px solid rgba(47, 100, 183, 0.16);
	}

	textarea {
		resize: vertical;
	}

	.site-footer {
		display: grid;
		grid-template-columns: minmax(220px, 1fr) minmax(190px, 0.75fr) minmax(220px, 0.8fr) minmax(
				150px,
				0.45fr
			);
		gap: clamp(28px, 5vw, 76px);
		background: #161616;
		color: #fff;
	}

	.footer-brand {
		display: block;
		width: min(260px, 100%);
		margin-bottom: 24px;
		filter: invert(1);
	}

	.footer-brand img {
		display: block;
		width: 100%;
		height: auto;
	}

	.site-footer h2 {
		margin: 0 0 18px;
		color: #86b7ef;
		font-size: 0.72rem;
		font-weight: 900;
		letter-spacing: 0.12em;
		line-height: 1.3;
		text-transform: uppercase;
	}

	.site-footer p,
	.site-footer a,
	.footer-hours {
		color: rgba(255, 255, 255, 0.74);
	}

	.site-footer p {
		margin-bottom: 0;
	}

	.site-footer > div:last-child {
		display: grid;
		align-content: start;
		gap: 12px;
	}

	.site-footer > div:nth-child(4) {
		display: grid;
		align-content: start;
		gap: 12px;
	}

	.footer-phone {
		display: inline-block;
		margin-bottom: 14px;
		color: #fff;
		font-size: 1.35rem;
		font-weight: 900;
	}

	.footer-hours li {
		grid-template-columns: minmax(82px, 0.7fr) 1fr;
		font-size: 0.95rem;
	}

	.footer-legal {
		grid-column: 1 / -1;
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		gap: 14px 28px;
		border-top: 1px solid rgba(255, 255, 255, 0.14);
		padding-top: 28px;
	}

	.footer-legal p,
	.footer-legal a {
		font-size: 0.82rem;
	}

	@media (prefers-reduced-motion: no-preference) {
		.hero-inner {
			animation: rise-in 700ms ease both 120ms;
		}

		[data-reveal] {
			animation: rise-in both;
			animation-duration: 700ms;
			animation-timing-function: ease;
			animation-timeline: view();
			animation-range: entry 0% cover 28%;
		}

		.hero-media {
			animation:
				hero-focus 800ms ease both 260ms,
				soft-float 7s ease-in-out 1.2s infinite;
		}

		.rating-strip {
			animation: rise-in 700ms ease both 420ms;
		}
	}

	@media (max-width: 900px) {
		.site-header {
			align-items: flex-start;
			flex-direction: column;
		}

		nav {
			width: 100%;
			justify-content: space-between;
			gap: 10px;
		}

		.hero {
			min-height: auto;
		}

		.hero-body {
			grid-template-columns: 1fr;
			padding-block: 56px;
		}

		.hero-media {
			aspect-ratio: 16 / 10;
		}

		.hero::after {
			top: 42%;
			right: -36vw;
			width: 86vw;
			height: 30vh;
		}

		.rating-strip,
		.statement,
		.section-heading,
		.service-grid,
		.proof,
		.review-grid,
		.contact,
		.site-footer {
			grid-template-columns: 1fr;
		}

		.rating-strip > * {
			min-height: 56px;
		}
	}

	@media (max-width: 560px) {
		.hero {
			padding-inline: 18px;
		}

		.brand {
			width: min(100%, 260px);
		}

		nav {
			font-size: 0.68rem;
			flex-wrap: wrap;
			justify-content: flex-start;
		}

		h1 {
			font-size: clamp(3rem, 18vw, 5.2rem);
		}

		.button,
		button {
			width: 100%;
			text-align: center;
		}

		.statement,
		.services,
		.proof,
		.reviews,
		.contact,
		.site-footer {
			padding-inline: 18px;
		}

		.proof-list div {
			grid-template-columns: 1fr;
			gap: 8px;
		}

		.hours-card li,
		.footer-hours li {
			grid-template-columns: 1fr;
			gap: 2px;
		}
	}
</style>
