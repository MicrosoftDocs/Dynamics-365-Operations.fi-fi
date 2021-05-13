---
title: Ympäristön määrittäminen päätietojen hakua varten
description: Tässä aiheessa kerrotaan, miten ympäristö määritetään käyttämään veron laskennan perustietojen hakutoimintoa.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924151"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Ympäristön määrittäminen päätietojen hakua varten

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten ympäristö määritetään käyttämään veron laskennan perustietojen hakutoimintoa.

1. Määritä power platformin integraatio Lifecycle Services (LCS) -palveluissa. Lisätietoja on kohdassa [Microsoft Power Platform -apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Määritä Dynamics 365 Finance ja Microsoft Dataverse. Lisätietoja on kohdassa [Ratkaisun saaminen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ja [todennus ja hyväksyntä](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Määritä seuraavat yksiköt. Lisätietoja on kohdassa [Virtuaaliyksiköiden käyttöönotto](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
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
4. Määritä Dynamics 365 Regulatory Configuration Service (RCS) -palvelu. 
5. Luo Microsoftille palvelupyyntö, jonka avulla voidaan ottaa käyttöön seuraavien ominaisuuksien lento:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraavat ominaisuudet:

      - (Esiversio) Sähköisen raportoinnin Dataverse -tietolähteet tukevat
      - (Esiversio) Veropalvelun Dataverse-tietolähteiden tuki
      - (Esiversio) Globalisaatio-ominaisuudet

5. Kirjaudu RCS-malliin vuokraajatiliä käyttäen.
6. Siirry kohtaan **sähköinen raportointi** > **Liittyvät sovellukset**. 
7. Lisää tietue valitsemalla **Uusi** ja lisää seuraavat kenttätiedot. 

   - Anna nimi **Nimi**-kenttään.
   - Valitse **Tyyppi**-kentässä **Dataverse**.
   - Kirjoita **Sovellus**-kenttään Dataverse-URL-osoitteesi.
   - Kirjoita **Vuokraaja**-kenttään vuokraajasi.
   - Kirjoita **Mukautetun URL-osoitteen** kenttään Dataverse-URL-osoite ja liitä siihen teksti "/api/data/v9.1".

8. Valitse **Tarkista yhteys** ja viimeistele yhteysprosessi. 

   [![Tarkista yhteys -painike](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Siirry kohtaan **sähköinen raportointi** > **Verokonfiguraatiot** ja tuo verokonfiguraatiot kohteesta [Vero-konfiguraatiot](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Verokonfiguraatiot-sivu, Verotietomallipuu](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Siirry **verotettavaan tiedostomallin määritykseen** tai **Dataverse-mallimääritykseen**, jos käytät Microsoft-konfiguraatiota, ja valitse **Yhteydessä oleva sovellus** -kentästä tietue, jonka loit vaiheessa 7.
11. Määritä **Mallin yhdistämisasetuksen oletusarvoksi** **Kyllä**.

   [![Mallimäärityksen sivu](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
