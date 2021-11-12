---
title: Ympäristön määrittäminen päätietojen hakua varten
description: Tässä aiheessa kerrotaan, miten ympäristö määritetään käyttämään veron laskennan perustietojen hakutoimintoa.
author: kai-cloud
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 901f8bcb0220355866952b68e92bc2dd906bb430
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/27/2021
ms.locfileid: "7700401"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Ympäristön määrittäminen päätietojen hakua varten

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten ympäristö määritetään käyttämään veron laskennan perustietojen hakutoimintoa.

1. Määritä Microsoft Power Platformin integraatio Microsoft Dynamics Lifecycle Services (LCS) -palveluissa. Lisätietoja on kohdassa [Microsoft Power Platform -apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Kun olet suorittanut tämän vaiheen, Microsoft Power Platform -ympäristön nimi näkyy **Power Platform -integrointi** -osassa.
2. Siirry [Microsoft Power Platformin hallintakeskukseen](https://admin.powerplatform.microsoft.com/environments) ja valitse ympäristön nimi. Ympäristön URL-osoite annetaan.
3. Määritä Dynamics 365 Finance ja Dataverse. Lisätietoja: [Virtuaaliyksikköratkaisun hankkiminen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) ja [todennus ja hyväksyntä](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Määritä seuraavat yksiköt. Lisätietoja: [Microsoft Dataversen virtuaaliyksikköjen käyttöönotto](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCityEntity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity

5. Määritä Regulatory Configuration Service (RCS). Avaa **Ominaisuuksien hallinta** -työtila ja ota käyttöön seuraavat ominaisuudet:

    - Sähköisen raportoinnin Dataverse-tietolähteiden tuki
    - Veropalvelun Dataverse-tietolähteiden tuki
    - Globalisaatio-ominaisuudet

6. Kirjaudu RCS-malliin vuokraajatiliä käyttäen.
7. Siirry kohtaan **sähköinen raportointi** > **Liittyvät sovellukset**. 
8. Lisää tietue valitsemalla **Uusi** ja lisää seuraavat kenttätiedot. 

    - Anna nimi **Nimi**-kenttään.
    - Valitse **Tyyppi**-kentässä **Dataverse**.
    - Kirjoita **Sovellus**-kenttään Dataverse-URL-osoitteesi.
    - Kirjoita **Vuokraaja**-kenttään vuokraajasi.
    - Kirjoita **Mukautetun URL-osoitteen** kenttään Dataverse-URL-osoite ja liitä siihen teksti "/api/data/v9.1".

9. Valitse **Tarkista yhteys** ja viimeistele yhteysprosessi. 

    [![Tarkista yhteys -painike.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Siirry kohtaan **sähköinen raportointi** > **Verokonfiguraatiot** ja tuo verokonfiguraatiot kohteesta [Vero-konfiguraatiot](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Verokonfiguraatiot-sivu, Verotietomallipuu.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Siirry **verotettavaan tiedostomallin määritykseen** tai **Dataverse-mallimääritykseen**, jos käytät Microsoft-konfiguraatiota, ja valitse **Yhteydessä oleva sovellus** -kentästä tietue, jonka loit vaiheessa 7.
12. Määritä **Mallin yhdistämisasetuksen oletusarvoksi** **Kyllä**.

    [![Mallimäärityksen sivu.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
