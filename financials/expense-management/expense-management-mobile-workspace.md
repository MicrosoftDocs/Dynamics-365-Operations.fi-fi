---
title: "Kulujenhallinnan mobiilityötila"
description: "Tässä aiheessa on tietoja Kulujenhallinnan mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Operationsin mobiilisovelluksessa. Työtilan avulla käyttäjät voivat siepata ja ladata kuitteja, jotka voi liittää myöhemmin kuluraportteihin. Mobiilityötilassa käyttäjät voivat myös luoda kulurivejä nopeasti käyttämällä liitettyä kuittia."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
ms.sourcegitcommit: 8bc47c5b170fd7dd8f6288682aad6eae1d2dc09a
ms.openlocfilehash: 9d3b7a4d5184c3c4958f4298f1d3dd4de0cd06d6
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2017


---

# <a name="expense-management-mobile-workspace"></a>Kulujenhallinnan mobiilityötila

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Tässä aiheessa on tietoja Kulujenhallinnan mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Operationsin mobiilisovelluksessa. Työtilan avulla käyttäjät voivat siepata ja ladata kuitteja, jotka voi liittää myöhemmin kuluraportteihin. Mobiilityötilassa käyttäjät voivat myös luoda kulurivejä nopeasti käyttämällä liitettyä kuittia.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Yhteenveto Kulujenhallinnan mobiilityötilasta
---------------------------------------------------

Moni organisaatio edellyttää, että työntekijän hyvitettäväksi lähetettäviin matka- tai yritystoimintaan liittyvään kuluraporttiin liitetään kuitti. **Kulujenhallinnan** mobiilityötilan avulla käyttäjät voivat nopeasti luoda uusia kulurivejä valitsemassaan mobiililaitteessa liittämällä kuitista valokuvakopion. Käyttäjät voivat myös ottaa kuvan kuitista ja liittää sen kuluraporttiin myöhemmin. **Kulujenhallinnan** mobiilityötilan avulla käyttäjä voi siis:

-   Ottaa kuvan kuitista ja ladata sen Microsoft Dynamics for Operationsiin. Käyttäjän voi sitten liittää kuvan kuluraporttiin myöhemmin.
-   Ladata tiedoston siepattuna kuittina. Käyttäjän voi sitten liittää tiedoston kuluraporttiin myöhemmin.
-   Luoda uuden kulurivin liitetystä kuitista. Käyttäjä voi sitten lisätä rivinimikkeen kuluraporttiin myöhemmin, ja lähettää sen hyväksyntää ja hyvitystä varten.

Ohjeen jäljellä olevat osat käsittelevät **Kulujenhallinnan** mobiilityötilan käyttöönottoa ja käyttöä.

## <a name="prerequisites"></a>Edellytykset
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
<td>Jos organisaatiosi ei ole vielä ottanut Dynamics 365 for Operations -sovellusta käyttöön, järjestelmänvalvojasi tulisi tutustua <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Microsoft Dynamics 365 for Operations -kokeiluympäristön käyttöönotto</a>-ohjeeseen.</td>
</tr>
<tr class="even">
<td>KB 4019015 on oltava asennettu.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 4019015 (X++-päivitys tai metatietojen korjaus) sisältää neljä mobiilia työtilaa toimitusketjun hallintaan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4019015 -päivityksen:
<ol>
<li>Lataa KB 4019015 Microsoft Dynamicsin elinkaaripalveluista (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Luo käyttöön otettava paketti</a>, joka sisältää <strong>ApplicationSuite</strong>- ja <strong>ExpenseMobile</strong>-mallit ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Asenna käyttöön otettava paketti</a> omaan Dynamics 365 for Operations -järjestelmääsi.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Kulujenhallinnan</strong> mobiilityötila on myös julkaistava Dynamics 365 for Operations -mobiilisovellukseen.</td>
<td>Järjestelmänvalvoja</td>
<td><ol>
<li>Käynnistä Dynamics 365 for Operations selaimessa.</li>
<li>Valitse <strong>Järjestelmäparametrit</strong> -sivulta <strong>Mobiilityötilojen hallinta</strong>.</li>
<li>Valitse <strong>Kulujenhallinnan</strong> työtila.</li>
<li>Valitse <strong>Julkaise mobiilityötila</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Lataa ja asenna Dynamics 365 for Operations -mobiilisovellus
Lataa ja asenna Microsoft Dynamics 365 for Operations -mobiilisovellus sovelluskaupastasi.

-   Android - [Dynamics 365 for Operations Google Play Storessa](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone - [Dynamics 365 for Operations iTunes App Storessa](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)
-   Windows-puhelimet (Universaali Windows-ympäristö \[UWP\]): Tulossa pian!

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Kirjaudu sisään Dynamics 365 for Operations -mobiilisovellukseen
1.  Käynnistä sovellus mobiililaitteessa.
2.  Syötä Dynamics 365 for Operationsin URL-osoite.
3.  annan yritys, johon kirjaudutaan. Kirjoita esimerkiksi **USMF**.
4.  Ensimmäisellä kerralla, kun kirjaudut sisään, sinulta pyydetään Dynamics 365 for Operations -tilisi käyttäjänimeä ja salasanaa. Kirjota tunnistetiedot.
5.  Kun olet kirjautunut sisään, näet yrityksen käytettävissä olevat työtilat. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, voit päivittää mobiilien työtilojen luettelon vetämällä alaspäin. [![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kuittien sieppaaminen kulujenhallinnan mobiilityötilassa
1.  Valitse mobiililaitteessasi **Kulujenhallinnan** työtila.
2.  Valitse **Sieppaa kuitti**.
3.  Valitse **Ota kuva** tai **Valitse kuva**.
4.  Jos valitsit **Ota kuva** -vaihtoehdon, toimi seuraavasti:
    1.  Sinut siirretään mobiililaitteesi kameraan, jotta voit ottaa kuitista kuvan. Kun olet ottanut kuvan, hyväksy se napauttamalla **OK**.
    2.  Valinnainen: Anna kuvalle nimi ja syötä muistiinpanoja.

     tai Jos valitsit **Valitse kuva**, toimi seuraavasti:
    1.  Valitse kuva luettelosta.
    2.  Valinnainen: Anna kuvalle nimi ja syötä muistiinpanoja.

5.  Valitse **Valmis**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Kulujen pikasyöttö kulujenhallinnan mobiilityötilassa
1.  Valitse mobiililaitteessasi **Kulujenhallinnan** työtila.
2.  Valitse **Kulun pikasyöttö**.
3.  Valitse kulun luokka. Näet luettelon kululuokista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää. Lisätietoa sovelluskehittäjille löytyy kohdasta [Dynamics 365 for Operationsin mobiiliympäristö](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Jos luokka ei ole luettelossa, valitse **Haku** tehdäksesi online-haun Dynamics 365 for Operationsissa. Etsi kululuokan tai -tyypin perusteella.
4.  Anna kulun tapahtumapäivämäärä.
5.  Valinnainen: anna kulun myyjä.
6.  Syötä kulun summa.
7.  Valitse kulun valuutta. Näet luettelon valuuttakoodeista, jotka on ladattu sovellukseesi offline-käyttöä varten. Oletusarvon mukaan ladataan 400 valuuttaa, mutta sovelluskehittäjä voi muuttaa tätä määrää. Lisätietoa sovelluskehittäjille löytyy kohdasta [Dynamics 365 for Operationsin mobiiliympäristö](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/). Jos valuutta ei ole luettelossa, valitse **Haku** tehdäksesi online-haun Dynamics 365 for Operationsissa. Etsi valuutan tai nimen mukaan.
8.  Valitse **Ota kuva** tai **Valitse kuva**.
9.  Jos valitsit **Ota kuva**, sinut siirretään mobiililaitteesi kameraan, jotta voit ottaa kuitista kuvan. Kun olet ottanut kuvan, hyväksy se napauttamalla **OK**.  tai Jos valitsit **Valitse kuva**, valitse kuva luettelosta.
10. Valitse **Valmis**.






