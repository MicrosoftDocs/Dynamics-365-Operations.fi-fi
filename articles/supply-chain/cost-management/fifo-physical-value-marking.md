---
title: FIFO-merkintä ja fyysinen arvo
description: FIFO (First In, First Out) on varastomalli, jossa ensimmäiset vastaanotot otetaan varastosta ensin. Rahoituksellisesti päivitetyt varasto-otot täsmäytetään ensimmäisiä rahoituksellisesti päivitettyjä varastovastaanottoja vasten varastotapahtuman rahoituspäivämäärän perusteella.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5280498a23df26873dda1f380f686796f5e1055f
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092137"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO-merkintä ja fyysinen arvo

[!include [banner](../includes/banner.md)]


FIFO (First in, first out) on varastonhallinta- ja arvostusmenetelmä, jossa ensimmäiseksi tuotettu tai hankittu varasto myydään, käytetään tai myydään ensimmäisenä. Microsoft Dynamics 365 Supply Chain Managementin varaston sulkemisprosessin aikana järjestelmä luo täsmäytykset, joissa ensimmäinen vastaanotto täsmäytetään ensimmäistä varastostaottoa vasten ja niin edelleen.

Selvitykset ja täsmäytysperiaate perustuvat varastotapahtumien taloushallintopäivämäärään. Selvitykset ja oikaisut voidaan arvioida alustavasti suorittamalla varaston uudelleenlaskentaprosessi.

Voit ohittaa FIFO-periaatteen merkitsemällä varastotapahtumat niin, että tietyn nimikkeen vastaanotto selvitetään tiettyä varastostaottoa vasten. Varaston kausittainen sulkeminen on pakollinen FIFO-varastomallia käytettäessä luodaksesi täsmäytyksen ja oikaistaksesi varasto-ottojen arvon FIFO-periaatteella. Varasto-ottotapahtumat arvotetaan fyysisten ja taloudellisten päivitysten suorituksen keskiarvon mukaan, kunnes varaston sulkemisprosessi suoritetaan. Jos et käytä merkintää, juokseva keskiarvo lasketaan, kun fyysinen tai taloudellinen päivitys suoritetaan. Seuraavissa esimerkeissä havainnollistetaan FIFO-mallin käyttämisen vaikutus kolmea eri määritystä käytettäessä:

- FIFO ilman **Sisällytä fyysinen arvo** -asetusta
- FIFO ja **Sisällytä fyysinen arvo** -asetus
- FIFO ja merkintä

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO ilman Sisällytä fyysinen arvo -asetusta

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
- 7\. Varaston sulkeminen on suoritettu. FIFO-menetelmään perustuen ensimmäinen rahoituksellisesti päivitetty varasto-otto täsmäytetään ensimmäisen rahoituksellisesti päivitetyn vastaanoton kanssa jne. Tässä esimerkissä luodaan yksi tilitys 1b- ja 3b-kohteiden välille. Kohteeseen 3b tehdään oikaisu -6,00 USD, ja tuloksena syntyvä lopullinen kustannus on 10,00 USD.

Uusi keskimääräinen kustannushinta vastaa rahoituksellisesti päivitettyjen tapahtumien keskiarvoa. Seuraavissa kuvissa havainnollistamme FIFO-varastointimallia tässä tapahtumasarjassa, kun **Sisällytä fyysinen arvo** -asetus ei ole käytössä.

![FIFO ilman Sisällytä fyysinen arvo -asetusta.](./media/fifo-without-include-physical-value.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO ja Sisällytä fyysinen arvo -asetus

Jos **Sisällytä fyysinen arvo** -valintaruutu on valittuna nimikkeen **Nimikemalliryhmä**-sivulla, järjestelmä käyttää juoksevan keskimääräisen kustannushinnan laskennassa sekä fyysisiä että rahoituksellisia vastaanottotapahtumia. Järjestelmä tekee myös oikaisuja fyysisesti päivitettyyn varastostaottotapahtumaan, jos tämä on aiheellista. Varaston sulkeminen FIFO-varastomallia käyttäen tekee vain rahoituksellisesti päivitettyjen tapahtumien täsmäytyksiä. Seuraavassa on kuvattu näitä tapahtumia:

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
- 7\. Varaston sulkeminen on suoritettu. FIFO-menetelmään perustuen ensimmäinen rahoituksellisesti päivitetty varasto-otto täsmäytetään ensimmäisen rahoituksellisesti päivitetyn vastaanoton kanssa jne. Tässä esimerkissä luodaan yksi tilitys 1b- ja 3b-kohteiden välille. Kohteeseen 3b tehdään oikaisu -6,00 USD, ja tuloksena syntyvä lopullinen kustannus on 10,00 USD. Lisäksi tapahtuma 6a oikaistaan vastaanottotapahtuman kustannuksen 2b mukaiseksi. Järjestelmä ei täsmäytä näitä tapahtumia, koska vastaanotto päivitetään vain fyysisesti, ei rahoituksellisesti. Sen sijaan fyysiseen varasto-ottotapahtumaan kirjataan vain oikaisu -1,67 USD, ja tuloksena syntyvä oikaistu kustannus on 22,00 USD.

![FIFO ja Sisällytä fyysinen arvo -asetus.](./media/fifo-with-include-physical-value.png)

Huomaa, että varaston sulkemisprosessin tulos on sama riippumatta siitä, valitaanko **Sisällytä fyysinen arvo** -vaihtoehto **Nimikemalliryhmä**-sivulla. **Sisällytä fyysinen arvo** -asetus vaikuttaa vain käyttökeskiarvoon.

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

## <a name="fifo-with-marking"></a>FIFO ja merkintä

Merkintä on prosessi, jonka avulla voit linkittää (eli merkitä) varaston ottotapahtuman vastaanottotapahtumaan. Merkintä voi tapahtua joko ennen tapahtuman kirjaamista tai sen jälkeen. Merkinnän avulla voit varmistaa tarkan varastokustannuksen, kun tapahtuma kirjataan tai kun varaston sulkeminen suoritetaan.

Oletetaan esimerkiksi, että asiakaspalveluosasto on hyväksynyt kiireellisen tilauksen tärkeältä asiakkaalta. Koska tilaus on kiireellinen, tästä nimikkeestä on maksettava tavallista enemmän, jotta asiakkaan pyynnön voi toteuttaa. Sinun on varmistettava, että varastonimikkeen kustannus otetaan huomioon myyntitilauslaskun katteessa (tai myydyn tavaran kustannuksissa). Kun ostotilaus kirjataan, varasto vastaanotetaan hintaan 120,00 USD. Jos myyntitilausasiakirja on merkitty ostotilaukseen ennen pakkausluettelon tai laskun kirjaamista, myydyn tavaran kustannukseksi tulee 120,00 USD nimikkeen nykyisen käyttökeskiarvokustannuksen sijaan. Jos myyntitilauksen pakkausluettelo tai lasku kirjataan ennen merkintää, myydyn tavaran kustannus kirjataan käyttäen käyttökeskiarvon mukaista kustannushintaa. Ennen varaston sulkemista nämä kaksi tapahtumaa voidaan vielä merkitä toisiinsa.

Kun vastaanottotapahtuma merkitään varasto-ottotapahtumaan, nimikkeen malliryhmässä määritetty arvostustapa ohitetaan, ja järjestelmä täsmäyttää nämä tapahtumat toisiaan vasten. Voit manuaalisesti merkitä tapahtuman myyntitilausrivillä **Myyntitilauksen tiedot** -sivulla valitsemalla **Varasto \> Merkintä** **Myyntitilausrivit**-pikavälilehdessä. Voit tarkastella avoimia vastaanottotapahtumia **Merkintä**-sivulla. Voit täsmäyttää tai merkitä varastostaottotapahtuman varastoidun nimikkeen avoimeen vastaanottotapahtumaan kirjatusta varaston oikaisukirjauskansiosta. Seuraavassa on kuvattu näitä tapahtumia:

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
- 7\. Varaston sulkeminen on suoritettu. FIFO-menetelmää käyttävän merkintäperiaatteen mukaan merkityt tapahtumat täsmäytetään toisiaan vasten. Tässä esimerkissä 3b täsmäytetään 2b:tä vasten ja 6,00 USD kirjataan 3b:lle, jolloin arvo on 22,00 USD. Tässä esimerkissä ei tehdä muita tilitysitä, koska sulkeminen luo täsmäytyksen vain taloudellisesti päivitettyjä tapahtumia varten.

Seuraavassa kuvassa havainnollistetaan FIFO-varastomallin käyttämisen vaikutus tähän tapahtumien sarjaan kun merkintä varasto-ottojen ja vastaanottojen välillä on käytössä.

![FIFO ja merkintä.](./media/fifo-with-marking.png)

**Kaavion selite**

- Pystysuorat nuolet kuvaavat varastotapahtumia.
- Fyysisiä tapahtumia kuvastavat lyhyemmät vaalean harmaat nuolet.
- Kirjanpitotapahtumia kuvastavat pidemmät mustat nuolet.
- Aikajanan yläpuolella olevat pystysuorat nuolet kuvaavat vastaanottoja varastoon.
- Aikajanan alapuolella olevat pystysuorat nuolet kuvaavat varastostaottoja.
- Kukin uusi vastaanotto- tai varastostaottotapahtuma on merkitty uudella otsikolla.
- Kukin pystysuora nuoli on merkitty järjestystunnuksella, kuten *1a*. Tunnukset ilmaisevat varastotapahtumakirjausten järjestyksen aikajanalla.
- Jokainen kaavion päivämäärä erotetaan ohuella mustalla pystysuoralla viivalla. Päivämäärä näkyy kaavion alareunassa.
- Varaston sulkemiset on kuvattu punaisella pystysuoralla katkoviivalla.
- Varaston sulkemisen suorittamat selvitykset ja merkinnät on kuvattu punaisilla katkoviivanuolilla, jotka kulkevat vinosti vastaanotosta varastostaottoon.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
