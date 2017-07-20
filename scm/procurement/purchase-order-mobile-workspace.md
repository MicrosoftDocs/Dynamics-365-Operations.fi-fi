---
title: "Ostotilauksen hyväksymisen mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja ostotilauksen hyväksymisen mobiilityötilasta, jossa voit tarkastella ostotilauksia ja vastata niihin eri toiminnoilla. Voit esimerkiksi hyväksyä tai hylätä ostotilauksen."
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: a2ab719b971c325be184d1d950f6c03815e4cea2
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017

---

# <a name="purchase-order-approval-mobile-workspace"></a>Ostotilauksen hyväksymisen mobiilityötila

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Tässä ohjeaiheessa on tietoja **ostotilausten hyväksymisen** mobiilityötilasta. Voit tarkastella työtilassa ostotilauksia ja vastata niihin eri toiminnoilla. Voit esimerkiksi hyväksyä tai hylätä ostotilauksen.
 
## <a name="overview"></a>Yleiskuvaus 
Hyväksymistä edellyttävät ostotilaukset läpäisevät hyväksymistyönkulun. Työnkulussa voi olla erilaisia vaiheita, jotka edellyttävät vähintään yhden henkilön tekemiä toimia. Henkilön on ehkä esimerkiksi suoritettava tehtävä loppuun tai hyväksyttävä ostotilaus. 

**Ostotilauksen hyväksymisen** työtilassa on helppo tarkastella ostotilauksia ja reagoida niihin mobiililaitteessa. Työtilassa voi myös tehdä samoja toimia kuin Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin verkkoasiakasohjelmassa.

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä Finance and Operationsin versio on otettu käyttöön organisaatiossa.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Edellytykset, jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys 
Jos Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys on otettu organisaatiossa käyttöön, järjestelmänvalvojan on julkaistava **ostotilauksen hyväksymisen** mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operationsin versio 1611, johon on asennettu vähintään ympäristöpäivitys 3
Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operationsin versio 1611, jossa on vähintään ympäristöpäivitys 3, järjestelmänvalvojan on toteutettava seuraavat edellytykset. 

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
<td>KB 4017918 -käyttöönotto.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 4017918 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>ostotilausten hyväksymisen</strong> mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4017918 -päivityksen.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Lataa metatietojen hotfix-korjaus Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Ota käyttöönotettava paketti käyttöön</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vapauta <strong>ostotilauksen hyväksymisen</strong> mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen
Lataa ja asenna Microsoft Dynamics 365 for Unified Operations -mobiilisovellus:

- [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
- [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen

1. Käynnistä sovellus mobiililaitteessa.
2. Anna oman Microsoft Dynamics 365:n URL-osoite.
3. Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
4. Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

![Ostotilauksen hyväksymisen työtila käytettävissä olevien työtilojen luettelossa](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Käyttäjälle määritettyjen tilausten tarkasteleminen
1. Valitse mobiililaitteessa **Ostotilauksen hyväksyntä** -työtila.
2. Valitsemalla ostotilauksen hyväksymisen työtilassa **Minulle määritetyt tilaukset** voit tarkastella kaikki ostotilauksia, joissa sinua on pyydetty tekemään toimia.
3. Valitse tilaus. Näet **Tilauksen tiedot** -sivulla tilauksen otsikon tiedot ja rivit. Työkulkutehtävässä on myös ohjeet.
4. Avaa **Otsikon kirjanpidollinen jako** -sivu valitsemalla **Kirjanpidolliset jaot**.
5. Palaa **Tilauksen tiedot** -sivulle ja valitse rivi. Voit tilausrivin tiedoissa rivikohtaisiin kirjanpidollisiin jakoihin.

## <a name="complete-an-action-on-the-purchase-order"></a>Ostotilauksen toiminnon viimeistely
Kun olet tarkastellut sinulle määritettyä ostotilausta ja lukenut työnkulun ohjeet, olet valmis tekemään toimintoja.

1. Valitse mobiililaitteessa **Ostotilauksen hyväksyntä** -työtila.
2. Valitsemalla ostotilauksen hyväksymisen työtilassa **Minulle määritetyt tilaukset** voit tarkastella kaikki ostotilauksia, joissa sinua on pyydetty tekemään toimia.
3. Valitse tilaus ja tutustu tietosivun tietoihin.
4. Tuo käytettävissä olevat toiminnot näkyviin valitsemalla **Toiminnot**. Käytettävissä olevat toiminnot määräytyvät sinulle määritetyn tehtävän mukaan.

    | Tehtävätoiminto    | Hyväksymistoiminto  |
    |----------------|------------------|
    | Kokonaistoimitus       | Hyväksy          |
    | Palautus         | Hylkää           |
    | Pyydä muutosta | Pyydä muutosta   |
    | Edustaja       | Edustaja         |

5. Valitse asianmukainen toiminto.
6. Kirjoita kommentti **Suorita tehtävä** -sivulle. Huomaa, että jos valitset **Delegoi**-toiminnon, sinun on valittava käyttäjä, jolle tehtävä delegoidaan.
7. Valitse **Valmis**. Kun päivität työtilan, ostotilaus ei ole enää luettelossasi. 
