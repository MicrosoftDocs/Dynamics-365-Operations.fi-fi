---
title: "Kustannusseurannan mobiilityötila"
description: "Tässä aiheessa on tietoja Kustannusseurannan mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Operationsin mobiilisovelluksessa. Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa."
author: YuyuScheller
manager: AnnBe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 31a9650774b2ddb70827ffa210154ca10c761236
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Kustannusseurannan mobiilityötila

[!include[banner](../includes/banner.md)]


Tässä aiheessa on tietoja Kustannusseurannan mobiilityötilasta, joka on saatavilla Microsoft Dynamics 365 for Operationsin mobiilisovelluksessa. Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Yhteenveto Kustannustenhallinnan mobiilityötilasta
-------------------------------------------------

**Kustannusten hallinnan** mobiilityötila sisältää kustannuspaikkojen nykyisen suorituskyvyn välittömän näkymän vertaamalla toteutuneita kustannuksia budjetoituihin kustannuksiin. Voit porautua yksittäisten kustannuselementtien tiloihin. Työntekijä voi esimerkiksi saada kutsun kansainväliseen konferenssiin, mutta organisaation on katettava kaikki matkakulut. Työntekijä kysyy esimieheltään, voiko hän osallistua kokoukseen. Esimies avaa nopeasti **kustannusten hallinnan** mobiilityötilan puhelimessaan nähdäkseen, onko budjetissa varaa työntekijän osallistumiseen kokoukseen.

### <a name="data-security"></a>Tietoturva

**Kustannusten hallinnan** mobiilityötilan tiedot suojataan käyttäjän tunnistetietojen mukaan. Kustannuspaikan johtajan on sallittu nähdä vain tiedot omasta kustannuspaikastaan. Käyttöoikeustason tietoturva on hallittu **Kustannuslaskenta**-moduulissa. Kustannusten kirjanpitäjät määrittävät **kustannusten hallinnan** mobiilityötilan **Kustannuslaskenta**-moduulissa. Työtila on saatavissa, kun se on julkaistu Microsoft Dynamics 365 for Operations -mobiilisovellukseen. Näin varmistetaan, että kaikkien kustannuspaikkojen johtajat organisaatiossa näkevät tiedot samassa muodossa.

### <a name="actions-views-and-links"></a>Toiminnot, näkymät ja linkit

**Kustannusten hallinnan** Dynamics 365 for Operations -mobiilityötila tarjoaa seuraavat toiminnot, näkymät ja linkit:

-   **Toiminnot:**
    -   Valitse asettelu **Valitse konfiguraatio** -kohdassa.
    -   Valitse kustannuspaikat, joiden tiedot suodatetaan **Valitse kustannusobjekti** -kohdassa. **Huomautus:** luettelossa näytettävät kustannuspaikat riippuvat **kustannuslaskennan** moduulissa annetuista käyttöoikeuksista.
-   **Näkymät:** valittujen toimintojen sekä **Kustannuslaskenta**-moduulissa valitun konfiguraation perusteella, voit tarkastella seuraavia tietoja korteissa.
    -   Todellinen vs. budjetti (nykyinen kausi)
    -   Todellinen vs tarkistettu budjetti (nykyinen kausi)
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
    
    [![Kustannuselementin kortti ](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Edellytykset
Varmista ennen **kustannusten hallinnan** mobiilityötilan käyttöä, että järjestelmänvalvoja on toteuttanut seuraavat vaatimukset.

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
<td><strong>Kustannusten hallinnan</strong> mobiilityötila on myös julkaistava Dynamics 365 for Operations -mobiilisovellukseen.</td>
<td>Järjestelmänvalvoja</td>
<td><ol>
<li>Käynnistä Dynamics 365 for Operations selaimessa.</li>
<li>Valitse <strong>Järjestelmäparametrit</strong> -sivulta <strong>Mobiilityötilojen hallinta</strong>.</li>
<li>Valitse <strong>Kustannusobjektin kuvaus</strong> -työtila.</li>
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





