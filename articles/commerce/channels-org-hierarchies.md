---
title: Organisaatiohierarkioiden määrittäminen
description: Tässä artikkelissa käsitellään organisaatiohierarkioiden määrittämistä Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: 2555378c119e4c096c4bf0c0adc11e3a50cbfe38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280444"
---
# <a name="set-up-organization-hierarchies"></a>Organisaatiohierarkioiden määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään organisaatiohierarkioiden määrittämistä Microsoft Dynamics 365 Commercessa.

Ennen kanavien luontia on varmistettava, että organisaatiohierarkiat on määritetty.

Voit käyttää organisaatiohierarkioita liiketoiminnan tarkastelemiseen ja raportointiin eri näkökulmista. Voit esimerkiksi määrittää yhden hierarkian veroraportteja tai oikeudellista tai lakisääteistä raportointia varten. Voit määrittää toisen hierarkian raportoimaan sellaiset taloustiedot, joiden raportointia lainsäädäntö ei edellytä mutta joita käytetään sisäisessä raportoinnissa.

Ennen organisaatiohierarkian luomista sinun on luotava organisaatiot. Lisätietoja on kohdassa [Yritysten luominen](channels-legal-entities.md) tai [Toimintayksiköiden luominen](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Lisätietoja on seuraavissa artikkeleissa.
- [Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Organisaatiohierarkian suunnitteleminen](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Organisaation hierarkian luominen](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

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

![Esimerkki organisaatiohierarkiasta.](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Organisaatioiden lisääminen hierarkiaan

Lisää organisaatiot hierarkiaan seuraavien ohjeiden mukaan.

1. Etsi haluamasi tietue luettelosta ja valitse se. Valitse hierarkia.
1. Valitse toimintoruudussa **Näytä**.
1. Lisää organisaatioita tarvittaessa.
1. Lisää organisaatio valitsemalla ensin **Muokkaa** ja sitten **Lisää**. Kun olet tehnyt haluamasi muutokset, voit tallentaa luonnoksen ja julkaista muutokset.

Seuraavassa kuvassa on hierarkian juureen lisätty yritys ja neljä kustannuspaikkaa: ostoskeskus-, outlet-, verkko- ja puhelinkeskuskanavat. Kuhunkin voidaan sitten lisätä erilaisia vähittäismyynti-, puhelinkeskus- ja verkkokanavia.

![Esimerkki hierarkian suunnittelutoiminnosta.](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Lisäresurssit

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisaatiohierarkian suunnitteleminen](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Yritysten luominen](channels-legal-entities.md)

[Toimintayksiköiden luominen](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Kanavien yleiskatsaus](channels-overview.md)

[Kanava-asetusten edellytykset](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
