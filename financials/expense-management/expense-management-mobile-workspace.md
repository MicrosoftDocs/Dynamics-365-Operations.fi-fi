---
title: "Kulujenhallinnan mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja kulujenhallinnan mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Finance and Operationsin mobiilisovelluksessa. Työtilan avulla käyttäjät voivat siepata ja ladata kuitteja, jotka voi liittää myöhemmin kuluraportteihin. Mobiilityötilassa käyttäjät voivat myös luoda kulurivejä nopeasti käyttämällä liitettyä kuittia."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 0e52d1c5dde7f79c4a8ac5ac2d9c3b25bba9c2cd
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Kulujenhallinnan mobiilityötila
<a id="expense-management-mobile-workspace" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa on tietoja kulujenhallinnan mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Finance and Operationsin mobiilisovelluksessa. Työtilan avulla käyttäjät voivat siepata ja ladata kuitteja, jotka voi liittää myöhemmin kuluraportteihin. Mobiilityötilassa käyttäjät voivat myös luoda kulurivejä nopeasti käyttämällä liitettyä kuittia.

Yhteenveto Kulujenhallinnan mobiilityötilasta
<a id="overview-of-the-expense-management-mobile-workspace" class="xliff"></a>
---------------------------------------------------

Moni organisaatio edellyttää, että työntekijän hyvitettäväksi lähetettäviin matka- tai yritystoimintaan liittyvään kuluraporttiin liitetään kuitti. **Kulujenhallinnan** mobiilityötilan avulla käyttäjät voivat nopeasti luoda uusia kulurivejä valitsemassaan mobiililaitteessa liittämällä kuitista valokuvakopion. Käyttäjät voivat myös ottaa kuvan kuitista ja liittää sen kuluraporttiin myöhemmin. **Kulujenhallinnan** mobiilityötilan avulla käyttäjä voi siis:

-   ottaa kuvan kuitista ja ladata sen Microsoft Dynamics for Finance and Operationsiin. Käyttäjän voi sitten liittää kuvan kuluraporttiin myöhemmin.
-   Ladata tiedoston siepattuna kuittina. Käyttäjän voi sitten liittää tiedoston kuluraporttiin myöhemmin.
-   Luoda uuden kulurivin liitetystä kuitista. Käyttäjä voi sitten lisätä rivinimikkeen kuluraporttiin myöhemmin, ja lähettää sen hyväksyntää ja hyvitystä varten.

Ohjeen jäljellä olevat osat käsittelevät **Kulujenhallinnan** mobiilityötilan käyttöönottoa ja käyttöä.

## Edellytykset
<a id="prerequisites" class="xliff"></a>
Varmista ennen **kulujenhallinnan** mobiilityötilan käyttöönottoa, että järjestelmänvalvoja on toteuttanut seuraavat vaatimukset.

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
<td>Jos organisaatiosi ei ole vielä ottanut Finance and Operationsia käyttöön, järjestelmänvalvojan kannattaa tutustua ohjeaiheeseen<a href="/dynamics365/unified-operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Finance and Operations -kokeiluympäristön käyttöönotto</a>.</td>
</tr>
<tr class="even">
<td>KB 4019015 on oltava asennettu.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 4019015 (X++-päivitys tai metatietojen korjaus) sisältää neljä mobiilia työtilaa toimitusketjun hallintaan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4019015 -päivityksen:
<ol>
<li>Lataa KB 4019015 Microsoft Dynamicsin elinkaaripalveluista (LCS).</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>ApplicationSuite</strong>- ja <strong>ExpenseMobile</strong>-mallit ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Asenna käyttöön otettava paketti</a> omaan Finance and Operations -järjestelmään.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Kulujenhallinnan</strong> mobiilityötila on julkaistava myös Finance and Operations -mobiilisovellukseen.</td>
<td>Järjestelmänvalvoja</td>
<td><ol>
<li>Käynnistä Finance and Operations selaimessa.</li>
<li>Valitse <strong>Järjestelmäparametrit</strong> -sivulta <strong>Mobiilityötilojen hallinta</strong>.</li>
<li>Valitse <strong>Kulujenhallinnan</strong> työtila.</li>
<li>Valitse <strong>Julkaise mobiilityötila</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## Finance and Operations -mobiilisovelluksen lataaminen ja asentaminen
<a id="download-and-install-the-finance-and-operations-mobile-app" class="xliff"></a>
Lataa ja asenna Finance and Operations -mobiilisovellus sovelluskaupasta.

-   Android: [Finance and Operations Google Play Storessa](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone: [Finance and Operations iTunes App Storessa](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## Finance and Operations -mobiilisovellukseen kirjautuminen
<a id="sign-in-to-the-finance-and-operations-mobile-app" class="xliff"></a>
1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna Finance and Operationsin URL-osoite.
3.  annan yritys, johon kirjaudutaan. Kirjoita esimerkiksi **USMF**.
4.  Kun kirjaudut ensimmäisen kerran sisään, sinulta kysytään Finance and Operations -tilin käyttäjänimeä ja salasanaa. Kirjota tunnistetiedot.
5.  Kun olet kirjautunut sisään, näet yrityksen käytettävissä olevat työtilat. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, voit päivittää mobiilien työtilojen luettelon vetämällä alaspäin. 

[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## Kuittien sieppaaminen kulujenhallinnan mobiilityötilassa
<a id="capture-a-receipt-by-using-the-expense-management-mobile-workspace" class="xliff"></a>
1.  Valitse mobiililaitteessasi **Kulujenhallinnan** työtila.
2.  Valitse **Sieppaa kuitti**.
3.  Valitse **Ota kuva** tai **Valitse kuva**.
4.  Jos valitsit **Ota kuva** -vaihtoehdon, toimi seuraavasti:
    1.  Sinut siirretään mobiililaitteesi kameraan, jotta voit ottaa kuitista kuvan. Kun olet ottanut kuvan, hyväksy se napauttamalla **OK**.
    2.  Valinnainen: Anna kuvalle nimi ja syötä muistiinpanoja.

     **Tai:** Jos valitsit **Valitse kuva**, toimi seuraavasti:
    1.  Valitse kuva luettelosta.
    2.  Valinnainen: Anna kuvalle nimi ja syötä muistiinpanoja.

5.  Valitse **Valmis**.

## Kulujen pikasyöttö kulujenhallinnan mobiilityötilassa
<a id="quick-expense-entry-by-using-the-expense-management-mobile-workspace" class="xliff"></a>
1.  Valitse mobiililaitteessasi **Kulujenhallinnan** työtila.
2.  Valitse **Kulun pikasyöttö**.
3.  Valitse kulun luokka. Näet luettelon kululuokista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Finance and Operationsin mobiiliympäristö](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Jos luokka ei ole luettelossa, valitse **Haku** ja tee verkkohaku Finance and Operationsissa. Etsi kululuokan tai -tyypin perusteella.
4.  Anna kulun tapahtumapäivämäärä.
5.  Valinnainen: anna kulun myyjä.
6.  Syötä kulun summa.
7.  Valitse kulun valuutta. Näet luettelon valuuttakoodeista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 400 valuuttaa, mutta sovelluskehittäjä voi muuttaa tätä määrää. Sovelluskehittäjille on lisätietoja ohjeaiheessa [Finance and Operationsin mobiiliympäristö](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Jos valuutta ei ole luettelossa, valitse **Haku** ja tee verkkohaku Finance and Operationsissa. Etsi valuutan tai nimen mukaan.
8.  Valitse **Ota kuva** tai **Valitse kuva**.
9.  Jos valitsit **Ota kuva**, sinut siirretään mobiililaitteesi kameraan, jotta voit ottaa kuitista kuvan. Kun olet ottanut kuvan, hyväksy se napauttamalla **OK**.  tai Jos valitsit **Valitse kuva**, valitse kuva luettelosta.
10. Valitse **Valmis**.






