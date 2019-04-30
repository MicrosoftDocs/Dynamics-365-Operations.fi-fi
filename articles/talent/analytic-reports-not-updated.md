---
title: Analyysiraportit eivät päivity
description: Tässä ohjeaiheessa kerrotaan, mitä pitää tehdä, jos asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtiloissa.
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
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "857450"
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
