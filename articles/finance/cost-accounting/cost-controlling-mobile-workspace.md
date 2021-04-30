---
title: Kustannusseurannan mobiilityötila
description: Tässä ohjeaiheessa on tietoja kustannusseurannan mobiilityötilasta. Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa.
author: AndersGirke
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 569f932b256054f2d93a6d699ca5d5af3da08ca6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897933"
---
# <a name="cost-controlling-mobile-workspace"></a>Kustannusseurannan mobiilityötila

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **Kustannusseuranta**-mobiilityötilasta. Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa.

Tämä mobiilityötila on tarkoitettu käytettäväksi Finance and Operations -mobiilisovelluksen kanssa.

## <a name="overview"></a>Yleiskuvaus
**Kustannusten hallinnan** mobiilityötila sisältää kustannuspaikkojen nykyisen suorituskyvyn välittömän näkymän vertaamalla toteutuneita kustannuksia budjetoituihin kustannuksiin. Voit porautua yksittäisten kustannuselementtien tilaan.

Työntekijä voi esimerkiksi saada kutsun kansainväliseen konferenssiin, mutta organisaation on katettava kaikki matkakulut. Työntekijä pyytää esimieheltä lupaa osallistua konferenssiin. Esimies avaa nopeasti **kustannusten hallinnan** mobiilityötilan puhelimessaan nähdäkseen, onko budjetissa varaa työntekijän osallistumiseen kokoukseen.

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

    Kun valitset linkin, kullekin kustannuselementille näytetään kortti. Kullakin kortilla näytetään seuraavat summat: Todellinen, budjetti, budjetin varianssi, budjetin varianssi-%, muokattu budjetti, muokattu budjetin varianssi ja muokattu budjetin varianssi-%.
    
    [![Kustannuselementin kortti ](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Edellytykset, jos käytössä on Microsoft Dynamics 365 Finance
Jos Finance on otettu käyttöön organisaatiossa, järjestelmänvalvojan on julkaistava **Kustannusten hallinta** -mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

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
<td>Ota KB 4013633 käyttöön.</td>
<td>Järjestelmänvalvoja</td>

<td>KB 4013633 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>Kustannusseuranta</strong>-mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4013633 -päivityksen.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Ota käyttöönotettava paketti käyttöön</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Julkaise <strong>Kustannusseuranta</strong>-mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</td>
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]