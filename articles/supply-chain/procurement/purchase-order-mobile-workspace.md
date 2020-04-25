---
title: Ostotilauksen hyväksymisen mobiilityötila
description: Tässä ohjeaiheessa on tietoja ostotilauksen hyväksymisen mobiilityötilasta, jossa voit tarkastella ostotilauksia ja vastata niihin eri toiminnoilla. Voit esimerkiksi hyväksyä tai hylätä ostotilauksen.
author: mkirknel
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 68676fba895dcc91fd3dba065788f3be3a6e9ee4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207945"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Ostotilauksen hyväksymisen mobiilityötila

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **ostotilausten hyväksymisen** mobiilityötilasta. Voit tarkastella työtilassa ostotilauksia ja vastata niihin eri toiminnoilla. Voit esimerkiksi hyväksyä tai hylätä ostotilauksen.
 
## <a name="overview"></a>Yleiskuvaus 
Hyväksymistä edellyttävät ostotilaukset läpäisevät hyväksymistyönkulun. Työnkulussa voi olla erilaisia vaiheita, jotka edellyttävät vähintään yhden henkilön tekemiä toimia. Henkilön on ehkä esimerkiksi suoritettava tehtävä loppuun tai hyväksyttävä ostotilaus. 

**Ostotilauksen hyväksymisen** työtilassa on helppo tarkastella ostotilauksia ja reagoida niihin mobiililaitteessa. Työtilassa voi tehdä myös samoja toimia kuin verkkoasiakasohjelmassa.

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä Supply Chain Management -versio on otettu käyttöön organisaatiossasi.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Managementin käytön edellytykset 
Jos Supply Chain Management on otettu käyttöön organisaatiossasi, järjestelmänvalvojan on julkaistava **Ostotilauksen hyväksyntä** -mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operationsin versio 1611 ja Platform update 3 tai uudempi
Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operationsin versio 1611 ja Platform update 3 tai uudempi, järjestelmänvalvojan on toteutettava seuraavat edellytykset. 

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
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Ota käyttöönotettava paketti käyttöön</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vapauta <strong>ostotilauksen hyväksymisen</strong> mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen
Finance and Operations -mobiilisovelluksen lataaminen ja asentaminen:

- [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
- [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen

1. Käynnistä sovellus mobiililaitteessa.
2. Anna Microsoft Dynamics 365:n URL-osoite.
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
