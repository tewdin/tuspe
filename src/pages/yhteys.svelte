<script>
	import { metatags } from "@sveltech/routify"
	let title = "Pistetään bisnekset pyörimään"
	let desc = "Ota rohkeasti yhteyttä ja tilaa ilmainen kartoitus nykyiselle kotisivulle tai verkkokaupalle."
	let img_alt = "Pistetään pallo kentälle ja suunnitellaan strategioita"
	let url = "https://tuspe.com/yhteys"
	metatags.title = title +" | Tuspe Design"
	metatags.description = desc
	metatags.url = url
	metatags.canonical = url
	metatags["twitter:card"] = "summary_large_image"
	metatags["twitter:title"] = title
	metatags["twitter:description"] = desc
	metatags["twitter:image:alt"] = img_alt
	let sites = [
		{
			title: "Molentum Oy",
			logo: "molentum",
			url: "https://molentum.fi/"
		}, {
			title: "SatuMo Oy",
			logo: "satumo",
			url: "https://www.satumo.fi/"
		}, {
			title: "BlackFly Oy",
			logo: "blackfly",
			url: "https://blackfly.fi/"
		}, {
			title: "Ratsukko Solutions Oy",
			logo: "ratsukko",
			url: "https://www.ratsukko.com/"
		}, {
			title: "Dataline Group Oy",
			logo: "dataline",
			url: "https://www.dataline.fi/"
		}
	]
	let state
	async function sendSubmit(event) {
		const formData = new FormData()
		formData.append('name', names.value)
		formData.append('email', email.value)
		formData.append('phone', phone.value)
		formData.append('body', message.value)
		formData.append('site', 'Tuspe Design Oy')
		const res = await fetch("https://api.timoanttila.com/emails.php", {
			method: 'POST',
			body: formData,
			cors: true
		});
		if (res.ok === true) {
			state = 1
		}
	}
</script>
<svelte:head>
	<link rel="stylesheet" href="/page.css">
	<style>
		form input,
		form textarea {
			width: 100%;
			padding: 10px;
			border: 1px solid #999;
			font-size: 15px
		}
		form input { margin-bottom: 6px }
		form button {
			background-color: darkgreen;
			color: rgba(255 255 255 / 87%);
			width: 100%;
			padding: 10px 20px;
			border: 0;
			margin-top: 10px;
			font-size: 15px
		}
		#hitMe .btn {
			width: 100%;
			margin-top: 20px
		}
		a.logo {
			padding: 10px 20px
		}
		a.logo img {
			width: auto;
		}
		#partners {
			background-color: #fff;
			border: 1px solid #ddd;
			width: calc(100% - 4rem)
		}
		#molentum { max-height: 30px }
		#satumo { max-height: 80px }
		#dataline { max-height: 35px }
		#about p + h3 { margin-top: 20px }
		#about h3 { font-size: 1.2rem }
		.extraSmall { max-width: 400px }
		#regs { margin-top: 15px }
	</style>
</svelte:head>

<div id="page">

<section id="about">
	<div class="img left">
		<picture>
			<source srcset="/images/sport-page-mobile.webp" media="(max-width:1000px)" type="image/webp">
			<source srcset="/images/sport-page.webp" media="(min-width:1001px)" type="image/webp">
			<source srcset="/images/sport-page-mobile.jpg" media="(max-width:1000px)" type="image/jpeg">
			<source srcset="/images/sport-page.jpg" media="(min-width:1001px)" type="image/jpeg">
			<img src="/images/sport-page.jpg" alt={img_alt}>
		</picture>
	</div>
	<div class="txt cell mxa">
		<div class="content">
			<h1 class="w3">Yhteystiedot</h1>
			<h3 class="w3">Tuspe Design Oy</h3><p>Petäjäpolku 11-15 K 70<br>37130 Nokia<br>3129423-2</p>
			<h3 class="w3">Timo Anttila</h3><p>Teknologiajohtaja<br><a class="cw" href="mailto:myynti@tuspe.com" rel="nofollow">myynti@tuspe.com</a><br><a class="cw" href="tel:+358407746121" rel="nofollow">040 774 6121</a></p>
			<h3 class="w3">Urheiluseurat</h3><p><a href="mailto:myynti@dataline.fi">myynti@dataline.fi</a><br><a href="tel:+358400273150" rel="nofollow">0400 273 150</a></p>
		</div>
	</div>
</section>

<section id="hitMe" class="p3">
	<div class="container mxa small tc"><h2 class="w3 sub1">Valmiina kehittämään kotisivuja tai kuuntelemaan ilmaisia vinkkejä?</h2></div>
	<div class="container mxa extraSmall tc">
		{#if !state}
		<form on:submit|preventDefault={sendSubmit}>
			<div class="mb"><input id="name" type="text" name="names" minlength="2" maxlength="30" placeholder="Nimi / yritys" required></div>
			<div class="mb"><input id="phone" type="text" name="phone" minlength="5" maxlength="15" placeholder="Puhelin" required></div>
			<div class="mb"><input id="email" type="email" name="email" minlength="6" maxlength="50" placeholder="Sähköposti" required></div>
			<div class="mb"><textarea id="message" name="message" maxlength="1000" placeholder="Miten voimme auttaa?" required></textarea></div>
			<div class="tc mb"><button class="up" type="submit">Lähetä</button></div>
			<div id="regs"><small><a href="/tietosuoja" rel="nofollow">rekisteri- ja tietosuojaseloste</a></small></div>
		</form>
		{:else}
		<p>Kiitos erinomaisesta valinnastasi. Olemme yhteydessä mahdollisimman pian.</p>
		{/if}
	</div>
</section>

<section id="partners" class="p3 mxa">
	<div class="container mxa small tc"><h2 class="w3 sub1">Huippujoukko kumppaneina</h2></div>
	<div class="container mxa wide tc">
		<div id="logos">
		{#each sites as item}
			<a class="logo inl" href={item.url} target="_blank">
				<picture>
					<source srcset={"/images/partners/"+ item.logo +".webp"} type="image/webp">
					<source srcset={"/images/partners/"+ item.logo +".png"} type="image/png">
					<img id={item.logo} src={"/images/partners/"+ item.logo +".png"} alt={item.title}>
				</picture>
			</a>
		{/each}
		</div>
	</div>
</section>

</div>
