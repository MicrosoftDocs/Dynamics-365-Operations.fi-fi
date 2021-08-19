---
title: Dynamics 365 Supply Chain Managementin (Resurssien hallinta) integrointi Dynamics 365 Guidesin kanssa
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft  Dynamics 365 Supply Chain Managementin käyttöomaisuudenhallintamoduuli integroidaan Dynamics 365 Guidesin kanssa, jotta voidaan hyödyntää päivittäisissä huolto- ja ylläpitotyökuluissa yhdistetyn todellisuuden oppaita.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 94d98aa011d0db3991c14596f5d6bdecc0fb6c831915ae124f623fa57277fcfe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721532"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Dynamics 365 Supply Chain Managementin (Resurssien hallinta) integrointi Dynamics 365 Guidesin kanssa

Microsoft Dynamics 365 Supply Chain Managementin **käyttöomaisuudenhallinta**-moduuli integroidaan Dynamics 365 Guidesin kanssa, jotta voidaan hyödyntää päivittäisissä huolto- ja ylläpitotyökuluissa yhdistetyn todellisuuden oppaita. Jos opas liittyy käyttöomaisuuden hallinnan työtilaukseen, työntekijä, joka avaa työtilauksen ylläpidon tarkistusluettelon Supply Chain Managementin (Dynamics 365) -mobiilisovelluksessa, näkee, että opas on käytettävissä. Työntekijä voi sitten etsiä ja avata oppaan Dynamics 365 Guidesin HoloLens-sovelluksessa.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit liittää ohjeita käyttöomaisuuden hallinnan työtilauksiin, sinun on täytettävä seuraavat edellytykset:

- [Asenna Dynamics 365 Supply Chain Management -sovelluksen](../../fin-ops-core/fin-ops/index.md) versio 10.0.9 tai uudempi.
- [Ota käyttöön kaksoiskirjoituslähde Supply Chain Management -sovelluksissa](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Ota väliversio käyttöön](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) **MRGuidesFeature** -ominaisuudesta. (Tuotantoympäristöissä on ensin lähetettävä tukipyyntö, jotta vuokralaisesi lisätään flighting-ryhmään.)
- [Ota seuraavat konfigurointiavaimet käyttöön](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) **käyttöoikeuksienmääritys** -sivulla:

    - Resurssienhallinta \> Resurssienhallinnan yhdistetty todellisuus
    - Yhdistetty todellisuus \> Yhdistetyn todellisuuden opas

- [Asenna Dynamics 365 Guides -sovelluksen](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versio 200.0.0.96 tai uudempi.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Käytä Dynamics 365 Guidesia resurssienhallinnan kanssa

Jos haluat liittää oppaan, käytä resurssienhallinnassa ylläpidon tarkistuslistaa. Voit luoda liitoksen ylläpidon tarkistuslistamallin, ylläpitotyön tyypin tai työtilauksen kautta, koska kaikki kolme sisältävät ylläpidon tarkistuslistarivejä. Voit säästää aikaa mallin avulla, koska malli voidaan liittää kaikkiin sitä käyttävien kunnossapitotöiden tyyppeihin. Esimerkiksi kunnossapitotyötyyppiin liittyvä opas liitetään automaattisesti kaikkiin työtilauksiin, jotka määrittävät tämän työlajin. Toisaalta työtilaukseen suoraan liittyvä opas on olemassa vain kyseisessä työtilauksessa.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Oppaan ja ylläpidon tarkistuslistamallin kytkeminen

Seuraa näitä ohjeita, oppaan ja ylläpidon tarkistuslistamallin kytkemiseksi.

1. Luo opas Dynamics 365 Guides -PC:n ja HoloLens-sovellusten avulla. Lisätietoja kunkin oppaan luomisesta on seuraavissa ohjeaiheissa.

    - [Oppaan luominen PC-sovelluksen avulla](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Aseta hologrammit HoloLens-sovelluksen avulla](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. Luo toimitusketjun hallinnassa [ylläpidon tarkistuslistamalli](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Liitä uusi ylläpidon tarkistuslistarivillä luomasi opas ylläpidon tarkistuslistamalliin:

    1. Valitse **Ylläpidon tarkistuslistarivit** -pikavälilehdessä rivi, johon haluat liittää oppaan.
    1. Valitse **Liittyvät Oppaat** -pikavälilehdessä **Lisää opas**.

        ![Oppaan ja ylläpidon tarkistuslistarivin kytkeminen.](media/am-guides-integration-add-guide.png "Oppaan ja ylläpidon tarkistuslistarivin kytkeminen")

    1. Valitse **Nimi**-kentässä opas ja valitse sitten **Tallenna**.

        ![Valitse opas Nimi-kentästä.](media/am-guides-integration-select-guide.png "Valitse opas nimikentästä")

1. Työtyypin ja ylläpidon tarkistuslistamallin kytkeminen:

    1. [Luo ylläpitotöiden tyyppi](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) tai valitse aiemmin luotu ylläpitotyön tyyppi.
    1. Valitse toimintoruudun **Ylläpitotöiden tyypin oletusasetukset**.

        ![Ylläpitotyön tyyppien oletukset -painike.](media/am-guides-integration-job-defaults.png "Ylläpitotyön tyyppien oletusten painike")

    1. Luo rivi ja valitse **Tallenna**.

        ![Luo rivi.](media/am-guides-integration-add-line.png "Luo rivi")

    1. Valitse toimintoruudussa **Ylläpidon tarkistuslista**.

        ![Ylläpidon tarkistuslista -painike.](media/am-guides-integration-maintenance-checklist.png "Ylläpidon tarkistuslistapainike")

    1. Lisää **ylläpidon tarkistuslistarivit** -pikavälilehdessä rivi ja muuta sitten **Tyyppi**-kentän arvoksi **Malli**.

        ![Muuta Tyyppi-arvoa.](media/am-guides-integration-checklist-lines.png "Muuta tyypin arvo")

    1. Valitse **Rivitiedot**-pikavälilehden **Malli**-kentässä malli, johon opas on liitetty, ja valitse sitten **Tallenna**.

        ![Valitse malli.](media/am-guides-integration-checklist-line-details.png "Valitse malli")

1. [Luo työtilaus](work-orders/manually-created-workorders.md#create-work-order) ja valitse sitten ylläpitotyön tyyppi, joka käyttää oppaaseen liitettyä ylläpidon tarkistuslistamallia. Opas liitetään automaattisesti työtilaukseen.

    ![Valitse ylläpitotyön tyyppi.](media/am-guides-integration-create-work-order.png "Valitse ylläpitotyön tyyppi")

1. Näytä työtilaukseen ja työntekijöihin liittyvä opas:

    1. Avaa [resurssinhallinnan mobiilityötila](asset-management-mobile-workspace.md), jotta voit käyttää työtilausta.
    1. [Avaa työtilauksen ylläpidon tarkistuslista](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job).
    1. Valitse tarkistuslistarivi tarkastellaksesi liittyvää opasta.

        ![Tarkistuslistariviin liittyvä opas.](media/am-guides-integration-show-guide.png "Tarkistuslistariviin liittyvä opas")

    1. Avaa HoloLens-tehtäväopas.

        ![Avaa HoloLens-tehtäväopas.](media/am-guides-integration-hololens-select.png "Avaa HoloLens-tehtäväopas")

> [!NOTE]
> Voit liittää oppaan myös suoraan työtilauksen tai työlajin ylläpidon tarkistuslistaan.

> [!IMPORTANT]
> On tunnettu ongelma, että kun liität ylläpidon tarkistuslistamallin ja oletusylläpitotyötyypin, malliin linkitetty opas ei näy **ylläpitotyötyypin oletukset**-sivun **liitetyt oppaat**-pikavälilehdessä. Opas tulee kuitenkin näkyviin sen jälkeen, kun työlajia käytetään **Liittyvät oppaat** -pikavälilehden työtilaukseen.

## <a name="see-also"></a>Lisätietoja

- [Kaksoiskirjoituksen yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Resurssien hallinnan yleiskatsaus](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]