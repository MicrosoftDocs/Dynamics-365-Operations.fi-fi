---
title: LIFO-merkintä ja fyysinen arvo
description: LIFO (Last in, First out) on varastomalli, jossa varastoon viimeiseksi hankittujen (uusimpien) vastaanottojen varasto-otto tapahtuu ensin. Varasto-otot täsmäytetään viimeisiä varastovastaanottoja vasten varastotapahtuman päivämäärän perusteella.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45316c40cce988c0758e70af627b0123ec1f7873
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670437"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO-merkintä ja fyysinen arvo

[!include [banner](../includes/banner.md)]

LIFO (Last in, first out) on varastonhallinta- ja arvostusmenetelmä, jossa viimeksi tuotettu tai hankittu varasto myydään, käytetään tai myydään ensimmäisenä. Microsoft Dynamics 365 Supply Chain Managementin varaston sulkemisprosessin aikana järjestelmä luo täsmäytykset, joissa viimeinen vastaanotto täsmäytetään ensimmäistä varastostaottoa vasten ja niin edelleen. Selvitykset ja täsmäytysperiaate perustuvat varastotapahtumien taloushallintopäivämäärään. Selvitykset ja oikaisut voidaan arvioida alustavasti suorittamalla varaston uudelleenlaskentaprosessi.

Voit ohittaa LIFO-periaatteen merkitsemällä varastotapahtumat niin, että tietyn nimikkeen vastaanotto selvitetään tiettyä varastostaottoa vasten. Varaston kausittainen sulkeminen on pakollinen LIFO-varastomallia käytettäessä luodaksesi täsmäytyksen ja oikaistaksesi varasto-ottojen arvon LIFO-periaatteella. Varasto-ottotapahtumat arvotetaan fyysisten ja taloudellisten päivitysten suorituksen keskiarvon mukaan, kunnes varaston sulkemisprosessi suoritetaan. Jos et käytä merkintää, juokseva keskiarvo lasketaan, kun fyysinen tai taloudellinen päivitys suoritetaan.

Seuraavissa esimerkeissä havainnollistetaan LIFO-mallin käyttämisen vaikutus kolmea eri määritystä käytettäessä:

- LIFO ilman **Sisällytä fyysinen arvo** -asetusta
- LIFO ja **Sisällytä fyysinen arvo** -asetus
- LIFO ja merkintä

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO ilman Sisällytä fyysinen arvo -asetusta

Tässä esimerkissä vapautetun tuotteen nimikemalliryhmän **Sisällytä fyysinen arvo** -valintaruudun valinta on tyhjä. Seuraavassa on kuvattu näitä tapahtumia:

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
- 7\. Varaston sulkeminen on suoritettu. LIFO-menetelmään perustuen ensimmäinen rahoituksellisesti päivitetty varasto-otto täsmäytetään viimeisen rahoituksellisesti päivitetyn vastaanoton kanssa jne. Tässä esimerkissä luodaan yksi tilitys 5b- ja 3b-kohteiden välille. Kohteeseen 3b tehdään oikaisu 14,00 USD, ja tuloksena syntyvä lopullinen kustannus on 30,00 USD.

Seuraavassa kuvassa havainnollistetaan FIFO-varastointimallia tässä tapahtumasarjassa, kun **Sisällytä fyysinen arvo** -asetus ei ole käytössä.

![LIFO ilman Sisällytä fyysinen arvo -asetusta.](./media/lifo-without-including-physical-value.png)

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

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO ja Sisällytä fyysinen arvo -asetus

Jos **Sisällytä fyysinen arvo** -valintaruutu on valittuna nimikkeen **Nimikemalliryhmät**-sivulla, järjestelmä käyttää juoksevan keskimääräisen kustannushinnan laskennassa sekä fyysisiä että rahoituksellisia vastaanottotapahtumia. Järjestelmä tekee myös oikaisuja fyysisesti päivitettyyn varastostaottotapahtumaan, jos tämä on aiheellista. Jos **Sisällytä fyysinen arvo** -valintaruudun valinta poistetaan, varaston sulkeminen LIFO-varastomallia käyttämällä täsmäyttää vain kirjanpidollisesti päivitetyt tapahtumat.

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
- 7\. Varaston sulkeminen on suoritettu. LIFO-menetelmään perustuen ensimmäinen rahoituksellisesti päivitetty varasto-otto täsmäytetään viimeisen rahoituksellisesti päivitetyn vastaanoton kanssa jne. Tässä esimerkissä luodaan yksi tilitys 3b- ja 5b-kohteiden välille. Kohteeseen 3b tehdään oikaisu 14,00 USD, ja tuloksena syntyvä lopullinen kustannus on 30,00 USD. Lisäksi tapahtuma 6a oikaistaan vastaanottotapahtuman kustannuksen 4a mukaiseksi. Järjestelmä ei täsmäytä näitä tapahtumia, koska vastaanotto päivitetään vain fyysisesti, ei rahoituksellisesti. Sen sijaan fyysiseen varasto-ottotapahtumaan kirjataan vain oikaisu 1,33 USD, ja tuloksena syntyvä oikaistu kustannus on 25,00 USD.

Seuraavassa kuvassa havainnollistamme LIFO-varastointimallia tässä tapahtumasarjassa, kun **Sisällytä fyysinen arvo** -asetus on käytössä.

![LIFO ja Sisällytä fyysinen arvo -asetus.](./media/lifo-with-included-physical-value.png)

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

## <a name="lifo-with-marking"></a>LIFO ja merkintä

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
- 3c. Kohteen 3b varaston taloudellinen varasto-otto on merkitty taloudelliseen varasto-ottoon 2b.
- 4a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 25,00 USD.
- 5a. Varaston fyysinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 5b. Varaston taloudellinen vastaanotto määrälle 1 yksikkökustannuksen ollessa 30,00 USD.
- 6a. Varaston fyysinen varastostaotto määrälle 1 kustannushintaan 23,00 USD (taloudellisesti kirjattujen tapahtumien käyttökeskiarvo)
- 7\. Varaston sulkeminen on suoritettu. LIFO-menetelmää käyttävän merkintäperiaatteen mukaan merkityt tapahtumat täsmäytetään toisiaan vasten. Tässä esimerkissä 3b täsmäytetään 2b:tä vasten ja 6,00 USD kirjataan 3b:lle, jolloin arvo on 22,00 USD. Tässä esimerkissä ei tehdä muita tilitysitä, koska sulkeminen luo täsmäytyksen vain taloudellisesti päivitettyjä tapahtumia varten.

Uusi kustannushinnan käyttökeskiarvo 27,50 USD on laskettu taloudellisesti ja fyysisesti päivitettyjen tapahtumien mukaan.

Seuraavassa kuvassa havainnollistetaan LIFO-varastomallin käyttämisen vaikutus tähän tapahtumien sarjaan kun merkintä varasto-ottojen ja vastaanottojen välillä on käytössä.

![LIFO ja merkintä.](./media/lifo-with-marking.png)

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
