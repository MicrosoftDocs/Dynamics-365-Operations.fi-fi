--- 
title: "Toimittajan laskun kirjaaminen ja täsmäyttäminen vastaanotettuihin määriin"
description: "Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 3b0ba3a29514351a89cf83f1ce7a3e147626e721
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Toimittajan laskun kirjaaminen ja täsmäyttäminen vastaanotettuihin määriin

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


