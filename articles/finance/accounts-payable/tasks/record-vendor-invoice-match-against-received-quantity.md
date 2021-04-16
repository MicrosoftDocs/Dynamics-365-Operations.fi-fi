---
title: Toimittajan laskun kirjaaminen ja täsmäyttäminen vastaanotettuihin määriin
description: Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi.
author: ShivamPandey-msft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9d3fab4be1de90783d5885cf46b9e0cf6ee74b5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820614"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Toimittajan laskun kirjaaminen ja täsmäyttäminen vastaanotettuihin määriin

[!include [banner](../../includes/banner.md)]

Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi. Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna. 

Varmista Ostoreskontran parametrit -sivulla, että Ota käyttöön laskujen täsmäytyksen vahvistus -asetus on valittu, Kirjaa lasku, jossa on ristiriitoja -kentän arvoksi on määritetty Edellytä hyväksyntä ja Rivien vastaavuuskäytäntö -kentän arvoksi on määritetty Kolmisuuntainen vastaavuus.

Näissä toimintaohjeissa käytetään esittely-yritystä USMF. Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli.


## <a name="create-a-purchase-order"></a>Luo ostotilaus
1. Siirry Kaikki ostotilaukset -kohtaan.
2. Valitse Uusi.
3. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
4. Kirjoita arvo Toimittajan tili -kenttään.
5. Valitse OK.
6. Valitse Lisää rivi.
7. Kirjoita arvo Nimiketunnus-kenttään.
8. Valitse toimintoruudussa Osta.
9. Valitse Vahvista.

## <a name="post-a-product-receipt"></a>Tuotteen vastaanoton kirjaaminen
1. Valitse toimintoruudussa Vastaanota.
2. Valitse Tuotteen vastaanotto.
3. Merkitse valittu rivi luettelossa.
4. Kirjoita arvo Tuotteen vastaanotto -kenttään.
5. Valitse OK.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Toimittajan laskun tallentaminen ja täsmäyttäminen tuotteen vastaanoton kanssa
1. Valitse toimintoruudussa Lasku.
2. Valitse Lasku.
3. Kirjoita arvo Numero-kenttään.
4. Valitse Oletusarvo kohteesta: Tilattu määrä, kun haluat avata valintaikkunan.
5. Valitse vaihtoehto Rivien oletusmäärä -kentässä.
6. Valitse OK.
7. Valitse Kyllä.
8. Valitse Täsmäytä tuotteiden vastaanotot.
9. Valitse OK.
10. Valitse toimintoruudussa Tarkista.
11. Valitse Täsmäytyksen tiedot.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]