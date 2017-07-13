---
title: "Myyntitilausten mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja Myyntitilaukset-mobiilityötilasta. Tämän työtilan avulla pysyt ajan tasalla myyntitilauksista milloin ja missä tahansa."
author: Mirzaab
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: a0edbad63c51d111d7c8985aa7fdf7312da6149d
ms.openlocfilehash: 1a05c6c12d4b6d98886e418aadcc0bdb2c2fc8ef
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Myyntitilausten mobiilityötila
<a id="sales-orders-mobile-workspace" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **Myyntitilaukset**-mobiilityötilasta. Tämän työtilan avulla pysyt ajan tasalla myyntitilauksista milloin ja missä tahansa. 

Tätä mobiilityötilaa on tarkoitettu käytettäväksi Microsoft Dynamics 365 for Unified Operations -mobiilisovelluksella.

## Yleiskuvaus
<a id="overview" class="xliff"></a>
**Myyntitilaukset** -mobiilin työtilan avulla voit tarkastella kunkin myyntitilauksen yksityiskohtaisia tietoja. Näihin tietoihin kuuluvat tilauksen tila, asiakkaan yhteystiedot ja tilauksen vastaanottajan yhteystiedot. **Myyntitilausten** mobiilityötilassa on pikanäyttö myyntitilauksista. Voit tarkastella myyntitilauksia asiakaskohtaisesti, näyttää kaikki myyntitilaukset tai tarkastella yksittäisen myyntitilauksen tietoja. 

Mobiili työtila tarjoaa kaksi näkymää, joilla voit analysoida myyntitilausten yksityiskohtia.

### Näytä kaikki myyntitilaukset
<a id="view-all-sales-orders" class="xliff"></a>
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

### Tarkastele asiakkaan tilauksia
<a id="view-orders-for-a-customer" class="xliff"></a>
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

## Edellytykset
<a id="prerequisites" class="xliff"></a>
Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.

### Edellytykset, jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys
<a id="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update" class="xliff"></a> 
Jos Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys on otettu organisaatiossa käyttöön, järjestelmänvalvojan on julkaistava **Myyntitilaukset**-mobiilityötilassa. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operationsin versio 1611, johon on asennettu vähintään ympäristöpäivitys 3
<a id="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later" class="xliff"></a>
Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operationsin versio 1611, jossa on vähintään ympäristöpäivitys 3, järjestelmänvalvojan on toteutettava seuraavat edellytykset. 

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
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Lataa metatietojen hotfix-korjaus Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Ota käyttöönotettava paketti käyttöön</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Julkaise <strong>Myyntitilaukset</strong>-mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## Mobiilisovelluksen lataaminen ja asentaminen
<a id="download-and-install-the-mobile-app" class="xliff"></a>
Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:

-   [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
-   [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## Kirjautuminen mobiilisovellukseen
<a id="sign-in-to-the-mobile-app" class="xliff"></a>

1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna Dynamics 365 -URL-osoitteesi.
3.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
4.  Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## Tarkastele asiakkaan myyntitilausten tietoja mobiilin Myyntitilaukset-työtilan avulla.
<a id="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace" class="xliff"></a>

1.  Valitse mobiililaitteessasi **Myyntitilaukset** -työtila.
2.  Valitse **Tarkastele asiakkaan tilauksia**.
3.  Etsi haluamasi asiakas tilin **tai asiakkaan nimen avulla.
4.  Valitse asiakas.
5.  Valitse **Yhteystiedot** tai **Myyntitilaukset**. Jos valittuna on **Myyntitilaukset**, näyttöön tulee luettelo asiakkaan myyntitilauksista.
6.  Valitse **Myyntitilaus**. Voit nyt tarkastella tietoja myyntitilausriveistä, toimituksista, asiakkaan yhteystiedoista ja tilauksen vastaanottajan yhteystiedoista.

