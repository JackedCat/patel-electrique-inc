<script lang="ts">
	import heroInstallation from '$lib/assets/patel-hero-installation.jpg';
	import panelInspection from '$lib/assets/patel-panel-inspection.jpg';
	import logo from '$lib/assets/patel_electrique.png';

	const phoneDisplay = '(514) 684-3844';
	const phoneHref = 'tel:+15146843844';
	const address = '64 Rue Audubon, Dollard-des-Ormeaux, QC H9B 3E9';

	const hours = [
		{ day: 'Lundi', time: '8h00-17h00' },
		{ day: 'Mardi', time: '8h00-17h00' },
		{ day: 'Mercredi', time: '8h00-17h00' },
		{ day: 'Jeudi', time: '8h00-17h00' },
		{ day: 'Vendredi', time: '8h00-17h00' },
		{ day: 'Samedi', time: 'Ferme' },
		{ day: 'Dimanche', time: 'Ferme' }
	];

	const services = [
		{
			title: 'Residentiel',
			text: 'Installation, renovation, diagnostic et entretien electrique pour les maisons, condos et immeubles.'
		},
		{
			title: 'Commercial',
			text: 'Interventions fiables pour commerces, bureaux et proprietes locatives, avec un travail documente et soigne.'
		},
		{
			title: 'Mise aux normes',
			text: 'Conseils clairs, execution conforme au code et aucune solution rapide qui compromet la securite.'
		}
	];

	const reviews = [
		{
			quote:
				'Absolument excellent. Tres competent, professionnel et humain. Tout etait explique clairement et le travail a ete fait efficacement.',
			name: 'Avis Google'
		},
		{
			quote:
				'Utilise depuis plus de 10 ans pour des proprietes residentielles et commerciales. Toujours professionnel, fiable et hautement qualifie.',
			name: 'Client residentiel et commercial'
		},
		{
			quote:
				'Conseils professionnels, travail termine a temps et confiance que le projet sera fait selon le code, sans raccourcis.',
			name: 'Avis Google'
		}
	];
</script>

<svelte:head>
	<title>Patel Electrique Inc | Electriciens residentiels et commerciaux</title>
	<meta
		name="description"
		content="Patel Electrique Inc offre des services electriques residentiels et commerciaux a Dollard-des-Ormeaux. Appelez le (514) 684-3844 pour un travail propre, fiable et conforme au code."
	/>
</svelte:head>

<main>
	<section class="hero" id="accueil">
		<header class="site-header" aria-label="Navigation principale">
			<a class="brand" href="#accueil" aria-label="Patel Electrique Inc">
				<img src={logo} alt="Patel Electrique Inc" />
			</a>

			<nav>
				<a href="#services">Services</a>
				<a href="#avis">Avis</a>
				<a href="#contact">Contact</a>
				<a class="nav-phone" href={phoneHref}>{phoneDisplay}</a>
			</nav>
		</header>

		<div class="hero-body">
			<div class="hero-inner">
				<p class="eyebrow">Electriciens residentiels et commerciaux</p>
				<h1>Un travail electrique propre, ponctuel et conforme.</h1>
				<p class="intro">
					Patel Electrique Inc accompagne les proprietaires et les entreprises avec des conseils
					clairs, une execution precise et une reputation batie sur la confiance.
				</p>

				<div class="hero-actions">
					<a class="button primary" href="#contact">Demander une estimation</a>
					<a class="button call" href={phoneHref}>Appeler {phoneDisplay}</a>
					<a class="button secondary" href="#avis">Voir les avis</a>
				</div>
			</div>

			<figure class="hero-media" data-reveal>
				<img
					src={heroInstallation}
					alt="Installation electrique residentielle propre dans un interieur lumineux"
					loading="eager"
					decoding="async"
				/>
				<figcaption>Installation residentielle</figcaption>
			</figure>
		</div>

		<div class="rating-strip" aria-label="Evaluation Google">
			<strong>5,0</strong>
			<span>136 avis Google</span>
			<span>Travail bien fait et propre</span>
			<span>A l'heure prevue</span>
			<a href={phoneHref}>Appel direct {phoneDisplay}</a>
		</div>
	</section>

	<section class="statement" data-reveal>
		<div>
			<p class="section-kicker">Patel Electrique Inc</p>
			<h2>Des interventions serieuses, sans raccourcis.</h2>
		</div>
		<p>
			Chaque mandat est traite avec le meme standard: comprendre le besoin, expliquer les options,
			proteger les lieux, executer avec precision et laisser une installation securitaire.
		</p>
	</section>

	<section class="services" id="services" aria-labelledby="services-title" data-reveal>
		<div class="section-heading">
			<p class="section-kicker">Services</p>
			<h2 id="services-title">Pour proprietes privees et espaces de travail.</h2>
		</div>

		<div class="service-grid">
			{#each services as service}
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
			<p class="section-kicker">Methode</p>
			<h2 id="proof-title">Clair avant, propre pendant, conforme apres.</h2>
			<p>
				Les avis clients reviennent sur les memes points: ponctualite, professionnalisme,
				explications simples et travaux faits avec soin. C'est le standard applique sur chaque
				intervention.
			</p>
		</div>

		<div class="proof-stack">
			<figure class="proof-media">
				<img
					src={panelInspection}
					alt="Panneau electrique organise avec outil de mesure et cablage soigne"
					loading="lazy"
					decoding="async"
				/>
				<figcaption>Inspection et verification</figcaption>
			</figure>

			<div class="proof-list">
				<div>
					<strong>01</strong>
					<span>Evaluation du besoin et conseils pratiques</span>
				</div>
				<div>
					<strong>02</strong>
					<span>Execution efficace avec respect des lieux</span>
				</div>
				<div>
					<strong>03</strong>
					<span>Travail termine selon le code et sans compromis</span>
				</div>
			</div>
		</div>
	</section>

	<section class="reviews" id="avis" aria-labelledby="reviews-title" data-reveal>
		<div class="section-heading">
			<p class="section-kicker">Avis</p>
			<h2 id="reviews-title">Une note parfaite, portee par la constance.</h2>
		</div>

		<div class="review-grid">
			{#each reviews as review}
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
				<p class="section-kicker">Contact</p>
				<h2 id="contact-title">Parlez-nous de votre projet.</h2>
				<p>
					Pour une demande rapide, appelez directement. Sinon, decrivez le travail a faire,
					l'adresse du projet et vos disponibilites.
				</p>
			</div>

			<div class="contact-details" aria-label="Coordonnees">
				<a class="detail-card phone-card" href={phoneHref}>
					<span>Telephone</span>
					<strong>{phoneDisplay}</strong>
				</a>

				<div class="detail-card">
					<span>Adresse</span>
					<strong>{address}</strong>
				</div>

				<div class="detail-card hours-card">
					<span>Heures d'ouverture</span>
					<ul>
						{#each hours as item}
							<li>
								<strong>{item.day}</strong>
								<time>{item.time}</time>
							</li>
						{/each}
					</ul>
					<p>Les horaires peuvent varier les jours feries.</p>
				</div>
			</div>
		</div>

		<form name="contact" method="post">
			<label>
				Nom
				<input name="name" type="text" autocomplete="name" required />
			</label>

			<label>
				Courriel
				<input name="email" type="email" autocomplete="email" required />
			</label>

			<label>
				Type de projet
				<select name="project" required>
					<option value="">Selectionner</option>
					<option>Residentiel</option>
					<option>Commercial</option>
					<option>Mise aux normes</option>
					<option>Autre demande</option>
				</select>
			</label>

			<label>
				Message
				<textarea name="message" rows="5" required></textarea>
			</label>

			<button type="submit">Envoyer la demande</button>
		</form>
	</section>

	<footer class="site-footer">
		<div>
			<a class="footer-brand" href="#accueil" aria-label="Patel Electrique Inc">
				<img src={logo} alt="Patel Electrique Inc" />
			</a>
			<p>Electriciens residentiels et commerciaux a Dollard-des-Ormeaux.</p>
		</div>

		<div>
			<h2>Coordonnees</h2>
			<a class="footer-phone" href={phoneHref}>{phoneDisplay}</a>
			<p>{address}</p>
		</div>

		<div>
			<h2>Heures</h2>
			<ul class="footer-hours">
				{#each hours as item}
					<li>
						<span>{item.day}</span>
						<span>{item.time}</span>
					</li>
				{/each}
			</ul>
		</div>

		<div>
			<h2>Navigation</h2>
			<a href="#services">Services</a>
			<a href="#avis">Avis</a>
			<a href="#contact">Contact</a>
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
