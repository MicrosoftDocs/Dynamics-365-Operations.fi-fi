---
title: Asiakkaan alkuperäisen maksuennustemallin arvioiminen (esiversio)
description: Tässä ohjeaiheessa kuvataan vaiheet, joiden avulla opit lisää asiakkaan maksuennustemallista ja voit arvioida sen tehokkuuden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 9cbe0308902071c066d18ce71e6e33422207e8ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245589"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a>Asiakkaan alkuperäisen maksuennustemallin arvioiminen (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten ennustemalli arvioidaan sen jälkeen, kun Finance Insights on otettu käyttöön ja ensimmäinen malli on luotu ja koulutettu. Tässä ohjeaiheessa käsitellään asiakasmaksujen ennustamiseen liittyviä malleja. Siinä kuvataan vaiheet, joiden avulla opit lisää asiakkaan maksuennustemallista ja voit arvioida sen tehokkuuden.

## <a name="getting-details-about-the-model"></a>Mallin tietojen hakeminen

**Finance Insights -parametrit** -sivulla Microsoft Dynamics 365 Financessa tarkkuuspisteiden vieressä on **Paranna mallin tarkkuutta** -linkki.

[![Paranna mallin tarkkuutta -linkki](./media/prediction-model.png)](./media/prediction-model.png)

Tämä linkki vie AI Builderiin, josta saat lisätietoja nykyisestä mallista. Voit myös parantaa mallia siellä. Seuraavassa kuvassa on näyttöön avautuva sivu.

[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)

Avautuva sivu sisältää seuraavat tiedot:

- **Suorituskyky**-osan mallin suorituskykyluokka kertoo mallin laadusta. Lisätietoja tästä luokasta on kohdassa [Ennustemallin suorituskyky](https://docs.microsoft.com/ai-builder/prediction-performance) AI Builderin dokumentaatiossa.
- **Vaikuttavimmat tiedot** -osassa näkyy, miten tärkeitä tietojen eri syöttötyypit olivat mallille. Voit arvioida tämän luettelon ja vastaavat prosenttiosuudet ja määrittää, ovatko tiedot yhdenmukaisia yrityksen ja markkinoiden kanssa.

    [![Ennustemallin Suorituskyky- ja Vaikuttavimmat tiedot -osat](./media/models.png)](./media/models.png)

- Valitse **Suorituskyky**-osassa **Katso tiedot**, jos haluat lisätietoja luokasta ja muista kohdista. Seuraavassa kuvassa nähdään, että malli käyttää vähemmän tietoja kuin suositellaan. Siksi järjestelmä on luonut varoitussanoman.

    [![Mallin suorituskykyyn liittyviä varoituksia](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Lisätietoja

Vaikka tarkkuus on hyvä aloituskohta mallin arvioinnissa, ja suorituskyvyn luokka tarjoaa näkökulman, AI Builder sisältää yksityiskohtaisempia mittareita arviointia varten. Jos haluat ladata tiedot, valitse **Suorituskyky**-osassa kolmen pisteen painike (**...**) **Käytä mallia** -painikkeen vieressä. Valitse sitten **Lataa yksityiskohtaiset mittarit**.

[![Lataa yksityiskohtaiset mittarit -komento](./media/performance.png)](./media/performance.png)

Seuraavassa kuvassa näkyy muoto, josta tiedot voidaan ladata.

[![Ladattujen tietojen muoto](./media/data-format.png)](./media/data-format.png)

Tulosten tarkempi analyysi on hyvä aloittaa tarkastelemalla sekaannusmatriisimittaria. Tässä on esimerkiksi tietoja, jotka näkyvät kyseiselle mittarille edellisessä kuvassa.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

Voit laajentaa nämä tiedot seuraavalla tavalla.

|                          | Ennustettu ajoissa | Ennustettu myöhässä | Ennustettu erittäin paljon myöhässä |
|--------------------------|-------------------|----------------|---------------------|
| Todellinen ajoissa tehty maksu   | **71**            | 0              | 21                  |
| Todellinen myöhässä oleva maksu      | 5                 | **0**          | 27                  |
| Todellinen erittäin paljon myöhässä oleva maksu | 2                 | 0              | **45**              |

Sekaannusmatriisi näyttää satunnaisesti valitun testitietojoukon tulokset koulutusprosessista. Koska näitä suljettuja laskuja ei käytetty mallin kouluttamisessa, ne ovat mallin kannalta hyviä testitapauksia. Koska laskun todellinen tila on tiedossa, nähdään myös mallin suorituskyky.

Ensimmäiseksi etsittävä seikka on yleisin todellinen arvo. Vaikka tämä arvo ei ehkä ole täysin yhdenmukainen koko tietojoukon kanssa, se on kohtuullinen arvio. Tässä tapauksessa **Todellinen ajoissa tehty maksu** tapahtuu 92 laskussa kaikista 171 laskusta. Se on yleisin todellinen arvo. Siksi se on hyvä mallin perustaso. Jos vain arvasit, että kaikki laskut maksetaan ajoissa, olet oikeassa 92 kertaa 171 laskun kohdalla (eli 54 prosenttia arvattiin oikein).

On tärkeää ymmärtää, miten tasapainoinen tietojoukko on. Tässä tapauksessa 92 laskua kaikkiaan 171 laskusta maksettiin ajoissa. 32 maksettiin myöhässä ja 47 erittäin paljon myöhässä. Nämä arvot osoittavat, että tietojoukko on suhteellisen tasapainoinen. Tämä siksi, koska missään luokituksessa ei ole triviaaleja tuloksia. Tilanne, jossa yksi näistä tiloista saa hyvin vähän tuloksia, voi olla haastava koneoppimismallille.

Mallin tarkkuus ilmaisee testitietojoukon oikeiden ennusteiden määrän. Nämä oikeat ennusteet ovat arvoja, jotka näkyvät edellä olevassa esimerkissä lihavoituna. Tässä tapauksessa arvot tuottavat lasketuksi tarkkuudeksi 67,8 prosenttia (= \[71 + 0 + 45\] ÷ 171). Tämä arvo merkitsee 14 prosentin parannusta perusarvaukseen, joka oli 54 prosenttia. Se on yksi mallin laadun ilmaisin.

Jos tarkastelemme lähemmin sekaannusmatriisia, huomaamme, että malli toimii hyvin ennustaessaan ajallaan ja erittäin paljon myöhässä suoritettavia maksuja. Se on kuitenkin väärässä kaikissa 32 laskussa, jotka maksettiin myöhässä (mutta ei erittäin paljon myöhässä). Tämä tulos viittaa siihen, että on tarpeen tutkia ja parantaa mallia.

Tarkkuutta paremmin mallin suorituskykyä osoittava luku on F1-makropistemäärä. Tämä pistemäärä osoittaa kunkin luokituksen tilan tulokset (ajallaan, myöhässä, erittäin paljon myöhässä). Tässä on esimerkiksi tietoja, jotka näkyvät F1-makromittarille edellisessä kuvassa.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

Tässä tapauksessa F1-makropistemäärä, noin 49.3 prosenttia, osoittaa, että malli ei tuota tehokkaita ennusteita kaikissa tiloissa, vaikka yleinen tarkkuuspistemäärä näyttää olevan suhteellisen korkea.

## <a name="improving-the-model"></a>Mallin parantaminen

Kun olet ymmärtänyt ensimmäisen mallin tulokset paremmin, voit parantaa mallia lisäämällä tai poistamalla toimintosarakkeita tai suodattamalla kaikki tietojoukon osat, jotka eivät tue tarkkoja ennusteita. Sulje AI Builder ja käytä sitten **Paranna mallia** -linkkiä Dynamics 365 Financessa ja käynnistä AI Builder -prosessi uudelleen. Voit kokeilla erilaisia ominaisuuksia vaikuttamatta julkaistuun malliin. Julkaistua mallia muutetaan vain, kun valitset **Julkaise**. Muista, että Dynamics 365 Finance -esiintymässä käytetään yhtä mallia. Tämän vuoksi sinun on tarkistettava kaikki uudet mallit huolellisesti ennen julkaisemista.

## <a name="for-more-information"></a>Lisätietoja

Lisätietoja ennustemallien arvioimisesta on kohdassa [Koneoppimismallien tulokset](/confusion-matrix.md)

#### <a name="privacy-notice"></a>Tietosuojatiedot
Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]