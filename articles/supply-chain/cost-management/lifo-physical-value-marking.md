---
title: "LIFO-merkintä ja fyysinen arvo"
description: "LIFO (Last in, First out) on varastomalli, jossa varastoon viimeiseksi hankittujen (uusimpien) vastaanottojen varasto-otto tapahtuu ensin. Varasto-otot täsmäytetään viimeisiä varastovastaanottoja vasten varastotapahtuman päivämäärän perusteella."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9910919d8b2a4f670710099b5150d7c7858a87cb
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="lifo-with-physical-value-and-marking"></a>LIFO-merkintä ja fyysinen arvo

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


LIFO (Last in, First out) on varastomalli, jossa varastoon viimeiseksi hankittujen (uusimpien) vastaanottojen varasto-otto tapahtuu ensin. Varasto-otot täsmäytetään viimeisiä varastovastaanottoja vasten varastotapahtuman päivämäärän perusteella. 

LIFO (Last in, First out) -varastomallissa varastoon viimeiseksi hankittujen (uusimpien) vastaanottojen varasto-otto tapahtuu ensin. Varasto-otot täsmäytetään viimeisiä varastovastaanottoja vasten varastotapahtuman päivämäärän perusteella. Kun käytät LIFO-ominaisuutta, LIFO-sääntöä ei tarvitse noudattaa. Sen sijaan voit merkitä varastotapahtumat niin, että tietyn nimikkeen varasto-otto selvitetään tiettyä vastaanottoa vasten. Varaston kausittainen sulkeminen on suositeltavaa käytettäessä LIFO-varastomallia. 

Seuraavissa esimerkeissä havainnollistetaan LIFO-mallin käyttämisen vaikutus kolmea eri määritystä käytettäessä:

-   LIFO ilman **Sisällytä fyysinen arvo** -asetusta
-   LIFO ja **Sisällytä fyysinen arvo** -asetus
-   LIFO ja merkintä

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO ilman Sisällytä fyysinen arvo -asetusta
Tässä esimerkissä nimikemalliryhmää ei ole merkitty sisällyttämään fyysistä arvoa. Seuraavassa on kuvattu näitä tapahtumia:

-   1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   3a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
-   4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   4b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   5a. Fyysinen varasto-otto, jossa määrä on 1 ja kappaleen kustannushinta 20,00 Yhdysvaltain dollaria (USD) (rahoituksellisesti päivitettyjen tapahtumien keskiarvo).
-   5b. Rahoituksellinen varasto-otto, jossa määrä on 1 ja kappaleen kustannushinta 20,00 Yhdysvaltain dollaria (USD) (rahoituksellisesti päivitettyjen tapahtumien keskiarvo).
-   6. Varaston sulkeminen on suoritettu. LIFO-menetelmään perustuen viimeinen rahoituksellisesti päivitetty varasto-otto täsmäytetään viimeistä rahoituksellisesti päivitettyä vastaanottoa vasten. Varasto-ottotapahtumalle tehdään 10,00 Yhdysvaltain dollarin (USD) oikaisu.

Uusi kustannushinnan käyttökeskiarvo (15,00 USD) on laskettu taloudellisesti päivitettyjen tapahtumien mukaan. Seuraavassa kuvassa havainnollistetaan LIFO-varastointimallia tässä tapahtumasarjassa, kun **Sisällytä fyysinen arvo** -asetus ei ole käytössä. ![LIFO - fyysistä arvoa ei sisällytetä](./media/lifowithoutincludephysicalvalue.gif) 

**Kaavion selite**

-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unit -hinta.
-   Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Varastotapahtuman arvo, joka ei ole sulkeissa, tarkoittaa, että varastotapahtuma on kirjattu varastoon kirjanpidollisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO ja Sisällytä fyysinen arvo -asetus
Jos **Sisällytä fyysinen arvo** -valintaruutu on valittuna nimikkeen **Nimikemalliryhmät**-sivulla, järjestelmä käyttää juoksevan keskimääräisen kustannushinnan laskennassa sekä fyysisiä että rahoituksellisia vastaanottotapahtumia. Järjestelmä tekee myös oikaisuja fyysisesti päivitettyyn varastostaottotapahtumaan, jos tämä on aiheellista. Jos **Sisällytä fyysinen arvo** -valintaruutu ei ole valittuna, varaston sulkeminen LIFO-varastomallia käyttäen selvittää vain kirjanpidollisesti päivitetyt tapahtumat. 

Seuraavassa on kuvattu näitä tapahtumia:

-   1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   3a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
-   4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   4b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   5a. Fyysinen varasto-otto, jossa määrä on 1 ja kappaleen kustannushinta 21,25 Yhdysvaltain dollaria (USD) (rahoituksellisesti ja fyysisesti päivitettyjen tapahtumien keskiarvo).
-   5b. Rahoituksellinen varasto-otto, jossa määrä on 1 ja kappaleen kustannushinta 21,25 Yhdysvaltain dollaria (USD) (rahoituksellisesti ja fyysisesti päivitettyjen tapahtumien keskiarvo).
-   6a. Varaston fyysinen varastostaotto määrälle 1 yksikkökustannushintaan 21,25 USD.
-   7. Varaston sulkeminen on suoritettu. LIFO-menetelmään perustuen viimeinen varasto-ottotapahtuma oikaistaan viimeisen päivitetyn vastaanoton mukaiseksi tai täsmäytetään sitä vasten.

Tapahtuma 6a oikaistaan vastaanottotapahtuman 4b mukaiseksi. Järjestelmä ei täsmäytä näitä tapahtumia, koska vastaanotto päivitetään vain fyysisesti, ei rahoituksellisesti. Sen sijaan fyysiselle varasto-ottotapahtumalle kirjataan ainoastaan 8,75 Yhdysvaltain dollarin (USD) oikaisu. Tapahtuma 5b oikaistaan fyysisen vastaanottotapahtuman 3a mukaiseksi. Järjestelmä ei täsmäytä näitä tapahtumia, koska molemmat tapahtumat eivät ole rahoituksellisesti päivitettyjä. Sen sijaan tähän varasto-ottotapahtumaan tehdään vain –3,75 Yhdysvaltain dollarin (USD) negatiivinen oikaisu. Uusi kustannushinnan käyttökeskiarvo 20,00 USD on laskettu taloudellisesti ja fyysisesti päivitettyjen tapahtumien mukaan. 

Seuraavassa kuvassa havainnollistamme LIFO-varastointimallia tässä tapahtumasarjassa, kun**Sisällytä fyysinen arvo** -asetus on käytössä. ![LIFO - fyysinen arvo sisällytetään](./media/lifowithincludephysicalvalue.gif) 

**Kaavion selite**

-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unit -hinta.
-   Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Varastotapahtuman arvo, joka ei ole sulkeissa, tarkoittaa, että varastotapahtuma on kirjattu varastoon kirjanpidollisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="lifo-with-marking"></a>LIFO ja merkintä
Merkintä on prosessi, jonka avulla voit linkittää (eli merkitä) varaston ottotapahtuman vastaanottotapahtumaan. Merkintä voi tapahtua joko ennen tapahtuman kirjaamista tai sen jälkeen. Merkinnän avulla voit varmistaa tarkan varastokustannuksen, kun tapahtuma kirjataan tai kun varaston sulkeminen suoritetaan. Oletetaan esimerkiksi, että asiakaspalveluosasto on hyväksynyt kiireellisen tilauksen tärkeältä asiakkaalta. Koska tilaus on kiireellinen, tästä nimikkeestä on maksettava tavallista enemmän, jotta asiakkaan pyynnön voi toteuttaa. 

Sinun on varmistettava, että tämän varastonimikkeen kustannus otetaan huomioon myyntitilauslaskun katteessa (tai myydyn tavaran kustannuksissa). Kun ostotilaus kirjataan, varasto vastaanotetaan hintaan 120,00 USD. Jos tämä myyntitilausasiakirja on merkitty ostotilaukseen ennen pakkausluettelon tai laskun kirjaamista, myydyn tavaran kustannukseksi tulee 120,00 USD nimikkeen nykyisen käyttökeskiarvokustannuksen sijaan. Jos myyntitilauksen pakkausluettelo tai lasku kirjataan ennen merkintää, myydyn tavaran kustannus kirjataan käyttäen käyttökeskiarvon mukaista kustannushintaa. 

Ennen varaston sulkemista nämä kaksi tapahtumaa voidaan vielä merkitä toisiinsa. 

Voit merkitä varastostaottotapahtuman vastaanottoon kirjauksen jälkeen. Voit tehdä tämän myyntitilausrivin **Myyntitilauksen tiedot** -sivulla. Voit tarkastella avoimia vastaanottotapahtumia **Merkintä**-sivulla. 

Voit merkitä varastostaottotapahtuman vastaanottoon myös tapahtuman kirjauksen jälkeen. Voit täsmäyttää tai merkitä varastostaottotapahtuman varastoidun nimikkeen avoimeen vastaanottotapahtumaan kirjatusta varaston oikaisukirjauskansiosta. 

Seuraavassa on kuvattu näitä tapahtumia:

-   1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   3a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
-   4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   4b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   5a. Varaston fyysinen varastostaotto määrälle 1 yksikkökustannushintaan 21,25 USD (taloudellisten ja fyysisten päivitettyjen tapahtumien käyttökeskiarvo).
-   5b. Varaston taloudellinen vastaanotto määrälle 1 merkitään varaston vastaanottoon 2b ennen tapahtuman kirjaamista. Tämä tapahtuma kirjataan käyttäen yksikkökustannushintaa 20,00 USD.
-   6a. Varaston fyysinen varastostaotto määrälle 1 yksikkökustannushintaan 21,25 USD.
-   7. Varaston sulkeminen on suoritettu. Koska taloudellisesti päivitetty FIFO-tapahtuma on merkitty vastaanottoon, nämä tapahtumat täsmäytetään toisiaan vasten, eikä oikaisua tehdä.

Uusi kustannushinnan käyttökeskiarvo 27,50 USD on laskettu taloudellisesti ja fyysisesti päivitettyjen tapahtumien mukaan. 

Seuraavassa kuvassa havainnollistetaan LIFO-varastomallin käyttämisen vaikutus tähän tapahtumien sarjaan kun merkintä varasto-ottojen ja vastaanottojen välillä on käytössä. ![LIFO merkinnän kanssa    ](./media/lifowithmarking.gif) 

**Kaavion selite**

-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unit -hinta.
-   Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Varastotapahtuman arvo, joka ei ole sulkeissa, tarkoittaa, että varastotapahtuma on kirjattu varastoon kirjanpidollisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.





