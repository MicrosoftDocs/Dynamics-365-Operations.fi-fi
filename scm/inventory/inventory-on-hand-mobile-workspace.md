---
title: "Käytettävissä olevan varaston mobiilityötila"
description: "Tässä aiheessa on tietoja käytettävissä olevan varaston mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Operationsin mobiilisovelluksessa. Käytettävissä olevan varaston mobiilityötila auttaa syventämään näkemyksiä varatusta ja käytettävissä olevasta varastosta mobiilisti milloin tahansa ja missä tahansa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e703ae80800b993ebca1c7bee455af1be41c7d5f
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Käytettävissä olevan varaston mobiilityötila

[!include[banner](../includes/banner.md)]


Tässä aiheessa on tietoja käytettävissä olevan varaston mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Operationsin mobiilisovelluksessa. Käytettävissä olevan varaston mobiilityötila auttaa syventämään näkemyksiä varatusta ja käytettävissä olevasta varastosta mobiilisti milloin tahansa ja missä tahansa.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Yhteenveto käytettävissä olevan varaston mobiilityötilasta
--------------------------------------------------

Yleensä yrityksillä on useita varaston toimituksia ja vastaanottoja joka päivä. Näiden siirrot muuttavat jatkuvasti käytettävissä olevan varaston tilaa. **Käytettävissä olevan varaston** mobiilityötilassa näet koko yrityksen käytettävissä olevan varaston tilan, jolloin voit hyödyntää uusimpia varastotietoja haluamassasi mobiililaitteessa. Riippumatta siitä, työskenteletkö fyysisessä varastossa, ostossa, myynnissä, tuotannossa, yrityksen johdossa tai muussa roolissa, voit käyttää käytettävissä olevan varaston tietoja milloin tahansa ja missä tahansa. Mobiilityötila sisältää välittömän näkymän käytettävissä olevan varaston tilasta kaikissa tiloissa. Sen avulla voit tarkastella käytettävää varastoa eri tiloissa, nykyisiä materiaalivarauksia ja varaamatonta, käytettävissä olevaa varastoa. Voit myös syöttää nimikenumeron suorittaaksesi kyselyjä käytettävissä olevaan varastoon ja suorittaa suodatetun haun varastotuotteille ja varianteille. Erityisesti mobiilityötilassa on nämä ominaisuudet:

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
Varmista ennen **käytettävissä olevan varaston** mobiilityötilan käyttöä, että järjestelmänvalvoja on toteuttanut seuraavat vaatimukset.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Edellytys</th>
<th>Rooli</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Käytössä on oltava Microsoft Dynamics 365 for Operations -versio 1611, johon on asennettu ympäristöpäivitys 3.</td>
<td>Järjestelmänvalvoja</td>
<td>Jos organisaatiosi ei ole vielä ottanut Dynamics 365 for Operations -sovellusta käyttöön, järjestelmänvalvojasi tulisi tutustua <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Microsoft Dynamics 365 for Operations -kokeiluympäristön käyttöönotto</a>-ohjeeseen.</td>
</tr>
<tr class="even">
<td>KB 4013633 on oltava asennettu.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 4013633 (X++-päivitys tai metatietojen korjaus) sisältää neljä mobiilia työtilaa toimitusketjun hallintaan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4013633 -päivityksen:
<ol>
<li>Lataa KB 4013633 Microsoft Dynamicsin elinkaaripalveluista (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Asenna käyttöön otettava paketti</a> omaan Dynamics 365 for Operations -järjestelmääsi.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Käytettävissä olevan varaston</strong> mobiilityötila on myös julkaistava Dynamics 365 for Operations -mobiilisovellukseen.</td>
<td>Järjestelmänvalvoja</td>
<td><ol>
<li>Käynnistä Dynamics 365 for Operations selaimessa.</li>
<li>Valitse <strong>Järjestelmäparametrit</strong> -sivulta <strong>Mobiilityötilojen hallinta</strong>.</li>
<li>Valitse <strong>käytettävissä olevan varaston</strong> työtila.</li>
<li>Valitse <strong>Julkaise mobiilityötila</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Lataa ja asenna Dynamics 365 for Operations -mobiilisovellus
Lataa ja asenna Microsoft Dynamics 365 for Operations -mobiilisovellus sovelluskaupastasi.

-   Android - [Dynamics 365 for Operations Google Play Storessa](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone - [Dynamics 365 for Operations iTunes App Storessa](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Kirjaudu sisään Dynamics 365 for Operations -mobiilisovellukseen
1.  Käynnistä sovellus mobiililaitteessa.
2.  Syötä Dynamics 365 for Operationsin URL-osoite.
3.  annan yritys, johon kirjaudutaan. Kirjoita esimerkiksi **USMF**.
4.  Ensimmäisellä kerralla, kun kirjaudut sisään, sinulta pyydetään Dynamics 365 for Operations -tilisi käyttäjänimeä ja salasanaa. Kirjota tunnistetiedot.
5.  Kun olet kirjautunut sisään, näet yrityksen käytettävissä olevat työtilat. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, voit päivittää mobiilien työtilojen luettelon vetämällä alaspäin. 

    [![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Tarkastele tuotteen käytettävissä olevaa määrää käytettävissä olevan varaston mobiilityötilan avulla
1.  Valitse mobiililaitteessasi **Käytettävissä oleva varasto** -työtila.
2.  Valitse **Tarkistaa käytettävissä oleva varasto nimikkeelle**. Näet luettelon tuotteista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Lisätietoa sovelluskehittäjille löytyy kohdasta [Dynamics 365 for Operationsin mobiiliympäristö](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/).
3.  Jos nimike ei ole luettelossa, valitse **Hae lisää** tehdäksesi online-haun Dynamics 365 for Operationsissa. Etsi tuotteen numeron mukaan tai vaihda hakuun tuotteen nimen mukaan.
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






