---
title: Talent ei näy Microsoft Dynamics 365 -sovellusten yhteydessä (CDS1.0)
description: Tässä ohjeaiheessa kerrotaan, mitä on tehtävä, jos asiakas ei näe Microsoft Dynamics 365 for Talent -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304243"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Talent ei näy Microsoft Dynamics 365 -sovellusten yhteydessä (CDS1.0)

[!include [banner](includes/banner.md)]

**Varasto-otto**

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
