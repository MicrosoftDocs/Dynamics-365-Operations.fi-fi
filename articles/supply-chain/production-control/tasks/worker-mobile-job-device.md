---
title: Määritä työssä mobiililaitetta käyttävä työntekijä
description: Tässä ohjeaiheessa kerrotaan, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä.
author: ShylaThompson
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd1f191e3d1a0d5ba245082dbb56bb291236ed8d39c4ad0dd379a662ef3dfee7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717912"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Määritä työssä mobiililaitetta käyttävä työntekijä

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Varmista, että työntekijälle on määritetty tietty rooli

Tässä esimerkissä tarkistetaan, että käyttäjälle "SHANNON" on määritetty koneoperaattorin rooli ennen työntekijätilin määrittämistä.

1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Käyttäjät > Käyttäjät**.
2. Etsi käyttäjä pikasuodattimesta. Syötä tässä esimerkissä arvoksi `shannon`.
3. Valitse näyttöön tulevassa käyttäjätilissä **Käyttäjätunnus**-sarakkeessa oleva linkki.
4. Valitse **Käyttäjän roolit** -puussa **Roolit > Koneenkäyttäjä**.
5. Palaa kotisivulle sulkemalla **Käyttäjän tiedot**- ja **Käyttäjät**-sivut.

## <a name="configure-worker-account"></a>Määritä työntekijän tili
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Henkilöstöhallinto > Työntekijät > Työntekijät**.
2. Etsi käyttäjä pikasuodattimesta. Syötä tässä esimerkissä arvoksi `shannon`.
3. Valitse näyttöön tulevassa käyttäjätilissä **Nimi**-sarakkeessa oleva linkki.
4. Valitse **Aikarekisteröinti**-välilehti.
5. Valitse **Aktivoi rekisteröintipäätteissä**.
6. Valitse tai kirjoita arvot seuraaviin kenttiin:  

    - **Laskentaryhmä**  
    - **Oletuslaskentaryhmä**  
    - **Hyväksyntäryhmä**  
    - **Vakioprofiili**  
    - **Profiiliryhmä**  

7. Valitse **OK**.
8. Anna uuden aikarekisteröinnin työntekijän nimilapun numero valitsemalla **Muokkaa**. Anna arvo **Nimilapun tunnus**-kentässä.
9. Valitse **Tallenna**.
10. Sulje **Työntekijän tiedot**- ja **Työntekijät**-sivut.

## <a name="assign-worker-to-device-group"></a>Määritä työntekijä laiteryhmään
1. Valitse **Tuotannonhallinta > Asetukset > Tuotannonohjaus > Konfiguroi työkortti laitteita varten**.
2. Valitse **Lisää**.
3. Valitse luettelosta haluamasi työntekijä. Valitse tässä esimerkissä **SHANNON**.
4. Valitse **OK**.
5. Valitse **Muokkaa**.
6. Voit määrittää **Tuotantoyksikkö**-kentässä työntekijän oletussuodattimen. Tämä varmistaa, että vain valittujen tuotantoyksiköiden tuotantotyöt näytetään, kun työntekijä kirjautuu laitteeseen. Anna haluttu arvo.
7. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]