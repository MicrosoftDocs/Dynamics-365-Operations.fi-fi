---
title: Myyntitilausten mobiilityötila
description: Tässä artikkelissa on tietoja Myyntitilaukset-mobiilityötilasta. Tämän työtilan avulla pysyt ajan tasalla myyntitilauksista milloin ja missä tahansa.
author: Henrikan
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 38971f2a5f3f3d2692de0e52365e2215170101cc
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103177"
---
# <a name="sales-orders-mobile-workspace"></a>Myyntitilausten mobiilityötila

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Tässä artikkelissa on tietoja **Myyntitilaukset**-mobiilityötilasta. Tämän työtilan avulla pysyt ajan tasalla myyntitilauksista milloin ja missä tahansa. 

Tämä mobiilityötila on tarkoitettu käytettäväksi talous- ja toimintosovellusten (Dynamics 365) mobiilisovelluksen kanssa.

## <a name="overview"></a>Yleiskuvaus
**Myyntitilaukset** -mobiilin työtilan avulla voit tarkastella kunkin myyntitilauksen yksityiskohtaisia tietoja. Näihin tietoihin kuuluvat tilauksen tila, asiakkaan yhteystiedot ja tilauksen vastaanottajan yhteystiedot. **Myyntitilausten** mobiilityötilassa on pikanäyttö myyntitilauksista. Voit tarkastella myyntitilauksia asiakaskohtaisesti, näyttää kaikki myyntitilaukset tai tarkastella yksittäisen myyntitilauksen tietoja. 

Mobiili työtila tarjoaa kaksi näkymää, joilla voit analysoida myyntitilausten yksityiskohtia.

### <a name="view-all-sales-orders"></a>Näytä kaikki myyntitilaukset
Tämä näkymä sisältää kaikki myyntitilaukset.

-   Valitse tarkasteltavat myyntitilaukset seuraavien suodattimien avulla:

    -   Etsi myyntitilauksen perusteella
    -   Etsi asiakastilin perusteella
    -   Etsi asiakkaan nimen perusteella
    -   Etsi tilan perusteella
    -   Etsi vapautustilan perusteella
    -   Etsi luontipäivämäärän ja -ajan perusteella
    
-   Kun olet valinnut myyntitilaukset, voit tarkastella tiettyjen tilausten lisätietoja. Voit tarkastella seuraavia tietoja:

    -   Asiakkaan nimi ja osoitetiedot
    -   Myyntitilauksen päivämäärät, kuten pyydetty lähetyspäivämäärä ja vahvistettu lähetyspäivämäärä
    -   Tilauksen vastaanottajan yhteystiedot
    -   Asiakkaan yhteystiedot
    -   Tilausrivit
    -   Lähetykset, joista näet miten ja milloin myyntitilaus on toimitettu

### <a name="view-orders-for-a-customer"></a>Tarkastele asiakkaan tilauksia
Tässä näkymässä on asiakaskohtainen luettelo myyntitilauksista.

-   Voit tarkastella asiakkaan myyntitilauksia seuraavien suodattimien avulla:

    -   Etsi nimen perusteella
    -   Etsi tilin perusteella

-   Kun olet valinnut asiakkaan, tarkasteltavana ovat seuraavat tiedot:

    -   Asiakkaan nimi ja ryhmä
    -   Asiakkaan yhteystiedot
    -   Asiakkaan myyntitilaukset ja tilausten tiedot:
    
        -   Asiakkaan nimi ja osoitetiedot
        -   Myyntitilauksen eri päivämäärät
        -   Tilauksen vastaanottajan yhteystiedot
        -   Asiakkaan yhteystiedot
        -   Tilausrivit
        -   Lähetykset, joista näet miten ja milloin myyntitilaus on toimitettu

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Managementin käytön edellytykset 
Jos Supply Chain Management on otettu käyttöön organisaatiossasi, järjestelmänvalvojan on julkaistava **Myyntitilaukset**-mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Edellytykset, jos käytössä on Dynamics 365 for Operationsin versio 1611 ja platform update 3 tai uudempi
Jos organisaatiossa on otettu käyttöön Dynamics 365 for Operationsin versio 1611 ja platform update 3 tai uudempi, järjestelmänvalvojan on toteutettava seuraavat edellytykset. 

<table>
<thead>
<tr class="header">
<th>Edellytys</th>
<th>Rooli</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ota KB 4013633 käyttöön.</td>
<td>Järjestelmänvalvoja</td>

<td>KB 4013633 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>Myyntitilaukset</strong>-mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4013633 -päivityksen.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Ota käyttöönotettava paketti käyttöön</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Julkaise <strong>Myyntitilaukset</strong>-mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen
Talous- ja toimintosovellusten (Dynamics 365) mobiilisovelluksen lataaminen ja asentaminen:

-   [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
-   [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen

1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna Dynamics 365 -URL-osoitteesi.
3.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
4.  Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

[![Päivittäminen vetämällä.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Tarkastele asiakkaan myyntitilausten tietoja mobiilin Myyntitilaukset-työtilan avulla.

1.  Valitse mobiililaitteessasi **Myyntitilaukset** -työtila.
2.  Valitse **Tarkastele asiakkaan tilauksia**.
3.  Etsi haluamasi asiakas tilin tai asiakkaan nimen avulla.
4.  Valitse asiakas.
5.  Valitse **Yhteystiedot** tai **Myyntitilaukset**. Jos valittuna on **Myyntitilaukset**, näyttöön tulee luettelo asiakkaan myyntitilauksista.
6.  Valitse **Myyntitilaus**. Voit nyt tarkastella tietoja myyntitilausriveistä, toimituksista, asiakkaan yhteystiedoista ja tilauksen vastaanottajan yhteystiedoista.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

