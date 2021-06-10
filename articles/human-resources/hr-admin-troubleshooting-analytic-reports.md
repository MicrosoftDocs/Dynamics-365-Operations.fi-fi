---
title: Analyysiraporttien vianmääritys
description: Tässä artikkelissa kerrotaan, mitä pitää tehdä, jos asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtiloissa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053536"
---
# <a name="troubleshoot-analytic-reports"></a>Analyysiraporttien vianmääritys

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Lähetä**

Asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtilojen **Analytiikka**-välilehdillä.

**Syy**

Microsoft Power BI -raportit päivitetään oletusarvoisesti neljän tunnin välein Ota mitta käyttöön -erätyön aikataulun mukaisesti.

**Tarkkuus**

Ajoitus voi siis selittää tämän ongelman. Päivitä analytiikkatyötilat aloittamalla erätyö seuraavien ohjeiden mukaisesti.

1. Avaa **Erätyöt**-sivut valitsemalla **Järjestelmänvalvoja \> Linkit \> Erätyöt \> Erätyöt**. Vaihtoehtoisesti voit käyttää hakutoimintoa ja hakusanaa **Erätyöt**.
1. Etsi **Ota mitta käyttöön** -työ luettelosta.
1. Valitse sivun yläosassa **Muokkaa** ja määritä ajoitetuksi aloituspäiväksi ja -ajaksi arvo, joka päivittää analytiikkaan lähellä kuluvaa ajankohtaa.

![Erätyöt](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]