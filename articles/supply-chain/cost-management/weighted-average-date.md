---
title: Painotetun keskiarvon päivämäärä
description: Painotetun keskiarvon päivämäärä on painotetun keskiarvon periaatteeseen perustuva varastomalli, jossa varasto-otot arvotetaan varastoon vastaanotettujen nimikkeiden keskiarvon mukaan kunakin erillisenä päivänä varaston sulkemiskauden aikana.
author: AndersGirke
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9990df3e57d65c77a75913efaf30675528d411b4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343697"
---
# <a name="weighted-average-date"></a>Painotetun keskiarvon päivämäärä

[!include [banner](../includes/banner.md)]

Painotetun keskiarvon päivämäärä on varastomalli, joka perustuu painotetun keskiarvon periaatteeseen. Painotetun keskiarvon periaatteessa varasto-otot arvotetaan varastoon vastaanotettujen nimikkeiden keskiarvon mukaan kunakin päivänä varaston sulkemiskauden aikana. 

Kun suoritat varaston sulkemisen käyttämällä painotetun keskiarvon päivämäärää, kaikki päivittäiset vastaanotot täsmäytetään virtuaaliseen varasto-ottoon. Virtuaalinen varasto-otto sisältää kyseisenä päivänä vastaanotetun kokonaismäärän ja -arvon. Tähän virtuaalivarasto-ottoon liittyy vastaava virtuaalivastaanotto, josta varasto-otot selvitetään. Näin kaikille varastostaotoille tulee sama keskimääräinen kustannus. Virtuaalivarastostaoton ja -vastaanoton voi nähdä virtuaalisiirtona, jota kutsutaan *painotetun keskiarvon varastonsulkemissiirroksi*. 

Jos ennen määrättyä päivämäärää on tapahtunut vain yksi vastaanotto, keskiarvoa ei tarvita. Koska kaikki varasto-otot selvitetään kyseisestä vastaanotosta, virtuaalisiirtoa ei voi luoda. Samoin jos kyseisenä päivänä tapahtuu vain varasto-ottoja, ei ole vastaanottoja, joista keskiarvo laskettaisiin, eikä virtuaalisiirtoa siis luoda. Sen sijaan voit painotetun keskiarvon päivämäärää käyttäessäsi merkitä varastotapahtumat niin, että tietyn nimikkeen vastaanotto selvitetään tiettyä varastostaottoa vasten. Tällöin et käytä painotetun keskiarvon päivämääräsääntöä. On suositeltavaa sulkea varasto kuukausittain, kun käytetään painotetun keskiarvon päivämäärän varastomallia. 

Painotetun keskiarvon päivämäärän varaston kustannuslaskentamenetelmä lasketaan seuraavan kaavan mukaan: 

Painotettu keskiarvo = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*) 

Varaston sulkemisen aikana laskenta suoritetaan päivittäin seuraavan kuvan esittämällä tavalla. 

![Painotetun keskiarvon päivämäärän päivittäislaskentamalli.](./media/weightedaveragedatedailycalculationmodel.gif) 

Varasto-otoista lähtevät varastotapahtumat, mukaan lukien myyntitilaukset, varastokirjauskansiot, ostohyvityslaskut ja tuotantotilaukset, tapahtuvat kirjauspäivämääränä ja arvioidun kustannushinnan mukaisina. Tähän arvioituun kustannushintaan viitataan myös termillä kustannushinnan käyttökeskiarvo. Varaston sulkupäivämääränä järjestelmä analysoi edellisten kausien, edellisten päivien ja kuluvan päivän varastotapahtumat. Tämän analyysin avulla määritetään, kumpaa seuraavista sulkemisperiaatteista käytetään:

-   Suora täsmäytys
-   yhteenvetotäsmäytys.

Selvitykset ovat varaston sulkemiskirjauksia, jotka säätävät varastostaotot sulkemispäivän oikean painotetun keskiarvon mukaisiksi. 

**Huomautus:** Lisätietoja selvityksistä on varaston sulkuja koskevassa artikkelissa. Seuraavissa esimerkeissä kuvataan painotetun keskiarvon käytön vaikutusta viidessä eri konfiguraatiossa:

-   Painotetun keskiarvon päivämäärän suora selvitys ilman **Sisällytä fyysinen arvo** -asetusta
-   Painotetun keskiarvon päivämäärän yhteenvetoselvitys ilman **Sisällytä fyysinen arvo** -asetusta
-   Painotetun keskiarvon päivämäärän suora selvitys **Sisällytä fyysinen arvo** -asetuksella
-   Painotetun keskiarvon päivämäärän yhteenvetoselvitys **Sisällytä fyysinen arvo** -asetuksella
-   Painotetun keskiarvon päivämäärä käyttäen merkintää

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Painotetun keskiarvon päivämäärän suora selvitys ilman Sisällytä fyysinen arvo -asetusta
Nykyisessä versiossa käytettävä suora täsmäytysperiaate on sama kuin aiemmissa versioissa käytetty painotetun keskiarvon periaate. Järjestelmä tekee suoran selvityksen vastaanottojen ja varastostaottojen välillä. Järjestelmä käyttää tätä suoran selvityksen periaatetta määrätyissä tilanteissa:

-   Kauden aikana on kirjattu yksi vastaanotto ja vähintään yksi varastostaotto.
-   Kauden aikana on kirjattu vain varastostaottoja, ja varasto sisältää käytettävissä olevia nimikkeitä aiemmasta sulkemisesta.

Seuraavassa esimerkkitilanteessa on kirjattu vastaanotto ja varastostaotto, jotka on päivitetty kirjanpitoon. Varaston sulkemisen aikana järjestelmä selvittää vastaanoton suoraan varastostaottoa vasten, eikä varastostaottoa varten tarvita kustannushinnan muutosta. 

Seuraavassa on kuvattu näitä tapahtumia:

-   1a. Fyysinen varastovastaanottopäivitys. Määrä on 5 ja kappalehinta 10,00 Yhdysvaltain dollaria (USD).
-   1b. Rahoituksellinen varastovastaanottopäivitys. Määrä on 5 ja kappalehinta 10,00 Yhdysvaltain dollaria (USD).
-   2a. Varaston fyysinen varastostaotto päivitetty määrälle 2 yksikkökustannuksen ollessa 10,00 USD.
-   2b. Varaston taloudellinen varastostaotto päivitetty määrälle 2 yksikkökustannuksen ollessa 10,00 USD.
-   3. Varaston sulkeminen toteutettiin käyttämällä suoran selvityksen menetelmää varaston taloudellisen vastaanoton ja varaston taloudellisen varastostaoton väliseen selvitykseen.

![Painotetun keskiarvon päivämäärän suora selvitys ilman Sisällytä fyysinen arvo -asetusta.](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) 

**Kuvan selitys:**

-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa *määrä*@*yksikköhinta*.
-   Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Ilman sulkeita esitetty varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon taloudellisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Painotetun keskiarvon päivämäärän yhteenvetoselvitys ilman Sisällytä fyysinen arvo -asetusta
Painotettu keskiarvo perustuu periaatteelle, että kaikista sulkemiskauden vastaanotoista tehdään yhteenveto uuteen varastonsiirtotapahtumaan. Tapahtumaa kutsutaan *painotetun keskiarvon varaston sulkemiseksi*. Kaikki päivän vastaanotot selvitetään tämän luodun uuden varastosiirtotapahtuman varastostaottoa vasten. Kaikki päivän varastostaotot selvitetään luodun uuden varastosiirtotapahtuman vastaanottoa vasten. Jos käytettävissä oleva varasto on varaston sulkemisen jälkeen positiivinen, käytettävistä olevasta varastosta ja varaston arvosta tehdään yhteenveto uuteen varastosiirtotapahtumaan (vastaanotto). Jos käytettävissä oleva varasto on varaston sulkemisen jälkeen negatiivinen, käytettävissä oleva varasto ja varaston arvo ovat sellaisten yksittäisten varastostaottojen summa, joita ei ole täysin selvitetty. 

Seuraavassa esimerkkitilanteessa on kirjattu useita vastaanottoja ja varastostaottoja, jotka on päivitetty kirjanpitoon kauden aikana. Varaston sulkemisen yhteydessä järjestelmä arvioi jokaisen päivän ja määrittää, miten sitä tulee käsitellä sulkemisessa. 

Seuraavassa on kuvattu näitä tapahtumia: 

**1. päivä:**

-   1a. Fyysinen varastovastaanottopäivitys. Määrä on 3 ja kappalehinta 15,00 Yhdysvaltain dollaria (USD).
-   1b. Rahoituksellinen varastovastaanottopäivitys. Määrä on 3 ja kappalehinta 15,00 Yhdysvaltain dollaria (USD).
-   2a. Varaston fyysinen varastostaotto määrälle 1 kustannuksen käyttökeskiarvolla 15,00 USD.
-   2b. Varaston taloudellinen varastostaotto määrälle 1 kustannuksen käyttökeskiarvolla 15,00 USD.

Järjestelmä käyttää suoran selvityksen menetelmää päivälle 1. 

**2. päivä:**

-   3a. Varaston fyysinen varastostaotto määrälle 1 kustannuksen käyttökeskiarvolla 15,00 USD
-   3b. Varaston taloudellinen varastostaotto määrälle 1 kustannuksen käyttökeskiarvolla 15,00 USD

Järjestelmä käyttää suoran selvityksen menetelmää päivälle 2. 

**3. päivä:**

-   4a. Varaston fyysinen varastostaotto määrälle 1 kustannuksen käyttökeskiarvolla 15,00 USD
-   4b. Varaston taloudellinen varastostaotto määrälle 1 kustannuksen käyttökeskiarvolla 15,00 USD
-   5a. Varaston fyysinen vastaanotto määrälle 1 yksikköhintaan 17,00 USD
-   5b. Varaston taloudellinen vastaanotto määrälle 1 yksikköhintaan 17,00 USD

Varaston sulkeminen on suoritettu. Suoraa selvitystä on käytettävä, koska vastaanottoja on useita usean päivän aikana.

-   7a. Painotetun keskiarvon varaston sulkemistapahtuman taloudellinen varastostaotto luodaan määrälle 2 hintaan 32,00 USD. Näin muodostetaan yhteenveto kaikista tähän päivämäärään mennessä tapahtuneista varaston taloudellisista vastaanotoista, joita ei ole vielä suljettu.
-   7b. Painotetun keskiarvon varaston sulkemistapahtuman taloudellinen vastaanotto luodaan vastatapahtumaksi tapahtumalle 7a.

Järjestelmä luo ja kirjaa yhteenvetovarastosiirron tapahtuman. Lisäksi järjestelmä selvittää kaikki päivän vastaanotot ja edellisten päivien käytettävissä olevan varaston yhteenvetovarastosiirron varastostaottotapahtumaa vasten. Kaikki päivän varastostaotot selvitetään yhteenvetovarastosiirron vastaanottotapahtumaa vasten. Painotetuksi keskiarvokustannushinnaksi on laskettu 16,00 USD. Painotettuun keskiarvokustannukseen perustuvaa oikaisua varten tehdään varastostaoton muutos 1,00 USD. Uusi kustannushinnan käyttökeskiarvo on 16,00 USD. 

Seuraava kaavio kuvaa painotetun keskiarvon varastomallin ja yhteenvetotäsmäytyksen vaikutusta tähän tapahtumien sarjaan, kun **Sisällytä fyysinen arvo** -vaihtoehtoa ei käytetä. 

![Painotetun keskiarvon päivämäärän yhteenvetoselvitys ilman Sisällytä fyysinen arvo -asetusta.](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Kuvan selitys:**

-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa *määrä*@*yksikköhinta*.
-   Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Ilman sulkeita esitetty varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon taloudellisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.
-   Punaiset vinottaiset nuolet kuvaavat vastaanottotapahtumia, jotka selvitetään järjestelmän luomia varastostaottotapahtumia vasten.
-   Vihreä vinottainen viiva kuvaa järjestelmän vastatapahtumaksi luomaa vastaanottotapahtumaa, jota vasten alunperin kirjattu varastostaottotapahtuma on selvitetty.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Painotetun keskiarvon päivämäärän suora selvitys Sisällytä fyysinen arvo -asetuksella
Nykyisessä versiossa käytettävä suora täsmäytysperiaate on sama kuin aiemmissa versioissa käytetty painotetun keskiarvon päivämäärän periaate. Järjestelmä tekee suoran selvityksen vastaanottojen ja varastostaottojen välillä. Järjestelmä käyttää tätä suoran selvityksen periaatetta määrätyissä tilanteissa:

-   Kauden aikana on kirjattu yksi vastaanotto ja vähintään yksi varastostaotto.
-   Kauden aikana on kirjattu vain varastostaottoja, ja varasto sisältää käytettävissä olevan varaston aiemmasta sulkemisesta.

Jos **Sisällytä fyysinen arvo** -valintaruutu on valittuna nimikkeen **nimikemalliryhmän** sivulla, järjestelmä käyttää juoksevan arvioidun tai keskimääräisen kustannushinnan laskennassa fyysisesti päivitettyjä vastaanottotapahtumia. Varastostaotot kirjataan tämän arvioidun kustannushinnan perusteella kauden aikana. Varaston sulkemisen aikana vain taloudellisesti päivitetyt vastaanotot otetaan huomioon painotetun keskiarvon laskennassa.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Painotetun keskiarvon päivämäärän yhteenvetoselvitys Sisällytä fyysinen arvo -asetuksella
Jos **Sisällytä fyysinen arvo** -valintaruutu on valittuna nimikkeen **nimikemalliryhmän** sivulla, järjestelmä käyttää juoksevan arvioidun tai keskimääräisen kustannushinnan laskennassa fyysisesti päivitettyjä vastaanottotapahtumia. Varastostaotot kirjataan tämän arvioidun kustannushinnan perusteella kauden aikana. Varaston sulkemisen aikana vain taloudellisesti päivitetyt vastaanotot otetaan huomioon painotetun keskiarvon laskennassa. Painotetun keskiarvon selvittäminen perustuu periaatteelle, jossa kaikista sulkemiskauden vastaanotoista tehdään yhteenveto uuteen varastosiirtotapahtumaan nimeltä *Painotetun keskiarvon varaston sulkeminen*. Kaikki päivän vastaanotot selvitetään tämän luodun uuden varastosiirtotapahtuman varastostaottoa vasten. Kaikki päivän varastostaotot selvitetään luodun uuden varastosiirtotapahtuman vastaanottoa vasten. Jos käytettävissä oleva varasto on varaston sulkemisen jälkeen positiivinen, käytettävistä olevasta varastosta ja varaston arvosta tehdään yhteenveto uuteen varastosiirtotapahtumaan (vastaanotto). Jos käytettävissä oleva varasto on varaston sulkemisen jälkeen negatiivinen, käytettävissä oleva varasto ja varaston arvo ovat sellaisten yksittäisten varastostaottojen summa, joita ei ole täysin selvitetty.

## <a name="weighted-average-date-when-marking-is-used"></a>Painotetun keskiarvon päivämäärä käyttäen merkintää
Merkintä on prosessi, jonka avulla voit yhdistää varaston ottotapahtuman vastaanottotapahtumaan. Merkintä voi tapahtua joko ennen tapahtuman kirjaamista tai sen jälkeen. Merkinnän avulla voit varmistaa tarkan varastokustannuksen, kun tapahtuma kirjataan tai kun varaston sulkeminen suoritetaan. 

Oletetaan esimerkiksi, että yrityksesi asiakaspalveluosasto on hyväksynyt kiireellisen tilauksen tärkeältä asiakkaalta. Koska tilaus on kiireellinen, tästä nimikkeestä on maksettava tavallista enemmän, jotta asiakkaan pyynnön voisi toteuttaa. Sinun on varmistettava, että tämän varastonimikkeen kustannus otetaan huomioon myyntitilauslaskun katteessa (tai myydyn tavaran kustannuksissa). Kun ostotilaus kirjataan, varasto vastaanotetaan hintaan 120,00 USD. Myyntitilausasiakirja on merkitty ostotilaukseen ennen pakkausluettelon tai laskun kirjausta. Tämän jälkeen myytyjen tuotteiden kustannukset ovat 120,00 USD nimikkeen nykyisen keskimääräinen käyttökustannuksen sijaan. Jos myyntitilauksen pakkausluettelo tai lasku kirjataan ennen merkintää, myydyn tavaran kustannus kirjataan käyttäen käyttökeskiarvon mukaista kustannushintaa. Ennen varaston sulkemista nämä kaksi tapahtumaa voidaan vielä merkitä toisiinsa. Kun vastaanottotapahtuma merkitään varasto-ottotapahtumalle, nimikkeen malliryhmässä määritetty arvostustapa ohitetaan. Sen sijaan järjestelmä selvittää nämä tapahtumat toisiaan vasten. 

Voit merkitä varastostaottotapahtuman vastaanottoon kirjauksen jälkeen. Voit tehdä tämän myyntitilausrivin **Myyntitilauksen tiedot** -sivulla. Voit tarkastella avoimia vastaanottotapahtumia **Merkintä**-sivulla. Voit merkitä varastostaottotapahtuman vastaanottoon tapahtuman kirjauksen jälkeen. Voit täsmäyttää tai merkitä varastostaottotapahtuman varastoidun nimikkeen avoimeen vastaanottotapahtumaan kirjatusta varaston oikaisukirjauskansiosta. Seuraavassa on kuvattu näitä tapahtumia:

-   1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannushinnan ollessa 10,00 USD.
-   1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannushinnan ollessa 10,00 USD.
-   2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannushinnan ollessa 20,00 USD.
-   2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannushinnan ollessa 20,00 USD.
-   3a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannushinnan ollessa 25,00 USD.
-   4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannushinnan ollessa 30,00 USD.
-   4b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannushinnan ollessa 30,00 USD.
-   5a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 21,25 USD (taloudellisten ja fyysisten päivitettyjen tapahtumien käyttökeskiarvo).
-   5b. Varaston taloudellinen varastostaotto määrälle 1 merkitään varaston vastaanottoon 2b ennen tapahtuman kirjaamista. Tämä tapahtuma kirjataan kustannushintaan 20,00 USD.
-   6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 21,25 USD.
-   7. Varaston sulkeminen on suoritettu. Koska taloudellisesti päivitetty tapahtuma on merkitty vastaanottoon, nämä tapahtumat selvitetään toisiaan vasten, eikä oikaisua tehdä.

Uusi kustannushinnan käyttökeskiarvo 27,50 USD on laskettu taloudellisesti ja fyysisesti päivitettyjen tapahtumien mukaan. Seuraavassa kaaviossa havainnollistetaan painotetun keskiarvon päivämäärän varastomallin ja merkinnän käyttämisen vaikutus tähän tapahtumien sarjaan.

![Painotetun keskiarvon päivämäärä käyttäen merkintää.](./media/weightedaveragedatewithmarking.gif) 

**Kuvan selitys:**

-   Pystysuorat nuolet kuvaavat varastotapahtumia.
-   Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
-   Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
-   Kunkin pystysuoran nuolen ylä- tai alapuolella näkyy varastotapahtuman arvo muodossa *määrä*@*yksikköhinta*.
-   Sulkeissa oleva varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon fyysisesti.
-   Ilman sulkeita esitetty varastotapahtuman arvo tarkoittaa, että varastotapahtuma on kirjattu varastoon taloudellisesti.
-   Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
-   Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
-   Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla ja merkinnällä *Inventory Close*.
-   Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]