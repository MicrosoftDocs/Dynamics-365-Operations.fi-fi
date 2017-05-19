---
title: "Myyntitilausten mobiilityötila"
description: "Tässä aiheessa on tietoja Myyntitilausten mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Operationsin mobiilisovelluksessa. Tämän työtilan avulla pysyt ajan tasalla myyntitilauksista milloin ja missä tahansa."
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
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 119b80e5d8067ffbf75d8b067f4803558c2c94b0
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Myyntitilausten mobiilityötila

[!include[banner](../includes/banner.md)]


Tässä aiheessa on tietoja Myyntitilausten mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Operationsin mobiilisovelluksessa. Tämän työtilan avulla pysyt ajan tasalla myyntitilauksista milloin ja missä tahansa. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Yhteenveto Myyntitilausten mobiilityötilasta
---------------------------------------------

**Myyntitilaukset** -mobiilityötila käyttää Microsoft Dynamics 365 for Operationsia ja antaa mahdollisuuden tarkastella myyntitilausten tarkkoja tietoja. Näihin tietoihin kuuluvat tilauksen tila, asiakkaan yhteystiedot ja tilauksen vastaanottajan yhteystiedot. **Myyntitilausten** mobiilityötilassa on pikanäyttö myyntitilauksista. Voit tarkastella myyntitilauksia asiakaskohtaisesti, näyttää kaikki myyntitilaukset tai tarkastella yksittäisen myyntitilauksen tietoja. Mobiili työtila tarjoaa kaksi näkymää, joilla voit analysoida myyntitilausten yksityiskohtia.

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
Varmista ennen **myyntitilausten** mobiilityötilan käyttöä, että järjestelmänvalvoja on toteuttanut seuraavat vaatimukset.

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
<td>Käytössä on oltava Dynamics 365 for Operations -versio 1611, johon on asennettu ympäristöpäivitys 3.</td>
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
<td><strong>Myyntitilausten</strong> mobiilityötila on myös julkaistava Dynamics 365 for Operations -mobiilisovellukseen.</td>
<td>Järjestelmänvalvoja</td>
<td><ol>
<li>Käynnistä Dynamics 365 for Operations selaimessa.</li>
<li>Valitse <strong>Järjestelmäparametrit</strong> -sivulta <strong>Mobiilityötilojen hallinta</strong>.</li>
<li>Valitse <strong>Myyntitilaukset</strong>-työtila.</li>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Tarkastele asiakkaan myyntitilausten tietoja mobiilin työtilan avulla.
1.  Valitse mobiililaitteessasi **Myyntitilaukset** -työtila.
2.  Valitse **Tarkastele asiakkaan tilauksia**.
3.  Etsi haluamasi asiakas tilin **tai asiakkaan nimen avulla.
4.  Valitse asiakas.
5.  Valitse **Yhteystiedot** tai **Myyntitilaukset**. Jos valittuna on **Myyntitilaukset**, näyttöön tulee luettelo asiakkaan myyntitilauksista.
6.  Valitse **Myyntitilaus**. Voit nyt tarkastella tietoja myyntitilausriveistä, toimituksista, asiakkaan yhteystiedoista ja tilauksen vastaanottajan yhteystiedoista.





