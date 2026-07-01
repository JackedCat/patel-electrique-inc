<script lang="ts">
	import logo from '$lib/assets/patel_electrique.png';

	const phoneDisplay = '(514) 684-3844';
	const phoneHref = 'tel:+15146843844';
	const address = '64 Rue Audubon, Dollard-des-Ormeaux, QC H9B 3E9';
	const currentYear = new Date().getFullYear();
</script>

<svelte:head>
	<title>Politique de confidentialite | Patel Electrique Inc</title>
	<meta
		name="description"
		content="Politique de confidentialite de Patel Electrique Inc, electriciens residentiels et commerciaux a Dollard-des-Ormeaux."
	/>
</svelte:head>

<main class="privacy-page">
	<header class="privacy-header">
		<a class="brand" href="/" aria-label="Retour a l'accueil Patel Electrique Inc">
			<img src={logo} alt="Patel Electrique Inc" />
		</a>
		<a class="phone" href={phoneHref}>{phoneDisplay}</a>
	</header>

	<article class="policy">
		<p class="eyebrow">Patel Electrique Inc</p>
		<h1>Politique de confidentialite</h1>
		<p class="updated">Derniere mise a jour : 1 juillet 2026</p>

		<section>
			<h2>Renseignements recueillis</h2>
			<p>
				Lorsque vous communiquez avec Patel Electrique Inc, nous pouvons recueillir les
				renseignements que vous choisissez de nous transmettre, notamment votre nom, votre adresse
				courriel, votre numero de telephone, l'adresse du projet, le type de service demande et le
				contenu de votre message.
			</p>
		</section>

		<section>
			<h2>Utilisation des renseignements</h2>
			<p>
				Ces renseignements servent a repondre a votre demande, planifier une intervention, preparer
				une estimation, communiquer avec vous au sujet du service et assurer le suivi necessaire
				apres les travaux.
			</p>
		</section>

		<section>
			<h2>Conservation et protection</h2>
			<p>
				Nous conservons les renseignements seulement pour la duree raisonnablement necessaire aux
				fins de service, de suivi administratif ou d'obligations legales applicables. Nous prenons
				des mesures raisonnables pour limiter l'acces aux renseignements aux personnes qui en ont
				besoin pour traiter votre demande.
			</p>
		</section>

		<section>
			<h2>Partage des renseignements</h2>
			<p>
				Patel Electrique Inc ne vend pas vos renseignements personnels. Ils peuvent etre partages
				seulement lorsque cela est necessaire pour fournir le service demande, respecter une
				obligation legale ou proteger les droits et la securite de l'entreprise, des clients ou du
				public.
			</p>
		</section>

		<section>
			<h2>Donnees techniques</h2>
			<p>
				Comme la plupart des sites web, certains renseignements techniques peuvent etre traites par
				l'hebergement ou les outils essentiels au fonctionnement du site, par exemple l'adresse IP,
				le type d'appareil, le navigateur utilise et les journaux de serveur.
			</p>
		</section>

		<section>
			<h2>Vos choix</h2>
			<p>
				Vous pouvez communiquer avec nous pour demander l'acces, la correction ou la suppression de
				renseignements personnels que vous nous avez transmis, sous reserve des obligations de
				conservation applicables.
			</p>
		</section>

		<section>
			<h2>Nous joindre</h2>
			<p>
				Pour toute question concernant cette politique, contactez Patel Electrique Inc au
				<a href={phoneHref}>{phoneDisplay}</a> ou a l'adresse suivante : {address}.
			</p>
		</section>

		<a class="back-link" href="/">Retour a l'accueil</a>
	</article>

	<footer class="privacy-footer">
		<p>&copy; {currentYear} Patel Electrique Inc. Tous droits reserves.</p>
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

		section {
			grid-template-columns: 1fr;
			gap: 12px;
		}
	}
</style>
