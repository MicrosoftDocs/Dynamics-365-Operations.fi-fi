---
title: Optimoi suorituskyky aikatauluttamalla erätyöt sulkemisajan jälkeen
description: Tässä ohjeaiheessa selitetään, miten voit ratkaista Microsoftin Dynamics 365 Human Resourcesin suorituskykyongelmia aikatauluttamalla pitkään jatkuvia erätöitä sulkemisajan jälkeen.
author: andreabichsel
manager: tfehr
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 0b13853598bbdec239bce98029e534991a53876b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467214"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimoi suorituskyky aikatauluttamalla erätyöt sulkemisajan jälkeen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Otto

Microsoft Dynamics 365 Human Resourcesissa voi ilmetä suorituskykyongelmia, jos pitkään jatkuvat erätyöt suoritetaan tavallisten aukioloaikojen aikana.

## <a name="resolution"></a>Tarkkuus

Aikatauluta seuraavat erätyöt sulkemisajan jälkeen. Suosittelemme myös usein suoritettavien erätöiden suoritusvälien tarkastamista. Jos mahdollista, vähennä erätyön toistuvuutta. Monissa tapauksissa oletusväli riittää.

Seuraavat erätyöt tulisi suorittaa yöaikaan tai sulkemisajan jälkeen. Muista tarkistaa näiden toistuvien erätöiden aikavyöhyke. Jotkin erätyöt voivat käyttää Pacific Standard Time (PST) -aikaa.

| Erätyö | Oletusesiintyminen |
| --- | --- |
| Erätyöhistorian siivous | 1 kerran kuukaudessa |
| Viennin väliaikaisen tallennuksen tietojen puhdistus | 1 kerran päivässä |
| Common Data Service -integroinnin vastaamattoman pyynnön synkronointi | 1 kerran päivässä |
| Tietokannan pakkausjärjestelmätyö, joka pitää suorittaa säännöllisesti sulkemisajan jälkeen | 1 kerran päivässä |
| Tietokannan indeksin uudelleenmuodostustyö, joka pitää suorittaa säännöllisesti sulkemisajan jälkeen | 1 kerran päivässä |

1. Valitse Human Resourcesissa **Järjestelmän hallinta**.

2. Hae **Haku**-palkissa yhtä yllä mainituista erätöistä.

3. Valitse **Suorita taustalla** ja sitten **Toistuminen**.

   ![Määritä toistuminen](media/talent-batch-history-cleanup-recurrence.png)

4. Valitse **Määritä toistuvuus** -osiosta **Aloituspäivä** ja **Aloitusaika** tapahtumaan ruuhka-aikojen ulkopuolella tai viikonloppuna. Valitse **Ei päättymispäivää**. 

   ![Määritä toistuvuuden alkamispäivä ja -aika](media/talent-batch-history-cleanup-define-recurrence.png)

5. Valitse **OK**.

6. Muuta tarvittaessa mitä tahansa muita parametreja kohdassa **Suorita taustalla** ja valitse sitten **OK**.

## <a name="additional-resources"></a>Lisäresurssit

[Optimoi suorituskyky automaattisilla tyhjennystehtävillä](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]