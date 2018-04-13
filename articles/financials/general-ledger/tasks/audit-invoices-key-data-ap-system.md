--- 
title: Laskujen ja avaintietojen tarkistaminen ostoreskontrassa
description: "Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5cd9448c95b7ec0c4a82aca3d21d961259dfb109
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Laskujen ja avaintietojen tarkistaminen ostoreskontrassa

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


