---
title: Synkronoi tuoteluokitukset Dynamics 365 Retailissa
description: Tässä ohjeaiheessa kerrotaan, miten tuoteluokitukset synkronoidaan Microsoft Dynamics 365 Retail -sovelluksessa.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698162"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a>Synkronoi tuoteluokitukset Dynamics 365 Retailissa

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten tuoteluokitukset synkronoidaan Microsoft Dynamics 365 Retail -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Jotta monikanavien, kuten myyntipisteen ja puhelinkeskusten, tuoteluokituksia voidaan käyttää, luokitusten ja arvostelujen palvelun tuotteiden luokitukset on tuotava Retail-sovelluksen kanavatietokantaan. Kun tuoteluokitukset ovat käytettävissä monikanavissa, ne auttavat asiakkaita epäsuorasti myyjien kanssa tehtävässä vuorovaikutuksessa.

Tässä ohjeaiheessa esitellään seuraavat tehtävät:

1. Määritä Retail-erätyö ja tuo tuoteluokitukset.
1. Tarkista, että tuoteluokituksen synkronoinnin erätyö onnistui.
1. Määritä tuoteluokitukset käytettäviksi myyntipisteessä.

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a>Retail-erätyön määrittäminen tuoteluokitusten tuontia varten

> [!IMPORTANT]
> Varmista ennen aloittamista, että asennettuna on Retail-versio 10.0.6 tai uudempi versio.

### <a name="initialize-the-retail-scheduler"></a>Retail-ajastuksen alustaminen

Alusta Retail-ajastus noudattamalla seuraavia vaiheita:

1. Siirry kohtaan **Retail \> Headquarters-asetus \> Retail-ajastus \> Alusta Retail-ajastus**. Vaihtoehtoisesti voit tehdä haun käyttämällä Alusta Retail-ajoitus -lausetta.
1. Varmista **Alusta Retail-ajastus** -valintaikkunassa, että **Poista olemassa oleva määritys** -vaihtoehdon arvoksi on määritetty **Ei**. Valitse sitten **OK**.

### <a name="verify-the-retailproductrating-subjob"></a>RetailProductRating-alityön tarkistaminen

Seuraavalla tavalla voit tarkistaa, että **RetailProductRating**-alityö on olemassa.

1. Siirry kohtaan **Retail \> Headquarters-asetus \> Retail-ajastus \> Ajastuksen alityöt**. Vaihtoehtoisesti voit tehdä haun käyttämällä Ajastuksen alityöt -lausetta.
1. Etsi alityöluettelosta **RetailProductRating**-alityö tai hae sitä.

Seuraavassa kuvassa on esimerkki Retail-sovelluksen alityön tiedoista.

![RetailProductRating-alityön tiedot](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Jos et löydä **RetailProductRating**-alityötä, **Synkronoi tuoteluokitukset** -työ on jo ehkä suoritettu ja **1040 CDX**-työ on jo ehkä suoritettu ennen Retail-ajastuksen alustusta. Tässä tapauksessa suorita **Tietojen täydellinen synkronointi** -työ seuraavasti.
>
> 1. Siirry kohtaan **Retail \> Headquarters-asetus \> Retail-ajastus \> Kanavatietokanta**. Vaihtoehtoisesti voit tehdä haun käyttämällä kanavatietokanta-sanaa.
> 1. Valitse synkronoitava kanavatietokanta.
> 1. Valitse toimintoruudusta **Tietojen täydellinen synkronointi**.
> 1. Valitse avattavasta **Valitse jakeluaikataulu** -luettelosta **1040 - tuotteet** ja valitse sitten **OK**.
> 1. Toista edellisen proseduurin vaiheet ja varmista, että **RetailProductRating**-alityö on luotu.

### <a name="import-product-ratings"></a>Tuoteluokitusten tuominen

Voit tuoda tuoteluokitukset Retail-sovelluksiin luokitusten ja arvostelujen palvelusta seuraavasti.

1. Siirry kohtaan **Retail \> Headquarters-asetus \> Retail-ajastus \> Synkronoi tuoteluokitukset -työ**. Vaihtoehtoisesti voit tehdä haun käyttämällä Synkronoi tuoteluokitukset -työ -lausetta.
1. Valitse **Nouda tuoteluokitukset** -valintaikkunan **Suorita taustalla** -pikavälilehdessä **Toistuminen**.
1. Määritä **Määritä toistuminen** -valintaikkunassa toistumisen malli. (Ehdotettu arvo on kaksi tuntia.) Älä ajoita toistumista, joka on pienempi kuin yksi tunti.
1. Valitse **OK**.
1. Määritä **Eräkäsittely**-vaihtoehdon arvoksi **Kyllä**. Tämän asetuksen avulla voidaan varmistaa, että lokeja voi valvoa ja että erätyön suorituksen tilan voi tarkistaa.
1. Ajoita erätyö valitsemalla **OK**.

Seuraavassa kuvassa on esimerkki Retail-sovelluksen erätyön määrityksestä.

![Synkronoi tuoteluokitukset -erätyön määritys](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Varmista, että tuoteluokituksen synkronoinnin erätyö onnistui

Seuraavalla tavalla voit varmistaa, että **Synkronoi tuoteluokitukset** -erätyö onnistui.

1. Siirry kohtaan **Retail \> Järjestelmänvalvoja \> Kyselyt \> Erätyöt** tai jos käytössä on Retail-sovelluksen varastointiyksikkö, siirry kohtaan **Retail \> Kyselyt ja raportit \> Erätyöt**. Vaihtoehtoisesti voit tehdä haun erätyöt-sanalla.
1. Jos haluat tarkastella erätyön tietoja, hae erätyöluettelon **Työn kuvaus** -sarakkeessa kuvausta, jossa on maininta Nouda tuoteluokitukset.
1. Valitse työn tunnus, jos haluat tarkastella erätyön tietoja, kuten ajoituksen aloituspäivää ja aikaa ja toistuvaa tekstiä.

Seuraavassa kuvassa on esimerkki erätyön tiedoista Retail-sovelluksessa, kun erätyö on ajoitettu suoritettavaksi kahden tunnin välein.

![Synkronoi tuoteluokitus -erätyön tiedot](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Määritä tuoteluokitukset käytettäviksi myyntipisteessä

Dynamics 365 Commercen luokitusten ja arvosteluiden ratkaisu on monikanavaratkaisu. Tuotteiden luokitukset eivät kuitenkaan näy myyntipisteessä oletusarvoisesti. Jos haluat auttaa myymälöissä käyviä asiakkaita näkemään luokitukset ja arvostelut silloin, kun myyjät palvelevat heitä, ota tuoteluokitukset käyttöön myyntipisteessä.

Voit ottaa tuoteluokitukset käyttöön myyntipisteessä seuraavasti.

1. Valitse **Vähittäismyynti \> Retail-asetukset \> Parametrit \> Retail-parametrit**. Vaihtoehtoisesti voit tehdä haun Retail-parametrit-sanoilla.
1. Valitse **Määrityksen parametrit** -välilehdessä **Uusi**.
1. Anna nimi, kuten **RatingsAndReviews.EnableProductRatingsForRetailStores**, ja määritä arvoksi **Tosi**.
1. Valitse **Tallenna**.
1. Siirry kohtaan **Vähittäismyynti \> Vähittäismyynnin IT \> Jakeluaikataulu**. Vaihtoehtoisesti voit tehdä haun jakeluaikataulu-sanalla.
1. Valitse työluettelosta **1110** (**Yleinen määritys**) ja valitse sitten **Suorita nyt**.
1. Kun työ on suoritettu, tarkista, että tuotteiden luokitukset näkyvät nyt myyntipisteessä.

Seuraavassa kuvassa on esimerkki Retail-parametrien määrityksestä, joita käytetään myyntipisteen tuotteiden luokitusten käyttöönotossa.

![Myyntipisteen tuoteluokitusten Retail-parametrien määritys](media/rnr-hq-enable-ratings-in-pos.png)

Seuraavassa kuvassa on esimerkki myyntipisteen tuoteluokituksista.

![Myyntipisteen tuoteluokitukset](media/rnr-pos-catalog-ratings.png)

Seuraavassa kuvassa on esimerkki puhelinkeskuskanavien tuoteluokituksista.

![Puhelinkeskuskanavan tuoteluokitukset](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Osallistu käyttääksesi luokituksia ja arvosteluja](opt-in-ratings-reviews.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Määritä luokitukset ja arvostelut](configure-ratings-reviews.md)
