---
title: Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (19. marraskuuta 2019)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa984a01e9da30e6da07516fa2986833366a882b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527141"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Dynamics 365 Talent:n uudet tai muuttuneet ominaisuudet (19. marraskuuta 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa käsitellään Dynamics 365 Talentin uusia tai muuttuneita toimintoja.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2621. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Ympäristön päivitys 31 Finance and Operations -sovelluksille

Lisätietoja on kohdassa [Finance and Operations -sovellusten Platform update 31 -päivityksen esiversiotoiminnot (tammikuu 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31).

### <a name="feature-management-workspace-383856"></a>Toimintojen hallinta -työtila (383856)

**Toimintojen hallinta** -työtilassa on luettelo kussakin julkaisussa toimitetuista toiminnoista. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota. Lisätietoja Toimintojen hallinnasta on kohdassa [Toimintojen hallinnan yleiskuvaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kaikki uudet toiminnot pysyvät esiversiossa ainakin 30 päivää ja yleensä 30–60 päivää. Tärkeimmät toiminnot ovat yleensä saatavana kunkin vuoden lokakuussa ja huhtikuussa esiversiojakson jälkeen. Voit ottaa uudet ominaisuudet käyttöön heti, kun näet ne **Toimintojen hallinta** -työtilassa. Jotkin toiminnot on ehkä otettu käyttöön oletusarvoisesti.
 
Joskus keskeinen toiminto on otettu käyttöön oletusarvoisesti eikä sitä voi poistaa käytöstä (esimerkiksi **Toimintojen hallinta** -työtilassa).
 
Kun toiminto on yleisesti saatavana, se voidaan ottaa käyttöön tai poistaa käytöstä tuotantoympäristöissä. **Toimintojen hallinta** -työtila ilmaisee, milloin esiversiotoiminto tulee pakolliseksi. Tämä päivämäärä on yleensä 1. lokakuuta tai 1. huhtikuuta eli ne vastaavat puolivuotisia julkaisusuunnitelmia. Pakollisia toimintoja ei voi poistaa käytöstä. Toiminnon voi ottaa käyttöön ja poistaa käytöstä kaikissa ympäristöissä siihen saakka, että muuttuu pakolliseksi.

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>Sanoma avautuu, kun toimella on peruutettu toimenpide (382887)

Seuraava sanoma ei enää avaudu, kun valitset tietyn toimen ja toimessa on käytettävissä vain peruutettu toimenpide: **Toimelle xxxxxx on meneillään keskeneräinen toiminto**.

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>Oppimisanalytiikan kurssin tyypin ja tilan tiedot ovat virheelliset (381151)

Tämän viikon julkaisu päivitti oppimisanalytiikan näyttämään **kurssin tyypin** ja **tilan** oikein.

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>Henkilönumeron pitäisi näkyä Uusi työntekijä -lomakkeen ilmoituspalkissa (383832)

**Henkilönumero** näkyy **Uusi työntekijä** -lomakkeen ilmoituspalkissa, josta sen voi nopeasti tarkistaa.

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>Toimen aloituspäivä määrittää, millä työtietueella kompensaatiotaso noudetaan työhönoton aikana (350361)

Tässä julkaisussa **Kompensaation alkamispäivä** määrittää uudelle työlle määritetyn tason.

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>Toimi-taulun mukautettuja keräysluettelokenttiä ei synkronoida Common Data Serviceen (387503)

Tässä versiossa keräysluettelonimikkeet synkronoidaan nyt Common Data Servicen kanssa.

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>Työntekijän osoiteyksikköä ei synkronoida Common Data Servicen kanssa uusia tietoja tuotaessa (349673)

Tämän viikon julkaisussa osoitetiedot synkronoidaan nyt Common Data Servicen kanssa uusia tietoja tuotaessa.

## <a name="in-preview"></a>Esiversiossa

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Katso lisätietoja Dynamics 365: vuoden 2019 julkaisuaallon 2 suunnitelman kohdasta [Kehityskeskustelujen tulostaminen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews).


[!INCLUDE[footer-include](../includes/footer-banner.md)]