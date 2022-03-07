---
title: Human Resources ei näy Microsoft Dynamics 365 -sovelluksissa
description: Tässä aiheessa käsitellään, miten toimitaan, jos Microsoft Dynamics 365 Human Resources ei ole Microsoft Dynamics 365 -sovellusten luettelossa.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dfed82463eece882bed66c7b2dac1dd30e04720e
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413398"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources -sovellus ei näy Microsoft Dynamics 365 -sovelluksissa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Ongelma**

Asiakas ei näe Dynamics 365 Human Resourcesia Microsoft Dynamics 365 -sovellusten joukossa.

**Ratkaisu**

Käyttäjä on lisättävä ympäristön tekijän rooliin Microsoft Power Appsin ympäristössä.

1. Järjestelmänvalvoja, jolla on Power Apps-palvelupaketin 2 käyttöoikeus, on avattava [Power Appsin hallintaportaali](https://preview.admin.powerapps.com/).

2. Valitse ensin **Ympäristöt** ja sitten oikea Human Resourcesin ympäristö.

3. Valitse **Ympäristöroolit**-välilehden **Suojaus**-välilehdessä **Ympäristön tekijä**.

    ![Ympäristöroolit-välilehti.](media/environment-roles.png)

4. Lisää käyttäjä tai organisaatio **Käyttäjät**-välilehdessä.

    ![Käyttäjät-välilehti.](media/environment-maker.png)

5. Valitse **Tallenna**.

6. Käyttäjän on nyt kirjauduttava [Microsoft Dynamics 365:een](https://home.dynamics.com/).

7. Päivitä käyttäjän sovellukset valitsemalla **Synkronoi**.

    ![Synkronointipainike.](media/get-more.png)

    Kun synkronointi on valmis, Human Resources näkyy aloitussivulla.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
