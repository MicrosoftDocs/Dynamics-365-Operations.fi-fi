---
title: Käsittele kirjanpidon kohdistuskirjauskansio
description: Tässä ohjeaiheessa kerrotaan, miten kohdistuspyyntö käsitellään Dynamics 365 Finance -ohjelmassa.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33e989d3641ae1eaa28a55398fcf51674ac1ed72
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442794"
---
# <a name="process-ledger-allocation-journal"></a>Käsittele kirjanpidon kohdistuskirjauskansio

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten kohdistuspyyntö käsitellään. Voit luoda Käsittele kohdistuspyyntö -sivulla kohdistuskirjauskansion, joka voidaan tarkistaa ja hyväksyä ennen kirjanpitoon kirjaamista tai kirjata kirjanpitoon suoraan. Ennen kohdistuskirjauskansion luomista käytössä on oltava vähintään yksi aktiivinen kirjanpidon kohdistussääntö. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Kirjanpito > Kohdistukset > Käsittele kohdistuspyyntö**.
2. Valitse **Sääntö**-kentässä avattavasta valikosta haluamasi tietue.
3. Lisää **Alkupäivämäärä** -kenttään päivämäärä.

    - **Alkupäivämäärä** on erittäin tärkeä, kun kirjanpito on säännön tietolähde. Tämä päivämäärä määrittää, mitkä kirjanpidon saldot sisällytetään kohdistukseen.  
    - Valitse **Lähdearvo nolla** -kentässä **Pysäytä**. Kohdistusprosessi pysäytetään ja näyttöön avautuu sanoma, jonka mukaan lähdesumma on nolla.  

4. Valitse **Ehdotuksen asetukset** -kentässä **Vain ehdotus**. Valitsemalla **Vain ehdotus** voit tarkastella ja halutessasi hyväksyä tuloksen kohdistuskirjauskansioissa ennen kohdistuksen kirjaamista kirjanpitoon.  
5. Lisää päivämäärä Kirjanpidon kirjauspäivä -kenttään.
6. Valitse **OK**.
7. Siirry siirtymisruudussa kohtaan **Moduulit > Kirjanpito > Kohdistukset > Kohdistuskirjauskansiot**.
8. Valitse **Rivit**.
9. Valitse **Kirjaa**.
10. Valitse **Kirjaa**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]