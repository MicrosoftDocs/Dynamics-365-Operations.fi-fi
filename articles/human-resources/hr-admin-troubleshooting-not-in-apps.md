---
title: Human Resources ei näy Microsoft Dynamics 365 -sovelluksissa
description: Tässä artikkelissa kerrotaan, mitä on tehtävä, jos asiakas ei näe Microsoft Dynamics 365 Human Resources -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 658c6a4f17c022c3d0e3e49d16eb89624c4be27c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803966"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources ei näy Microsoft Dynamics 365 -sovelluksissa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Lähetä**

Asiakas ei näe Dynamics 365 Human Resourcesia Microsoft Dynamics 365 -sovellusten joukossa.

**Ratkaisu**

Käyttäjä on lisättävä ympäristön tekijän rooliin Microsoft Power Appsin ympäristössä.

1. Järjestelmänvalvoja, jolla on Power Apps-palvelupaketin 2 käyttöoikeus, on avattava [Power Appsin hallintaportaali](https://preview.admin.powerapps.com/).

2. Valitse ensin **Ympäristöt** ja sitten oikea Human Resourcesin ympäristö.

3. Valitse **Ympäristöroolit**-välilehden **Suojaus**-välilehdessä **Ympäristön tekijä**.

    ![Ympäristöroolit-välilehti](media/environment-roles.png)

4. Lisää käyttäjä tai organisaatio **Käyttäjät**-välilehdessä.

    ![Käyttäjät-välilehti](media/environment-maker.png)

5. Valitse **Tallenna**.

6. Käyttäjän on nyt kirjauduttava [Microsoft Dynamics 365:een](https://home.dynamics.com/).

7. Päivitä käyttäjän sovellukset valitsemalla **Synkronoi**.

    ![Synkronointipainike](media/get-more.png)

    Kun synkronointi on valmis, Human Resources näkyy aloitussivulla.


[!INCLUDE[footer-include](../includes/footer-banner.md)]