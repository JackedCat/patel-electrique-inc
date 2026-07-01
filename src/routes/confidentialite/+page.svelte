<script lang="ts">
	import logo from '$lib/assets/patel_electrique.png';

	const phoneDisplay = '(514) 684-3844';
	const phoneHref = 'tel:+15146843844';
	const address = '64 Rue Audubon, Dollard-des-Ormeaux, QC H9B 3E9';
	const currentYear = new Date().getFullYear();

	type Language = 'fr' | 'en';

	let language = $state<Language>('fr');

	const copy = {
		fr: {
			metaTitle: 'Politique de confidentialité | Patel Électrique Inc',
			metaDescription:
				'Politique de confidentialité de Patel Électrique Inc, électriciens résidentiels et commerciaux à Dollard-des-Ormeaux.',
			backHomeAria: "Retour à l'accueil Patel Électrique Inc",
			kicker: 'Patel Électrique Inc',
			title: 'Politique de confidentialité',
			updated: 'Dernière mise à jour : 1 juillet 2026',
			sections: [
				{
					title: 'Renseignements recueillis',
					text: "Lorsque vous communiquez avec Patel Électrique Inc, nous pouvons recueillir les renseignements que vous choisissez de nous transmettre, notamment votre nom, votre adresse courriel, votre numéro de téléphone, l'adresse du projet, le type de service demandé et le contenu de votre message."
				},
				{
					title: 'Utilisation des renseignements',
					text: 'Ces renseignements servent à répondre à votre demande, planifier une intervention, préparer une estimation, communiquer avec vous au sujet du service et assurer le suivi nécessaire après les travaux.'
				},
				{
					title: 'Conservation et protection',
					text: "Nous conservons les renseignements seulement pour la durée raisonnablement nécessaire aux fins de service, de suivi administratif ou d'obligations légales applicables. Nous prenons des mesures raisonnables pour limiter l'accès aux renseignements aux personnes qui en ont besoin pour traiter votre demande."
				},
				{
					title: 'Partage des renseignements',
					text: "Patel Électrique Inc ne vend pas vos renseignements personnels. Ils peuvent être partagés seulement lorsque cela est nécessaire pour fournir le service demandé, respecter une obligation légale ou protéger les droits et la sécurité de l'entreprise, des clients ou du public."
				},
				{
					title: 'Données techniques',
					text: "Comme la plupart des sites web, certains renseignements techniques peuvent être traités par l'hébergement ou les outils essentiels au fonctionnement du site, par exemple l'adresse IP, le type d'appareil, le navigateur utilisé et les journaux de serveur."
				},
				{
					title: 'Vos choix',
					text: "Vous pouvez communiquer avec nous pour demander l'accès, la correction ou la suppression de renseignements personnels que vous nous avez transmis, sous réserve des obligations de conservation applicables."
				}
			],
			contactTitle: 'Nous joindre',
			contactText:
				'Pour toute question concernant cette politique, contactez Patel Électrique Inc au',
			contactConnector: "ou à l'adresse suivante :",
			backHome: "Retour à l'accueil",
			rights: 'Tous droits réservés.'
		},
		en: {
			metaTitle: 'Privacy Policy | Patel Electrique Inc',
			metaDescription:
				'Privacy Policy for Patel Electrique Inc, residential and commercial electricians in Dollard-des-Ormeaux.',
			backHomeAria: 'Back to Patel Electrique Inc home',
			kicker: 'Patel Electrique Inc',
			title: 'Privacy Policy',
			updated: 'Last updated: July 1, 2026',
			sections: [
				{
					title: 'Information collected',
					text: 'When you contact Patel Electrique Inc, we may collect the information you choose to provide, including your name, email address, phone number, project address, type of service requested, and the content of your message.'
				},
				{
					title: 'Use of information',
					text: 'This information is used to respond to your request, schedule service, prepare an estimate, communicate with you about the service, and provide any necessary follow-up after the work is completed.'
				},
				{
					title: 'Retention and protection',
					text: 'We retain information only for as long as reasonably necessary for service, administrative follow-up, or applicable legal obligations. We take reasonable steps to limit access to people who need the information to handle your request.'
				},
				{
					title: 'Sharing of information',
					text: 'Patel Electrique Inc does not sell your personal information. It may be shared only when necessary to provide the requested service, comply with a legal obligation, or protect the rights and safety of the company, clients, or the public.'
				},
				{
					title: 'Technical data',
					text: 'Like most websites, some technical information may be processed by hosting services or tools essential to the operation of the site, such as IP address, device type, browser used, and server logs.'
				},
				{
					title: 'Your choices',
					text: 'You may contact us to request access to, correction of, or deletion of personal information you have provided to us, subject to applicable retention obligations.'
				}
			],
			contactTitle: 'Contact us',
			contactText: 'For any question about this policy, contact Patel Electrique Inc at',
			contactConnector: 'or at the following address:',
			backHome: 'Back to home',
			rights: 'All rights reserved.'
		}
	} as const;

	const content = $derived(copy[language]);
</script>

<svelte:head>
	<title>{content.metaTitle}</title>
	<meta name="description" content={content.metaDescription} />
</svelte:head>

<main class="privacy-page">
	<header class="privacy-header">
		<a class="brand" href="/" aria-label={content.backHomeAria}>
			<img src={logo} alt="Patel Electrique Inc" />
		</a>
		<div class="header-actions">
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
			<a class="phone" href={phoneHref}>{phoneDisplay}</a>
		</div>
	</header>

	<article class="policy">
		<p class="eyebrow">{content.kicker}</p>
		<h1>{content.title}</h1>
		<p class="updated">{content.updated}</p>

		{#each content.sections as section}
			<section>
				<h2>{section.title}</h2>
				<p>{section.text}</p>
			</section>
		{/each}

		<section>
			<h2>{content.contactTitle}</h2>
			<p>
				{content.contactText}
				<a href={phoneHref}>{phoneDisplay}</a>
				{content.contactConnector}
				{address}.
			</p>
		</section>

		<a class="back-link" href="/">{content.backHome}</a>
	</article>

	<footer class="privacy-footer">
		<p>&copy; {currentYear} Patel Electrique Inc. {content.rights}</p>
	</footer>
</main>

<style>
	:global(*) {
		box-sizing: border-box;
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
		line-height: 1.6;
	}

	:global(a) {
		color: inherit;
		text-decoration: none;
	}

	.privacy-page {
		min-height: 100svh;
		display: grid;
		grid-template-rows: auto 1fr auto;
	}

	.privacy-header,
	.privacy-footer {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 24px;
		padding: 24px clamp(20px, 4vw, 64px);
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

	.header-actions {
		display: flex;
		align-items: center;
		gap: 12px;
	}

	.language-switch {
		display: inline-grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 1px;
		border: 1px solid #161616;
		background: #161616;
	}

	.language-switch button {
		min-height: 42px;
		border: 0;
		padding: 10px 12px;
		background: #fff;
		color: #161616;
		font: inherit;
		font-size: 0.72rem;
		font-weight: 900;
		letter-spacing: 0.1em;
		text-transform: uppercase;
		cursor: pointer;
		transition:
			background-color 180ms ease,
			color 180ms ease;
	}

	.language-switch button.active {
		background: #161616;
		color: #fff;
	}

	.language-switch button:hover {
		background: #2f64b7;
		color: #fff;
	}

	.phone,
	.back-link {
		border: 1px solid #161616;
		padding: 12px 16px;
		font-size: 0.74rem;
		font-weight: 900;
		letter-spacing: 0.1em;
		text-transform: uppercase;
		transition:
			background-color 180ms ease,
			border-color 180ms ease,
			color 180ms ease,
			transform 180ms ease;
	}

	.phone {
		background: #161616;
		color: #fff;
	}

	.phone:hover,
	.back-link:hover {
		border-color: #2f64b7;
		background: #2f64b7;
		color: #fff;
		transform: translateY(-2px);
	}

	.policy {
		width: min(980px, calc(100% - 40px));
		margin: 0 auto;
		padding: clamp(54px, 8vw, 108px) 0;
	}

	.eyebrow,
	.updated {
		color: #134f8b;
		font-size: 0.72rem;
		font-weight: 900;
		letter-spacing: 0.14em;
		text-transform: uppercase;
	}

	h1 {
		max-width: 820px;
		margin: 0 0 18px;
		font-size: clamp(3rem, 8vw, 7rem);
		font-weight: 850;
		letter-spacing: 0;
		line-height: 0.92;
	}

	.updated {
		margin: 0 0 56px;
	}

	section {
		display: grid;
		grid-template-columns: minmax(180px, 0.34fr) 1fr;
		gap: clamp(20px, 5vw, 72px);
		border-top: 1px solid rgba(22, 22, 22, 0.16);
		padding: 28px 0;
	}

	h2 {
		margin: 0;
		font-size: 1rem;
		letter-spacing: 0;
	}

	p {
		margin: 0;
		color: #4b4b4b;
	}

	section a {
		color: #134f8b;
		font-weight: 850;
	}

	.back-link {
		display: inline-block;
		margin-top: 36px;
	}

	.privacy-footer {
		border-top: 1px solid rgba(22, 22, 22, 0.12);
	}

	.privacy-footer p {
		color: #4b4b4b;
		font-size: 0.88rem;
	}

	@media (max-width: 760px) {
		.privacy-header,
		.privacy-footer {
			align-items: flex-start;
			flex-direction: column;
		}

		.header-actions {
			align-items: flex-start;
			flex-direction: column;
		}

		section {
			grid-template-columns: 1fr;
			gap: 12px;
		}
	}
</style>
