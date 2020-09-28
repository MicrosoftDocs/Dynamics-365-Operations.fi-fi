---
title: Liukuva keskiarvo
description: Liukuva keskiarvo on keskiarvon periaatteeseen perustuva pysyvä kustannuslaskentamenetelmä, jossa varasto-ottojen kustannukset eivät muutu, vaikka ostokustannus muuttuu. Ero aktivoidaan. Se perustuu suhteelliseen laskelmaan. Jäljelle jäävä summa siirretään kuluksi.
author: AndersGirke
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40cb135c285afb4466f36dbe637368829fec196f
ms.sourcegitcommit: 097e92f4da7ed9c33f8eb0a7e09969260c399446
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763606"
---
# <a name="moving-average"></a>Liukuva keskiarvo

[!include [banner](../includes/banner.md)]

Liukuva keskiarvo on keskiarvon periaatteeseen perustuva pysyvä kustannuslaskentamenetelmä, jossa varasto-ottojen kustannukset eivät muutu, vaikka ostokustannus muuttuu. Ero aktivoidaan. Se perustuu suhteelliseen laskelmaan. Jäljelle jäävä summa siirretään kuluksi.

Kun käytössä on liukuva keskiarvo, varastotilityksiä ja varastomerkintöjä ei tueta. Varaston sulkeminen ei vaikuta tuotteisiin, joilla on liukuva keskiarvo varastomalliryhmänä. Sulkeminen ei luo tapahtumien välille tilityksiä.

Liukuvan keskiarvon kustannuksen käyttöä kustannuslaskennassa koskevat seuraavat edellytykset.

1. Määritä **Nimikemalliryhmät**-sivulla nimikemalliryhmä, jolle on valittu **Liukuva keskiarvo** -asetus **Varastomalli**-kentästä.

    > [!NOTE]
    > Kun **Liukuva keskiarvo** -asetus valitaan, oletusarvoisesti myös **Kirjaa varastotilanne**- ja **Kirjaa kirjanpitovarasto** -kentät tulevat valituiksi.

1. Määritä **Kirjaus**-sivulla tilit **Liukuvan keskiarvon hintaero** -kohtaan. Voit käyttää **Liukuvan keskiarvon hintaero** -tiliä, kun kustannus on kirjattava suhteellisesti. Tämä tapahtuu seuraavissa kahdessa skenaariossa:
    - Syynä tähän on ostotilauksen vastaanoton ja ostolaskun välinen kustannusten erotus sekä alkuperäisen varastomäärän ja käytettävissä olevan määrän välinen erotus.
    - Tapahtumat tuovat varaston negatiivisesta nollaan. Tapahtumakustannuksen ja nykyisen liukuvan keskimääräisen kustannuksen välillä on ero.

1. Määritä **Kirjaus**-sivulla tilit **Liukuvan keskiarvon kustannuksen uudelleenarvostu** -tileille **Varasto**-välilehdessä. Voit käyttää **Liukuvan keskiarvon kustannuksen uudelleenarvostus** -tiliä, jos haluat oikaista liukuvan keskiarvon kustannuksen tuotteelle, jolla on uusi yksikköhinta.

1. Lisää **Vapautetut tuotteet** -sivulla liukuvan keskiarvon nimikemalliryhmä tuotteeseen.

    > [!NOTE]
    > Varaston sulkemisprosessi sulkee vain tilikauden. Se ei vaikuta tuotteisiin, joihin on lisätty liukuva keskiarvo nimikemalliryhmänä.

## <a name="convert-to-the-moving-average-costing-method"></a>Muuntaminen liukuvan keskiarvon kustannuslaskentamenetelmään

Tuotteet voidaan muuttaa käyttämään liukuvan keskiarvon varastonarvostusmenetelmää. Tämäntyyppinen muunto tehdään tavallisesti vuoden lopussa sen jälkeen, kun kuluvan vuoden viimeinen kuukausi on suljettu. Muunnossa käytetään tuotteen nykyistä kustannuslaskentamallia. Voit vaihtaa varaston kustannuslaskentamenetelmän keskimääräiseen tai standardikustannukseen perustuvasta liukuvaan keskiarvoon perustuvaan menetelmään.

Jos vaihdat kustannuslaskentamenetelmän standardikustannuksesta liukuvan keskiarvon menetelmään, sinun täytyy suorittaa seuraavat tehtävät:

1. Muuta varastomäärät ja -arvot nollaan.
1. Kun varastoarvo ja -määrä ovat nollassa (0), muuta nimikemalliryhmä käyttämään liukuvaa keskiarvoa.
1. Muuta määrä ja arvo takaisin varastoon.

Et voi muuttaa varaston kustannuslaskentamenetelmää liukuvan keskiarvon menetelmästä FIFO- tai LIFO-menetelmäksi tai painotetun keskiarvon menetelmäksi.

> [!NOTE]
> Muuntaminen standardikustannuksesta liukuvan painotetun keskiarvon menetelmään tapahtuu manuaalisesti.

Seuraavissa esimerkeissä on kuvattu liukuvan keskiarvon kustannuslaskentamenetelmän vaikutus. Määrityksiä on neljä:

- Ostotilauksen ja suhteellisesti kirjattujen kustannusten ero
- Liukuvan keskiarvon tuote ja varaston oikaisu
- Liukuva keskiarvo ja tuotanto
- Liukuva keskiarvo ja takautuva tapahtuma.

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Ostotilauksen ja suhteellisesti kirjattujen kustannusten ero

Liukuvaa keskiarvoa käytettäessä tuotteen kustannukset määräytyvät oston vastaanoton mukaan. Jos ostolaskua kirjattaessa oston vastaanoton ja ostolaskun välisissä kustannuksissa on eroa, ero oikaistaan suhteellisesti nykyisiksi varastossa oleviksi tuotteiksi ja loppusumma kirjataan kuluksi.

Tässä esimerkissä ostotilausta luotaessa ja vastaanotettaessa kirjataan yksi kustannus ja ostolaskusta eri kustannus.

1. Luo ostotilaus, jonka määrä on 2 ja yksikköhinta 10,00.
1. Luo tuotteen ostokuittaus.
1. Luo myyntitilaus, jonka määrä on 1 ja yksikköhinta 10,00.
1. Luo ostolasku, jonka määrä on 2 ja yksikköhinta 12,00.

Yksikköhinnan 2,00 erotus kirjataan liukuvan keskiarvon hintaeron tilille ostolaskun kirjaamisen yhteydessä. Syynä tähän on se, että tuotteita ostettiin kaksi, ja ostokustannukset olivat 20,00. Toinen tuote myytiin yksikköhintaan 10,00. Ostolaskulle kirjattiin yksikköhinnaksi 12,00 ja määräksi 2. Tuotteen yksikköhinnaksi ei voi kirjata 14,00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Liukuvan keskiarvon tuote ja varaston oikaisu

Jos tuotteen liukuvan keskiarvon kustannusta täytyy oikaista, varaston oikaisuja voi tehdä kuluvasta päivästä lukien. Tuotteen liukuvan keskiarvon kustannusta ei voi korjata tekemällä varaston oikaisua takautuvasti. Kustannus eivät voi siirtyä seuraaviin tapahtumiin.

Tässä esimerkissä oikaistaan tuotteen liukuvan keskiarvon kustannusta.

1. Valitse tuote, jonka liukuvan keskiarvon kustannusta haluat oikaista. 

 > [!NOTE]
 > **Liukuvan keskiarvon uudelleenarvostus** -sivu tarkistaa tuotteen käytettävissä olevan varaston. Valitun tuotteen kirjattu määrä on 1, kirjattu arvo 12,00, kirjattu yksikkökustannus 12,00 ja yksikkökustannus 12,00.
    
1. Päivitä **Yksikkökustannus**-kentän arvoksi 16,00. Järjestelmä laskee muut kentät.
1. Oikaisu kirjataan.

> [!NOTE]
> Liukuvan keskiarvon kustannusta voi oikaista vain kuluvasta päivämäärästä lukien.

**Tositteen täsmäytykset** -sivulla näkyy oikaisu 4,00, joka on kirjattu Liukuvan keskiarvon kustannuksen uudelleenarvostus -tilille.

## <a name="moving-average-with-production"></a>Liukuva keskiarvo ja tuotanto

Liukuva keskiarvo tukee valmistettuja nimikkeitä. Jos aiot käyttää liukuvaa keskiarvoa tuotantoympäristössä, valitse **Tuotannonhallinnan parametrit** -sivulla oleva **Käytä arvioitua kustannushintaa** -liukusäädin. Tämä tarkoittaa sitä, että todellisen tuoterakennelaskennan kustannushinnan sijasta käytetään arvioinnin aikana laskettua kustannushintaa.

## <a name="moving-average-with-a-backdated-transaction"></a>Liukuva keskiarvo ja takautuva tapahtuma.

Takautuville tapahtumille määritetään nykyinen liukuvan keskiarvon kustannus ja tuotteen fyysinen määrä päivittyy, mutta tämä ei vaikuta tuotteen liukuvan keskiarvon kustannukseen. Tässä liukuvaa keskiarvoa koskevassa esimerkissä kirjataan liukuvan keskiarvon tuotteeseen liittyvä takautuva tapahtuma.

1. Luo liukuvan keskiarvon tuotteelle varaston oikaisu, jonka määrä on 1 ja kustannus 20,00.
1. Tuotteen varastotapahtumahistoria näyttää tällöin seuraavalta:
    - Varastotapahtuma, määrä 1, kustannus 16,00, kirjauspäivämäärä 15.1. ja tapahtumapäivämäärä 15.1.
    - Varaston oikaisu, määrä 1, kustannus 20,00, kirjauspäivämäärä 1.1. ja tapahtumapäivämäärä 15.1.
1. Kirjaa oikaisu.

**Varastotapahtumat**-sivulla näkyy, että kirjattu kulu on 4,00, sillä tuotteen nykyinen liukuva keskiarvo on 16,00. Voit tehdä kirjauksen aiempaan ajankohtaan, mutta kustannuksen erotus kirjataan, joten se ei vaikuta liukuvan keskiarvon kustannukseen.

## <a name="negative-inventory-balances"></a>Negatiiviset varastosaldot

Tapahtumia käsitellään eri tavoin sen mukaan, onko uusi käytettävissä oleva määrä tapahtuman jälkeen negatiivinen, nolla vai positiivinen.

### <a name="new-balance-is-negative-or-zero"></a>Uusi saldo on negatiivinen tai nolla

Jos uusi käytettävissä oleva määrä on negatiivinen tai nolla, tapahtuman hinta lasketaan nykyisten keskimääräisten kustannusten mukaan. Jos ostohinta ja nykyiset keskimääräiset kustannukset eroavat toisistaan, ero kirjataan **Liukuvan keskiarvon hintaero** -kohtaan.

### <a name="new-balance-is-positive"></a>Uusi saldo on positiivinen

Jos uusi käytettävissä oleva määrä on positiivinen tapahtuman jälkeen, tapahtuma jaetaan kahteen osaan ja se lasketaan eri tavalla, kuten seuraavan taulukon yhteenvedossa on näkyvissä.

| Osa | kuvaus |
|---|---|
| Määrä negatiivisesta nollaan | Varasto käyttää nimikkeen nykyistä liukuvaa keskimääräistä kustannusta mieluummin kuin sen vastaaonttomäärän osan tapahtumakustannusta, joka lisää käytettävissä olevaa saldoa negatiivisesta nollaan. Tapahtuman kustannus ja nykyiset liukuvat keskimääräiset kustannukset eroavat toisistaan. Ero kirjataan **Liukuvan keskiarvon hintaero** -kohtaan. |
| Määrä nollasta positiiviseen | Varasto käyttää vastaanottomäärän tapahtumakustannusta siinä osassa, joka lisää käytettävissä olevan saldon nollasta positiiviseen.                                                  |

## <a name="inventory-value-report"></a>Varaston arvon raportti

Tässä liukuvaa keskiarvoa koskevassa esimerkissä varastoarvon raportti tulostetaan tueksi tuotteen nykyisen liukuvan keskiarvon laskennassa. Varastoarvon raportti voi tulostaa tapahtumat aikajärjestyksessä yhdessä kustannusten kanssa tuotteen liukuvan keskiarvon kustannuslaskennan tueksi. Raportissa näkyy tuotteen liukuvan keskiarvon kustannus. **Varastoarvon raportit** -valintaikkunassa olevan päivämäärävälin avulla voit valita **Tapahtuman aika**- tai **Kirjauspäivämäärä**-vaihtoehdon, jonka perusteella raportti lajitellaan. Raportti tulostetaan perinteisesti **Kirjauspäivämäärä**-vaihtoehdon mukaan. **Tapahtuman aika** -vaihtoehto on päivämäärä, jolta tapahtuma raportoidaan ja jona tuotteen liukuvan keskiarvon kustannus päivitetään. Voit tulostaa varastoarvon raportin käyttämällä **Lajittelu tapahtuman ajan mukaan** -vaihtoehtoa, jos haluat nähdä liukuvan keskiarvon kustannuslaskennan tietyltä aikaväliltä. Seuraavassa taulukossa näkyvät tuotteen tapahtumat, joista raportti tulostetaan, kun **Lajittelu tapahtuman ajan mukaan** -vaihtoehto on käytössä.

| Tapahtuman aika | Päivämäärä         | Tapahtumatyyppi           | Määrä | Summa | Keskimääräinen yksikkökustannus |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. lokakuuta    | Alkusaldo          | 0        | 0,00   | 0,00              |
| 8. lokakuuta        | 28. syyskuuta | Takautuva vastaanotto          | 1        | 16,00  | 16,00             |
| 3. lokakuuta        | 3. lokakuuta    | Oston vastaanotto           | 2        | 20,00  | 12,00             |
| 5. lokakuuta        | 5. lokakuuta    | Myyntitilaus                | -1       | –10,00 | 13,00             |
| 7. lokakuuta        | 7. lokakuuta    | Ostolasku           |          | 2,00   | 14,00             |
| 8. lokakuuta        | 8. lokakuuta    | Liukuvan keskiarvon uudelleenarvostus |          | 4.00   | 16.00             |
|                  | 31. lokakuuta   | Yhteensä                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> Kirjanpitoa ei voi täsmäyttää varaston kanssa käyttämällä **Tapahtuma-ajan lajittelu** -vaihtoehtoa. Raportti täytyy tulostaa käyttämällä **Kirjauspäivämäärä**-vaihtoehtoa.
