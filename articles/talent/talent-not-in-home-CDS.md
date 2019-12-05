---
title: Talent ei näy Microsoft Dynamics -sovellusten yhteydessä (Common Data Service 1.0)
description: Tässä ohjeaiheessa kerrotaan, mitä on tehtävä, jos asiakas ei näe Microsoft Dynamics 365 Talent -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7f0cc1c7ec1234b7eedaade0ffadb66965ed2121
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772985"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent ei näy Microsoft Dynamics -sovellusten yhteydessä (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Varasto-otto**

Asiakas ei näe Microsoft Dynamics 365 Talent -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.

**Tarkkuus**

Käyttäjä on lisättävä ympäristön tekijän rooliin Microsoft Power Appsin ympäristössä.

1. Järjestelmänvalvoja, jolla on Power Apps-palvelupaketin 2 käyttöoikeus, on avattava [Power Appsin hallintaportaali](https://preview.admin.powerapps.com/).
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
