---
title: Toimittajalaskun arvonlisäveron laskeminen ja täsmäytys
description: Tässä ohjeaiheessa kerrotaan, miten toimittajan laskun arvonlisäveroa oikaistaan Dynamics 365 Financessa.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd98f42b501ddabdc0cc26d2a264c533410731f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815209"
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