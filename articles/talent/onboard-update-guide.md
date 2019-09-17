---
title: Perehdytysoppaiden päivittäminen Dynamics 365 for Talent - Onboardissa
description: Tässä ohjeaiheessa käsitellään perehdytysoppaiden päivittämistä Microsoft Dynamics 365 for Talent - Onboardissa ja muutosten siirtämistä aiemmin luotuihin oppaisiin.
author: andreabichsel
manager: ''
ms.date: 06/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d2be450685724510db2f0fd2af8545f8f40278e7
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731454"
---
# <a name="update-onboarding-guides-in-dynamics-365-for-talent-onboard"></a>Perehdytysoppaiden päivittäminen Dynamics 365 for Talent: Onboardissa

[!include [banner](includes/banner.md)]

Jos perehdytysoppaisiin on tehtävä muutoksia Microsoft Dynamics 365 for Talent: Onboardissa, voit päivittää ne ja siirtää muutokset, vaikka oppaat olisi jo lähetetty. Perehdytysoppaan voi päivittää kahdella tavalla:

- Muokkaa perehdytysopasta suoraan ja tallenna tekemäsi muutokset.
- Muokkaa perehdytysmallia ja siirrä sitten muutokset kaikkiin siitä luotuihin perehdytysoppaisiin.

## <a name="edit-an-onboarding-guide-directly"></a>Perehdytysoppaan suora muokkaus

1. Valitse vasemmassa valikossa **Oppaat**.
2. Valitse muokattava opas.
3. Tee kaikki tarvittavat muutokset ja valitse sitten **Tallenna**-painike (levysymboli).

    ![[Perehdytysoppaan muutosten tallentaminen](./media/onboard-save.png)](./media/onboard-save.png)

Onboard lähettää automaattisesti uudelleen työntekijälle muutoksista ilmoittavan sähköpostiviestin. Muutokset on helppo tunnistaa, sillä kunkin muutoksen vieressä on **Uusi**-tunniste.

## <a name="update-multiple-guides-by-editing-the-onboarding-template"></a>Useiden oppaiden päivittäminen perehdytysmallia muokkaamalla

1. Valitse vasemmassa valikossa **Mallit**.
2. Valitse **Omat mallit** -kohdassa muokattava malli.
3. Tee kaikki tarvittavat muutokset ja valitse sitten **Tallenna**-painike (levysymboli).
4. Siirrä muutokset kaikkiin malliin perustuviin oppaisiin valitsemalla **Siirrä nämä muutokset**.

    ![[Perehdytysmallin muutosten siirtäminen kaikkiin siitä luotuihin oppaisiin](./media/onboard-push-changes.png)](./media/onboard-push-changes.png)

Perehdytysoppaita avaavat uudet työntekijät näkevät nämä muutokset. Onboard ei kuitenkaan ilmoita sähköpostihälytyksillä uusille työntekijöille, että perehdytysopas on muuttunut. Muutokset on helppo tunnistaa, sillä kunkin muutoksen vieressä on **Uusi**-tunniste. 
