---
title: Yhdistä varastoerät
description: Tässä artikkelissa on tietoja kahden tai useamman varastoerän konsolidoinnista yhdistetyksi eräksi.
author: pjacobse
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4c9443c6e659602ae09e4744396651186874ad3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008013"
---
# <a name="merge-inventory-batches"></a>Yhdistä varastoerät

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja kahden tai useamman varastoerän konsolidoinnista yhdistetyksi eräksi.

Kun yhdistät eriä, laskelmat voivat auttaa optimoimaan yhdistetyn erän ominaisuudet ja erämääritteet. Kun lähde-erät on valittu, yhdistetyn erän voi tarkistaa ja sitä voi vielä muuttaa ennen kirjausta. Voit myös siirtää erän yhdistämisen varastokirjauskansioon hyväksyttäväksi. Varasto voidaan varata tai kirjata suoraan varastokirjauskansiosta. Yhdistetyt erän kirjatessasi varasto oikaistaan lähde-erillä ja yhdistetyllä erällä.

## <a name="are-there-any-prerequisites"></a>Onko tiettyjä edellytyksiä?
Kyllä, on asioita, jotka on määritettävä ennen erän yhdistämisen työkalujen käyttöä. Seuraavassa taulussa kuvataan edellytykset.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sivu</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kirjauskansioiden nimet, Varasto</td>
<td>Sinun on luotava oletusarvoisesti käytettävä tuoterakenne-tyyppiä oleva kirjauskansionimi, jota käytetään erän yhdistämisten kirjaamiseen varastokirjauskansioissa. On myös suositeltavaa määrittää, että varaukset tehdään automaattisesti, kun erän yhdistäminen siirretään varastokirjauskansioon. Muussa tapauksessa on mahdollista, että käytettävissä olevaan varastoon voidaan tehdä muutos sen jälkeen, kun eräyhdistämisen tiedot on määritetty ja kirjauskansio kirjattu. Jos haluat ottaa käyttöön automaattiset varaukset kirjauskansion nimelle, valitse <strong><strong>Varaus</strong> </strong>-kentässä <strong>Automaattinen</strong>.</td>
</tr>
<tr class="even">
<td>Varasto ja varastonhallinnan parametrit</td>
<td>Sinun on määritettävä oletusarvoinen kirjauskansion nimi varastokirjauskansioille.</td>
</tr>
<tr class="odd">
<td>Vapautetut tuotteet</td>
<td>Nimikkeen suositeltavat asetukset ovat seuraavat:
<ul>
<li>Jos haluat luoda yhdistetyille erille eränumerot automaattisesti, kohdista vapautettu tuote eränumeroryhmään. Voit määrittää myös eränumeron manuaalisesti, kun luot yhdistettyjä eriä tai valitset aiemmin luodun eränumeron. Jos valitset olemassa olevan eränumeron, varmista, että valittu erä ei sisälly mihinkään varastotapahtumaan.</li>
<li>Jos käytät vapautetun tuotteen säilyvyysaikaa tai parasta ennen -päiviä, yhdistetyn erän päivämäärät lasketaan <strong>Erän yhdistämispäivämäärän laskenta</strong> -kentän valinnan perusteella. Valittavissa ovat seuraavat vaihtoehdot:
<ul>
<li><strong>Aikaisintaan</strong> – Laskenta perustuu aikaisimpaan päivämäärään, joka on määritetty erän yhdistämiselle valitulle lähde-erälle.</li>
<li><strong>Viimeistään</strong> – Laskenta perustuu viimeisimpään päivämäärään, joka on määritetty erän yhdistämiselle valitulle lähde-erälle.</li>
<li><strong>Manuaalinen</strong> – Laskelmaa ei ole tehty. Jos päivämäärä on sama kaikissa lähde-erissä, päivämäärää ehdotetaan. Voit muuttaa päivämäärää. Jos lähde-erien päivämäärä ei ole sama, voit lisätä sen manuaalisesti.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Eränumeroryhmä</td>
<td>Voit halutessasi luoda eränumeron luodessasi yhdistetyn erän määrittämällä vapautetulle tuotteelle eränumeroryhmän. Muussa tapauksessa erän numero voidaan syöttää manuaalisesti.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Milloin kannattaa yhdistää varaston erät?
Seuraavat skenaariot ovat esimerkkejä siitä, milloin erien yhdistäminen saattaa olla hyödyllistä.

-   Sammy kulkee varastossaan ja huomaa, että samasta nimikkeestä on useita eriä, joiden määrät ovat pieniä. Hän odottaa saavansa useita toimituksia ja hän havaitsee, että hän voi vapauttaa työtilaa yhdistämällä uuteen erään parittomat määrät.
-   Sammy vastaanottaa varastoa ja haluaa yhdistää uuden erän sellaiseen erään, joka hänellä jo on, ja parantaa näin aiemman erän erämääritteen arvoa. Näin luot uuden erän.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Voinko yhdistää eri toimipaikkojen ja yritysten eriä?
Ei, voit yhdistää vain eriä, joilla on sama toimipaikka ja varaston varastodimensiot yhdessä yrityksessä. Voit määrittää yhdistetylle erälle toisen sijainnin ja kuormalavan tunnuksen.

## <a name="can-i-merge-partial-quantities"></a>Voinko yhdistää osittaisia määriä?
Et, voit yhdistää vain erien täyden määrän. Eräyhdistämistoiminto on tarkoitettu varasto-ominaisuudeksi (ei tuotanto-ominaisuudeksi).

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Mitä jos erillä on erilaiset erämääritearvot?
Kun valitset tiettyyn erään yhdistettävät lähde-erät, Supply Chain Management tarkistaa, onko kaikilla erillä samat ominaisuudet tai määritearvot. Kun määritteen arvo on sama, yhdistetylle erälle ehdotetaan arvoa. Tätä arvoa voi muuttaa. Yhdistetyn erän toisistaan poikkeavat määritearvot jätetään tyhjiksi. Voit lisätä nämä arvot manuaalisesti. Jos määritearvon erämääritetyyppi on kokonaisluku tai murtoluku, eivätkä arvot ole samoja kaikille lähde-erille, arvo lasketaan käyttämällä painotettua keskiarvoa. Laskettu arvo pyöristetään ylös- tai alaspäin lähimpään lisäykseen. Jos lähde-erän arvo on tyhjä, erää ja sen määrää ei sisällytetä laskentaan. **Esimerkki** Seuraavissa esimerkeissä kuvataan painotetun keskiarvon laskenta yhdistetylle erälle. Kahdella lähde-erällä on tyhjä arvo erämääritetyypille, joka on kokonaisluku. Seuraava määrite on liitetty lähde-eriin.

| Ominaisuus | Minimi | Lisäys | Maksimi |
|-----------|---------|-----------|---------|
| Palkkaluokka     | 3       | 3         | 30      |

Lähde-erillä on seuraavat määritearvot **Palkkaluokka**-erämääritteelle.

| Erä | Määrä | Ominaisuus | Määritteen arvo |
|-------|----------|-----------|-----------------|
| B1    | 10       | Palkkaluokka     | Tyhjä           |
| B2    | 15       | Palkkaluokka     | 15              |
| B3    | 20       | Palkkaluokka     | 20              |
| B4    | 25       | Palkkaluokka     | Tyhjä           |
| B5    | 30       | Palkkaluokka     | 25              |

Kun nämä erät lisätään lähde-eriksi, yhdistetylle erälle määritetään seuraavat arvot.

| Erä | Määrä | Ominaisuus | Määritteen arvo |
|-------|----------|-----------|-----------------|
| B6    | 100      | Palkkaluokka     | 21              |

Erien B1 ja B4 arvoja ja määriä ei sisällytetä painotetun keskiarvon laskentaan. Tämän vuoksi yhdistetyn erän arvo lasketaan seuraavasti.

| Arvo | Määrä (paino)                              | Suhteellinen paino | Suhteellinen paino x arvo                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0,230769231     | 3,461538462                                                           |
| 20    | 20                                             | 0,307692308     | 6,153846154                                                           |
| 25    | 30                                             | 0,461538462     | 11,53846154                                                           |
|       | **Yhteensä:** 65, joka on painojen summa |                 | **Yhteensä:** 21,5384615, pyöristetty 21:een (lähin korotus) |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Mitä jos erillä on erilaiset erän päivämäärät?
Jos erillä on eri eräpäivämäärät, osa päivämääristä lasketaan **Erän yhdistäminen** -sivun **Yhdistetty erä** -pikavälilehden **Erän päivämäärät** -ryhmän arvojen perusteella. Järjestelmä laskee **Erän päivämäärät** -ryhmän kenttien arvot. Arvoihin sisältyvät valmistuspäivämäärä, vanhentumispäivämäärä, suositeltavan varastointiajan päivämäärä sekä parasta ennen -päivämäärä. Päivämäärät lasketaan nimikkeen **Vapautetut tuotteen tiedot** -sivun **Nimiketiedot**-kentän asetusten perusteella. Voit tarvittaessa muuttaa arvoja tai kirjata ne manuaalisesti. Muiden päivämäärien osalta ei suoriteta laskentaa. Samaa periaatetta käytetään erämääritteen arvoille. Jos päivämäärä on sama kaikille lähde-erille, yhdistetylle erälle ehdotetaan tätä päivämäärää. Jos päivämäärä ei ole sama kaikille lähde-erille, yhdistetyn erän päivämäärä on tyhjä, ja sen voi kirjoittaa manuaalisesti.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Mitä jos dimensiot ovat erilaiset erissä, jotka haluan yhdistää?
Tuotedimensiot, seurantadimensiot ja varastodimensiot käsitellään seuraavasti:

-   **Tuotedimensiot** – Kaikkien valitun nimikkeen tuotedimensioiden on oltava samat. Eriä ei voi yhdistää tuotedimensioiden kesken.
-   **Seurantadimensiot** – Uusi eränumero luodaan automaattisesti, jos nimikkeelle on määritetty eränumeroryhmä. Jos nimikkeelle ei ole määritetty eränumeroryhmää, voit valita aiemmin luodun erän tai syöttää numeron manuaalisesti. Sarjanumerot siirretään lähde-erästä yhdistetyt yhdistetyn erän varaston kirjauskansioriveille.
-   **Varastodimensiot** – Toimipaikka- ja varastodimensioiden on oltava samat kaikille lähde-erille ja yhdistetylle erälle. Voit määrittää yhdistetylle erälle uuden sijainnin ja kuormalavan tunnuksen.

## <a name="how-does-posting-work"></a>Kirjauksen toiminta
Kirjaaminen toimii kahdella eri tavalla sen mukaan, käytetäänkö hyväksyntäprosessia kirjauskansioita varten. **Siirto kirjauskansioon**- ja **Kirjaa erän yhdistäminen** -toimintojen avulla voit siirtää erän yhdistämisen kirjauskansioon, jossa se voidaan tarkistaa ja kirjata, tai voit kirjata erän yhdistämisen suoraan. Olennaisin ero kahden toiminnon välillä on se, että siirtäminen kirjauskansioon ei kirjaa erien yhdistämistä. Molemmat toiminnot luovat uuden erän, jos aiemmin luotua erää ei ole valittuna, päivittävät kaikki erätiedot ja määritearvot ja luovat varastokirjauskansion.

-   **Siirto kirjauskansioon** – Siirtää erän yhdistämisen tiedot uuteen varastokirjauskansioon. Jos olet määrittänyt automaattisia varauksia, lähde-erän määrät varataan. Erän yhdistämistietoja ei voi muuttaa. Jos sinun on muokattava erän yhdistämistä, kirjauskansio on poistettava. Kirjauskansiota voi käyttää tehtävänä, joka toisen työntekijän on suoritettava myöhemmin. Erän määrän varaus kirjauskansioon suojataan. Tämän kohdistuksen avulla laatusuunnittelija tai varastopäällikkö voi luoda tehtäviä omille työntekijöilleen.
-   **Kirjaa erän yhdistäminen** – Kirjaa erän yhdistämisen suoraan. Tämän toiminnon voi suorittaa fyysisen yhdistämisen jälkeen.

Voit hyväksyä erän yhdistämisen varastokirjauskansion **Kaikki erän yhdistämiset** -luettelosivulta. Valitse **Kirjauskansio** &gt; **Kirjaa**. Kun kirjauskansio on kirjattu, et voi muuttaa yhdistetyn erän tietoja. Kun olet siirtänyt erän yhdistämisen varastokirjauskansioon, voit muuttaa tietoja vain, jos kirjauskansio on poistettu.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Miksi en näe todellista painoa varaston kirjauskansiossa, kun olen yhdistänyt todellisen painon nimikkeen?
Voit yhdistää todellisen painon nimikkeiden eriä samalla tavalla kuin muitakin nimikkeitä. Todellisen painon tietoja ei kuitenkaan näytetä varastokirjauskansiossa. Suosittelemme, että varmistat todelliset painotiedot ennen erän yhdistämisen siirtämistä varaston kirjauskansioon.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]