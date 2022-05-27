---
title: Analyysiraporttien vianmääritys
description: Tässä aiheessa käsitellään ongelmien vianmääritystä ja diagnosointia, jos asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtiloissa.
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
ms.openlocfilehash: 7e81bae4d9cb0bb0b77bb57bac16cc67bbbcf9ea
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694057"
---
# <a name="troubleshoot-analytic-reports"></a>Analyysiraporttien vianmääritys


[!INCLUDE [PEAP](../includes/peap-2.md)]

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

![Erätyöt.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
