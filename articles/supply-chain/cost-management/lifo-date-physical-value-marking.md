---
title: LIFO-päivämäärä sekä fyysinen arvo ja merkintä
description: LIFO-päivämäärä on varastomalli, joka perustuu LIFO-periaatteeseen. Varasto-otot täsmäytetään viimeisiä varastovastaanottoja vasten varastotapahtuman päivämäärän perusteella. Jos LIFO-päivämäärä on määritetty eikä ennen ottoa ei ole vastaanottoa, otto täsmäytetään oton päivämäärän jälkeen tapahtuneiden vastaanottojen mukaan. Jos samana päivänä on useita ottoja, ne täsmäytetään järjestyksessä viimeinen otto, viimeinen vastaanotto.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ca344e6ca81814e787046f6ece97625d035346d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671447"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO-päivämäärä sekä fyysinen arvo ja merkintä

[!include [banner](../includes/banner.md)]

LIFO (Last in, first out) -päivämäärä on varastonhallinta- ja arvostusmenetelmä, jossa viimeksi tuotettu tai hankittu varasto myydään, käytetään tai myydään ensimmäisenä. Microsoft Dynamics 365 Supply Chain Managementin varaston sulkemisprosessin aikana järjestelmä luo täsmäytykset, joissa viimeisin vastaanotto täsmäytetään ensimmäistä varastostaottoa vasten kullekin annetulle päivämäärälle vanhimmasta päivämäärästä alkaen, ja niin edelleen. Jos käytät LIFO-päivämäärään perustuvaa varastomallia eikä ennen varastostaottoa ole vastaanottoa, varastostaotto täsmäytetään oton päivämäärän jälkeen tapahtuneita vastaanottoja vastaan. Selvitykset ja täsmäytysperiaate perustuvat varastotapahtumien taloushallintopäivämäärään. Kun samana päivänä on useita varasto-ottoja, ne täsmäytetään järjestyksessä viimeinen otto, viimeinen vastaanotto. Selvitykset ja oikaisut voidaan arvioida alustavasti suorittamalla varaston uudelleenlaskentaprosessi.

Voit ohittaa LIFO-päivämäärän periaatteen merkitsemällä varastotapahtumat niin, että tietyn nimikkeen vastaanotto selvitetään tiettyä varastostaottoa vasten. Varaston kausittainen sulkeminen on pakollinen LIFO-päivämäärän varastomallia käytettäessä luodaksesi täsmäytyksen ja oikaistaksesi varasto-ottojen arvon LIFO-periaatteella. Varasto-ottotapahtumat arvotetaan fyysisten ja taloudellisten päivitysten suorituksen keskiarvon mukaan, kunnes varaston sulkemisprosessi suoritetaan. Jos et käytä merkintää, juokseva keskiarvo lasketaan, kun fyysinen tai taloudellinen päivitys suoritetaan.

Varaston kausittainen sulkeminen on suositeltavaa käytettäessä LIFO-päivämäärän varastomallia.

Seuraavissa esimerkeissä on esitetty LIFO-päivämäärän käyttämisen vaikutus kolmea eri määritystä käytettäessä:

- LIFO-päivämäärä ilman **Sisällytä fyysinen arvo** -asetusta
- LIFO-päivämäärä, kun **Sisällytä fyysinen arvo** -asetus on käytössä
- LIFO-päivämäärä merkinnän kanssa

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-päivämäärä ilman Sisällytä fyysinen arvo -asetusta

Tässä esimerkissä nimikemalliryhmää ei ole merkitty sisällyttämään fyysistä arvoa. Seuraavassa on kuvattu näitä tapahtumia:

- 1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
- 2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 22,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo)
- 7\. Varaston sulkeminen on suoritettu. LIFO-päivämäärän menetelmään perustuen ensimmäinen rahoituksellisesti päivitetty varasto-otto täsmäytetään viimeisen rahoituksellisesti päivitetyn vastaanoton kanssa alkaen ensimmäisestä päivämäärästä jne. Tässä esimerkissä luodaan yksi tilitys 3b- ja 2b-kohteiden välille. Kohteeseen 3b tehdään oikaisu 6,00 USD, ja tuloksena syntyvä lopullinen kustannus on 22,00 USD.

Seuraavassa on kuvattu LIFO-päivämäärään perustuvan varastomallin vaikutusta, kun **Sisällytä fyysinen arvo** -asetusta ei käytetä.

![LIFO-päivämäärä ilman Sisällytä fyysinen arvo -asetusta.](media/lifo-date-without-include-physical-value.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-päivämäärä, kun Sisällytä fyysinen arvo -asetus on käytössä

Jos **Sisällytä fyysinen arvo** -valintaruutu on valittuna nimikkeen **Nimikemalliryhmät**-sivulla, järjestelmä käyttää juoksevan keskimääräisen kustannushinnan laskennassa sekä fyysisiä että rahoituksellisia vastaanottotapahtumia. Järjestelmä tekee myös oikaisuja fyysisesti päivitettyyn varastostaottotapahtumaan, jos tämä on aiheellista. Jos **Sisällytä fyysinen arvo** -valintaruudun valinta poistetaan, varaston sulkeminen LIFO-päivämäärään perustuvaa varastomallia käyttämällä täsmäyttää vain kirjanpidollisesti päivitetyt tapahtumat.

Tässä esimerkissä nimikemalliryhmä on merkitty sisällyttämään fyysinen arvo. 

Seuraavassa on kuvattu näitä tapahtumia:

- 1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
- 2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 22,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,67 USD (fyysisesti ja taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 7\. Varaston sulkeminen on suoritettu. LIFO-päivämäärän menetelmään perustuen ensimmäinen rahoituksellisesti päivitetty varasto-otto täsmäytetään viimeisen rahoituksellisesti päivitetyn vastaanoton kanssa kullekin päivämäärälle alkaen ensimmäisestä päivämäärästä jne. Tässä esimerkissä luodaan yksi tilitys 2b- ja 3b-kohteiden välille. Kohteeseen 3b tehdään oikaisu 6,00 USD, ja tuloksena syntyvä lopullinen kustannus on 22,00 USD. Lisäksi tapahtuma 6a oikaistaan vastaanottotapahtuman kustannuksen 5b mukaiseksi. Järjestelmä ei täsmäytä näitä tapahtumia, koska vastaanotto päivitetään vain fyysisesti, ei rahoituksellisesti. Sen sijaan fyysiseen varasto-ottotapahtumaan kirjataan vain oikaisu 6,33 USD, ja tuloksena syntyvä oikaistu kustannus on 30,00 USD.

Seuraavassa on kuvattu LIFO-päivämäärään perustuvan varastomallin vaikutusta, kun **Sisällytä fyysinen arvo** -asetus on käytössä.

![LIFO-päivämäärä, kun Sisällytä fyysinen arvo -asetus on käytössä.](media/lifo-date-with-include-physical-value.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="lifo-date-with-marking"></a>LIFO-päivämäärä merkinnän kanssa

Merkintä on prosessi, jonka avulla voit linkittää (eli merkitä) varaston ottotapahtuman vastaanottotapahtumaan. Merkintä voi tapahtua joko ennen tapahtuman kirjaamista tai sen jälkeen. Merkinnän avulla voit varmistaa tarkan varastokustannuksen, kun tapahtuma kirjataan tai kun varaston sulkeminen suoritetaan. Oletetaan esimerkiksi, että asiakaspalveluosasto on hyväksynyt kiireellisen tilauksen tärkeältä asiakkaalta. Koska tilaus on kiireellinen, nimikkeestä on maksettava tavallista enemmän, jotta asiakkaan pyynnön voi toteuttaa.

Sinun on varmistettava, että varastonimikkeen kustannus otetaan huomioon myyntitilauslaskun katteessa (tai myydyn tavaran kustannuksissa). Kun ostotilaus kirjataan, varasto vastaanotetaan hintaan 120,00 USD. Jos tämä myyntitilausasiakirja on merkitty ostotilaukseen ennen pakkausluettelon tai laskun kirjaamista, myydyn tavaran kustannukseksi tulee 120,00 USD nimikkeen nykyisen käyttökeskiarvokustannuksen sijaan. Jos myyntitilauksen pakkausluettelo tai lasku kirjataan ennen merkintää, myydyn tavaran kustannus kirjataan käyttäen käyttökeskiarvon mukaista kustannushintaa.

Ennen varaston sulkemista nämä kaksi tapahtumaa voidaan vielä merkitä toisiinsa.

Voit merkitä varastostaottotapahtuman vastaanottoon kirjauksen jälkeen. Voit tehdä tämän merkinnän myyntitilausrivillä **Myyntitilauksen tiedot** -sivulla valitsemalla **Varasto \> Merkintä** **Myyntitilausrivit**-pikavälilehdessä. Voit tarkastella avoimia vastaanottotapahtumia **Merkintä**-sivulla.

Voit merkitä varastostaottotapahtuman vastaanottoon myös tapahtuman kirjauksen jälkeen. Voit täsmäyttää tai merkitä varastostaottotapahtuman varastoidun nimikkeen avoimeen vastaanottotapahtumaan kirjatusta varaston oikaisukirjauskansiosta.

Seuraavassa on kuvattu näitä tapahtumia:

- 1a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 1b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 10,00 USD.
- 2a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 20,00 USD.
- 2b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 22,00 USD.
- 3a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3b. Varaston taloudellinen varastostaotto määrälle 1 kustannushintaan 16,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo).
- 3c. Kohteen 3b varaston taloudellinen varasto-otto on merkitty taloudelliseen varasto-ottoon 1b.
- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo)
- 7\. Varaston sulkeminen on suoritettu. LIFO-päivämäärän menetelmää käyttävän merkintäperiaatteen mukaan merkityt tapahtumat täsmäytetään toisiaan vasten. Tässä esimerkissä 3b täsmäytetään 1b:tä vasten ja -6,00 USD kirjataan 3b:lle, jolloin arvo on 10,00 USD. Tässä esimerkissä ei tehdä muita tilitysitä, koska sulkeminen luo täsmäytyksen vain taloudellisesti päivitettyjä tapahtumia varten.

Seuraavassa on kuvattu LIFO-päivämäärän varastomallin vaikutusta, kun käytetään varastostaottojen ja vastaanottojen välistä merkintää. 

![LIFO-päivämäärä merkinnän kanssa.](media/lifo-date-with-marking.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Akselin yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Akselin alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset ja merkinnät on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
