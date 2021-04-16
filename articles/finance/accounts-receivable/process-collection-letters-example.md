---
title: Käsittele maksukehotuksia – esimerkki
description: Tämä ohjeaihe käy läpi esimerkin, jossa käsitellään maksukehotuksen luonti-, tulostus- ja kirjausprosessia.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1b80532463d86dd59b867fca2ee24675396ce717
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826344"
---
# <a name="process-collection-letters-example"></a>Käsittele maksukehotuksia – esimerkki

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe käy läpi esimerkin, jossa käsitellään maksukehotuksen luonti-, tulostus- ja kirjausprosessia. Esimerkki perustuu **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -toimintoon luotonvalvonnassa. Se käyttää USMF-demoyrityksen ja uuden asiakkaan,US-045:n tietoja.

Aloita kohdassa **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat** valitsemalla **Uusi** ja kirjoita sitten tarvittavat tiedot, jotta asiakas US-045 luodaan.

Noudata näitä vaiheita, kun olet valmis.

1. Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Määritä maksukehotusten järjestys** ja määritä maksukehotusten järjestys seuraavassa asiakkaan kirjausprofiiliin liitetyssä taulukossa kuvatulla tavalla.

|     Maksukehotuksen koodi      |     kuvaus                           |     Valuutta      |     Päätili        |     Lisämaksu valuuttana     |     Minimi yli        |     Päivien esto      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     Maksukehotus 1         |     Toinen ilmoitus ja lisämaksu        |     USD           |                           |     0,00                  |     0,00                  |     2                 |
|     Maksukehotus 2         |     Toinen ilmoitus ja lisämaksu        |     USC           |     403150                |     20.00                 |     10.00                 |     3                 |
|     Perittävä                    |     Viimeinen ilmoitus ja lisämaksu         |     USD           |     403150                |     50.00                 |     100.00                |     15                |

Seuraavassa kuvassa on taulukossa näkyvät tiedot, kuten ne näkyvät **maksukehotussivulla**. 

[![Maksukehotusjärjestyksen määrittäminen](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Tässä esimerkissä on nyt määritettävä kaksi parametria.

2. Valitse ensin **Luotonvalvonta \> Asetukset \> Myyntireskontran parametrit** ja toimi seuraavasti:

    1. Määritä **Perintä**-välilehdessä **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -arvoksi **Kyllä**.
    2. Varmista, että **Luo maksukehotus per** -kentän arvoksi on määritetty **Asiakas**.

    [![Myyntireskontran parametrien määrittäminen perintää varten](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Siirry kohtaan **Myyntireskontra \> Laskut \> Kaikki vapaatekstilaskut**, valitse **Uusi** ja noudata seuraavia ohjeita:

    1. Valitse **Asiakastili**-kentässä **US-045**.
    2. Lisää **Laskun päivämäärä** -kenttään **15.1.2021**.
    3. Syötä **Eräpäivä**-kenttään arvo **16.1.2021**.
    4. Kirjoita **Laskurivit**-pikavälilehden **Päätili**-kenttään **401100**.
    5. Kirjoita **Yksikköhinta**-kentässä **500.00**.
    6. Valitse **Kirjaa**.

    Sinun on nyt kirjoitettava asiakkaalle kaksi hyvityslaskua.

4. Valitse **Uusi** ja toimi sitten seuraavasti:

    1. Valitse **Asiakastili**-kentässä **US-045**.
    2. Lisää **Laskun päivämäärä** -kenttään **15.1.2021**.
    3. Syötä **Eräpäivä**-kenttään arvo **16.1.2021**.
    4. Kirjoita **Laskurivit**-pikavälilehden **Päätili**-kenttään **401100**.
    5. Syötä **Yksikköhinta**-kentän arvoksi **-100,00**.
    6. Valitse **Kirjaa**.

5. Toista vaihe 4, mutta kirjoita **Yksikköhinta**-kenttään **-200,00**.
6. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat** ja valitse asiakas **US-045**. Tämän jälkeen voit tarkistaa aiemmin kirjaamiasi asiakastapahtumia valitsemalla toimintoruudusta **Tapahtumat \> Tapahtumat**.

    [![Kirjattujen asiakastapahtumien tarkistaminen](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Asiakkaalle US-045 on nyt luotava maksukehotuksia.

7. Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Luo maksukehotukset** ja noudata seuravia ohjeita:

    1. Määritä **Lasku**- ja **Hyvityslasku**-asetuksiksi **Kyllä**.

        Oletusarvon mukaan **Maksukehotus**-kentän arvoksi tulee **Perittävää asiakasta kohti**.

    2. Lisää **Maksukehotuksen päivämäärä** -kenttään **19.1.2021**.
    3. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja lisää sitten **Asiakastili**-kentässä asiakas **US-045**.
    4. Valitse **OK**.
    5. Luo maksukehotukset valitsemalla **OK**.

8. Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Tarkastele ja käsittele maksukehotuksia** ja noudata seuravia ohjeita:

    1. Huomaa, että sekä otsikon että tapahtumarivien maksukehotuskoodi on **Maksukehotus 1**, koska tämä maksukehotus on sarjan ensimmäinen maksukehotus. (Jos haluat tarkastella tapahtumarivejä, sinun on ehkä valittava **Tapahtumat**-pikavälilehti.)

   [![Saman maksukehotuskoodin tarkistaminen otsikossa ja riveillä](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Valitse toimintoruudussa **Kirjaa**.
    3. Lisää **Kirjauspäivämäärä** -kenttään **19.1.2021**.

    Asiakkaalle US-045 on jälleen luotava maksukehotuksia.

9. Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Luo maksukehotukset** ja noudata seuravia ohjeita:

    1. Määritä **Lasku**- ja **Hyvityslasku**-asetuksiksi **Kyllä**.

        Oletusarvon mukaan **Maksukehotus**-kentän arvoksi tulee **Perittävää asiakasta kohti**.

    2. Lisää **Maksukehotuksen päivämäärä** -kenttään **23.1.2021**.
    3. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja lisää sitten **Asiakastili**-kentässä asiakas **US-045**.
    4. Valitse **OK**.
    5. Luo maksukehotukset valitsemalla **OK**.

10. Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Tarkastele ja käsittele maksukehotuksia** ja noudata seuravia ohjeita:

    1. Huomaa, että otsikon maksukehotuskoodi on **Maksukehotus 1**. Tapahtumarivien koodi on kuitenkin **Maksukehotus 2**.

   [![Eri maksukehotuskoodien tarkistaminen otsikossa ja riveillä](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  Koodit ovat eri, koska **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -arvoksi on määritetty **Kyllä**.

  2. Älä kirjaa tätä maksukehotusta.

11. Siirry kohtaan **Luotonvalvonta \> Asetukset \> Myyntireskontran parametrit** ja määritä sitten **Perintä**-välilehdessä **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -asetukseksi **Ei**.

    [![Määritetään Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia -asetukseksi Ei](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Asiakkaalle US-045 on jälleen luotava maksukehotuksia.

12. Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Luo maksukehotukset** ja noudata seuravia ohjeita:

    1. Määritä **Lasku**- ja **Hyvityslasku**-asetuksiksi **Kyllä**.

        Oletusarvon mukaan **Maksukehotus**-kentän arvoksi tulee **Perittävää asiakasta kohti**.

    2. Lisää **Maksukehotuksen päivämäärä** -kenttään **23.1.2021**.
    3. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja lisää sitten **Asiakastili**-kentässä asiakas **US-045**.
    4. Valitse **OK**.
    5. Luo maksukehotukset valitsemalla **OK**.

13. Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Tarkastele ja käsittele maksukehotuksia** ja huomaa, että sekä otsikon että tapahtumarivien maksukehotuskoodi on **Maksukehotus 2**.

    [![Näytetään taas, että sama maksukehotuskoodi on otsikossa ja riveillä](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Sama koodi on molemmissa paikoissa, koska **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -arvoksi on määritetty nyt **Ei**.
