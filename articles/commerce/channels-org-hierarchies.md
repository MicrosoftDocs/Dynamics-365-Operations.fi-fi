---
title: Organisaatiohierarkioiden määrittäminen
description: Tässä ohjeaiheessa käsitellään organisaatiohierarkioiden määrittämistä Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6c19542089526c1e17fb1133d52cf042f244fb80
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002332"
---
# <a name="set-up-organization-hierarchies"></a>Organisaatiohierarkioiden määrittäminen


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään organisaatiohierarkioiden määrittämistä Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Ennen kanavien luontia on varmistettava, että organisaatiohierarkiat on määritetty.

Voit käyttää organisaatiohierarkioita liiketoiminnan tarkastelemiseen ja raportointiin eri näkökulmista. Voit esimerkiksi määrittää yhden hierarkian veroraportteja tai oikeudellista tai lakisääteistä raportointia varten. Voit määrittää toisen hierarkian raportoimaan sellaiset taloustiedot, joiden raportointia lainsäädäntö ei edellytä mutta joita käytetään sisäisessä raportoinnissa.

Ennen organisaatiohierarkian luomista sinun on luotava organisaatiot. Lisätietoja on kohdassa [Yritysten luominen](channels-legal-entities.md) tai [Toimintayksiköiden luominen](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Lisätietoja on seuraavissa aiheissa:
- [Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies)
- [Organisaatiohierarkian suunnitteleminen](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy?toc=/dynamics365/commerce/toc.json)
- [Organisaation hierarkian luominen](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Organisaatiohierarkian luominen

Luo organisaatiohierarkia seuraavien ohjeiden mukaan.

1. Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan asetukset \> Organisaatiohierarkiat**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna **Nimi**-kenttään arvo.
1. Valitse **Tarkoitus**-osassa **Määritä tarkoitus**.
1. Etsi haluamasi tietue luettelosta ja valitse se. Valitse tarkoitus määritettäväksi organisaatiohierarkiaan.
1. Valitse **Määritetyt hierarkiat** -kohdassa **Lisää**.
1. Merkitse valittu rivi luettelossa. Etsi juuri luomasi hierarkia.
1. Valitse **OK**.

Seuraavassa kuvassa on esimerkki organisaatiohierarkiasta, joka luotu kuvitteelliselle Adventure Works -myymäläketjulle.

![Esimerkki organisaatiohierarkiasta](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Organisaatioiden lisääminen hierarkiaan

Lisää organisaatiot hierarkiaan seuraavien ohjeiden mukaan.

1. Etsi haluamasi tietue luettelosta ja valitse se. Valitse hierarkia.
1. Valitse toimintoruudussa **Näytä**.
1. Lisää organisaatioita tarvittaessa.
1. Lisää organisaatio valitsemalla ensin **Muokkaa** ja sitten **Lisää**. Kun olet tehnyt haluamasi muutokset, voit tallentaa luonnoksen ja julkaista muutokset.

Seuraavassa kuvassa on hierarkian juureen lisätty yritys ja neljä kustannuspaikkaa: ostoskeskus-, outlet-, verkko- ja puhelinkeskuskanavat. Kuhunkin voidaan sitten lisätä erilaisia vähittäismyynti-, puhelinkeskus- ja verkkokanavia.

![Esimerkki hierarkian suunnittelutoiminnosta](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Lisäresurssit

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkian suunnitteleminen](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Yritysten luominen](channels-legal-entities.md)

[Toimintayksiköiden luominen](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Kanavien yleiskatsaus](channels-overview.md)

[Kanava-asetusten edellytykset](channels-prerequisites.md)
