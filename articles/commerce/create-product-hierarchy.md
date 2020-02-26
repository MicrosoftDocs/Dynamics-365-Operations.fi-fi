---
title: Uuden tuotehierarkian luominen
description: Tässä ohjeaiheessa käsitellään uuden tuotehierarkian luontia Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: 73cecb0c6aacebf5c6fcf8a0edbc7513b3ce175d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001895"
---
# <a name="create-a-new-product-hierarchy"></a>Uuden tuotehierarkian luominen


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään uuden tuotehierarkian luontia Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Dynamics 365 Commerce tukee useita vähittäismyynnin kanavia. Vähittäismyyntikanavia ovat verkkokaupat, puhelinkeskukset ja vähittäismyymälät (eli kivijalkakaupat). Jokaisella vähittäismyymäläkanavalla voi olla omat maksuvälineet, hintaryhmät, kassakoneet, tulo- ja kulutilit sekä oma henkilökunta. Sinun on määritettävä kaikki nämä elementit, ennen kuin voit luoda vähittäismyymäläkanavan. 

Commerce-tuotehierarkiaa käytetään organisaation yleisen tuotehierarkian määrittämiseen. Commerce-tuotehierarkiaa voi käyttää markkinoinnissa, hinnoittelussa ja kampanjoissa, raportoinnissa sekä valikoiman suunnittelussa. Organisaatiolle voidaan määrittää vain yksi Commerce-tuotehierarkia.

## <a name="create-and-configure-a-product-hierarchy"></a>Tuotehierarkian luonti ja määritys

Voit luoda ja määrittää uuden Commerce-tuotehierarkian seuraavasti.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Kanavan siirtymisluokat**.
1. Jos hierarkiaa ei vielä ole, valitse **Toimintoruutu**-elementissä **Uusi** luodaksesi päähierarkian.
1. **Yleistä**-kohdassa:
    1. Anna nimi **Nimi**-ruutuun.
    1. Syötä **Kuvaus**-ruutuun kuvaus.
    1. Syötä **Kutsumanimi**-ruutuun kutsumanimi.
    1. Aseta **Aktiivinen**-asetuksen arvoksi **Kyllä**.

## <a name="add-hierarchy-nodes"></a>Hierarkiasolmujen lisäys

Voit lisätä hierarkiasolmuja seuraavien ohjeiden avulla.

1. Valitse toimintoruudusta **Muokkaa luokkahierarkiaa**.
1. Valitse pääsolmu, johon haluat lisätä uuden solmun, ja valitse sitten **Uusi luokkasolmu**.
1. Anna **Yleistä**-osassa **Nimi**, **Kuvaus**, **Kutsumanimi** ja **Avainsanat**.
1. **Yleistä**-kohdassa:
    1. Anna nimi **Nimi**-ruutuun.
    1. Syötä **Kuvaus**-ruutuun kuvaus.
    1. Syötä **Kutsumanimi**-ruutuun kutsumanimi.
    1. Syötä **Avainsanat**-ruutuun tarvittavat avainsanat.
    1. Syötä **Näyttöjärjestys**-ruutuun numero, joka edustaa näyttöjärjestystä (valinnainen).
1. Valitse toimintoruudussa **Tallenna**.
1. Voit lisätä lisää solmuja toistamalla edellä esitetyt vaiheet.

Seuraavassa kuvassa näytetään, miten uusi tuotehierarkiasolmu luodaan.

![Tuotehierarkian luominen](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Muut asetukset

Kullekin ryhmälle voi myös lisätä luokkamääriteryhmiä tarpeen mukaan.  

## <a name="additional-resources"></a>Lisäresurssit

[Vähittäismyyntihierarkiat](retail-hierarchies.md)

[Tuoteluokkien ja tuotteiden hallinta](category-management-product-creation.md)

[Esillepanokohteiden lajittelujärjestyksen muuttaminen](custom-order-categories-nav-retail-prod-hierarchy.md)
