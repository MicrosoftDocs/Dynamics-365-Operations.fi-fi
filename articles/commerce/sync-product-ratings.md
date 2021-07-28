---
title: Synkronoi tuoteluokitukset Dynamics 365 Commercessa
description: Tässä ohjeaiheessa kerrotaan, miten tuoteluokitukset synkronoidaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6f23b4c15937a0e61eb64b25eadef58c1fda231e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354610"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>Synkronoi tuoteluokitukset Dynamics 365 Commercessa

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten tuoteluokitukset synkronoidaan Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskuvaus

Jotta monikanavien, kuten myyntipisteen ja puhelinkeskusten, tuoteluokituksia voidaan käyttää, luokitusten ja arvostelujen palvelun tuotteiden luokitukset on tuotava Commerce-sovelluksen kanavatietokantaan. Kun tuoteluokitukset ovat käytettävissä monikanavissa, ne auttavat asiakkaita epäsuorasti myyjien kanssa tehtävässä vuorovaikutuksessa.

Tässä ohjeaiheessa esitellään seuraavat tehtävät:

1. **Tuoteluokitusten synkronointityön** määrittäminen erätyönä tuoteluokitusten synkronoimiseksi **Luokitus- ja arvostelupalvelussa**.
1. Tarkista, että tuoteluokituksen synkronoinnin erätyö onnistui.
1. Määritä tuoteluokitukset käytettäviksi myyntipisteessä.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Määritä erätyö ja synkronoi tuoteluokitukset

> [!IMPORTANT]
> Varmista ennen aloittamista, että asennettuna on Dynamics 365 Commerce -versio 10.0.6 tai uudempi versio.

### <a name="initialize-the-commerce-scheduler"></a>Commerce-ajastuksen alustaminen

Alusta Commerce-ajastus noudattamalla seuraavia vaiheita:

1. Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Commerce-ajastus \> Alusta Commerce-ajastus**. Vaihtoehtoisesti voit tehdä haun käyttämällä Alusta Commerce-ajoitus -lausetta.
1. Varmista **Alusta Commerce-ajastus** -valintaikkunassa, että **Poista olemassa oleva määritys** -vaihtoehdon arvoksi on määritetty **Ei**. Valitse sitten **OK**.

### <a name="verify-the-retailproductrating-subjob"></a>RetailProductRating-alityön tarkistaminen

Seuraavalla tavalla voit tarkistaa, että **RetailProductRating**-alityö on olemassa.

1. Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Commerce-ajastus \> Aikataulun alatyöt**. Vaihtoehtoisesti voit tehdä haun käyttämällä Ajastuksen alityöt -lausetta.
1. Etsi alityöluettelosta **RetailProductRating**-alityö tai hae sitä.

Seuraavassa kuvassa on esimerkki Commerce-sovelluksen alityön tiedoista.

![RetailProductRating-alityön tiedot.](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Jos et löydä **RetailProductRating**-alityötä, **Synkronoi tuoteluokitukset** -työ on jo ehkä suoritettu ja **1040 CDX**-työ on jo ehkä suoritettu ennen Commerce-ajastuksen alustusta. Tässä tapauksessa suorita **Tietojen täydellinen synkronointi** -työ seuraavasti.

> 1. Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Commerce-ajastus \> Kanavatietokanta**. Vaihtoehtoisesti voit tehdä haun käyttämällä kanavatietokanta-sanaa.
> 1. Valitse synkronoitava kanavatietokanta.
> 1. Valitse toimintoruudusta **Tietojen täydellinen synkronointi**.
> 1. Valitse avattavasta **Valitse jakeluaikataulu** -luettelosta **1040 - tuotteet** ja valitse sitten **OK**.
> 1. Toista edellisen proseduurin vaiheet ja varmista, että **RetailProductRating**-alityö on luotu.

### <a name="import-product-ratings"></a>Tuoteluokitusten tuominen

Voit tuoda tuoteluokitukset Commerce-sovelluksiin luokitusten ja arvostelujen palvelusta seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Headquarters-asetus \> Commerce-ajastus \> Synkronoi tuoteluokitukset -työ**. Vaihtoehtoisesti voit tehdä haun käyttämällä Synkronoi tuoteluokitukset -työ -lausetta.
1. Valitse **Nouda tuoteluokitukset** -valintaikkunan **Suorita taustalla** -pikavälilehdessä **Toistuminen**.
1. Määritä **Määritä toistuminen** -valintaikkunassa toistumisen malli. (Ehdotettu arvo on kaksi tuntia.) Älä ajoita toistumista, joka on pienempi kuin yksi tunti.
1. Valitse **OK**.
1. Määritä **Eräkäsittely**-vaihtoehdon arvoksi **Kyllä**. Tämän asetuksen avulla voidaan varmistaa, että lokeja voi valvoa ja että erätyön suorituksen tilan voi tarkistaa.
1. Ajoita erätyö valitsemalla **OK**.

Seuraavassa kuvassa on esimerkki Commerce-sovelluksen erätyön määrityksestä.

![Synkronoi tuoteluokitukset -erätyön määritys.](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Varmista, että tuoteluokituksen synkronoinnin erätyö onnistui

Seuraavalla tavalla voit varmistaa, että **Synkronoi tuoteluokitukset** -erätyö onnistui.

1. Siirry kohtaan **Retail ja Commerce \> Järjestelmänvalvoja \> Kyselyt \> Erätyöt** tai jos käytössä on Commerce-sovelluksen varastointiyksikkö, siirry kohtaan **Retail ja Commerce \> Kyselyt ja raportit \> Erätyöt**. Vaihtoehtoisesti voit tehdä haun erätyöt-sanalla.
1. Jos haluat tarkastella erätyön tietoja, hae erätyöluettelon **Työn kuvaus** -sarakkeessa kuvausta, jossa on maininta Nouda tuoteluokitukset.
1. Valitse työn tunnus, jos haluat tarkastella erätyön tietoja, kuten ajoituksen aloituspäivää ja aikaa ja toistuvaa tekstiä.

Seuraavassa kuvassa on esimerkki erätyön tiedoista Commerce-sovelluksessa, kun erätyö on ajoitettu suoritettavaksi kahden tunnin välein.

![Synkronoi tuoteluokitus -erätyön tiedot.](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Määritä tuoteluokitukset käytettäviksi myyntipisteessä

Dynamics 365 Commercen luokitusten ja arvosteluiden ratkaisu on monikanavaratkaisu. Tuotteiden luokitukset eivät kuitenkaan näy myyntipisteessä oletusarvoisesti. Jos haluat auttaa myymälöissä käyviä asiakkaita näkemään luokitukset ja arvostelut silloin, kun myyjät palvelevat heitä, ota tuoteluokitukset käyttöön myyntipisteessä.

Voit ottaa tuoteluokitukset käyttöön myyntipisteessä seuraavasti.

1. Valitse **Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Commerce-parametrit**. Vaihtoehtoisesti voit tehdä haun Commerce-parametrit-sanoilla.
1. Valitse **Määrityksen parametrit** -välilehdessä **Uusi**.
1. Anna nimi, kuten **RatingsAndReviews.EnableProductRatingsForRetailStores**, ja määritä arvoksi **Tosi**.
1. Valitse **Tallenna**.
1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**. Vaihtoehtoisesti voit tehdä haun jakeluaikataulu-sanalla.
1. Valitse työluettelosta **1110** (**Yleinen määritys**) ja valitse sitten **Suorita nyt**.
1. Kun työ on suoritettu, tarkista, että tuotteiden luokitukset näkyvät nyt myyntipisteessä.

Seuraavassa kuvassa on esimerkki Commerce-parametrien määrityksestä, joita käytetään myyntipisteen tuotteiden luokitusten käyttöönotossa.

![Myyntipisteen tuoteluokitusten Commerce-parametrien määritys.](media/rnr-hq-enable-ratings-in-pos.png)

Seuraavassa kuvassa on esimerkki myyntipisteen tuoteluokituksista.

![Myyntipisteen tuoteluokitukset.](media/rnr-pos-catalog-ratings.png)

Seuraavassa kuvassa on esimerkki puhelinkeskuskanavien tuoteluokituksista.

![Puhelinkeskuskanavan tuoteluokitukset.](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Lisäresurssit

[Luokitukset ja arvostelut – yleiskatsaus](ratings-reviews-overview.md)

[Luokitusten ja arvostelujen käytön hyväksyminen](opt-in-ratings-reviews.md)

[Hallitse luokituksia ja arvosteluja](manage-reviews.md)

[Määritä luokitukset ja arvostelut](configure-ratings-reviews.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]