---
title: Tallenna seuraavaa maksua varten -vaihtoehto ei tule näkyviin
description: Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa siinä, kun Tallenna seuraavaa maksua varten -valintaruutu ei näy sähköisen kaupankäynnin sivuston kassasivun Maksutapa-kohdassa.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3a4fbcd522651ed1b82b72b751ff6ead44c94a71
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585305"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Tallenna seuraavaa maksua varten -vaihtoehto ei tule näkyviin

[!include [banner](../../includes/banner.md)]

Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa siinä, kun **Tallenna seuraavaa maksua varten** -valintaruutu ei näy sähköisen kaupankäynnin sivuston kassasivun **Maksutapa**-kohdassa.

## <a name="description"></a>kuvaus

**Tallenna seuraavaa maksua varten** -valintaruutu ei näy sähköisen kaupankäynnin sivuston kassasivun **Maksutapa**-osassa.

Seuraavassa kuvassa on esimerkki kassasivusta, joka sisältää **Tallenna seuraavaa maksua varten** -valintaruudun.

![Tallenna seuraavaa maksua varten -valintaruutu maksumoduulissa](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Ratkaisu

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Tarkista, että Dynamics 365 Payment Connector Adyenia varten on määritetty oikein Commerce headquarters -sovelluksessa

Voit tarkistaa, että Dynamics 365 Payment Connector Adyenia varten on määritetty oikein Commerce headquarters -sovelluksessa, toimimalla seuraavasti.

1. Valitse **Retail ja Commerce \> Kanavat \> Verkkokaupat**.
1. Valitse verkkokauppa.
1. Varmista **Maksutilit**-pikavälilehdessä, että **Salli maksutietojen tallentaminen verkkokaupassa** -kentän arvoksi on määritetty **Tosi**.

![Salli maksutietojen tallentaminen verkkokaupassa -kenttä Commerce headquartersissa](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Lisäresurssit

[Maksumoduuli](../payment-module.md)

[Online-maksuvälineiden tallentaminen Adyen-yhdistimen avulla](../dev-itpro/adyen-connector-listPI.md)