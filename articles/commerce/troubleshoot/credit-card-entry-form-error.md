---
title: Luottokortin merkintäsivulla näkyy virhe uloskuittauksen yhteydessä
description: Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa silloin, kun Maksutapa-osaa ei ladata, ja näyttöön tulee virhesanoma.
author: Reza-Assadi
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
ms.openlocfilehash: d2c5f01d17df79c9b23fd513aaeb5c0605d657e9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801768"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Luottokortin merkintäsivulla näkyy virhe uloskuittauksen yhteydessä

[!include [banner](../../includes/banner.md)]

Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa silloin, kun **Maksutapa**-osaa ei ladata, ja näyttöön tulee virhesanoma.

## <a name="description"></a>kuvaus

Kun avaat online-myymälän kassasivun,**Maksutapa**-osaa ei ladata, ja näyttöön tulee seuraava virhesanoma: "Jokin meni vikaan. Yritä myöhemmin uudelleen."

![Maksumoduulin virhe](media/payment-module-error.jpg)

## <a name="resolution"></a>Ratkaisu

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Odota Commerce Scale Unit -välimuistin vanhentumista

Verkkokaupan kassasivun maksupalvelun asetukset tallennetaan välimuistiin Commerce Scale Unitissa, ja niiden näkyminen sähköisen kaupan sivustossa voi kestää 15 minuuttia. Nämä maksupalvelun asetukset sisältävät muutoksia myyjätilin tunnukseen, pilvipalvelun API-avaimeen ja erilaisiin maksutapaan liittyviin konfigurointiasetuksiin.

## <a name="additional-resources"></a>Lisäresurssit

[Online-kanavan määrittäminen](../channel-setup-online.md)
