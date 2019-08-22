---
title: Toimittajan laskun tallentaminen laskukirjauskansioon
description: Tässä ohjauksessa näytetään, miten ostotilauksiin liittämättömät toimittajan laskut tallennetaan.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97dd03a96389ab22e441acd0af1ad35852570be4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837009"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Toimittajan laskun tallentaminen laskukirjauskansioon

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjauksessa näytetään, miten ostotilauksiin liittämättömät toimittajan laskut tallennetaan. Tällaisia laskuja ovat esimerkiksi tarvikkeiden tai palveluiden kulut.  Tässä tallenteessa käytetään esittely-yritystä USMF.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Työtilat > Toimittajan laskun syöttö**.
2. Napsauta **Toimintoruudussa** **Uusi laskukirjauskansio**.
3. Valitse **Uusi**.
4. Avaa haku syöttämällä **Nimi**-kenttään kirjauskansion nimi tai valitsemalla avattavan valikon painike.
5. Kirjoita **Kuvaus**-kenttään arvo.
6. Valitse **toimintoruudussa** **Rivit**. Syötä **Päivämäärä**-kenttään kirjauspäivämäärä, joka päivittää kirjanpidon.  
7. Määritä **Tili**-kenttään **Toimittajan tili**.
8. Syötä **Lasku**-kenttään laskunumero.
9. Kirjoita **Kuvaus**-kenttään arvo.
10. Syötä **Kredit**-kenttään numero.
11. Avaa haku syöttämällä **Vastatili**-kenttään tilinumero nimi tai valitsemalla avattavan valikon painike
    * **Arvonlisäveroryhmän** oletusarvo saadaan toimittajan tililtä.  
    * **Nimikkeen arvonlisäveroryhmän** oletusarvo saadaan **Vastatili**-kentässä määritetyltä päätililtä.  
    * **Eräpäivä** lasketaan maksuehtojen perusteella.  
    * **Käteisalennuksen** oletusarvo saadaan toimittajan tililtä.  
12. Valitse **Kirjaa**.
13. Sulje sivu.

