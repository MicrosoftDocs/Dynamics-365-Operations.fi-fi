---
title: Vuokrasopimuksen irtisanomisen ehdotus
description: Tässä ohjeaiheessa kerrotaan, miten ehdotetaan vuokran päättämistä.
author: moaamer
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseTerminateLeaseListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 003eaa3f9e5ad653daed2e973044f384972b0331
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638485"
---
# <a name="propose-a-lease-for-termination"></a>Vuokran ehdottaminen irtisanomista varten

[!include [banner](../includes/banner.md)]

Jos vuokra päätetään etuajassa, käyttöomaisuuden vuokraus voi kirjata irtisanomisen kirjauskansiomerkinnän, joka poistaa vuokravelkaa, käyttöoikeutta (ROU) sekä kertyneitä poistoja, sekä kirjata voiton tai tappion. Varhaisen irtisanomisen prosessi päättää vuokra-ajan ja siihen liittyvät vuokrakirjat. Se ei päätä yksittäisiä vuokrakirjoja. Tässä aiheessa kuvataan toimintoja, jotka mahdollistaa vuokrasopimuksen ehdottamisen irtisanomista varten ja vuokran päättymisen kirjauskansion merkinnän käsittelemisen.

Jos vuokra ei ole luokiteltu lykättynä vuokrakäsittelyn vuokrasopimuksina eikä sitä ole liitetty käyttöomaisuuserään, käyttöomaisuuden vuokraus tuottaa seuraava lopetuksen kirjauskansiomerkintä.

| Tapahtuma                           | Debet (Dr.) | Kredit (Cr.) |
|---------------------------------------|-------------|--------------|
| Dr. Vuokrasopimusvelka                   | X           |              |
| Dr. kertynyt poisto          | X           |              |
| Dr. Vuokranmuokkauksen voitto/tappio | X           |              |
| Cr. Vuokraresurssi                       |             | X            |
| Cr. Vuokranmuokkauksen voitto/tappio |             | X            |

Jos vuokrakirja on luokiteltu lykätyksi vuokrakirjaksi, merkintä kirjaa lykätyn vuokran saldon ennen voitto- tai tappiotilille päättämistä, kuten tässä näkyy.

| Tapahtuma                           | Debet (Dr.) | Kredit (Cr.) | 
|---------------------------------------|-------------|--------------|
| Dr. Toteutumaton vuokra                     | X           |              |
| Cr. Vuokranmuokkauksen voitto/tappio |             | X            |
| Cr. Toteutumaton vuokra                     |             | X            |
| Dr. Vuokranmuokkauksen voitto/tappio | X           |              |

Jos vuokrakirja on liitetty käyttöomaisuuserään, ROU-resurssi otetaan huomioon käyttöomaisuudessa. Tämä kirjanpito sisältää varhaisten päättymisten kirjanpidon. Käyttöomaisuuden vuokraus tuottaa seuraavan kirjauskansiomerkinnän, jossa vuokravelka voidaan poistaa.

| Tapahtuma                           | Debet (Dr.) | Kredit (Cr.) |
|---------------------------------------|-------------|--------------|
| Dr. Vuokrasopimusvelka                   | X           |              |
| Cr. Vuokranmuokkauksen voitto/tappio |             | X            |

Lisätietoja oikeasta tavasta poistaa ROU-käyttöomaisuuserä on kohdassa [käyttöomaisuuserän poistaminen hävikkinä](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Vuokran ehdottaminen irtisanomista varten

1. Siirry vuokraan, joka on lopetettava, ja valitse sitten toimintoruudusta **Irtisanomisehdotus**.

    > [!NOTE]
    > **Irtisanomisehdotus**-painike ei ole käytettävissä, jos kirjaamattomia kirjauskansiomerkintöjä on mille tahansa kirjalle. Ennen kuin voit päättää vuokran, sinun on kirjattava tai poistettava kaikki vuokralle luodut kirjauskansiomerkinnät.

2. Määritä näyttöön tulevassa valintaikkunassa irtisanomisen kirjauskansiomerkinnän **Voimaantulopäivä** ja **Kirjauspäivämäärä**.
3. Valitse **Irtisanomisehdotus** ehdottaaksesi vuokraa päättämistä varten.
4. Valitse **Kirjaa vuokran päättyminen**, jos haluat kirjata vuokran päättymisen kirjauskansiomerkinnän automaattisesti.
5. Valitse **Vuokran päättymiset** -sivulla sen vuokrasopimuksen vuokratunnus, jota olet ehdottanut päätettäväksi nähdäksesi päättymisrivit. Irtisanomisriveillä näkyvät ROU-käyttöomaisuuden, vuokravelan, kertyneen poiston, lykättyn vuokran (jos sovellettavissa) ja voiton tai tappion arvo, joka on tunnistettava vuokran päättymisen yhteydessä.

Vuokra on nyt valmis päätettäväksi. Vuokrakirjan **Irtisanomistila**-kentän arvoksi tulee **Valmis päätettäväksi**. Tässä vaiheessa kirjauskansioon ei voi enää kirjata kirjauksia vuokraan tai muuttaa tai heikentää sitä. 

## <a name="process-leases-that-are-ready-for-termination"></a>Käsittele vuokrat, jotka ovat valmiita päätettäväksi

Toimi seuraavasti, kun haluat käsitellä vuokrat, jotka ovat valmiita irtisanomisen jälkeisiin työvaiheisiin ja kirjata irtisanomisen kirjauskansiomerkinnän.

1. Valitse **Vuokran irtisanomiset**-sivulla käsiteltävä vuokrasopimus ja valitse sitten **Irtisano**.
2. Valitse avautuvassa valintaikkunassa **OK**.

Järjestelmä kirjaa irtisanomisen kirjauskansiomerkinnän. Vuokrakirjan **Vuokran tila** -kentän arvoksi määritetään **Lopetettu** ja **Irtisanomisehdotuksen tila** -kentän arvoksi tulee **Valmis**.

## <a name="reverse-a-lease-termination"></a>Vuokran päättymisen peruutus

Peruuta vuokran päättymisen kirjauskansion kirjaus ja avaa vuokra, joka on päättynyt, seuraavasti:

- Valitse **Vuokran irtisanomiset**-sivulla palautettava vuokrasopimus ja valitse sitten **Peruuta irtisanominen**.

Järjestelmä peruttaa irtisanomisen kirjauskansiomerkinnän. Vuokrakirjan **Vuokran tila** -kentän arvoksi määritetään **Avoin**. Vuokra ei enää näy **Vuokrasopimuksen päättymiset** -sivulla, ja sitä voidaan ehdottaa uudelleen irtisanomista varten.

## <a name="example-of-a-lease-termination"></a>Esimerkki vuokran päättämisestä

Tässä esimerkissä vuokrasopimus liittyy ei-erikoistuneeseen resurssiin, ja se ei siirrä resurssin omistajuutta tai myönnä vuokralle ottajalle resurssin osto-oikeutta.

### <a name="setup"></a>Luo perustiedot

Seuraavissa taulukoissa ovat arvot, jotka on määritetty **Yleistiedot**- ja **Maksuaikataulun rivit** -välilehdille vuokrasopimuksessa, jota käytetään tässä esimerkeissä.

**Yleinen-välilehti**

| Kenttä                      | Arvo            |
|----------------------------|------------------|
| Resurssin käypä arvo    | 600,000          |
| Valuutta                   | USD              |
| Alkuvaiheen välittömät menot       | 1 000            |
| Inkrementaalinen lainakorko | 7 %               |
| Yhdistämisväli       | Vuosittain         |
| Käyttöomaisuuden käyttöikä (kuukautta) | 600              |
| Annuiteetin tyyppi               | Tavallinen annuiteetti |
| Aloituspäivämäärä          | 1.1.2019         |

**Maksusuunnitelmarivit-välilehti**

| Kenttä             | Arvo      |
|-------------------|------------|
| Aloituspäivä        | 1.1.2019   |
| Kausiväli   | Kuukausittain    |
| Kaudet           | 120        |
| Päättymispäivämäärä          | 31.12.2028 |
| Maksun toistuvuus | Vuosittain   |
| Maksun summa    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Vuokran päättämisen vaiheet

1. Kun olet luonut vuokrasopimuksen aiemmin tässä ohjeaiheessa kuvatulla tavalla, siirry vuokrauskirjaan ja vahvista maksuaikataulu. Kirjaa sitten alkuperäinen tuloutuksen kirjauskansiovienti. Alkuperäinen käyttöoikeusomaisuuserä on 71 235,81 $ ja vuokrasopimusvelan on oltava 70 235,81 $. Tässä esimerkissä vuokrasopimus luokiteltiin käyttöleasingsopimukseksi Accounting Standards Codification Topic 842:n (ASC 842) mukaan.
2. Suorita kirjauskansion eräprosessi kolme kertaa, jotta voit simuloida kolmen vuoden kulumista vuokrille, korkokuluille ja poistokuluille.
3. Kun kaikki kolme erätyötä on suoritettu, siirry takaisin vuokrauskirjaan ja avaa velka- ja resurssitapahtumien taulukot tarkastellaksesi resurssin ja vuokrasopimusvelan nykyistä kirjanpitoarvoa. Kolmen vuoden kuluttua velan arvon on oltava noin -53 893,00 dollaria ja resurssin arvon noin 54 593,00 dollaria.

    Kun nämä kolme vuotta ovat kuluneet, liike ja vuokraaja ovat sopineet, että vuokra päättyy. Sinun on näin ollen päätettävä vuokra.

4. Siirry vuokraan, joka on lopetettava, ja valitse sitten toimintoruudusta **Irtisanomisehdotus**. 
5. Kirjoita näyttöön tulevaan valintaikkunaan **Voimaantulopäivämäärä**- ja **Kirjauspäivämäärä**-kenttiin **1.1.2021**.
6. Valitse **Irtisanomisehdotus** ehdottaaksesi vuokraa päättämistä varten.

    Näkyviin tulee **Vuokrasopimuksen päättymiset** -sivu, joka sisältää irtisanottavan vuokran.

7. Voit tarkastella päättymisrivejä valitsemalla vuokrasopimuksen vuokratunnuksen, jota olet ehdottanut päätettäväksi. Irtisanomisriveillä näkyvät vuokran kirjanpitoarvot. Seuraavassa taulukossa on esitetty, mitä näiden arvojen pitäisi olla tässä esimerkissä. 

    | Kenttä                                                 | Arvo      |
    |-------------------------------------------------------|------------|
    | Sopimusvelan kirjanpidon saldo tapahtumavaluuttana | 53 892,89 $ |
    | Käyttöoikeusomaisuuserä tapahtumavaluuttana            | 71 235,81 $ |
    | Kertynyt poisto tapahtumavaluuttana      | 16 642,92 $ |
    | Voitto/tappio tapahtumavaluuttana                   | -700,00 $   |

8. Voit kirjata päättymisen kirjauskansiomerkinnän valitsemalla **Vuokran irtisanomiset**-sivulla vuokrasopimuksen ja valitsemalla sitten **Irtisano**.
9. Valitse avautuvassa valintaikkunassa **OK**.
10. Jos haluat tarkastella luotua ja kirjattua irtisanomiskirjauskansiota, siirry käyttöomaisuuserän vuokrakirjauskansioon vuokrakirjassa. Seuraavassa taulukossa on esitetty, miltä tämän tapahtuman pitäisi olla tässä esimerkissä.

    | Tapahtuma                           | Debet (Dr.) | Kredit (Cr.) |
    |---------------------------------------|-------------|--------------|
    | Dr. Vuokrasopimusvelka                   | 53,892.89   |              |
    | Dr. kertynyt poisto          | 16,642.92   |              |
    | Dr. Vuokranmuokkauksen voitto/tappio | 700.00      |              |
    | Cr. Vuokraresurssi                       |             | 71,235.81    |

11. Avaa velka- ja käyttöomaisuustapahtumataulut, jos haluat tarkastella irtisanomisen nettovaikutusta, jossa ROU-käyttöomaisuus ja vuokravelka ovat 0 (nolla).

Vuokraustilan olisi nyt oltava **Irtisanottu**. Tähän vuokraan ei kirjata muita kirjauskansiomerkintöjä, ellei irtisanomista peruta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
