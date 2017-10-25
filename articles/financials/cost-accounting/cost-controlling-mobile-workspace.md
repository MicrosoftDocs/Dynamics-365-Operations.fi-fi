---
title: "Kustannusseurannan mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja kustannusseurannan mobiilityötilasta. Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 0dc79371d63818fb0f6d55389a146012c269a684
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="cost-controlling-mobile-workspace"></a>Kustannusseurannan mobiilityötila

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **Kustannusseuranta**-mobiilityötilasta. Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa.

Tätä mobiilityötilaa on tarkoitettu käytettäväksi Microsoft Dynamics 365 for Unified Operations -mobiilisovelluksella.

## <a name="overview"></a>Yleiskuvaus
**Kustannusten hallinnan** mobiilityötila sisältää kustannuspaikkojen nykyisen suorituskyvyn välittömän näkymän vertaamalla toteutuneita kustannuksia budjetoituihin kustannuksiin. Voit porautua yksittäisten kustannuselementtien tilaan.

Työntekijä voi esimerkiksi saada kutsun kansainväliseen konferenssiin, mutta organisaation on katettava kaikki matkakulut. Työntekijä kysyy esimieheltään, voiko hän osallistua kokoukseen. Esimies avaa nopeasti **kustannusten hallinnan** mobiilityötilan puhelimessaan nähdäkseen, onko budjetissa varaa työntekijän osallistumiseen kokoukseen.

### <a name="data-security"></a>Tietoturva
**Kustannusten hallinnan** mobiilityötilan tiedot suojataan käyttäjän tunnistetietojen mukaan. Kustannuspaikan johtajan on sallittu nähdä vain tiedot omasta kustannuspaikastaan. Käyttöoikeustason tietoturva on hallittu **Kustannuslaskenta**-moduulissa.

Kustannusten kirjanpitäjät määrittävät **kustannusten hallinnan** mobiilityötilan **Kustannuslaskenta**-moduulissa. Työtila on käytettävissä sovelluksessa, kun se on julkaistu mobiilisovellukseen. Näin varmistetaan, että kaikkien kustannuspaikkojen johtajat organisaatiossa näkevät tiedot samassa muodossa.

### <a name="actions-views-and-links"></a>Toiminnot, näkymät ja linkit
Seuraavat toiminnot, näkymät ja linkit sisältyvät **Kustannusseuranta**-mobiilityötilassa:

-   **Toiminnot:**

    -   Valitse asettelu **Valitse konfiguraatio** -kohdassa.
    -   Valitse kustannuspaikat, joiden tiedot suodatetaan **Valitse kustannusobjekti** -kohdassa.
    
        > [!NOTE]
        > Luettelossa näytettävät kustannuspaikat riippuvat **Kustannuslaskenta**-moduulissa annetuista käyttöoikeuksista.

-   **Näkymät:** voit tarkastella korteissa valittujen toimintojen sekä **Kustannuslaskenta**-moduulissa valitun konfiguraation perusteella seuraavia tietoja:

    -   Todellinen vs. budjetti (kuluva kausi)
    -   Todellinen vs. muutettu budjetti (kuluva kausi)
    -   Todellinen vs. budjetti (edellinen kausi)
    -   Todellinen vs tarkistettu budjetti (edellinen kausi)
    -   Todellinen vs. budjetti (vuoden alusta)
    -   Todellinen vs tarkistettu budjetti (vuoden alusta)

    Jokaisella kortilla näytetään seuraavat summat: Todellinen, Budjetti, Varianssi ja Varianssi-%.

-   **Linkit:**

    -   Kuluvan kauden tiedot
    -   Edellisen kauden tiedot
    -   Kuluvan vuoden tiedot

    Kun valitset linkin, kullekin kustannuselementille näytetään kortti. Kullakin kortilla näytetään seuraavat summat: Todellinen, budjetti, budjetin varianssi, budjetin varianssi %, muokattu budjetti, muokattu budjetin varianssi ja muokattu budjetin varianssi %.
    
    [![Kustannuselementin kortti ](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Edellytykset, jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys
Jos Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys on otettu organisaatiossa käyttöön, järjestelmänvalvojan on julkaistava **Kustannusseuranta**-mobiilityötilassa. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operations -versio 1611, johon on asennettu vähintään ympäristöpäivitys 3.
Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operations -versio 1611, jossa on vähintään ympäristöpäivitys 3, järjestelmänvalvojan on toteutettava seuraavat edellytykset.

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

<td>KB 4013633 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>Kustannusseuranta</strong>-mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4013633 -päivityksen.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Lataa metatietojen hotfix-korjaus Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Ota käyttöönotettava paketti käyttöön</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Julkaise <strong>Kustannusseuranta</strong>-mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen
Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:

-   [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
-   [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen

1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna Dynamics 365 -URL-osoitteesi.
3.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
4.  Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Tarkastele kustannuspaikkasi suorituskykyä kustannusten hallinnan mobiilissa työtilassa

1.  Valitse mobiililaitteessasi **Kustannusten hallinta** -työtila.
2.  Valitse **Kustannusobjektin hallinta**.
3.  Valitse **Toiminnot**.
4.  Valitse **Valitse konfigurointi** valitaksesi kustannusten hallinnan asettelun.
5.  Valitse **Valmis**.
6.  Valitse **Toiminnot**.
7.  Valitse **Valitse kustannusobjekti** valitaksesi kustannuspaikat, joihin sinulla on käyttöoikeus.
8.  Valitse **Valmis**.
9.  Kustannuspaikan yleisen suorituskyvyn tarkasteleminen.
10. Napsauta **Kuluvan kauden tiedot** -linkkiä.
11. Yksittäisten kustannuselementtien suorituskyvyn tarkasteleminen.
12. Voit myös etsiä tiettyjä kustannuselementtejä.

