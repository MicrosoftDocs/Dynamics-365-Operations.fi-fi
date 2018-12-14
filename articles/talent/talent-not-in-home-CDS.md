---
title: "Talent ei näy yhtenä Microsoft Dynamics 365 -sovelluksena (CDS1.0)"
description: "Tässä ohjeaiheessa kerrotaan, mitä on tehtävä, jos asiakas ei näe Microsoft Dynamics 365 for Talent -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Talent ei näy yhtenä Microsoft Dynamics 365 -sovelluksena (CDS1.0)

[!include [banner](includes/banner.md)]

**Ongelma**

Asiakas ei näe Microsoft Dynamics 365 for Talent -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.

**Tarkkuus**

Käyttäjä on lisättävä ympäristön tekijän rooliin Microsoft PowerAppsin ympäristössä.

1. Järjestelmänvalvoja, jolla on PowerApps -palvelupaketin 2 käyttöoikeus, on avattava [PowerAppsin hallintaportaali](https://preview.admin.powerapps.com/).
2. Valitse ensin **Ympäristöt** ja sitten oikea Talentin ympäristö.
3. Valitse **Ympäristöroolit**-välilehden **Suojaus**-välilehdessä **Ympäristön tekijä**.

    ![Ympäristöroolit-välilehti](media/environment-roles.png)

4. Lisää käyttäjä tai organisaatio **Käyttäjät**-välilehdessä.

    ![Käyttäjät-välilehti](media/environment-maker.png)

5. Valitse **Tallenna**.
6. Käyttäjän on nyt kirjauduttava [Microsoft Dynamics 365:een](https://home.dynamics.com/).
7. Päivitä käyttäjän sovellukset valitsemalla **Synkronoi**.

    ![Synkronointipainike](media/get-more.png)

    Kun synkronointi on valmis, Talent näkyy aloitussivulla.

