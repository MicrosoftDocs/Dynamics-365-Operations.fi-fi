---
title: Analyysiraportit eivät päivity
description: Tässä ohjeaiheessa kerrotaan, mitä pitää tehdä, jos asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtiloissa.
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
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304175"
---
# <a name="analytic-reports-are-not-updated"></a>Analyysiraportit eivät päivity

[!include [banner](includes/banner.md)]

**Ongelma**

Asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtilojen **Analytiikka**-välilehdillä.

**Syy**

Microsoft Power BI -raportit päivittyvät oletusarvoisesti neljän tunnin välein Ota mitta käyttöön -erätyön aikataulun mukaisesti.

**Tarkkuus**

Ajoitus voi siis selittää tämän ongelman. Päivitä analytiikkatyötilat aloittamalla erätyö seuraavien ohjeiden mukaisesti.

1. Avaa **Erätyöt**-sivut valitsemalla **Järjestelmänvalvoja \> Linkit \> Erätyöt \> Erätyöt**. Vaihtoehtoisesti voit käyttää hakutoimintoa ja hakusanaa **Erätyöt**.
1. Etsi **Ota mitta käyttöön** -työ luettelosta.
1. Valitse sivun yläosassa **Muokkaa** ja määritä ajoitetuksi aloituspäiväksi ja -ajaksi arvo, joka päivittää analytiikkaan lähellä kuluvaa ajankohtaa.

![Erätyöt](media/batch-jobs.png)
