---
title: "Eliminointisäännöt"
description: "Tässä artikkelissa on tietoja eliminointisäännöistä ja eliminointien eri vaihtoehdoista."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 882b8f21be94b8cbb0c162c965ffc129b47d7edf
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="elimination-rules"></a>Eliminointisäännöt

[!INCLUDE [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja eliminointisäännöistä ja eliminointien eri vaihtoehdoista.

Eliminointitapahtumia tarvitaan, kun emoyritys suorittaa liiketoimia vähintään yhden tytäryhtiön kanssa ja käyttää konsolidoituja raportteja. Konsolidoiduissa raporteissa voi olla vain konsolidointiorganisaation ja kyseisten organisaatioiden muiden ulkopuolisten entiteettien välisiä tapahtumia. Tämän vuoksi samaan organisaatioon kuuluvien yritysten välillä tapahtuvat tapahtumat on poistettava tai eliminoitava kirjanpidosta, jotta ne eivät näy raporteissa. Eliminoinnin voi tehdä useilla eri tavoilla.

-   Eliminointisääntö voidaan luoda ja käsitellä konsolidointi- tai eliminointiyrityksessä.
-   Talousraportoinnin avulla voidaan näyttää tietyn rivin tai sarakkeen eliminoinnin tilit ja dimensiot.
-   Eliminointien seuraamisessa käytettävien manuaalisten tapahtumakirjausten kirjaamisessa voidaan käyttää erillistä yritystä.

Tässä ohjeaiheessa keskitytään konsolidointi- tai eliminointiyrityksessä käsiteltäviin eliminointisääntöihin. Määrittämällä eliminointisääntöjä voit luoda eliminointitapahtumia yritykseen, joka on määritetty eliminointien kohdeyritykseksi. Kohdetyritys tunnetaan nimellä eliminointiyritys. Eliminointikirjauskansioita voi muodostaa joko konsolidoinnin aikana tai eliminointikirjauskansion ehdotuksen avulla. Tutustu seuraaviin termeihin, ennen kuin määrität eliminointisääntöjä:

-   **Lähdeyritys** – Yritys, johon eliminoitavat summat kirjataan.
-   **Kohdeyritys** – Yritys, johon eliminointisäännöt kirjataan.
-   **Eliminoinnin kohdeyritys** – Yritys, joka määritetään eliminointien kohdeyritykseksi.
-   **Konsolidoitu yritys** – Yritys, joka luodaan ilmoittamaan taloudelliset tulokset yritysten ryhmälle. Yritysten taloushallinnon tiedot konsolidoidaan tähän yritykseen, ja raportti luodaan yhdistettyjen tietojen perusteella.

Seuraavassa taulukossa on esitetty tapahtumatyypit, jotka on ehkä eliminoitava.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tapahtumatyyppi</th>
<th>Esimerkki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Myyntitilausten käsittely ja laskutus (keskitetty käsittely)</td>
<td>Myyt tuotteen asiakkaalle toisen organisaatiosi yrityksen puolesta.</td>
</tr>
<tr class="even">
<td>Myyntitilauksen käsittely (konserniyritysten välinen / yrityksen sisäinen) ja laskutus</td>
<td>Myyt tuotteet yritysten välillä organisaatiossasi.</td>
</tr>
<tr class="odd">
<td>Ostotilaukset (keskitetty käsittely)</td>
<td>Ostat varastoa, toimituksia, palveluita, käyttöomaisuuseriä ja muita tuotteita toimittajalta toisen organisaatiosi yrityksen puolesta.</td>
</tr>
<tr class="even">
<td>Varastonhallinta (konserniyritysten välinen / yrityksen sisäinen)</td>
<td><ul>
<li>Siirrät yhden yrityksen varaston toisen yrityksen käyttöomaisuuteen organisaatiossasi.</li>
<li>Siirrät yhden yrityksen varaston toisen yrityksen varastoon organisaatiossasi.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kuljetettavan varaston seuranta</td>
<td>Siirrät nimikkeitä varastojen välillä samassa yrityksessä mutta maantieteellisesti eri toimipaikoissa.</td>
</tr>
<tr class="even">
<td>Ostoreskontran keskitetty laskujen käsittely</td>
<td>Tallennat laskun toisen organisaatiosi yrityksen puolesta.</td>
</tr>
<tr class="odd">
<td>Ostoreskontran keskitetty maksujen käsittely</td>
<td>Voit maksaa laskun toisen organisaatiosi yrityksen puolesta.</td>
</tr>
<tr class="even">
<td>Kassanhallinta / rahasto (keskitetty käsittely)</td>
<td><ul>
<li>Käsittelet maksetut verot, veronpalautukset, korkokulut, lainat, ennakot, osinkomaksut ja ennalta maksetut palkkiot tai provisiot.</li>
<li>Voit maksaa kulun toisen organisaatiosi yrityksen puolesta. Lasku syötetään kohdeyrityksen kirjoihin, ja sinun on suoritettava yritysten välinen selvitys. Esimerkiksi yksi yritys maksaa toisessa yrityksessä olevan työntekijän kuluraportin. Tässä tapauksessa työntekijän kuluraportissa on kuluja, jotka liittyvät toiseen yritykseen.</li>
<li>Siirrät käteisvaroja yhdestä yrityksestä toiseen organisaatiossasi.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Myyntireskontra (keskitetty käsittely)</td>
<td>Vastaanotat käteisvaroja toisen yrityksen myyntilaskua varten ja tallennat sekin kyseisen yrityksen pankkitilille.</td>
</tr>
<tr class="even">
<td>Palkanlaskenta (keskitetty käsittely, konserniyritysten välinen / yrityksen sisäinen)</td>
<td><ul>
<li>Voit maksaa toisen yrityksen palkanlaskennan. Yritys esimerkiksi maksaa omien työntekijöidensä palkkamenot, mutta veloittaa takaisin kyseisen palkka-ajon aikaisen työn, jonka työntekijä on tehnyt toisessa yrityksessä. Jos työntekijä on työskennellyt puolipäiväisesti yritykselle A ja puolipäiväisesti yritykselle B ja edut jakautuvat koko palkan ajalle Näissä tapauksissa työntekijän palkka sisältää palkan molemmilta yrityksiltä. Paitsi palkat myös palkkojen verot, edut, vähennykset ja siirtosaamiset kirjataan.</li>
<li>Siirrä työvoimaa yhdestä osastosta tai jaostosta toiseen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Käyttöomaisuuserät (konserniyritysten välinen / yrityksen sisäinen)</td>
<td>Siirrät käyttöomaisuutta toisen yrityksen käyttöomaisuuteen tai varastoon.</td>
</tr>
<tr class="even">
<td>Kohdistukset (konserniyritysten välinen / yrityksen sisäinen)</td>
<td>Käsittelet yrityksen kohdistukset. Kohdistukset ovat mihin tahansa kohdistettuun tiliin kohdistuvia toimia alkuperäisestä moduulista riippumatta.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Esimerkki
Yrityksesi nimeltä yritys A myy pienoisohjelmia toiselle organisaatiosi yritykselle nimeltä yritys B. Seuraava esimerkki kuvaa, kuinka kahden yrityksen väliset tapahtumat on ehkä eliminoitava:

-   Yritys A myy 10,00 euroa maksavan pienoisohjelman yritykselle B hintaan 10,00 euroa.
-   Yritys A myy 10,00 euroa maksavan pienoisohjelmanyritykselle B hintaan 10,00 euroa ja laskuttaa 2,00 euroa todellisia toimituskuluja.
-   Yritys A myy 10,00 euroa maksavan pienoisohjelman yritykselle B hintaan 15,00 euroa ja tunnustaa myynnin katteen.
-   Yritys A myy 10,00 euroa maksavan pienoisohjelman yritykselle B hintaan 15,00 euroa ja tunnustaa puolet myynnin katteesta. Yritys B tunnustaa toisen puoliskon myynnin marginaalista. Tämän vuoksi tuotto jaetaan. Jaettu tuotto tarjoaa mahdollisuuden tilata toiselta organisaation yritykseltä ulkoisen organisaation sijasta.

Kaikki nämä tapahtumat luovat konsernin sisäisiä tapahtumia, jotka kirjataan erääntymiskohteen ja -lähteen tileihin. Näissä tapahtumissa voi olla myös summien korotuksia ja alennuksia tilanteissa, joissa konserniyritysten välisen myynnin ja myytyjen tuotteiden kustannusten summat eivät täsmää.

## <a name="set-up-elimination-rules"></a>Määritä eliminointisääntöjä
Kun Microsoft Dynamics 365 for Finance and Operationsin eliminointisääntöjä määritetään, eliminointia varten kannattaa luoda oma taloushallinnon dimensio. Useimmat asiakkaat nimeävät sen Kaupankäynnin kumppaniksi tai jotain vastaavaa. Jos et halua käyttää taloushallinnon dimensiota, muista varmistaa, että sinulla on päätilit, jotka koskevat vain konserniyritysten välisiä tapahtumia. 

Konsolidoinnit-moduulin Asetukset-alueelta löytyy eliminoinnin asetukset. Kun kirjoitat säännön kuvauksen, sinun on valittava yritys, johon eliminoinnin kirjauskansio kirjaa. Tämän tulisi olla yritys, jonka asetuksissa on valittu **Käytetään taloushallinnon eliminointiprosessissa**. 

Voit määrittää päivämäärän, jolloin eliminointisääntö tulee voimaan ja (tarvittaessa) milloin se vanhentuu. On määritettävä **Aktiivinen** arvoksi **Kyllä**, jos haluat sen olevan saatavilla eliminoinnin ehdotusprosessissa. Valitse kirjauskansio, jonka tyyppi on **Eliminointi**.

Kun olet määritellyt perusteet, voit määrittää todelliset käsittelysäännöt valitsemalla **Rivit**. Vaihtoehtoja on kaksi eliminoinneissa: nettomuutossumman eliminointi tai kiinteän summan määrittäminen. 

Valitse lähdetili. Voit käyttää tähteä (\*) yleismerkkinä. Esimerkiksi 1\* valitsisi kaikki 1-alkuiset tilit kohdistuksen tietolähteenä. 

Kun olet valinnut lähdetilisi **Tilin määrittely** määrittää käytettävän tilin kohdeyrityksestä. Valitse **Lähde**, jos haluat käyttää samaa päätiliä, joka on määritelty **Lähde**-tilissä. Jos valitset **Käyttäjän määrittämä**, sinun on määritettävä kohdetili. 

Dimension määrittely toimii samalla tavalla. Jos valitset **Lähde**, se käyttää kohdeyrityksessä samoja dimensioita kuin lähdeyrityksessä. Jos valitset **Käyttäjän määrittämä**, sinun täytyy määrittää kohdeyrityksen dimensiot valitsemalla **Kohdedimensiot**-valikkovaihtoehtoa. 

Valitse lähdedimensiot ja taloushallinnon dimensiot ja eliminoinnin lähteenä käytettävät arvot.

## <a name="process-elimination-transactions"></a>Käsittele eliminointitapahtumia
On kaksi tapaa käsitellä eliminoinnin tapahtumia kokoa: konsolidoinnin online-prosessin aikana tai luomalla eliminoinnin kirjauskansio ja suorittamalla eliminoinnin ehdotusprosessi. Tässä osassa keskitytään kirjauskansion luomiseen ja eliminointiprosessin suorittamiseen. 

Valitse eliminointiyritykseksi määritellyssä yrityksessä **Eliminoinnin kirjauskansio** Konsolidoinnit-moduulissa. Kun olet valinnut kirjauskansion nimen, valitse **Rivit**. Valitsemalla voit suorittaa ehdotuksen valitsemalla **Ehdotukset**-valikon ja sitten **Eliminointiehdotus**.

Valitse yritys, joka on koottujen tietojen lähde ja valitse sääntö, jota haluat käsitellä. Anna aloituspäivämäärä käynnistääksesi eliminoinnin summien haun ja päättymispäivä eliminoinnin summien haun päivämäärävälin loppuun. **Kirjanpidon kirjauspäivä** -kenttä on päivämäärä, jolloin eliminointikirjauskansio kirjataan kirjanpitoon. Kun olet valinnut **OK**, voit tarkistaa määrät ja kirjata kirjauskansion.




