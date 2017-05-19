---
title: "Nimikkeiden ja raaka-aineiden seuranta varastossa, tuotannossa ja myynnissä"
description: "Tässä ohjeaiheessa kuvataan, kuinka voit määrittää nimikkeen seurannan avulla nimikkeiden ja raaka-aineiden aiemman, nykyisen ja tulevan käyttöpaikan tuotanto- ja myyntiprosesseissa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: b6c7158a4d0f941bf564c107bfb2560de6a09570
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Nimikkeiden ja raaka-aineiden seuranta varastossa, tuotannossa ja myynnissä

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kuvataan, kuinka voit määrittää nimikkeen seurannan avulla nimikkeiden ja raaka-aineiden aiemman, nykyisen ja tulevan käyttöpaikan tuotanto- ja myyntiprosesseissa. 

Nimikkeen seurantatoiminto on käytössä **Nimikkeen seuranta** -sivulla. Seuraavissa osissa kuvataan, kuinka nimikkeen seurantaa käytetään ja mitä asetuksia ja rajoituksia siihen liittyy.

## <a name="what-is-item-tracing"></a>Mitä on nimikkeen seuranta?
Nimikkeen seuranta on liiketoimintatyökalu, joka tarjoaa näkyvyyttä toimitusketjun nimikkeiden ja raaka-aineiden lähteeseen ja kohteeseen. Valmistajat voivat jäljittää nimikkeet, raaka-aineet tai ainesosat takaisin toimittajaan ja eteenpäin tuotannon ja valmiin tuotteen myynnin kautta. Nimikkeen seuranta auttaa valmistajia noudattamaan säädösten mukaisia vaatimuksia. Lisäksi se auttaa laadunvalvojia sekä tuotantopäällikköjä analysoimaan tuotteiden ja materiaalien laadun vaihtelua ja toimimaan tulosten perusteella. Seuraavassa on esimerkkejä tavoista, joilla valmistajat voivat käyttää nimikkeen seurantaa:

-   Määritä nimike tai raaka-aine, joka on varastossa ja missä sitä säilytetään.
-   Määritä lähetettyjen nimikkeiden tai raaka-aineiden määrä ja asiakkaat, joille nimikkeet on lähetetty..
-   Määritä suunnitellut toimitukset, jotka sisältävät nimikkeen tai raaka-aineen.
-   Etsi nimikettä tai raaka-ainetta käyttävät tuotantotilaukset, jotka on suunniteltu, käynnissä tai ilmoitettu valmiiksi.
-   Katso mistä nimike tai raaka-aine on ostettu.
-   Tarkista, missä nimike tai raaka-aineet kulutetaan toisen nimikkeen tuotannossa.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Mitä voin seurata, ja onko tähän rajoituksia?
Voit seurata nimikkeiden ja raaka-aineiden historiallisia varastotapahtumia perustuen nimiketunnukseen ja seurantadimensioon, kuten sarjanumero, eränumero tai toimittajan eränumero. Nimikettä tai raaka-ainetta voi seurata vain, jos sille on määritetty seurantadimensio. Seuranta perustuu varastotapahtumiin, joten nimikkeiden seurantaan liittyy joitakin rajoituksia. Rajoituksia liittyy esimerkiksi projektien, käyttöomaisuuden ja vähittäismyynnin tapahtumiin. Lisäksi seurannan tiedoissa näytetään oheistuotteet, mutta ei sivutuotteita. Seuranta sisältää kaikki varastotapahtumat paikasta toiseen. Tästä syystä käyttäjät voivat pitää tietomäärää liian suurena. Kerrallaan näkyy vain yhden yrityksen seuranta. Konsernin sisäisessä kontekstissa ei ole yritystenvälisiä toimintoja. Uusi seuranta on käynnistettävä jokaiselle yritykselle, jossa nimike vastaanotetaan tai otetaan varastosta.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Mitä kriteereitä voin määritellä nimikeseurannalle?
Nimikkeen seurantaan vaadittavat tiedot ovat nimiketunnus, seurantadimensio (kuten eränumero tai sarjanumero) sekä suunta. Seuraavassa taulukossa kuvataan ehdot, joita voit käyttää nimikkeen seurannassa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kenttäryhmä</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nimiketunnus</td>
<td>Kirjoita tunniste seuraamallesi nimikkeelle tai raaka-aineelle.</td>
</tr>
<tr class="even">
<td>Tuotedimensiot</td>
<td>Valinnainen: Jäljitä tuotteen määritelmän tiettyjä näkökohtia, esimerkiksi konfiguraatio, koko, väri tai tyyli.</td>
</tr>
<tr class="odd">
<td>Seurantadimensiot</td>
<td>Kirjoita eränumero, toimittajan eränumero tai sarjanumeron seurantadimensio. Kun käytät ehtona eränumeroa, toimittajan eränumero tulee näyttöön, jos olet tallentanut sen tiedon.</td>
</tr>
<tr class="even">
<td>Varastodimensiot</td>
<td>Valinnainen: Jäljitä nimikkeitä, jotka on tallennettu tietyssä paikassa.</td>
</tr>
<tr class="odd">
<td>Kausi</td>
<td>Valinnainen: Kirjoita päivämäärät rajoittaaksesi jäljityksen tiettyyn kauteen. Seurantatiedot näytetään vain sellaisille asiakirjoille ja tapahtumille, jotka on luotu näiden päivämäärien välillä.</td>
</tr>
<tr class="even">
<td>Eteen- tai taaksepäin</td>
<td>Valitse jäljityssuunta. Voit seurata eteenpäin tai taaksepäin:
<ul>
<li><strong>Taaksepäin</strong> – Seuranta tapahtuu taaksepäin, jotta voidaan määrittää lähde, käytettävissä oleva määrä sekä sellaiset tuotantotilaukset, jotka on ilmoitettu vähintään osittain valmiiksi.</li>
<li><strong>Eteenpäin</strong> – Seuranta tapahtuu eteenpäin, jotta kohde voidaan määrittää. Voit etsiä myyntitilauksia ja asiakkaita, joille seurattua nimikettä tai raaka-ainetta on ainakin osittain toimitettu.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>Mitä tietoja sisällytetään seurantatietoihin?
Seurannan tulokset näkyvät puurakenteessa kronologisessa järjestyksessä **Nimikkeen seuranta** lomakkeen **Tiedot**-pikavälilehdessä. Järjestys vaihtelee seurannan suunnasta riippuen. Tiedot sisältävät kaikki tapahtumat nimikkeen ostamisesta toimittajalta nimikkeen myyntiin asiakkaalle. Jäljityksen tulokset sisältävät myös väliaikaiset tuotteet, jotka liittyvät nimikkeeseen tai seurantaehdoissa määriteltyyn seurantadimensioon. Ylin solmu näyttää nimikkeen määrän varastoyksikössä, joka on käytettävissä. Näkymä perustuu varastodimensioihin, jotka määritettiin seurantaehdossa. **Huomautus:** Seurantatiedot ovat tilannevedos tiedoista, jotka olivat käytettävissä seurannan suorituksen aikana. Seurantatietoja ei päivitetä, jos tiedot muuttuivat seurannan suorittamisen jälkeen.

## <a name="why-dont-some-nodes-contain-any-details"></a>Miksi joidenkin solmujen sisällä ei ole mitään tietoja?
Seurantatiedoissa näkyvien tietojen määrän vähentämiseksi tiedot näkyvät vain nimikkeen tai raaka-aineen solmun ensimmäisessä näyttökerrassa. Jos valitussa solmussa ei ole tietoja, voit tarkastella solmua, jossa tietoja on. Valitse tällöin **Siirry seuratulle riville**. Voit palata lähtösolmuun valitsemalla **Palaa**.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Voinko tarkastella luetteloa kaikista tietyn tyyppisten asiakirjoista? Voinko esimerkiksi tarkastella vain tuotantotilauksia, asiakkaita tai toimittajia?
Kyllä, seurannan tiedoista voit avata luettelosivut, jotka sisältävät vain tietyntyyppisen tiedoston tai tapahtuman. Voit avata sivut toimintoruudun **Seuranta**-valikkovaihtoehdon **Nimike**-, **Myynti**-, **Osto**-, **Tuotanto**- ja **Laatu** -ryhmissä. Jos esimerkiksi haluat tarkastella seurantatiedoissa toimittajaluetteloa, valitse **Seuranta** &gt; **Osto** &gt; **Toimittajat**. Luettelosivut näyttävät yhteenvedon asiakirjoista tai seurantatietojen tapahtumista. **Odottavat tapahtumat**-, **Odottavat tilaukset**- ja **Myyntitilaukset, joita ei ole lähetetty** -luettelosivuilla näkyvät myös tietoja, joita ei ole sisällytetty seurantatietoihin. Lisäksi ne näyttävät aina tulokset nykyisestä päivämäärästä alkaen vaikka päivämääräväli olisi asetettu. Seuraavassa taulukossa kuvataan lisätiedot, joita nämä sivut voivat sisältää.

| Luettelot                    | Kuvaus                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Myyntitilaukset, joita ei ole lähetetty | Näytä myyntitilausrivit, joita ei ole keräilty ja joita ei siten näytetä seurantatiedoissa.                                                                                                                                                                                                                        |
| Odottavat tilaukset           | Näytä kaikki odottavat seuratun nimikkeen tuotantotilaukset riippumatta seurantaehdoissa määritellyistä seurantadimensioista. Voit myös tarkastella odottavia tuotantotilauksia, joissa seurattu nimike on ainesosa, ja joissa rekisteröintiä ei ole tehty eikä tapahtumia ole ilmoitettu valmiiksi tilaukselle. |
| Odottavat tapahtumat     | Näytä odottavat seuratun nimikkeen tuotantotilaukset mukaan lukien määritellyt seurantadimensiot tai tyhjän seurantadimension. Voit myös tarkastella nimikkeiden odottavien varastotapahtumien ja seurantadimensioiden yhdistelmiä tai tyhjäarvoa jäljitystiedoissa.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Miten monta tasoa voin seurata ylös tai alas tuoterakenteessa tai kaavassa?
Voit seurata yhden tason ylös tai alas tuoterakenteissa tai kaavassa. Esimerkiksi jos suoritat raaka-aineiden seurannan, näet lopputuotteen ja kaikki oheistuotteet. Jos seuraat oheistuotetta, seurantatiedot eivät sisällä lopputuotetta.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Miten tarkastella tarkempia tietoja tiedostosta tai tapahtumasta tietojen jäljityksessä?
**Tiedot**-pikavälilehdessä voit tarkastella lisätietoja seurantatiedoissa valitusta asiakirjasta tai tapahtumasta kahdella eri tavalla:

-   Kun valitset seurantatiedoista solmun **Tiedot**-pikavälilehdessä, muut sivun pikavälilehdet näyttävät asiakirjan tai tapahtuman tiedot solmussa.
-   Voit avata asiakirjan tietosivun valitussa solmussa valitsemalla **Näytä tiedot**. Jos esimerkiksi valitset solmun, joka kuvaa tuotantotilausta, ja valitset **Näytä tiedot**, näkyviin tulee **Tuotantotilauksen tiedot** -sivu.

Eräät pikavälilehdet sisältävät lisätietoja valitusta solmusta. Esimerkiksi **Määrityksistä poikkeamiset** -pikavälilehdessä voit tarkastella määrityksistä poikkeamisten historiatietoja valitsemalla **Kyselyt**. **Erä** -pikavälilehdessä voit **Varastoluettelo**-kohtaa napsauttamalla tarkastella käytettävissä olevan varaston määrää ja erään liittyviä varastotapahtumia.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Voinko suorittaa useita seurantoja ja verrata tietoja?
Kun olet suorittanut seurannan, voit suorittaa tapahtumalle uuden seurannan valitussa solmussa napsauttamalla **Seuraa solmusta** -painiketta ja valitsemalla haluamasi vaihtoehdon:

-   **Taaksepäin** tai **Eteenpäin** – Aloita valitun solmun uusi seuranta ja korvaa nykyisen seurannan tiedot.
-   **Uusi taaksepäin** tai **Uusi eteenpäin** – Aloita uusi seuranta uudessa ikkunassa ja säilytä nykyisen seurannan tiedot.

Jos haluat käyttää **Uusi taaksepäin**- tai **Uusi eteenpäin** -vaihtoehtoa, on käytettävä **Avaa uudessa ikkunassa** -toimintoa, jotta uusi seuranta näkyisi uudessa ikkunassa.

## <a name="can-i-save-the-trace-details"></a>Voinko tallentaa jäljitystiedot?
Voit tallentaa **Tiedot**-välilehden tiedot XML-tiedostoksi valitsemalla **Vie** toimintoruudun ****Seuranta**** -toiminnon alla. Seurantatietojen lisäksi XML-tiedosto sisältää seurantaehdot, ylätason solmun ja käytettävissä olevan määrän. Seurannan tietojen tallentamisesta on hyötyä esimerkiksi siinä tapauksessa, että haluat liittää tiedot laatutilaukseen tai muihin yhteensopivuusasiakirjoihin. Voit määrittää tiedoston tallennussijainnin. Voit tarkastella tiedostoa saman tien valitsemalla **Näytä tiedosto** -vaihtoehdon. **Huomautus:** Tiedosto tallennetaan aina, vaikka haluat vain tarkastella sitä. Oletusarvon mukaan XML-tiedosto avataan selaimen ikkunaan. Voit kuitenkin napsauttaa tiedostoa hiiren kakkospainikkeella, valitsemalla **Avaa sovelluksessa** ja valitsemalla sitten sisällön näyttämiseen käytettävän ohjelman.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Voinko laskea tietyn nimikkeen tai ainesosan saldon?
Voit viedä yhteenvetosivujen tiedot Microsoft Exceliin. Avaa haluamasi sivu napsauttamalla **Avaa Microsoft Officessa** -kuvaketta ja valitsemalla sitten **Vie Exceliin**. Tämä toiminto on erityisen hyödyllinen silloin, jos haluat laskea laajamittainen saldon nimikkeelle tai ainesosalle **Tapahtumien yhteenveto** -sivulla. **Tapahtumien yhteenveto** -sivulla voit suodattaa tiedot nimikkeen tai ainesosan ja halutessasi erän perusteella ja viedä tiedot sitten Exceliin. Excelissä voit esimerkiksi erotella käytettävissä olevan määrän, myydyn määrän ja tuotannossa käytetyn summan.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Voinko tutkia, onko nimikkeissä tai raaka-aineissa ollut aiemmin ongelmia?
Seurantatiedot sisältävät tietoja laatutilauksista ja määrityksistä poikkeamisista, jotka liittyvät nimikkeeseen tai raaka-aineeseen. Voit tarkastella yhteenvetoa laatutilauksista ja määrityksistä poikkeamisista valitsemalla toimintoruudussa **Laatutilaukset** tai **Määrityksistä poikkeamiset**. **Huomautus:** Destruktiivisia laatutilauksia voi esiintyä useammin kuin kerran seurantatiedoissa. Kun asiakirjalle luodaan destruktiivinen laatutilaus, kuten ostotilaus, se näkyy kullekin kyseisen asiakirjan tapahtumalle.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Liittyykö nimikkeen seurantaan raportointiominaisuuksia?
Voit luoda **Lähetetty asiakkaille** -raportin, jossa määritetään lähetetty nimike- tai raaka-ainemäärä sekä asiakkaat, joille ne on toimitettu. Yhteensopivuuteen liittyvälle kyselylle voit luoda raportin kaikille asiakkaille. Asiakaspalveluun liittyvälle kyselylle voit luoda raportin valitulle asiakkaalle. Jos tuote on raaka-aine, jota on käytetty valmiin nimikkeen tuotannossa, valmis nimike sisällytetään myös. **Huomautus:** Jos käytät ominaisuuksia toimintojen poistamista ja myyntitilausten arkistointia varten, raportin tuloksiin sisältyvät myös myyntitilaukset, jotka on poistettu tai arkistoitu.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Voinko jäljittää oheistuotteita ja sivutuotteita?
Voit seurata rinnakkaistuotteita, mutta et voi seurata sivutuotteita, koska niihin ei ole tavallisesti liitetty seurantadimensioita. Kun seuraat nimikettä, seurantatietoihin sisältyvät kaikki liittyvät oheistuotteet. Solmun, joka sisältää rinnakkaistuotteen lisätiedoissa on sana "rinnakkaistuote". Voit tarkastella tietoja oheistuotteesta myös valitsemalla seurantatietojen solmun ja napsauttamalla sitten **Tuotanto**-pikavälilehteä.




