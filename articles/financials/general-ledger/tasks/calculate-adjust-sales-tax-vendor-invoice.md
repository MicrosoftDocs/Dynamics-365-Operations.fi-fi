---
title: Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys
description: Tässä ohjeaiheessa kerrotaan, miten toimittajan laskun arvonlisäveroa oikaistaan Dynamics 365 for Finance and Operationsissa.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 684529087d5348c9e02310f812f8aa6f64c6655f
ms.sourcegitcommit: 016832198c306e8329ad21b5254e7d1cdff74c2f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862611"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten toimittajan laskun arvonlisäveroa oikaistaan Dynamics 365 for Finance and Operationsissa. Jos alkuperäinen lähdeasiakirja sisältää eri verosummat kuin lasketut summat, voit oikaista summat ennen kirjaamista. Tässä tehtävässä käytetään esittely-yritystä DEMF.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskukirjauskansio**.
2. Valitse **Uusi**.
3. Valitse uuden rivin **Nimi**-kentässä avattavasta valikosta vaihtoehto.
4. Valitse toimintoruudussa **Rivit**.
5. Määritä **Tili**-kenttään haluamasi arvot.
6. Kirjoita **Lasku**-kenttään arvo.
7. Syötä **Kredit**-kenttään numero.
8. Määritä **Vastatili**-kenttään haluamasi arvot.
9. Valitse **Arvonlisävero**.
10. Syötä **Toteutunut kokonaisarvonlisäverosumma** -kenttään numero.
11. Arvonlisäverosummat voidaan oikaista **Oikaisu**-välilehdessä arvonlisäverokoodin mukaan.
12. Valitse **Nollaa todellinen lasketuista summista**.
13. Valitse **OK**.
14. Valitse **Tallenna**.

