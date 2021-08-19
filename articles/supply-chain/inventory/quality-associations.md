---
title: Laatuliitokset
description: Tässä aiheessa kuvataan, kuinka voit käyttää laatuliitoksia Microsoft Dynamics 365 Supply Chain Managementissa luodaksesi automaattisesti myynti-, osto- ja tuotantoprosesseihin liittyviä laatutilauksia.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0705af8f8c40db82e412f294f45f704b7a628c1ced679cef25ce77d49642feb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724841"
---
# <a name="quality-associations"></a>Laatuliitokset

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka voit käyttää laatuliitoksia Microsoft Dynamics 365 Supply Chain Managementissa luodaksesi automaattisesti myynti-, osto- ja tuotantoprosesseihin liittyviä laatutilauksia.

Laatuliitos määrittää kaikki seuraavat muodostettavan laatutilauksen tiedot:

- Tapahtuma
- Nimikkeissä suoritettavat testit
- Hyväksyttävän laadun taso (AQL)
- Otantasuunnitelma

Laatuliitos on määritettävä kutakin sellaista liiketoimintaprosessin muutosta varten, joka edellyttää automaattista laatutilausten luontia. Laatutilaus voidaan esimerkiksi muodostaa ostotilausten, karanteenitilausten, myyntitilausten ja tuotantotilausten liiketoimintaprosesseille.

## <a name="working-with-quality-associations"></a>Laatuliitosten käsitteleminen

Laatuliitosta käyttävä liiketoimintoprosessi voidaan liittää eri lähdeasiakirjoihin, kuten ostotilauksiin, myyntitilauksiin tai tuotantotilauksiin.

Jokaisessa laatuliitostietueessa määritetään joukko testejä, hyväksyttävän laadun taso ja otantasuunnitelma, jota käytetään muodostettavissa laatutilauksissa. Laatuliitostietue on määritettävä liiketoimintaprosessin jokaiselle muunnokselle. Voit esimerkiksi määrittää laatuliitoksen, joka muodostaa laatutilauksen, kun ostotilauksen tuotteen vastaanotto päivitetään. Toimeenpanosuunnitelman asetusten mukaan itse käynnistysprosessi voidaan estää avoimen laatutilauksen yhteydessä. Vaihtoehtoisesti seuraavat prosessit, kuten ostotilauksen laskutus, voidaan estää.

> [!NOTE]
> Jos laatutilauksia on avoinna, varastomäärien otto estetään automaattisesti. **Nimikeotanta**-sivun **Täysi esto** -kentän mukaan laatu on joko laatutilauksen määrä tai lähdeasiakirjan rivin määrä. Lisätietoja on kohdassa [Laadunhallinnan nimikeotanta](quality-item-sampling.md).

Tietyn liiketoimintaprosessin laatuliitostietue tunnistaa tapahtuman ja ehdot, joille laatutilaus muodostetaan. Ehdot voivat olla joko toimipaikka- tai yrityskohtaisia. Tuhoavia testejä sisältävä laatutilaus voidaan muodostaa vain, kun tapahtumalla on käytettävissä oleva varasto.

Voit käyttää laatuliitoksia valitsemalla **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laatuliitokset**. Seuraavassa esimerkeissä käsitellään, miten laatuliitostietue määritetään kunkin liiketoimintaprosessin variaatioille. Seuraavassa taulussa on jokaisen esimerkin yhteenveto laatuliitostietueessa määritetyistä tapahtumista ja ehdoista.

<table>
<thead>
<tr>
<th>Viitetyyppi</th>
<th>Tapahtumatyyppi</th>
<th>Suoritus</th>
<th>Tapahtuman esto</th>
<th>Tiedostoviite</th>
</tr>
</thead>
<tbody>
<tr>
<td>Varasto</td>
<td>Ei käytettävissä</td>
<td>Ei käytettävissä</td>
<td>Ei mitään</td>
<td>Kaikki</td>
</tr>
<tr>
<td rowspan="7">Myynti</td>
<td rowspan="4">Keräysprosessi on ajoitettu</td>
<td rowspan="4">Ennen</td>
<td>Ei mitään</td>
<td rowspan="22">Tietty tunnus, ryhmä tai vain kaikki</td>
</tr>
<tr>
<td>Keräysprosessi</td>
</tr>
<tr>
<td>Pakkausluettelo</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="3">Pakkausluettelo</td>
<td rowspan="3">Ennen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Pakkausluettelo</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="15">Osto</td>
<td rowspan="7">Vastaanottoluettelo</td>
<td rowspan="4">Ennen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Vastaanottoluettelo</td>
</tr>
<tr>
<td>Tuotteen vastaanotto</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="3">Jälkeen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Tuotteen vastaanotto</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="3">Rekisteröinti</td>
<td rowspan="3">Ei käytettävissä</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Tuotteen vastaanotto</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="5">Tuotteen vastaanotto</td>
<td rowspan="3">Ennen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Tuotteen vastaanotto</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="2">Jälkeen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Lasku</td>
</tr>
<tr>
<td rowspan="8">Tuotanto</td>
<td rowspan="3">Rekisteröinti</td>
<td rowspan="3">Ei käytettävissä</td>
<td>Ei mitään</td>
<td rowspan="12">Kaikki</td>
</tr>
<tr>
<td>Ilmoita valmiiksi</td>
</tr>
<tr>
<td>Lopeta</td>
</tr>
<tr>
<td rowspan="5">Ilmoita valmiiksi</td>
<td rowspan="3">Ennen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Ilmoita valmiiksi</td>
</tr>
<tr>
<td>Lopeta</td>
</tr>
<tr>
<td rowspan="2">Jälkeen</td>
<td>Ei mitään</td>
</tr>
<tr>
<td>Lopeta</td>
</tr>
<tr>
<td rowspan="4">Karanteeni</td>
<td rowspan="3">Ilmoita valmiiksi</td>
<td rowspan="2">Ennen</td>
<td>Ilmoita valmiiksi</td>
</tr>
<tr>
<td>Lopeta</td>
</tr>
<tr>
<td>Jälkeen</td>
<td>Lopeta</td>
</tr>
<tr>
<td>Lopeta</td>
<td>Ennen</td>
<td>Lopeta</td>
</tr>
<tr>
<td rowspan="3">Reitityksen työvaihe</td>
<td rowspan="3">Ilmoita valmiiksi</td>
<td rowspan="2">Ennen</td>
<td>None</td>
<td rowspan="3">Tietty tunnus, ryhmä tai kaikki tai tietty resurssi, ryhmä tai kaikki</td>
</tr>
<tr>
<td>Ilmoita valmiiksi</td>
</tr>
<tr>
<td>Jälkeen</td>
<td>None</td>
</tr>
<tr>
<td rowspan="3">Oheistuotteen tuotanto</td>
<td>Rekisteröinti</td>
<td>Ei käytettävissä</td>
<td rowspan="3">None</td>
<td rowspan="3">Kaikki</td>
</tr>
<tr>
<td rowspan="2">Ilmoita valmiiksi</td>
<td>Ennen</td>
</tr>
<tr>
<td>Jälkeen</td>
</tr>
</tbody>
</table>

> [!NOTE]
> *Varastoprosessien laadunhallinta* -ominaisuus lisää laatutilausten käsittelytoiminnot tuotannoille, joiden **Tapahtumatyyppi**-kentän arvona on *Ilmoita valmiiksi* ja **Suoritus**-kenttä on määritetty arvoon *Jälkeen*, sekä ostoille, joiden **Tapahtumatyyppi**-kentän arvona on *Rekisteröinti*. Lisätietoja on kohdassa [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md).

Seuraavassa taulussa on lisätietoja laatutilausten muodostamisesta tietyntyyppisille prosesseille.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Prosessin tyyppi</th>
<th>Laatutilausten automaattinen luontiajankohta</th>
<th>Laatutilausten luontiajankohta, jos tuhoava testaus pakollinen</th>
<th>Ehdon tiedot</th>
<th>Manuaalisen luonnin tiedot</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ostotilaus</td>
<td>Ennen kuin vastaanotetun materiaalin vastaanottoluettelo tai tuotteen vastaanotto on kirjattu tai sen jälkeen</td>
<td>Vastaanotetun materiaalin tuotteen vastaanoton kirjauksen jälkeen, koska materiaalin on oltava käytettävissä tuhoavaa testausta varten</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu ostotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Karanteenitilaus</td>
<td>Ennen karanteenitilauksen ilmoittamista valmiiksi tai päättyneeksi tai sen jälkeen</td>
<td>Tuhoavia testejä edellyttäviä laatutilauksia ei voi luoda. Karanteenitilaustoiminnon oletetaan käsittelevän tuhottavan materiaalin käsittelyn.</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai toimittajaan tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu ostotilaukseen viittaava karanteenitilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Myyntitilaus</td>
<td>Ennen lähettävien nimikkeiden ajoitettua keräysprosessia tai pakkausluettelon päivitystä</td>
<td>Kaikissa vaiheissa</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai asiakkaaseen tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu myyntitilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Tuotantotilaus</td>
<td>Ennen tuotantotilauksen valmiiksi raportointia tai sen jälkeen</td>
<td>Tuotantotilauksen valmiiksi raportoinnin jälkeen</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan tai nimikkeeseen tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu tuotantotilaukseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Tuotantotilaus, jossa on reitityksen työvaihe</td>
<td>Ennen työvaiheen raportin valmistumista tai sen jälkeen</td>
<td>Viimeisen työvaiheen tuotannon valmiiksi raportoinnin jälkeen</td>
<td>Laatutilausvaatimus voi liittyä toimipaikkaan, nimikkeeseen tai operatiiviseen resurssiin tai näiden ehtojen yhdistelmään.</td>
<td>Manuaalisesti luotu reitityksen työvaiheeseen viittaava laatutilaus voi käyttää laatuliitostietueen tietoja, kuten testin otantasuunnitelmaa.</td>
</tr>
<tr>
<td>Varasto</td>
<td>Laatutilausta ei voi luoda automaattisesti varastokirjauskansion tapahtumalle eikä siirtotilaustapahtumille.</td>
<td></td>
<td></td>
<td>Laatutilaus on luotava manuaalisesti nimikkeen varastomäärälle. Fyysistä käytettävissä olevaa varastoa edellytetään.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Esimerkkejä laatutilausten automaattisesta luomisesta

### <a name="purchasing"></a>Osto

Jos asetat ostoissa **Tapahtumatyyppi**-kentän arvoksi *Tuotteen vastaanotto* ja **Suoritus**-kentän arvoksi *Jälkeen* **Laatuliitokset**-sivulla, saat seuraavat tulokset:

- Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään *Kyllä*, laatutilaus luodaan jokaista vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä sekä nimikeotannan asetukset. Joka kerta, kun määrä vastaanotetaan ostotilauksen perusteella, luodaaan uusia laatutilauksia juuri saadun määrän perusteella.
- Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään *Ei*, laatutilaus luodaan ensimmäistä vastaanottoa varten ostotilauksen perusteella, jolloin otetaan huomioon vastaanotettu määrä. Lisäksi jäljelle jäävän määrän perusteella luodaan seurantadimensioiden mukaan vähintään yksi laatutilaus. Laatutilauksia ei luoda ostotilauksen perusteella seuraavien vastaanottojen osalta.

### <a name="production"></a>Tuotantoympäristö

Jos asetat tuotannossa **Tapahtumatyyppi**-kentän arvoksi *Ilmoita valmiiksi* ja **Suoritus**-kentän arvoksi *Jälkeen* **Laatuliitokset**-sivulla, saat seuraavat tulokset:

- Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään *Kyllä*, laatutilaus luodaan jokaisen valmiin määrän ja nimikeotannan asetusten perusteella. Joka kerta, kun määrä ilmoitetaan valmiiksi tuotantotilauksen perusteella, luodaaan uusia laatutilauksia juuri valmiiksi saadun määrän perusteella. Tämä luontilogiikka on yhdenmukainen oston kanssa.
- Jos **Päivitettyä määrää kohden** -asetuksen arvoksi määritetään *Ei*, laatutilaus luodaan valmiiksi saadun määrän perusteella ensimmäisellä kerralla, kun määrä ilmoitetaan valmiiksi. Lisäksi jäljelle jäävän määrän perusteella luodaan nimikeotannan seurantadimensioiden mukaan vähintään yksi laatutilaus. Seuraaville valmiille määrille ei luoda laatutilauksia.

<table>
<thead>
<tr>
<th>Laatumääritys</th>
<th>Päivitettyä määrää kohden</th>
<th>Seurantadimension mukaan</th>
<th>Tulos</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prosenttiosuus: 10 %</td>
<td>Kyllä</td>
<td>
<p>Eränumero: Ei</p>
<p>Sarjanumero: Ei</p>
</td>
<td>
<p>Tilausmäärä: 100</p>
<ol>
<li>Ilmoita valmiiksi 30:n osalta
<ul>
<li>Laatutilaus 1 määrälle 3 (10 prosenttia 30:stä)</li>
</ul>
</li>
<li>Ilmoita valmiiksi 70:n osalta
<ul>
<li>Laatutilaus 2 määrälle 7 (10 % jäljellä olevasta tilausmäärästä eli 70:stä)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Kiinteä määrä: 1</td>
<td>Nro</td>
<td>
<p>Eränumero: Ei</p>
<p>Sarjanumero: Ei</p>
</td>
<td>Tilausmäärä: 100
<ol>
<li>Ilmoita valmiiksi 30:n osalta
<ul>
<li>Laatutilaus 1 määrälle 1 (ensimmäiselle valmiiksi ilmoitetulle määrälle, jolla on kiinteä arvo 1)</li>
<li>Laatutilaus 2 määrälle 1 (jäljelle olevalle määrälle, jolla on edelleen kiinteä arvo 1)</li>
</ul>
</li>
<li>Ilmoita valmiiksi 10:n osalta
<ul>
<li>Laatutilauksia ei luota.</li>
</ul>
</li>
<li>Ilmoita valmiiksi 60:n osalta
<ul>
<li>Laatutilauksia ei luota.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Kiinteä määrä: 1</td>
<td>Kyllä</td>
<td>
<p>Eränumero: Kyllä</p>
<p>Sarjanumero: Kyllä</p>
</td>
<td>
<p>Tilausmäärä: 10</p>
<ol>
<li>Ilmoita valmiiksi 3:n osalta: 1 eränumerolle b1, sarjanumero s1; 1 eränumerolle b2, sarjanumero s2; ja 1 eränumerolle b3, sarjanumero s3
<ul>
<li>Laatutilaus 1 määrälle 1 eränumerosta b1, sarjanumero s1</li>
<li>Laatutilaus 2 määrälle 1 eränumerosta b2, sarjanumero s2</li>
<li>Laatutilaus 3 määrälle 1 eränumerosta b3, sarjanumero s3</li>
</ul>
</li>
<li>Ilmoita valmiiksi 2:n osalta: 1 eränumerolle b4, sarjanumero s4; ja 1 eränumerolle b5, sarjanumero s5
<ul>
<li>Laatutilaus 4 määrälle 1 eränumerosta b4, sarjanumero s4</li>
<li>Laatutilaus 5 määrälle 1 eränumerosta b5, sarjanumero s5</li>
</ul>
</li>
</ol>
<p><strong>Huomautus:</strong> Erää voidaan käyttää uudelleen.</p>
</td>
</tr>
<tr>
<td>Kiinteä määrä: 2</td>
<td>Nro</td>
<td>
<p>Eränumero: Kyllä</p>
<p>Sarjanumero: Kyllä</p>
</td>
<td>
<p>Tilausmäärä: 10</p>
<ol>
<li>Ilmoita valmiiksi 4:n osalta: 1 eränumerolle b1, sarjanumero s1; 1 eränumerolle b2, sarjanumero s2; 1 eränumerolle b3, sarjanumero s3; ja 1 eränumerolle b4, sarjanumero s4
<ul>
<li>Laatutilaus 1 määrälle 1 eränumerosta b1, sarjanumero s1</li>
<li>Laatutilaus 2 määrälle 1 eränumerosta b2, sarjanumero s2</li>
<li>Laatutilaus 3 määrälle 1 eränumerosta b3, sarjanumero s3</li>
<li>Laatutilaus 4 määrälle 1 eränumerosta b4, sarjanumero s4</li>
</ul>
<ul>
<li>Laatutilaus 5 määrälle 2 ilman viittausta erä- ja sarjanumeroon</li>
</ul>
</li>
<li>Ilmoita valmiiksi 6:n osalta: 1 eränumerolle b5, sarjanumero s5; 1 eränumerolle b6, sarjanumero s6; 1 eränumerolle b7, sarjanumero s7; 1 eränumerolle b8, sarjanumero s8; 1 eränumerolle b9, sarjanumero s9; ja 1 eränumerolle b10, sarjanumero s10
<ul>
<li>Laatutilauksia ei luota.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallintaprosessit](quality-management-processes.md)
- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](enable-quality-management.md)
- [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
