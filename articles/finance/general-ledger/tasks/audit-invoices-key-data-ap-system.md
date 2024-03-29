---
title: Laskujen ja avaintietojen tarkistaminen ostoreskontrassa
description: Tässä artikkelissa näytetään, miten ostoreskontran laskut ja keskeiset tiedot voidaan tarkistaa.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4525534f906322c7fe4c232f0f6da5b308829087
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775212"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Laskujen ja avaintietojen tarkistaminen ostoreskontrassa

[!include [banner](../../includes/banner.md)]

Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi. Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna. 

Varmista **Ostoreskontran parametrit** -sivulla, että **Ota käyttöön laskujen täsmäytyksen vahvistus** -asetus on valittu, **Kirjaa lasku, jossa on ristiriitoja** -kentän arvoksi on määritetty **Edellytä hyväksyntä** ja **Rivien vastaavuuskäytäntö** -kentän arvoksi on määritetty **Kolmisuuntainen vastaavuus**.

Näissä toimintaohjeissa käytetään esittely-yritystä USMF. Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli.


## <a name="create-a-purchase-order"></a>Luo ostotilaus
1. Valitse **Kaikki ostotilaukset**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Toimittajan tili** -kenttään.
4. Napsauta **OK**.
5. Valitse **Lisää rivi**.
6. Kirjoita arvo **Nimiketunnus**-kenttään.
7. Valitse toimintoruudussa **Osto**.
8. Valitse **Vahvista**.

## <a name="post-a-product-receipt"></a>Tuotteen vastaanoton kirjaaminen
1. Valitse toimintoruudussa **Vastaanota**.
2. Valitse **Tuotteen vastaanotto**.
3. Kirjoita arvo **Tuotteen vastaanotto** -kenttään.
4. Napsauta **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Toimittajan laskun tallentaminen ja täsmäyttäminen tuotteen vastaanoton kanssa
1. Valitse toimintoruudussa **Lasku > Lasku**.
2. Kirjoita arvo **Numero**-kenttään.
3. Avaa valintaikkuna valitsemalla **Oletusarvo kohteesta: Tilattu määrä**.
4. Valitse vaihtoehto **Rivien oletusmäärä** -kentässä.
5. Napsauta **OK**.
6. Valitse **Kyllä**.
7. Valitse **Täsmäytä tuotteiden vastaanotot**.
8. Napsauta **OK**.
9. Valitse toimintoruudussa **Tarkista**.
10. Valitse **Täsmäytyksen tiedot**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
