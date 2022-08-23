---
title: Kanavan lisääminen organisaatiohierarkiaan
description: Tässä artikkelissa käsitellään kanavan lisäämistä organisaatiohierarkiaan Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 9def2d7c3cf17ecd9b74ce41f56bc3220a754597
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278594"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>Kanavan lisääminen organisaatiohierarkiaan


[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään kanavan lisäämistä organisaatiohierarkiaan Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Kanavat on liitettävä vähintään yhteen organisaatiohierarkiaan. Ennen kanavien luontia on varmistettava, että organisaatiohierarkiat on määritetty.  

Kohdassa [Organisaatiohierarkiat](channels-org-hierarchies.md) on lisätietoja organisaatiohierarkioiden luomisesta.

## <a name="select-a-hierarchy"></a>Hierarkian valinta

Valitse hierarkia seuraavien ohjeiden mukaisesti.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan asetukset \> Organisaatiohierarkiat**.
1. Valitse luettelosta organisaatiohierarkia, johon kanava lisätään.
1. Näytä hierarkian tiedot valitsemalla toimintoruudussa **Näytä**.

Seuraavassa kuvassa on valitun hierarkian organisaatiohierarkian tiedot.

![Valitun hierarkian organisaatiohierarkian tiedot.](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>Kanavan lisääminen hierarkiasolmuun

Voit lisätä kanavan hierarkiasolmuun seuraavasti.

1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse hierarkiasolmu, johon kanava lisätään, ja valitse sitten avattavasta **Lisää**-luettelosta **Vähittäismyyntikanava**. 
1. Valitse lisättävä kanava ja valitse sitten **OK**-painike.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Julkaise** ja anna sitten menneisyydessä oleva **Voimaantulopäivä**, jotta toiminto otetaan heti käyttöön.

Seuraava kuva osoittaa, miten hierarkiasolmuun lisättävä kanava valitaan.

![Hierarkiasolmuun lisättävän kanavan valitseminen.](media/channel-add-to-org-hierarchy-2.png)

Seuraavassa kuvassa on hierarkia, johon on lisätty useita kanavia.

![Hierarkia, johon on lisätty erilaisia kanavia.](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>Lisäresurssit

[Kanavien yleiskatsaus](channels-overview.md)

[Kanavan määrittämisen edellytykset](channels-prerequisites.md)

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkian suunnitteleminen](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkiat](channels-org-hierarchies.md)

[Vähittäismyyntikanavan määrittäminen](channel-setup-retail.md)
    
[Verkkokanavan määrittäminen](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
