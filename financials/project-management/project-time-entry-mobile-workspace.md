---
title: "Projektin aikamerkintöjen mobiilityötila Dynamics 365 for Operations -sovellusta varten"
description: "Tässä ohjeaiheessa on tietoja projektin aikamerkintöjen mobiilityötilasta. Työtilan avulla käyttäjät voivat syöttää ja tallentaa projektin aikakirjauksia mobiililaittella."
author: annbe
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9c592c301908898915164e9236850759b73543fe
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Projektin aikamerkintöjen mobiilityötila

[!include[banner](../includes/banner.md)]



Tässä aiheessa on tietoja projektin aikamerkintöjen mobiilityötilasta, joka on saatavilla Dynamics 365 for Operationsin mobiilisovelluksessa. Työtilan avulla käyttäjät voivat syöttää ja tallentaa projektin aikakirjauksia mobiililaittella.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Projektin aikamerkintöjen mobiilityötilan yleiskatsaus
---------------------------------------------------

Projektiresurssit ovat kohteessa tai liikkeellä osana päivittäistä työtään. **Projektin aikamerkinnät** -mobiilityötilan avulla käyttäjät voivat syöttää laskutettavan tai ei-laskutettavan aikansa projektiin valitsemallaan mobiililaitteella. Tämän ansiosta projektiresurssit voivat tehdä aikakirjauksia missä ja milloin tahansa. He voivat myös tarkastella aiemmin kirjattuja merkintöjä. 

Tarkkaan ottaen, **projektin aikakirjausten**mobiilityötilassa on nämä ominaisuudet:

-   Anna valitulle päivämäärällä tuntien määrä, jonka olet käyttänyt tietyn tehtävän suorittamiseen.
-   Hae projekti, jolle haluat kirjata tunteja projektin tai asiakkaan nimellä .
-   Määritä käyttämällesi ajalle luokka ja tehtävä.
-   Kirjaa aika projektiin laskutettavaksi tai ei-laskutettavaksi.
-   Voit myös kirjoittaa ulkoisia tai sisäisiä kommentteja.

**Projektin aikakirjausten** mobiilityötilan käyttöönotto-ohjeet löydät tämän aiheen seuraavista osista.

## <a name="prerequisites"></a>Edellytykset
Varmista ennen **projektin aikakirjausten** mobiilityötilan käyttöönottoa, että järjestelmänvalvoja on toteuttanut seuraavat vaatimukset.

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
<td>Jos organisaatiosi ei ole vielä ottanut Dynamics 365 for Operations -sovellusta käyttöön, järjestelmänvalvojasi tulisi tutustua <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operations -kokeiluympäristön käyttöönotto</a>-ohjeeseen.</td>
</tr>
<tr class="even">
<td>KB 4018050 on oltava asennettu.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 4018050 on X++-päivitys tai metatietojen korjaus, joka sisältää <strong>projektin aikakirjausten</strong> mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4018050 -päivityksen.
<ol>
<li>Lataa KB 4018050 Microsoft Dynamicsin elinkaaripalveluista (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>ApplicationSuite</strong>- ja <strong>ProjectMobile</strong>-mallit ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Asenna käyttöön otettava paketti</a> omaan Dynamics 365 for Operations -järjestelmääsi.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Projektin aikakirjausten</strong> mobiilityötila on myös julkaistava Dynamics 365 for Operations -mobiilisovellukseen.</td>
<td>Järjestelmänvalvoja</td>
<td><ol>
<li>Käynnistä Dynamics 365 for Operations selaimessa.</li>
<li>Valitse <strong>Järjestelmäparametrit</strong>-sivun <strong>Mobiilityötilojen hallinta</strong> -välilehdessä <strong>Projektin aikakirjaukset</strong> -työtila.</li>
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

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Aikakirjausten syöttäminen Projektin aikakirjausten mobiilityötilassa
1.  Valitse mobiililaitteessasi **Projektin aikakirjausten** työtila.
2.  Valitse **Aikamerkintä**. Näet kuluvan viikon kalenteripäivät.
3.  Napsauta valitun päivän kohdalla **Toiminnot** &gt; **Uusi kirjaus**.
4.  Anna kirjattava tuntien määrä.
5.  Valitse aikakirjauksen kohdeprojekti. Näet luettelon projekteista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Lisätietoa sovelluskehittäjille löytyy kohdasta [Dynamics 365 for Operationsin mobiiliympäristö](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
6.  Jos projekti ei ole luettelossa, valitse **Haku** tehdäksesi online-haun Dynamics 365 for Operationsissa. Voit hakea nimen, projektin nimen tai asiakkaan perusteella.
7.  Valitse luokka. Näet luettelon luokista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Lisätietoa sovelluskehittäjille löytyy kohdasta [Dynamics 365 for Operationsin mobiiliympäristö](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
8.  Jos luokka ei ole luettelossa, valitse **Haku** tehdäksesi online-haun Dynamics 365 for Operationsissa. Etsi luokan tai luokan nimen mukaan.
9.  Valitse tehtävä. Näet luettelon tehtävistä, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Lisätietoa sovelluskehittäjille löytyy kohdasta [Dynamics 365 for Operationsin mobiiliympäristö](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
10. Jos tehtävä ei ole luettelossa, valitse **Haku** tehdäksesi online-haun Dynamics 365 for Operationsissa. Etsi tehtävän numeron tai tarkoituksen mukaan.
11. Valitse rivin ominaisuus.
12. Voit myös kirjoittaa ulkoisia tai sisäisiä kommentteja.
13. Valitse **Valmis**.






