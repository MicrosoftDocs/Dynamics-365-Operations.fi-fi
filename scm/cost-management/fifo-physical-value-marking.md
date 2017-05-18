---
title: "FIFO-merkintä ja fyysinen arvo"
description: "FIFO (First In, First Out) on varastomalli, jossa ensimmäiset vastaanotot otetaan varastosta ensin. Rahoituksellisesti päivitetyt varasto-otot täsmäytetään ensimmäisiä rahoituksellisesti päivitettyjä varastovastaanottoja vasten varastotapahtuman rahoituspäivämäärän perusteella."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: b0be852bde33e8dfc82ceb42dd98be10537f318d
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="fifo-with-physical-value-and-marking"></a>FIFO-merkintä ja fyysinen arvo

[!include[banner](../includes/banner.md)]


FIFO (First In, First Out) on varastomalli, jossa ensimmäiset vastaanotot otetaan varastosta ensin. Rahoituksellisesti päivitetyt varasto-otot täsmäytetään ensimmäisiä rahoituksellisesti päivitettyjä varastovastaanottoja vasten varastotapahtuman rahoituspäivämäärän perusteella. 

Kun käytät FIFO-ominaisuutta, FIFO-sääntöä ei tarvitse noudattaa. Sen sijaan voit merkitä varastotapahtumat niin, että tietyn nimikkeen vastaanotto selvitetään tiettyä varastostaottoa vasten. Varaston kausittainen sulkeminen on suositeltavaa käytettäessä FIFO-varastomallia. Seuraavissa esimerkeissä havainnollistetaan FIFO-mallin käyttämisen vaikutus kolmea eri määritystä käytettäessä:

-   FIFO ilman **Sisällytä fyysinen arvo** -asetusta
-   FIFO ja **Sisällytä fyysinen arvo** -asetus
-   FIFO ja merkintä

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO ilman Sisällytä fyysinen arvo -asetusta
Tässä esimerkissä nimikemalliryhmää ei ole merkitty sisällyttämään fyysistä arvoa. Seuraavassa on kuvattu näitä tapahtumia:

-   1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto määrälle 2 yksikkökustannuksen ollessa 10,00 USD.
-   2b. Varaston taloudellinen vastaanotto määrälle 2 yksikkökustannuksen ollessa 10,00 USD.
-   3a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
-   4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   4b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   5a. Fyysinen varasto-otto, jossa määrä on 1 ja kappaleen kustannushinta 20,00 Yhdysvaltain dollaria (USD) (rahoituksellisesti päivitettyjen tapahtumien keskiarvo).
-   5b. Rahoituksellinen varasto-otto, jossa määrä on 1 ja kappaleen kustannushinta 20,00 Yhdysvaltain dollaria (USD) (rahoituksellisesti päivitettyjen tapahtumien keskiarvo).
-   6. Varaston sulkeminen on suoritettu. FIFO-menetelmään perustuen ensimmäinen rahoituksellisesti päivitetty varasto-otto täsmäytetään ensimmäisen rahoituksellisesti päivitetyn vastaanoton kanssa. Varasto-ottotapahtumalle tehdään –10,00 Yhdysvaltain dollarin (USD) oikaisu.

Uusi keskimääräinen kustannushinta vastaa rahoituksellisesti päivitettyjen tapahtumien keskiarvoa. Seuraavissa kuvissa havainnollistamme FIFO-varastointimallia tässä tapahtumasarjassa, kun**Sisällytä fyysinen arvo** -asetus ei ole käytössä. ![FIFO - fyysistä arvoa ei sisällytetä](./media/fifowithoutincludephysicalvalue.gif) 

**Kaavion selite**

-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
-   Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Varastotapahtuman arvo, joka ei ole sulkeissa, tarkoittaa, että varastotapahtuma on kirjattu varastoon kirjanpidollisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO ja Sisällytä fyysinen arvo -asetus
Jos **Sisällytä fyysinen arvo** -valintaruutu on valittuna nimikkeen **nimikemalliryhmän** sivulla, järjestelmä käyttää juoksevan keskimääräisen kustannushinnan laskennassa sekä fyysisiä että rahoituksellisia vastaanottotapahtumia. Järjestelmä tekee myös oikaisuja fyysisesti päivitettyyn varastostaottotapahtumaan, jos tämä on aiheellista. Jos **Sisällytä fyysinen arvo** -valintaruutu ei ole valittuna, varaston sulkeminen FIFO-varastomallia käyttäen selvittää vain kirjanpidollisesti päivitetyt tapahtumat. Seuraavassa on kuvattu näitä tapahtumia:

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
-   7. Varaston sulkeminen on suoritettu. FIFO-menetelmän perusteella ensimmäinen rahoituksellinen varasto-ottotapahtuma oikaistaan tai täsmäytetään ensimmäisen päivitetyn vastaanoton kanssa huolimatta siitä, onko se rahoituksellinen vai fyysinen.

Tapahtuma 5b täsmäytetään vastaanottotapahtuman 1b kanssa. Tälle varasto-ottotapahtumalle tehdään –11,25 Yhdysvaltain dollarin (USD) oikaisu. Uusi kustannushinnan käyttökeskiarvo 27,50 USD on laskettu taloudellisesti ja fyysisesti päivitettyjen tapahtumien mukaan. Seuraavassa kuvassa havainnollistamme FIFO-varastointimallia tässä tapahtumasarjassa, kun**Sisällytä fyysinen arvo** -asetus on käytössä. ![FIFO - fyysinen arvo sisällytetään](./media/fifowithincludephysicalvalue.gif) 

**Kaavion selite**

-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
-   Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Varastotapahtuman arvo, joka ei ole sulkeissa, tarkoittaa, että varastotapahtuma on kirjattu varastoon kirjanpidollisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="fifo-with-marking"></a>FIFO ja merkintä
Merkintä on prosessi, jonka avulla voit linkittää (eli merkitä) varaston ottotapahtuman vastaanottotapahtumaan. Merkintä voi tapahtua joko ennen tapahtuman kirjaamista tai sen jälkeen. Merkinnän avulla voit varmistaa tarkan varastokustannuksen, kun tapahtuma kirjataan tai kun varaston sulkeminen suoritetaan. Oletetaan esimerkiksi, että asiakaspalveluosasto on hyväksynyt kiireellisen tilauksen tärkeältä asiakkaalta. Koska tilaus on kiireellinen, tästä nimikkeestä on maksettava tavallista enemmän, jotta asiakkaan pyynnön voi toteuttaa. Sinun on varmistettava, että tämän varastonimikkeen kustannus otetaan huomioon myyntitilauslaskun katteessa (tai myydyn tavaran kustannuksissa). Kun ostotilaus kirjataan, varasto vastaanotetaan hintaan 120,00 USD. Jos tämä myyntitilausasiakirja on merkitty ostotilaukseen ennen pakkausluettelon tai laskun kirjaamista, myydyn tavaran kustannukseksi tulee 120,00 USD nimikkeen nykyisen käyttökeskiarvokustannuksen sijaan. Jos myyntitilauksen pakkausluettelo tai lasku kirjataan ennen merkintää, myydyn tavaran kustannus kirjataan käyttäen käyttökeskiarvon mukaista kustannushintaa. Ennen varaston sulkemista nämä kaksi tapahtumaa voidaan vielä merkitä toisiinsa. Kun vastaanottotapahtuma vastaa varasto-ottotapahtumaa, nimikkeen malliryhmässä määritetty arvostustapa ohitetaan, ja järjestelmä täsmäyttää nämä tapahtumat toisiaan vasten. Voit merkitä varastostaottotapahtuman vastaanottoon kirjauksen jälkeen. Voit tehdä tämän myyntitilausrivin **Myyntitilauksen tiedot** -sivulla. Voit tarkastella avoimia vastaanottotapahtumia **Merkintä**-sivulla. Voit merkitä varastostaottotapahtuman vastaanottoon myös tapahtuman kirjauksen jälkeen. Voit täsmäyttää tai merkitä varastostaottotapahtuman varastoidun nimikkeen avoimeen vastaanottotapahtumaan kirjatusta varaston oikaisukirjauskansiosta. Seuraavassa on kuvattu näitä tapahtumia:

-   1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   3a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
-   4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   4b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   5a. Varaston fyysinen varastostaotto määrälle 1 yksikkökustannushintaan 21,25 USD (taloudellisten ja fyysisten päivitettyjen tapahtumien käyttökeskiarvo).
-   5b. Varaston taloudellinen vastaanotto määrälle 1 merkitään varaston vastaanottoon 2b ennen tapahtuman kirjaamista. Tapahtuma kirjataan, ja sen kappalekohtainen kustannushinta on 20,00 Yhdysvaltain dollaria (USD).
-   6a. Varaston fyysinen varastostaotto määrälle 1 yksikkökustannushintaan 21,25 USD.
-   7. Varaston sulkeminen on suoritettu. Koska taloudellisesti päivitetty FIFO-tapahtuma on merkitty vastaanottoon, nämä tapahtumat täsmäytetään toisiaan vasten, eikä oikaisua tehdä.

Uusi kustannushinnan käyttökeskiarvo 27,50 USD on laskettu taloudellisesti ja fyysisesti päivitettyjen tapahtumien mukaan. Seuraavassa kuvassa havainnollistetaan FIFO-varastomallin käyttämisen vaikutus tähän tapahtumien sarjaan kun merkintä varasto-ottojen ja vastaanottojen välillä on käytössä. ![FIFO merkinnän kanssa](./media/fifowithmarking.gif) 

**Kaavion selite**

-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
-   Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Varastotapahtuman arvo, joka ei ole sulkeissa, tarkoittaa, että varastotapahtuma on kirjattu varastoon kirjanpidollisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.





