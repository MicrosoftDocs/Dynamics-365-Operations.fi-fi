---
title: "LIFO-päivämäärä, fyysinen arvo ja merkintä"
description: "LIFO-päivämäärä on varastomalli, joka perustuu LIFO-periaatteeseen. Varasto-otot täsmäytetään viimeisiä varastovastaanottoja vasten varastotapahtuman päivämäärän perusteella. Jos LIFO-päivämäärä on määritetty eikä ennen ottoa ei ole vastaanottoa, otto täsmäytetään oton päivämäärän jälkeen tapahtuneiden vastaanottojen mukaan. Jos samana päivänä on useita ottoja, ne täsmäytetään järjestyksessä viimeinen otto, viimeinen vastaanotto."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0b94d3f23c929c45a67894bd08706144c9226491
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO-päivämäärä, fyysinen arvo ja merkintä

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

LIFO-päivämäärä on varastomalli, joka perustuu LIFO-periaatteeseen. Varasto-otot täsmäytetään viimeisiä varastovastaanottoja vasten varastotapahtuman päivämäärän perusteella. Jos LIFO-päivämäärä on määritetty eikä ennen ottoa ei ole vastaanottoa, otto täsmäytetään oton päivämäärän jälkeen tapahtuneiden vastaanottojen mukaan. Jos samana päivänä on useita ottoja, ne täsmäytetään järjestyksessä viimeinen otto, viimeinen vastaanotto. 

Jos käytät LIFO-päivämäärään perustuvaa varastomallia eikä ennen varastostaottoa ole vastaanottoa, varastostaotto täsmäytetään oton päivämäärän jälkeen tapahtuneita vastaanottoja vastaan. Jos samana päivänä on useita varastostaottoja, ne voidaan täsmäyttää järjestyksessä viimeinen otto, viimeinen vastaanotto. Kun käytät LIFO-päivämäärää, LIFO-päivämääräsääntöä ei tarvitse noudattaa. Sen sijaan voit merkitä varastotapahtumat niin, että tietyn nimikkeen vastaanotto selvitetään tiettyä varastostaottoa vasten. 

Varaston kausittainen sulkeminen on suositeltavaa käytettäessä LIFO-päivämäärä-varastomallia. 

Seuraavissa esimerkeissä on esitetty LIFO-päivämäärän käyttämisen vaikutus kolmea eri määritystä käytettäessä:

-   LIFO-päivämäärä ilman **Sisällytä fyysinen arvo** -asetusta
-   LIFO-päivämäärä, kun **Sisällytä fyysinen arvo** -asetus on käytössä
-   LIFO-päivämäärä käyttäen merkintää

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-päivämäärä ilman Sisällytä fyysinen arvo -asetusta
Tässä esimerkissä nimikemalliryhmää ei ole merkitty sisällyttämään fyysistä arvoa. Seuraavassa on kuvattu näitä tapahtumia:

-   1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   3a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
-   4a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 15,00 USD (taloudellisesti päivitettyjen tapahtumien käyttökeskiarvo).
-   4b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 15,00 USD (taloudellisesti päivitettyjen tapahtumien käyttökeskiarvo).
-   5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   6. Varaston sulkeminen on suoritettu. LIFO-päivämäärämenetelmän mukaan viimeksi taloudellisesti päivitetty varastostaotto täsmäytetään päivämäärän perusteella viimeksi taloudellisesti päivitettyä vastaanottoa vastaan. Varastostaottotapahtumalle tehdään oikaisu, jonka summa on 5,00 USD. Nämä tapahtumat täsmäytetään toisiinsa.

Uusi kustannushinnan käyttökeskiarvo 15,00 USD on laskettu taloudellisesti päivitettyjen tapahtumien mukaan. 

Seuraavassa on kuvattu LIFO-päivämäärään perustuvan varastomallin vaikutusta, kun **Sisällytä fyysinen arvo** -asetusta ei käytetä. ![LIFO-päivämäärä - fyysinen arvo sisällytetään](./media/lifodatewithoutincludephysicalvalue.gif) 

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
- Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
- Varastotapahtuman arvo, joka ei ole sulkeissa, tarkoittaa, että varastotapahtuma on kirjattu varastoon kirjanpidollisesti.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-päivämäärä käyttäen Sisällytä fyysinen arvo -asetusta
Voit valita nimikkeelle **Sisällytä fyysinen arvo** -asetuksen **Nimikemalliryhmät**-sivulta. Tällöin järjestelmä käyttää sekä fyysisiä että taloudellisia vastaanottotapahtumia kustannushinnan käyttökeskiarvon laskemiseen. Järjestelmä tekee myös oikaisuja fyysisesti päivitettyyn varastostaottotapahtumaan, jos tämä on aiheellista. Jos **Sisällytä fyysinen arvo** -valintaruudun valinta poistetaan, varaston sulkeminen LIFO-päivämäärään perustuvaa varastomallia käyttämällä täsmäyttää vain kirjanpidollisesti päivitetyt tapahtumat. 

Tässä esimerkissä nimikemalliryhmä on merkitty sisällyttämään fyysinen arvo. 

Seuraavassa on kuvattu näitä tapahtumia:

-   1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
-   3a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
-   4a. Varaston fyysinen varastostaotto määrälle 1 yksikkökustannushintaan 18,33 USD (taloudellisesti päivitettyjen tapahtumien käyttökeskiarvo).
-   4b. Varaston taloudellinen varastostaotto määrälle 1 yksikkökustannushintaan 18,33 USD (taloudellisesti päivitettyjen tapahtumien käyttökeskiarvo).
-   5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
-   6. Varaston sulkeminen on suoritettu. LIFO-päivämäärämenetelmän mukaan viimeksi päivitetty varastostaotto oikaistaan tai täsmäytetään päivämäärän perusteella viimeksi päivitettyä vastaanottoa vastaan. Näitä tapahtumia ei täsmäytetä toisiinsa, sillä taloudellinen vastaanottotapahtuma on oikaistu fyysisen päivitystapahtuman mukaan. Sen sijaan varastostaottotapahtumalle tehdään vain oikaisu, jonka arvo on 6,67 USD.

Uusi kustannushinnan käyttökeskiarvo 20,00 USD on laskettu taloudellisesti päivitettyjen tapahtumien mukaan. 

Seuraavassa on kuvattu LIFO-päivämäärään perustuvan varastomallin vaikutusta, kun **Sisällytä fyysinen arvo** -asetus on käytössä. ![LIFO-päivämäärä - fyysinen arvo sisällytetään](./media/lifodatewithincludephysicalvalue.gif) 

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
- Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
- Varastotapahtuman arvo, joka ei ole sulkeissa, tarkoittaa, että varastotapahtuma on kirjattu varastoon kirjanpidollisesti.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="lifo-date-with-marking"></a>LIFO-päivämäärä käyttäen merkintää
Merkintä on prosessi, jonka avulla voit linkittää (eli merkitä) varaston ottotapahtuman vastaanottotapahtumaan. Merkintä voi tapahtua joko ennen tapahtuman kirjaamista tai sen jälkeen. Merkinnän avulla voit varmistaa tarkan varastokustannuksen, kun tapahtuma kirjataan tai kun varaston sulkeminen suoritetaan. 

Oletetaan esimerkiksi, että asiakaspalveluosasto on hyväksynyt kiireellisen tilauksen tärkeältä asiakkaalta. Koska tilaus on kiireellinen, tästä nimikkeestä on maksettava tavallista enemmän, jotta asiakkaan pyynnön voisi toteuttaa. Sinun on varmistettava, että tämän varastonimikkeen kustannus otetaan huomioon myyntitilauslaskun katteessa (tai myydyn tavaran kustannuksissa). 

Kun ostotilaus kirjataan, varasto vastaanotetaan hintaan 120,00 USD. Jos tämä myyntitilausasiakirja on merkitty ostotilaukseen ennen pakkausluettelon tai laskun kirjaamista, myydyn tavaran kustannukseksi tulee 120,00 USD nimikkeen nykyisen käyttökeskiarvokustannuksen sijaan. Jos myyntitilauksen pakkausluettelo tai lasku kirjataan ennen merkintää, myydyn tavaran kustannus kirjataan käyttäen käyttökeskiarvon mukaista kustannushintaa. 

Ennen varaston sulkemista nämä kaksi tapahtumaa voidaan vielä merkitä toisiinsa. 

Esimerkki: Varastostaottotapahtuma merkitään varastostaottotapahtumalle. Tässä tapauksessa nimikkeen nimikemalliryhmässä määritetty arvostusmenetelmä ohitetaan, ja järjestelmä täsmäyttää nämä tapahtumat keskenään. 

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
-   7. Varaston sulkeminen on suoritettu. Koska taloudellisesti päivitetty FIFO-tapahtuma on merkitty aiempaan vastaanottoon, nämä tapahtumat täsmäytetään toisiinsa, eikä oikaisua tehdä.

Uusi kustannushinnan käyttökeskiarvo 27,50 USD on laskettu taloudellisesti ja fyysisesti päivitettyjen tapahtumien mukaan. 

Seuraavassa on kuvattu LIFO-varastomallin vaikutusta, kun käytetään varastostaottojen ja vastaanottojen välistä merkintää. ![LIFO-päivämäärä merkinnän kanssa](./media/lifodatewithmarking.gif) 

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa Quantity@Unitprice.
- Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
- Varastotapahtuman arvo, joka ei ole sulkeissa, tarkoittaa, että varastotapahtuma on kirjattu varastoon kirjanpidollisesti.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.





