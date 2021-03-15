---
title: Kanavan lisääminen organisaatiohierarkiaan
description: Tässä ohjeaiheessa käsitellään kanavan lisäämistä organisaatiohierarkiaan Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 297bd34f9bde23d5cc7de266b8e8f49b1a752662
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993689"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>Kanavan lisääminen organisaatiohierarkiaan


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään kanavan lisäämistä organisaatiohierarkiaan Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Kanavat on liitettävä vähintään yhteen organisaatiohierarkiaan. Ennen kanavien luontia on varmistettava, että organisaatiohierarkiat on määritetty.  

Kohdassa [Organisaatiohierarkiat](channels-org-hierarchies.md) on lisätietoja organisaatiohierarkioiden luomisesta.

## <a name="select-a-hierarchy"></a>Hierarkian valinta

Valitse hierarkia seuraavien ohjeiden mukaisesti.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan asetukset \> Organisaatiohierarkiat**.
1. Valitse luettelosta organisaatiohierarkia, johon kanava lisätään.
1. Näytä hierarkian tiedot valitsemalla toimintoruudussa **Näytä**.

Seuraavassa kuvassa on valitun hierarkian organisaatiohierarkian tiedot.

![Valitun hierarkian organisaatiohierarkian tiedot](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>Kanavan lisääminen hierarkiasolmuun

Voit lisätä kanavan hierarkiasolmuun seuraavasti.

1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse hierarkiasolmu, johon kanava lisätään, ja valitse sitten avattavasta **Lisää**-luettelosta **Vähittäismyyntikanava**. 
1. Valitse lisättävä kanava ja valitse sitten **OK**-painike.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Julkaise** ja anna sitten menneisyydessä oleva **Voimaantulopäivä**, jotta toiminto otetaan heti käyttöön.

Seuraava kuva osoittaa, miten hierarkiasolmuun lisättävä kanava valitaan.

![Hierarkiasolmuun lisättävän kanavan valitseminen](media/channel-add-to-org-hierarchy-2.png)

Seuraavassa kuvassa on hierarkia, johon on lisätty useita kanavia.

![Hierarkia, johon on lisätty erilaisia kanavia](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>Lisäresurssit

[Kanavien yleiskatsaus](channels-overview.md)

[Kanava-asetusten edellytykset](channels-prerequisites.md)

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkian suunnitteleminen](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkiat](channels-org-hierarchies.md)

[Vähittäismyyntikanavan määrittäminen](channel-setup-retail.md)
    
[Verkkokanavan määrittäminen](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]