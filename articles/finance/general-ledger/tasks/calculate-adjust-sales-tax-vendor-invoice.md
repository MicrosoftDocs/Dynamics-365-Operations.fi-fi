---
title: Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys
description: Tässä ohjeaiheessa kerrotaan, miten toimittajan laskun arvonlisäveroa oikaistaan Dynamics 365 Financeissa.
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994712"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään toimittajan laskun arvonlisäveron oikaisemista. Jos alkuperäinen lähdeasiakirja sisältää eri verosummat kuin lasketut summat, voit oikaista summat ennen kirjaamista. Tässä tehtävässä käytetään esittely-yritystä DEMF.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]