---
title: Ostotilauksen hyväksymisen mobiilityötila
description: Tässä artikkelissa on tietoja ostotilauksen hyväksymisen mobiilityötilasta, jossa voit tarkastella ostotilauksia ja vastata niihin eri toiminnoilla. Voit esimerkiksi hyväksyä tai hylätä ostotilauksen.
author: GalynaFedorova
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b5336549937edca6beb94137896f84b460f257f7
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111327"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Ostotilauksen hyväksymisen mobiilityötila

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Tässä artikkelissa on tietoja **ostotilausten hyväksymisen** mobiilityötilasta. Voit tarkastella työtilassa ostotilauksia ja vastata niihin eri toiminnoilla. Voit esimerkiksi hyväksyä tai hylätä ostotilauksen.
 
## <a name="overview"></a>Yleiskuvaus 
Hyväksymistä edellyttävät ostotilaukset läpäisevät hyväksymistyönkulun. Työnkulussa voi olla erilaisia vaiheita, jotka edellyttävät vähintään yhden henkilön tekemiä toimia. Henkilön on ehkä esimerkiksi suoritettava tehtävä loppuun tai hyväksyttävä ostotilaus. 

**Ostotilauksen hyväksymisen** työtilassa on helppo tarkastella ostotilauksia ja reagoida niihin mobiililaitteessa. Työtilassa voi tehdä myös samoja toimia kuin verkkoasiakasohjelmassa.

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä Supply Chain Management -versio on otettu käyttöön organisaatiossasi.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Managementin käytön edellytykset 
Jos Supply Chain Management on otettu käyttöön organisaatiossasi, järjestelmänvalvojan on julkaistava **Ostotilauksen hyväksyntä** -mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

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
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Ota käyttöönotettava paketti käyttöön</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vapauta <strong>ostotilauksen hyväksymisen</strong> mobiilityötila.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen
Talous- ja toimintosovelluksen mobiiliversion lataaminen ja asentaminen:

- [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
- [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen

1. Käynnistä sovellus mobiililaitteessa.
2. Anna Microsoft Dynamics 365:n URL-osoite.
3. Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
4. Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

![Ostotilauksen hyväksymisen työtila käytettävissä olevien työtilojen luettelossa.](./media/po-workspaces.png)

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

