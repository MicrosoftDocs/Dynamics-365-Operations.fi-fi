---
title: Käytettävissä olevan varaston mobiilityötila
description: Tässä ohjeaiheessa on tietoja käytettävissä olevan varaston mobiilityötilasta. Käytettävissä olevan varaston mobiilityötila auttaa syventämään näkemyksiä varatusta ja käytettävissä olevasta varastosta mobiilisti milloin tahansa ja missä tahansa.
author: Mirzaab
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7d0440514369f8271004993d009ef7c3a36edb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008044"
---
# <a name="inventory-on-hand-mobile-workspace"></a>Käytettävissä olevan varaston mobiilityötila

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **käytettävissä olevan varaston** mobiilityötilasta. Tämä työtila auttaa syventämään näkemyksiä varatusta ja käytettävissä olevasta varastosta milloin tahansa ja missä tahansa.

Tämä mobiilityötila on tarkoitettu käytettäväksi Finance and Operations -mobiilisovelluksen kanssa.

## <a name="overview"></a>Yleiskuvaus
Yleensä yrityksillä on useita varaston toimituksia ja vastaanottoja joka päivä. Näiden siirrot muuttavat jatkuvasti käytettävissä olevan varaston tilaa. **Käytettävissä olevan varaston** mobiilityötilassa näet koko yrityksen käytettävissä olevan varaston tilan, jolloin voit hyödyntää uusimpia varastotietoja haluamassasi mobiililaitteessa. Riippumatta siitä, työskenteletkö fyysisessä varastossa, ostossa, myynnissä, tuotannossa, yrityksen johdossa tai muussa roolissa, voit käyttää käytettävissä olevan varaston tietoja milloin tahansa ja missä tahansa. 

Mobiilityötila sisältää välittömän näkymän käytettävissä olevan varaston tilasta kaikissa tiloissa. Sen avulla voit tarkastella käytettävää varastoa eri tiloissa, nykyisiä materiaalivarauksia ja varaamatonta, käytettävissä olevaa varastoa. Voit myös syöttää nimikenumeron suorittaaksesi kyselyjä käytettävissä olevaan varastoon ja suorittaa suodatetun haun varastotuotteille ja varianteille. 

Erityisesti mobiilityötilassa on nämä ominaisuudet:

-   Voit etsiä tuotenumerolla tai tuotteen nimellä löytääksesi tuotteita ja tarkastellaksesi niiden käytettävissä olevan varaston tilaa.
-   Voit tarkastella valittujen tuotteiden osalta seuraavia tietoja:

    -   Käytettävissä oleva varasto toimipaikan mukaan
    -   Käytettävissä oleva varasto fyysisten varastojen mukaan
    -   Käytettävissä oleva varasto sijaintien mukaan
    -   Käytettävissä oleva varasto erän mukaan (eräohjatuille tuotteille)
    -   Käytettävissä oleva varasto varastotilan mukaan
    
-   Tuotteen varastosaldo näkyy seuraavilla tavoilla:

    -   Fyysisen varaston mukaan (tämä näkymä edustaa kokonaismäärää).
    -   Fyysisen varaston varattujen mukaan (tämä näkymä edustaa varattua määrää).
    -   Käytettävissä olevan fyysisen varaston mukaan (tämä näkymä edustaa varaamatonta käytettävissä olevaa määrää).

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä Supply Chain Management -versio on otettu käyttöön organisaatiossasi.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Managementin käytön edellytykset
Jos Supply Chain Management on otettu käyttöön organisaatiossasi, järjestelmänvalvojan on julkaistava **Käytettävissä oleva varasto**-mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>Edellytykset, jos käytössä on Platform update 3 tai uudempi 
Jos organisaatiossa on otettu käyttöön Platform update 3 tai uudempi, järjestelmänvalvojan on toteutettava seuraavat edellytykset. 

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

<td>KB 4013633 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>käytettävissä olevan varaston</strong> mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4013633 -päivityksen.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Ota käyttöönotettava paketti käyttöön</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Julkaise <strong>käytettävissä olevan varaston</strong> mobiilityötila.</td>
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

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Tarkastele tuotteen käytettävissä olevaa varastoa käytettävissä olevan varaston mobiilityötilan avulla

1.  Valitse mobiililaitteessasi **Käytettävissä oleva varasto** -työtila.

2.  Valitse **Tarkistaa käytettävissä oleva varasto nimikkeelle**. Näet luettelon tuotteista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Jos nimike ei ole luettelossa, valitse **Hae lisää**. Etsi tuotteen numeron mukaan tai vaihda hakuun tuotteen nimen mukaan.

4.  Valitse tuote. Jos nimikkeellä on kuva, kuva näkyy.
5.  Valitse jokin seuraavista vaihtoehdoista tarkastellaksesi käytettävissä olevan varaston tilaa:

    -   Näytä käytettävissä oleva varasto toimipaikan mukaan
    -   Näytä käytettävissä oleva varaston fyysisen varaston mukaan
    -   Näytä käytettävissä oleva varasto sijaintien mukaan
    -   Näytä käytettävissä oleva varasto erän mukaan (eräohjatuille tuotteille)
    -   Näytä käytettävissä oleva varasto varaston tilan mukaan

    Tuotteen varastosaldo näkyy seuraavilla tavoilla:
    -   Fyysisen varaston mukaan (tämä näkymä edustaa kokonaismäärää).
    -   Fyysisen varaston varattujen mukaan (tämä näkymä edustaa varattua määrää).
    -   Käytettävissä olevan fyysisen varaston mukaan (tämä näkymä edustaa varaamatonta käytettävissä olevaa määrää).
