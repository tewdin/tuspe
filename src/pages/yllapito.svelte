<script>
	import { metatags } from "@sveltech/routify"
	let title = "Kotisivut yritykselle ketterästi ja ammattitaidolla"
	let desc = "Kotisivut ovat pelivälineesi digikentällä. Hyvin rakennetut ja toimivat sivut ovat ilo silmälle, aperitiivi ostohalulle sekä tehty maali asiakkaan bisnekseen."
	let img = "https://timoanttila.com/images/gallery/2019-deli-yawns.jpg"
	let url = "https://tuspe.com/referenssit"
	metatags.title = title +" | Tuspe Design"
	metatags.description = desc
	metatags.image = img
	metatags.url = url
	metatags.canonical = url
	metatags["twitter:card"] = "summary_large_image"
	metatags["twitter:title"] = title
	metatags["twitter:description"] = desc
	metatags["twitter:image"] = img
</script>

<svelte:head>
	<link rel="stylesheet" href="/page.css"> 
</svelte:head>

<div id="page">

<section id="about">
	<div class="img right">
		<picture>
			<source srcset="/images/hosting-page-mobile.webp" media="(max-width:999px)" type="image/webp">
			<source srcset="/images/hosting-page.webp" media="(min-width:1000px)" type="image/webp">
			<source srcset="/images/hosting-page-mobile.jpg" media="(max-width:999px)" type="image/jpeg">
			<source srcset="/images/hosting-page.jpg" media="(min-width:1000px)" type="image/jpeg">
			<img src="/images/hosting-page.jpg" alt={title}>
		</picture>
	</div>
	<div class="txt cell mxa">
		<div class="content">
			<h1 class="w3">Verkkosivujen luotettavat ylläpitopalvelut</h1>
			<p>Kun verkkosivuillesi on luotettava ylläpitopalvelu, voit varmistua siitä, että sivut toimivat, niistä on varmuuskopiot ja tarvittaessa saat nopeasti pienet tai suuremmatkin sivuston muutokset niille. Älä turhaan stressaa vaan keskity huoletta omaan ydinbisnekseen.</p>
			<p>Kaikki data on turvassa kahdella 24/7 monitoroidulla palvelimella ja voimme tarvittaessa palauttaa sivuston nopeasti varmuuskopiosta. Reiluina tyyppeinä emme veloita jokaisesta pienistä muutoksesta tai päivityksestä erikseen vaan semmoiset kuuluvat ylläpitoon.</p>
			<p>Tsekkaa alta mitä kaikkea pakettiin kuuluu.</p>
			<p><a class="btn up" href="/yllapito">Parasta pakettiin!</a></p>
		</div>
	</div>
</section>

<section class="p3">
	<div class="container mxa small">
		<h2 class="w3 sub1 tc">Kaikki tarvittavat palvelut</h2>
		<p>Tämän kaiken saat 15€:n kuukausimaksulla (18.60€ sis. ALV). Turvallisuus ja toimivuus ovat arvokkaita asioista, mutta niiden toteutumisen ei tarvitse olla kallista kukkarollesi. Hintamme ovat pysyvästi edulliset.</p>
		<ul>
			<li>Rajoittamaton ja nopea liikenne</li>
			<li>Aina sopivasti tilaa kotisivuille</li>
			<li>Varmuuskopiointi kahdesti päivässä</li>
			<li>Palautus aikaisempaan versioon varmuuskopiosta</li>
			<li>Pienet päivitykset kotisivuille (alle 15 min)</li>
			<li>SSL-sertifikaatti (https)</li>
			<li>Verkkokauppaan kehitetyt uudet ominaisuudet ja päivitykset.</li>
			<li>Alennetut hinnat uusille projekteille.</li>
			<li>Sisällönhallintaohjelmien ja niiden moduulien päivitykset</li>
			<li>Aina uusimpia paketteja ja suojausia käyttävä palvelin</li>
			<li>Uusi <a href="/verkkotunnukset">verkkotunnus</a> (domain) ensimmäiseksi vuodeksi (esim. fi tai com)</li>
			<li>Tarvittaessa nimipalvelut verkkotunnukselle (2)</li>
			<li>Tekninen tuki + hyvät vinkit tulevaisuudelle</li>
		</ul>
		<p>Hoidamme tarvittaessa myös yrityksesi sähköpostipalvelut kuntoon.<br>Meiltä onnistuvat omalla verkkotunnuksella ilmaiset Gmail tai Outlook sekä maksulliset <a href="https://gsuite.google.fi/intl/fi/pricing.html" target="_blank" rel="noopener">Google GSuite</a> tai <a href="https://www.microsoft.com/fi-fi/microsoft-365/enterprise/compare-office-365-plans" target="_blank" rel="noopener">Microsoft Office 365</a>. Myös käyttöopastusta.</p>
		<p>Palvelimilla käytössä peilaava RAID-levy sekä palvelimien tarjoaja, <a href="https://www.ovh-hosting.fi/" target="_blank" rel="noopener" hreflang="fi">OVH</a>, vamistaa 24/7 palvelimien laitteiston toimivuuden päivystävällä teknisellä tiimillä. He reagoivat heti jos palvelimissa havaitaan ongelmia.</p>
		<p>Suosimme ilmaista <a href="https://www.cloudflare.com/" title="Suojaa palvelusi Cloudflaren avulla" target="_blank" rel="noopener" hreflang="en">Cloudflaren</a> tarjoamaa nimipalvelua verkkotunnuksille omien turvallisten palvelimiemme lisäksi, koska heillä on palvelimia ympäri maailman runkoverkon tärkeimmissä paikoissa ja nimipalvelun avulla on mahdollista välimuistittaa eli kopioida meidän palvelimella oleva kotisivu heidän verkkoon ja näin vähentää vierailijan sivun latausaikaa huomattavasti. Heidän avullaan myös mahdollista suojata sivusto paremmin mahdollisilta palvelunestohyökkäyksiltä.</p>
		<p>Liian hyvää, mutta totta. Kaikki nämä palvelut sekä tekninen osaamisemme vain puhelinsoiton päässä. Siirretään palvelusi Tuspen hotelliin.</p>
	</div>
</section>

</div>
