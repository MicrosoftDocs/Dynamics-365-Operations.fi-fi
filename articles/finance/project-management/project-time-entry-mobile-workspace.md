---
title: Projektin aikamerkintöjen mobiilityötila
description: Tässä ohjeaiheessa on tietoja projektin aikamerkintöjen mobiilityötilasta. Työtilan avulla käyttäjät voivat syöttää ja tallentaa projektin aikakirjauksia mobiililaittella.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250366"
---
# <a name="project-time-entry-mobile-workspace"></a>Projektin aikamerkintöjen mobiilityötila

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **projektin aikamerkintöjen** mobiilityötilasta. Työtilan avulla käyttäjät voivat syöttää ja tallentaa projektin aikakirjauksia mobiililaittella.

Tätä mobiilityötilaa on tarkoitettu käytettäväksi Dynamics 365 Unified Ops -sovelluksella. 

## <a name="overview"></a>Yleiskuvaus
Projektiresurssit ovat kohteessa tai liikkeellä osana päivittäistä työtään. **Projektin aikamerkinnät** -mobiilityötilan avulla käyttäjät voivat syöttää laskutettavan tai ei-laskutettavan aikansa projektiin valitsemallaan mobiililaitteella. Tämän ansiosta projektiresurssit voivat tehdä aikakirjauksia missä ja milloin tahansa. He voivat myös tarkastella aiemmin kirjattuja merkintöjä. 

Käyttäjät voivat suorittaa seuraavat tehtävät **projektin aikamerkintöjen** mobiilityötilassa:

-   Anna valitulle päivämäärällä tuntien määrä, jonka olet käyttänyt tietyn tehtävän suorittamiseen.
-   Hae projekti, jolle haluat kirjata tunteja projektin tai asiakkaan nimellä .
-   Määritä käyttämällesi ajalle luokka ja tehtävä.
-   Kirjaa aika projektiin laskutettavaksi tai ei-laskutettavaksi.
-   Voit myös kirjoittaa ulkoisia tai sisäisiä kommentteja.

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Edellytykset, jos käytössä on Dynamics 365 Finance
Jos Finance on otettu käyttöön organisaatiossa, järjestelmänvalvojan on julkaistava **Projektin aikamerkintä** -mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Edellytykset, jos käytössä on versio 1611 ja Platform update 3 tai uudempi
Jos organisaatiossa on otettu käyttöön versio 1611 ja Platform update 3 tai uudempi, järjestelmänvalvojan on toteutettava seuraavat edellytykset. 

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

<td>KB 4018050 -käyttöönotto.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 4018050 on X++-päivitys tai metatietojen korjaus, joka sisältää <strong>projektin aikakirjausten</strong> mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4018050 -päivityksen.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Luo käyttöön otettava paketti</a>, joka sisältää <strong>ApplicationSuite</strong>- ja <strong>ProjectMobile</strong>-mallit ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Ota käyttöönotettava paketti käyttöön</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Julkaise <strong>projektin aikamerkintöjen</strong> mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen

Finance and Operations -mobiilisovelluksen lataaminen ja asentaminen:

-   [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
-   [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen
1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna Dynamics 365 -URL-osoitteesi.
3.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
4.  Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Aikakirjausten syöttäminen Projektin aikakirjausten mobiilityötilassa
1.  Valitse mobiililaitteessasi **Projektin aikakirjausten** työtila.
2.  Valitse **Aikamerkintä**. Kuluvan viikon kalenteripäivät näytetään.
3.  Napsauta valitun päivän kohdalla **Toiminnot** &gt; **Uusi kirjaus**.
4.  Anna kirjattava tuntien määrä.
5.  Valitse aikakirjauksen kohdeprojekti. Luettelo koostuu projekteista, jotka on ladattu sovellukseen offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Lisätietoja on ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Jos projekti ei ole luettelossa, valitse **Hae**. Voit hakea nimen, projektin nimen tai asiakkaan perusteella.
7.  Valitse luokka. Luettelo koostuu luokista, jotka on ladattu sovellukseen offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Lisätietoja on ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Jos luokka ei ole luettelossa, valitse **Hae**. Etsi luokan tai luokan nimen mukaan.
9.  Valitse tehtävä. Luettelo koostuu tehtävistä, jotka on ladattu sovellukseen offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Lisätietoja on ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Jos tehtävä ei ole luettelossa, valitse **Hae**. Etsi tehtävän numeron tai tarkoituksen mukaan.

11. Valitse rivin ominaisuus.
12. Voit myös kirjoittaa ulkoisia tai sisäisiä kommentteja.
13. Valitse **Valmis**.
