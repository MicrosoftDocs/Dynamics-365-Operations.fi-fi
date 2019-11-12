---
title: 'Perehdytysoppaiden päivittäminen Dynamics 365 Talent: Onboardissa'
description: 'Tässä ohjeaiheessa käsitellään perehdytysoppaiden päivittämistä Microsoft Dynamics 365 Talent: Onboardissa ja muutosten siirtämistä aiemmin luotuihin oppaisiin.'
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
ms.openlocfilehash: 071aa79ea75e9a94187dd74dabab940e2cce0f92
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551953"
---
# <a name="update-onboarding-guides-in-dynamics-365-talent---onboard"></a>Perehdytysoppaiden päivittäminen Dynamics 365 Talent: Onboardissa

[!include [banner](includes/banner.md)]

Jos perehdytysoppaisiin on tehtävä muutoksia Microsoft Dynamics 365 Talent: Onboardissa, voit päivittää ne ja siirtää muutokset, vaikka oppaat olisi jo lähetetty. Perehdytysoppaan voi päivittää kahdella tavalla:

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
