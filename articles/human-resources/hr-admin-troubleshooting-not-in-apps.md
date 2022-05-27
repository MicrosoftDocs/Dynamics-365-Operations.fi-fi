---
title: Human Resources ei näy Microsoft Dynamics 365 -sovelluksissa
description: Tässä aiheessa käsitellään, miten toimitaan, jos Microsoft Dynamics 365 Human Resources ei ole Microsoft Dynamics 365 -sovellusten luettelossa.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a973b10a15846f7a27bff955deb2a961f45d9701
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687726"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources -sovellus ei näy Microsoft Dynamics 365 -sovelluksissa


[!INCLUDE [PEAP](../includes/peap-2.md)]

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
