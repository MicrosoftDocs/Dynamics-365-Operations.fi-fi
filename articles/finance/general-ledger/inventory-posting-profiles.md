---
title: Varaston kirjausprofiilit
description: Tässä artikkelissa on varaston kirjausprofiilien yhteenveto.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cae5b39ef8e6e153fe522dee1874deae2a2cb86e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901339"
---
# <a name="inventory-posting-profiles"></a>Varaston kirjausprofiilit

[!include [banner](../includes/banner.md)]

Varaston kirjausprofiilit ohjaavat varaston alareskontrantapahtumien kirjaamista kirjanpitoon. Varaston alareskontran tapahtumat voidaan luoda useista moduuleista, kuten esimerkiksi **Myynti ja markkinointi**, **Hankinta** ja **Tuotannon hallinta**. Varaston alareskontran tapahtumat voidaan kirjata milloin tahansa, kun nimikettä käytetään myyntitilauksessa tai ostotilauksessa. 

Voit kirjata lisää varaston alareskontran tapahtumia:
- Aina, kun tiedosto päivitetään.
- Kun myyntitilauksen pakkausluettelo tai lasku kirjataan.
- Kun ostotilauksen tuotevastaanotto tai lasku luodaan.

Lisätietoja on kohdassa Varaston alareskontran tapahtumat.

## <a name="inventory-transaction-overview"></a>Varastotapahtumien yleiskatsaus

Kukin varaston alareskontran tapahtuma sisältää seuraavat tiedot:
 - Määrä 
 - Hinta 
 - Sivusto 
 - Varasto 
 - Toimipaikka 

Varaston alakirjanpitotapahtumat luovat kirjanpitoon kaksi merkintää fyysisen kirjauksen ja kirjanpitokirjauksen kautta. Lisätietoja on kohdassa [Fyysiset ja kirjanpidolliset päivitykset](/supply-chain/cost-management/physical-financial-updates.md).
Seuraavassa esimerkissä ostotilaus, joka sisältää kolme riviä. Tässä esimerkissä oletetaan, että koko tilaus on yhtä toimipaikkaa ja varastoa varten. Jokaiseen ostotilausriviin liittyy yksi liittyvä InventTrans-tietue eli varastotapahtuma, ja kunkin rivin määrä on 10. Seuraavassa kaaviossa havainnollistetaan yhden ostotilauksen otsikon ja kolmen ostotilausrivin suhdetta, joista jokaisella on yksi InventTrans-tietue.

![Ostotilauksen suhdekaavio, jossa on kolme riviä ja joista jokaisella on yksi InventTrans-tietue.](./media/InventTransRelationship.PNG)

Ensimmäisen ostotilauksen rivin määrästä on vastaanotettu 5. Toisen rivin koko määrä vastaanotetaan ja ostotilauksen kolmannella rivillä ei vastaanoteta mitään. Ensimmäiseen ostotilausriviin liittyy nyt toinen varastotapahtuma. Toisen ostotilausrivin tapahtumaksi päivitetään **Vastaanotettu**, ja kolmas tapahtuma säilyy samana. Seuraava kaavio havainnollistaa suhteen ensimmäisen ostotilausrivin ylimääräiseen InventTrans-tietueeseen.

![Suhdekaavio ostotilauksesta, jossa on kolme riviä. Yksi rivi vastaanotetaan osittain, ja se näyttää kaksi InventTrans-tietuetta.](./media/InventTransRelationshipPartialReceipt.PNG)

Tässä esimerkissä kirjanpitoon kirjataan tosite; tämä on fyysinen tosite. Nimikemalliryhmä on määritetty kirjaamaan fyysinen varasto, ja kaikissa nimikkeissä käytetään samaa nimikemalliryhmää. Varaston kirjausprofiilissa käytetään yhtä päätilijoukkoa. Yksi tosite luodaan, ja InventTrans-tietue linkittää sekä InventTrans 1- että InventTrans 2 -tietueen samaan tositteeseen.

Seuraavaksi lasku vastaanotetaan määrälle, joka on vastaanotettu riveillä 1 ja 2. Kirjanpitoon luodaan toinen tosite; tämä on kirjanpidollinen tosite. Nimikemalliryhmä määritetään kirjaamaan kirjanpitovarasto. Toinen tosite liittyy InventTrans 1- ja InventTrans 2 -tietueeseen.

Kustannuslaskentamallin mukaan varaston alakirjanpitotapahtumista voi olla olemassa kolmas kirjanpidon kirjaus, joka liittyy varaston sulkemiseen ja selvitykseen. Lisätietoja on kohdassa [Varaston sulkeminen](/supply-chain/cost-management/inventory-close.md). Voit tarkastella kaikkien varastotapahtumien tietoja kohdassa **Inventoinnin- ja varastonhallinta** > **Kyselyt ja raportit** > **Tapahtumat**.

>[!Important]
> Varastotapahtumat jaetaan kullekin varastodimensioiden yhdistelmälle ja kullekin osapäivitykselle. Se näkyy edellisessä esimerkissä osittaisia päivityksiä varten.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Varaston jakaminen varastodimensioesimerkin perusteella

Esimerkin ostotilausrivi 3 on sarjoitettu nimike. Ostotilaukselle rekisteröidään vastaanottoprosessin aikana kymmenen sarjanumeroa. Varastotapahtuma jaetaan 10 varastotapahtumaksi. Seuraavassa kaaviossa havainnollistetaan suhdetta ja muita varastotapahtumia, joista jokaisella on oma, ostotilausriviin 3 liittyvä sarjanumero.

![Suhdekaavio ostotilauksesta, jossa on kolme riviä. Yksi rivi on sarjoitettu, ja se näyttää InventTrans-lisätietueet](./media/InventTransRelationshipSerialNumber.PNG)

Jos jokainen sarjanumero vastaanotetaan yllä olevassa esimerkissä yhdessä tuotteen vastaanotossa, ohjelma luo yhden ylimääräisen tositteen. Fyysisen tositteen kenttä linkitetään kuhunkin sarjanumeroon. Sama koskee kirjanpitopäivitystä, kun ostotilaus laskutetaan.

## <a name="inventory-transactions"></a>Varastotapahtumat

Voit tarkastella varastotapahtumia **Varastotapahtumat**-sivulla kohdassa **Varastonhallinta** tai **Kustannushallinta**. Voit tarkastella myös tiettyyn lähdeasiakirjariviin, kuten ostotilausriviin tai myyntitilausriviin, liittyviä varastotapahtumiavalitsemalla **Varasto** ja valitsemalla sitten **Tapahtumat**. 

**Varastotapahtumat**-sivu sisältää seuraavat kentät.

| Kenttä            | Kuvaus                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Nimiketunnus      | Tapahtumaan liittyvä nimiketunnus.                                                                  |
| Fyysinen pvm.    | Päivämäärä, jolloin varasto saapuu fyysiseen varastoon, poistuu fyysisestä varastosta, kulutetaan tuotannossa tai sitä tuotetaan. Esimerkiksi kirjauspäivämäärä
myyntitilauksen tai tuotteen vastaanoton kirjauksen pakkausluettelon kirjaus ostotilauksessa.                             |
| Rahoituspvm.   | Päivämäärä, jolloin varastotapahtuma suljetaan ja kustannukset kirjataan kirjanpitoon. Esimerkiksi laskun kirjauspäivämäärä 
luonti myynti- tai ostotilaukselle. Viiteasiakirjan päivitykset eivät ole sallittuja, kun kirjanpitopäivämäärä on täytetty. |
| Viite        | Ilmaisee tapahtuman lähteen ja **Numero**-kentässä näkyvän tiedoston tyypin. Esimerkiksi myyntitilaus, ostotilaus tai siirtotilauksen vastaanotto.                                                 |
| Numero           | Ilmaisee tapahtuman viitetunnuksen. Jos **Viite**-kenttä ilmaisee esimerkiksi myyntitilauksen, **Numero**-kentässä näkyy myyntitilauksen numero.                                                       |
| Vastaanotto (tila) | Jos varastotapahtuma on vastaanotto, tämä kenttä ilmaisee vastaanoton tilan. Esimerkiksi ostotilaus on vastaanotto ja tila voi olla **Tilattu** tai **Ostettu**.                                                            |
| Varasto-otto (tila)   | Jos varastotapahtuma on varasto-otto, tämä kenttä ilmaisee varasto-oton tilan. Esimerkiksi myyntitilaus on varasto-otto, ja tilana voi olla **Tilauksessa** tai **Myyty**.                         |
| Määrä         | Varastotapahtuman määrä. Positiivisia lukuja käytetään varaston vastaanotoissa, kun taas negatiivisia lukuja käytetään varasto-ottojen yhteydessä.                                                                                                                          |
| Yksikkö             | Mittayksikkö, jota käyttäen määrä ilmaistaan.                                                                                   |
| Todellinen paino      | Tapahtuman todellisen painon määrä. Lisätietoja on kohdassa [Tietoja todellisen painon nimikkeistä](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Todellisen painon yksikkö          | Todellisen painon mittayksikkö, jota käyttäen todellisen painon määrä ilmaistaan.                                                         |
| Kustannusten summa      | Varastotapahtuman lopullinen kustannus. Tämä kenttä täytetään, kun tapahtuma päivitetään kirjanpitoon. Varaston sulkemis- ja oikaisuprosessi saattaa päivittää tämän kentän kustannuslaskentamenetelmän mukaan.                            |

## <a name="inventory-status"></a>Varaston tila

Kullakin varastotapahtumalla on tila, joka näkyy joko **Vastaanotto**- tai **Varasto-otto**-kentässä. Käytetty kenttä riippuu varastotapahtumien tyypistä. Vastaanotot ovat tapahtumia, jotka lisäävät varastoa. Esimerkiksi ostotilaus, jonka määrä on positiivinen, tai myyntitilauksen palautus, jossa on negatiivinen määrä. Varasto-otot ovat varastotapahtumia, jotka vähennetään varastosta. Esimerkiksi myyntitilaus, jonka määrä on positiivinen, tai ostotilauksen palautus, jossa on negatiivinen määrä.

### <a name="receipt-status"></a>Vastaanoton tila

Seuraavassa taulussa kuvataan **Vastaanotto**-tilaa.

| **Vastaanoton tila** | **Kuvaus**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Tilattu            | Vastaanottoa edustavan varastotapahtuman alkuperäinen tila. Tämä sisältää ostotilaukset, joiden määrä on positiivinen, tuotantotilaukset tai myyntitilauksen palautukset, joiden määrä on negatiivinen.                                                   |
| Rekisteröitynyt         | Tätä tilaa käytetään, kun on olemassa kaksivaiheinen vastaanottoprosessi tai kun nimikkeen saapumisen avulla ilmaistaan tuotteen saapuminen. Sitä käytetään, kun erä- tai sarjanumerot "kohdistetaan" tai rekisteröidään tilaukseen. Lisätietoja nimikkeen saapumisesta on [saapumisen yhteenvedossa](/supply-chain/inventory/arrival-overview.md). |
| Vastaanotettu           | Tätä tilaa käytetään, kun tapahtuma päivitetään fyysisesti. Ostotilaukselle tämä on tuotteen vastaanoton kirjaus. Myyntitilauksen palautukselle tämä on pakkausluettelon kirjaus.                                                                            |
| Ostettu          | Tätä tilaa käytetään, kun tapahtuma päivitetään kirjanpidossa. Esimerkiksi ostotilaukselle tai myyntitilauksen palautukselle tämä on laskun luonti.                                                                                             |

### <a name="issue-status"></a>Varasto-ottotila

Seuraavassa taulussa kuvataan **Varasto-otto**-tilaa.

| **Varasto-ottotila**  | **Kuvaus**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Tilauksessa          | Varasto-ottoa edustavan varastotapahtuman alkuperäinen tila. Tämä sisältää myyntitilaukset, joiden määrä on positiivinen, tuotantotilausten tuoterakenne- tai kaavarivit tai ostotilauksen palautukset, joiden määrä on negatiivinen.                                             |
| Tilaukseen varattu  | Tämä varastotila ilmaisee, että varasto on varattu tilaukselle, joka on luotu mutta ei vielä fyysisesti vastaanotettu varastoon. Kun varasto vastaanotetaan, tilaksi päivitetään automaattisesti **Varattu fyysinen**. Lisätietoja varauksista on kohdassa [Varastomäärien varaaminen](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Varattu fyysinen | Tämä tila ilmaisee, että varasto on kohdistettu tai varattu tiettyä tilausta varten. Kun varasto on varattu, se ei ole fyysisesti käytettävissä muille tilauksille.                                 |
| Keräilty         | Tämä ilmaisee, että varasto on kerätty varastosta. Varasto on vielä fyysisesti varastossa, sitä ei ole poistettu, mutta se ei ole muiden tilausten käytettävissä.  |
| Toimitettu          | Tätä tilaa käytetään, kun tapahtuma päivitetään fyysisesti. Myyntitilausta varten tämä tapahtuu pakkausluettelon kirjaamisen yhteydessä; jos ostotilauksen palautus on tehty, tämä tapahtuu, kun tuotteen vastaanotto kirjataan.                                                                      |
| Myyty              | Tätä tilaa käytetään, kun tapahtuma päivitetään kirjanpidossa. Esimerkiksi ostotilaukselle tai myyntitilaukselle tämä on laskun luonti.|

Lisätietoja varastotapahtumista on [varastotapahtumien erittelyssä](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Varaston kirjausprofiilin määrittäminen

Määritä varaston kirjausprofiili noudattamalla seuraavia ohjeita:

1.  Siirry kohtaan **Varastonhallinta** > **Määritys** > **Kirjaus** > **Kirjaus**.
2.  Valitse tapahtumatyypin välilehti. Valitse esimerkiksi **Ostotilaus**.
3.  Valitse kirjaustyypin valintapainike. Valitse esimerkiksi **Osto, kulu**.
4.  Valitse **Uusi**.
5.  Valitse **Nimikekoodi**-kentästä vaihtoehto kohteille **Taulukko**, **Ryhmä**, **Kaikki** tai **Luokka**. Jos haluat konfiguroida esimerkiksi tietyn nimikeryhmän kirjausprofiilin, valitse **Ryhmä**.
     - Jos valitsit vaiheessa 5 **Taulukko**, valitse kirjausprofiilin nimikenumero **Nimikesuhde**-kentästä.
     - Jos valitsit vaiheessa 5 **Ryhmä**, valitse kirjausprofiilin **Nimikeryhmä** **Nimikesuhde**-kentästä.
     - Jos valitsit vaiheessa 5 **Kaikki**, **Nimikesuhde**-kenttä jätetään tyhjäksi.
     - Jos valitsit vaiheessa 5 **Luokka**, **Nimikesuhde**-kenttä jätetään tyhjäksi. Valitse **Luokkasuhde**-kentässä kirjausprofiilin soveltuva luokka.

6.  Valitse **Tilikoodi**-kentästä vaihtoehto kohteille **Taulukko**, **Ryhmä** tai **Kaikki**. Jos haluat käyttää kirjausprofiilia esimerkiksi kaikille toimittajille, valitse **Kaikki**.
     - Jos valitsit vaiheessa 5 **Taulukko**, valitse kirjausprofiilin toimittajanumero **Tilisuhde**-kentästä.
     - Jos valitsit vaiheessa 5 **Ryhmä**, valitse kirjausprofiilin toimittajaryhmä **Tilisuhde**-kentästä.
     - Jos valitsit vaiheessa 5 **Kaikki**, **Tilisuhde**-kenttä jätetään tyhjäksi.

7.  Liitä valittuun kirjaustapaan tietty veroryhmä valitsemalla **Arvonlisäveroryhmä**. Jos tämä kenttä on tyhjä, kirjaustyyppi koskee kaikki veroryhmiä. Veroryhmille määritetty kirjaus koskee vain myynti- ja ostotapahtumia.
8.  Määritä **Päätili**-kentässä tilinumero, jolle tilityyppi kirjataan. Jos kirjaustavalle ei ole vielä luotu tilinumeroa, voit luoda uuden tilin. Voit luoda uuden tilin kirjanpidon **Päätilin tiedot** -sivulla.

## <a name="additional-resources"></a>Lisäresurssit

Kukin **Varaston kirjausprofiili** -sivun välilehti liittyy alareskontraan Dynamics 365 Supply Chain Managementissa. Lisätietoja on kohdassa:
-   [Myyntitilauksen kirjaaminen](sales-order-posting.md)
-   [Ostotilauksen kirjaus](purchase-order-posting.md)
-   [Varastokirjaus](inventory-posting.md)
-   [Tuotannonhallinnan kirjaus](production-posting.md)
-   [Vakiokustannusten varianssin kirjaus](standard-cost-variance-posting.md)
