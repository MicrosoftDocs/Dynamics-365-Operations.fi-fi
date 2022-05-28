---
title: Sähköisten sanomatoimintojen käyttäminen
description: Tässä ohjeaiheessa on tietoja sähköisten sanomien (EM) ominaisuuden käyttämisestä.
author: liza-golub
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a65971fa1da60b00bb525d450c0eb59aee57116e
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733760"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Sähköisten sanomatoimintojen käyttäminen

[!include [banner](../includes/banner.md)]

Jos työskentelet sanomatasolla, kannattaa käyttää **Sähköiset sanomat** -sivua (**Vero** \> **Kyselyt ja raportit** \> **Sähköiset sanomat** \> **Sähköiset sanomat**). Jos työskentelet tietojen keräyksen tai sanoman nimikkeen tasolla, sinun kannattaa käyttää **Sähköisen sanoman nimikkeet** -sivua (**Vero** \> **Kyselyt ja raportit** \> **Sähköiset sanomat** \> **Sähköisen sanoman nimikkeet**).

## <a name="electronic-messages"></a>Sähköiset sanomat

**Sähköiset sanomat** -sivulla on näkyvissä roolisi perusteella käytettävissä oleva käsittely. Käyttöoikeusroolit liitetään käsittelyyn kyseisen käsittelyn määrityksissä. Sivulla näytetään kunkin käytettävissä olevan käsittelyn sähköiset sanomat ja niihin liittyvät tiedot.

**Sanomat**-pikavälilehdessä näkyvät valitun käsittelyn sanomat. Valitun sanoman tilan ja esimääritetyn käsittelyn perusteella voit suorittaa joitakin toimintoja käyttämällä ruudukon yläpuolella olevia painikkeita:

- **Uusi** – tämä painike on liitetty **Luo viesti** -tyypin toimintoihin.
- **Poista** – Tämä painike on käytettävissä, jos **Salli poistaminen** -valintaruutu on valittu valitun sanoman nykyiselle tilalle.
- **Kerää tietoja** – tämä painike on liitetty **Täytä tietueet** -tyypin toimintoihin.
- **Luo raportti** – tämä painike on liitetty **Sähköisen raportoinnin vientiviesti** -tyypin toimintoihin.
- **Lähetä raportti** – tämä painike on liitetty **Verkkopalvelu**-tyypin toimintoihin.
- **Tuo vastaus** – tämä painike on liitetty **Sähköisen raportoinnin tuonti** -tyypin toimintoihin.
- **Päivitä tila** – tämä painike on liitetty **Viestitason käyttäjän käsittely** -tyypin toimintoihin.
- **Sanoman nimikkeet** – avaa **Sähköisen sanoman nimikkeet** -sivun.

**Toimintoloki**-pikavälilehdessä on tietoja kaikista valitulle sanomalle suoritetuista toiminnoista. Jos toiminto aiheutti virheen, virheen tiedot liitetään liittyvälle ruudukon riville. Voit tarkastella virheen tietoja valitsemalla ensin rivin ruudukosta ja valitsemalla sitten sivun oikeasta yläkulmasta **Liite**-painikkeen (paperiliitinsymboli).

**Sanoman lisäkentät** -pikavälilehdessä on kaikki lisäkentät, jotka on määritetty sanomille käsittelyn määrityksissä. Pikavälilehti sisältää myös kyseisten lisäkenttien arvot.

**Sanoman nimikkeet** -pikavälilehdessä on kaikki valittuun sanomaan liittyvät sanoman nimikkeet. Valitun sanoman nimikkeen tilan perusteella voit suorittaa joitakin toimintoja käyttämällä ruudukon yläpuolella olevia painikkeita:

- **Poista** – Tämä painike on käytettävissä, jos **Salli poistaminen** -valintaruutu on valittu valitun sanoman nykyiselle tilalle.
- **Päivitä tila** – tämä painike on liitetty **Käyttäjän käsittely** -tyypin toimintoihin.
- **Alkuperäinen tiedosto** – Avaa sivun, jossa näkyy valitun sanoman nimikkeen alkuperäinen tiedosto.

Jo luodut ja sanomalle vastaanotetut raportit on liitetty kyseiseen sanomaan. Voit tarkastella sanomaan liittyviä liitteitä valitsemalla ensin sanoman ja valitsemalla sitten sivun oikeasta yläkulmasta **Liite**-painikkeen (paperiliitinsymboli).

![Liitepainike](media/attachment-icon.png)

**Liitteet**-sivulla on kaikki valittuun sanomaan liittyvät liitteet. Voit tarkastella tiedostoa valitsemalla sen vasemmalla olevasta luettelosta ja valitsemalla sitten toimintoruudusta **Avaa**.

![Avaa-painike](media/open-button.png)

Voit tarkastella liitteitä, jotka liittyvät tiettyyn aiemmin sanomalle suoritettuun toimintoon. Valitse sanoma **Sähköiset sanomat** -sivun **Sanomat**-pikavälilehdestä. Valitse toiminto **Toimintoloki**-pikavälilehdestä ja valitse sitten sivun oikeasta yläkulmasta **Liite**-painike (paperiliitinsymboli).

Voit suorittaa koko käsittelyn tai vain tietyn toiminnon valitsemalla toimintoruudusta **Suorita käsittely**.

## <a name="electronic-message-items"></a>Sähköisen sanoman nimikkeet

**Sähköisen sanoman nimikkeet** -sivulla näytetään kaikki sanoman nimikkeet sekä loki kullekin sanoman nimikkeelle suoritetuista toiminnoista. Sivulla näytetään myös sanoman nimikkeille määritetyt lisäkentät sekä kyseisten kenttien arvot.

Seuraavassa taulukossa käsitellään **Sanoman nimikkeet** -välilehden kenttiä.

<table>
<thead>
<tr>
<th>Kenttä</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Käsittely</td>
<td>Sen käsittelyn nimi, jolla sanoman nimike luotiin.</td>
</tr>
<tr>
<td>Sanoman nimike</td>
<td>Sanoman nimikkeen tunnus. Tämä tunnus kohdistetaan automaattisesti <b>Kirjanpitoparametrit</b>-sivulla määritetyn <b>sanoman nimikkeiden</b> numerojärjestyksen perusteella.</td>
</tr>
<tr>
<td>Sanoman nimikkeen päivämäärä</td>
<td>Päivämäärä, jolloin sanoman nimike luotiin.</td>
</tr>
<tr>
<td>Sanoman nimiketyyppi</td>
<td>Sanoman nimiketyyppi. Samaa käsittelyä varten voidaan määrittää useita sanomien nimiketyyppejä. (Niitä ovat esimerkiksi <b>Saapuvat laskut</b> ja <b>Lähtevät laskut</b>). Tämä kenttä voidaan määrittää automaattisesti vain, kun lasku on lisätty Sanoman nimikkeet -taulukkoon.</td>
</tr>
<tr>
<td>Sanoman nimikkeen tila</td>
<td><p>Sanoman nimikkeen varsinainen tila. Käytettävissä olevat tilat vaihtelevat sanoman nimiketyypin mukaan. Seuraavassa on muutamia esimerkkejä:</p>
<ul>
<li><b>Täytetty</b> – tietue lisättiin Sanoman nimikkeet -taulukkoon.</li>
<li><b>Arvioitu</b> – sanoman nimikkeelle laskettiin lisämääritteitä.</li>
<li><b>Raportoitu</b> – sanoman nimikkeen lisääminen raporttiin onnistui.</li>
<li><b>Poissuljettu</b> – Tämä tila voi olla hyödyllinen, jos tietyt sanoman nimikkeet tulisi jättää pois raportista ennen sen vientiä.</li>
</ul>
</td>
</tr>
<tr>
<td>Lähetyspäivämäärä</td>
<td>Sanoman nimikkeen lähetyspäivämäärä, jos käsittely lähettää luodun raportin automaattisesti järjestelmän ulkopuolelle.</td>
</tr>
<tr>
<td>Asiakirjan numero</td>
<td>Tämä kenttä määritetään automaattisesti tietueiden täyttötoiminnon määritysten perusteella. Tämä kenttä voidaan määrittää automaattisesti vain, kun lasku on lisätty Sanoman nimikkeet -taulukkoon.</td>
</tr>
<tr>
<td>Tilinumero</td>
<td>Asiakkaan tai toimittajan tilinumero, tai muun kentän arvo, riippuen kentästä, joka määritettiin tietueiden täyttötoiminnossa. Tämä kenttä voidaan määrittää automaattisesti vain, kun lasku on lisätty Sanoman nimikkeet -taulukkoon.</td>
</tr>
<tr>
<td>Sanoma</td>
<td>Sanoman numero. Tämä numero kohdistetaan automaattisesti <b>Kirjanpitoparametrit</b>-sivulla määritetyn <b>sanomien</b> numerojärjestyksen perusteella.</td>
</tr>
<tr>
<td>Sanoman tila</td>
<td>Sähköisen sanoman varsinainen tila.</td>
</tr>
<tr>
<td>Seuraava toiminto</td>
<td>Seuraava toiminto, joka voidaan käynnistää sanoman nimikkeen nykyiselle tilalle.</td>
</tr>
</tbody>
</table>

**Lisäkentät**-välilehdessä on valitun sanoman nimikkeen lisäkentät ja niiden arvot.

### <a name="run-processing"></a>Suorita käsittely

Suorita sanoman nimikkeiden käsittely valitsemalla toimintaruudusta **Suorita käsittely**. Voit suorittaa tietyn toiminnon valitsemalla **Suorita käsittely** -valintaikkunan **Valitse toiminto** -asetukseksi **Kyllä** ja valitsemalla sitten toiminnon. Voit suorittaa koko käsittelyn jättämällä **Valitse toiminto** -asetukseksi **Ei**.

### <a name="generate-report"></a>Luo raportti

Valitse toimintoruudusta **Luo raportti**. Tämä painike on liitetty **Sähköisen raportoinnin vienti** -tyypin toimintoihin.

### <a name="update-status"></a>Päivitä tila

Päivitä yhden tai useamman sanoman nimikkeen tila valitsemalla toimintoruudusta **Päivitä tila**. Valitse päivitettävät sanoman nimikkeet **Päivitä tila** -valintaikkunan **Sisällytettävät tietueet** -pikavälilehdessä. Varmista, että määrität valintaehdot oikein, koska sanoman nimikkeiden tilat päivitetään näiden ehtojen, valitun toiminnon alkuperäisen tilan ja **Uusi tila** -kentässä määrittämäsi arvon mukaan. Kun tilan päivitys on valmis, päivitettyjä nimikkeitä on vaikea selvittää. Tämän vuoksi tilapäivityksen peruuttaminen on hankalaa.

### <a name="electronic-messages"></a>Sähköiset sanomat

Voit tarkastella valittuun sanoman nimikkeeseen liittyvää sähköistä sanomaa valitsemalla toimintoruudusta **Sähköiset sanomat**.

Voit myös tarkastella tiettyyn sanoman nimikkeeseen liittyviä tiedostoja. Valitse sanoman nimikkeen **Sanoma**-kenttä tai valitse toimintoruudusta **Sähköiset sanomat**. Valitse **Sähköiset sanomat** -sivulta sanoma, jonka tiedostoja haluat tarkastella, ja valitse sitten sivun oikeasta yläkulmasta **Liite**-painike (paperiliitinsymboli).

**Liitteet**-sivu näyttää kaikki sanomaan liittyvät liitteet. Voit tarkastella tiedostoa valitsemalla sen vasemmalla olevasta luettelosta ja valitsemalla sitten **Avaa** toimintoruudussa.

### <a name="original-document"></a>Alkuperäinen tiedosto

Avaa valitun sanoman nimikkeen alkuperäinen tiedosto valitsemalla toimintoruudusta **Alkuperäinen tiedosto**.
