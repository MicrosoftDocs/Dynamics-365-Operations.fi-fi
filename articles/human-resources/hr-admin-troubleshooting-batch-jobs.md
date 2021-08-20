---
title: Optimoi suorituskyky aikatauluttamalla erätyöt sulkemisajan jälkeen
description: Tässä ohjeaiheessa selitetään, miten voit ratkaista Microsoftin Dynamics 365 Human Resourcesin suorituskykyongelmia aikatauluttamalla pitkään jatkuvia erätöitä sulkemisajan jälkeen.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: d2369b3209901eb2d60232a47d89284779199e1c98a56142758353d65a1faaf7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766868"
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

   ![Määritä toistuminen.](media/talent-batch-history-cleanup-recurrence.png)

4. Valitse **Määritä toistuvuus** -osiosta **Aloituspäivä** ja **Aloitusaika** tapahtumaan ruuhka-aikojen ulkopuolella tai viikonloppuna. Valitse **Ei päättymispäivää**. 

   ![Määritä toistuvuuden alkamispäivä ja -aika.](media/talent-batch-history-cleanup-define-recurrence.png)

5. Valitse **OK**.

6. Muuta tarvittaessa mitä tahansa muita parametreja kohdassa **Suorita taustalla** ja valitse sitten **OK**.

## <a name="additional-resources"></a>Lisäresurssit

[Optimoi suorituskyky automaattisilla tyhjennystehtävillä](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]