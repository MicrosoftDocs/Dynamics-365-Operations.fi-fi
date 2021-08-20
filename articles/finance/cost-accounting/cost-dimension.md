---
title: Dimensioiden luonti ja dimensiojäsenten tuonti
description: Kustannuslaskenta on riippumaton moduuli, joka edellyttää muiden moduulien päätietoja.
author: ShylaThompson
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6febb8a48cf6496fb7f4c2ee9f5281d47aa1ccae1a8ecc51c908b3810302e11c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775119"
---
# <a name="create-dimensions-and-import-dimension-members"></a>Dimensioiden luonti ja dimensiojäsenten tuonti

[!include [banner](../includes/banner.md)]

Kustannuslaskenta on riippumaton moduuli, joka edellyttää muiden moduulien tietoja. Nämä tiedot luokitellaan seuraavasti:

-  Kustannustasot
-  Kustannusobjektit
-  Tilastodimensiot

**Kustannustaso** vastaa kustannusten kannalta merkittävää nimikettä tilikartassa. **Kustannusobjekti** voi olla mikä tahansa taloushallinnon dimensio, kuten tuote, kustannuspaikka, tai projekti, jota haluat arvioida tai mitata tai kohdistaa siihen kustannuksia suoraan. **Tilastodimensiota** ja sen jäseniä käytetään rekisteröitäessä ei-rahallisia merkintöjä. Tilastodimension jäseniä voidaan käyttää kohdistusperusteena esimerkiksi kustannusten jaossa ja kohdistuksessa. 

Seuraavassa kaaviossa kuvataan kustannuslaskennassa käytettävät dimensiot.

[![Kustannuslaskennan dimensiot.](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

Kun tiedot tuodaan kustannuslaskentaan, voit luoda sen avulla eri näkökulmia, jotka avustavat organisaation kaikkien tasojen johtajia. Seuraavissa ohjeaiheissa on tietoja dimensioiden luomisesta ja dimension jäsenten tuonnista. 

-  [Kustannustason dimensiot](cost-elements.md)
-  [Kustannustasojen luonti](./tasks/create-cost-elements.md)
-  [Kustannusobjektin dimensiot](cost-objects.md)
-  [Kustannustasodimension jäsenten yhdistäminen yhteiseen dimension jäsenten joukkoon](map-cost-elements-dimension-members.md)
-  [Määritä kustannustason dimensio](./tasks/map-cost-element-dimension.md)
-  [Tilastodimension jäsenet ja tilastomittauksen lähdemallit](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]