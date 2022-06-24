---
title: Luottokortin merkintäsivulla näkyy virhe uloskuittauksen yhteydessä
description: Tässä artikkelissa on vianmääritysohjeita, jotka voivat auttaa silloin, kun Maksutapa-osaa ei ladata, ja näyttöön tulee virhesanoma.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 6d1f7ba2d1a63430431af94ed4bed3222c85f14d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910440"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Luottokortin merkintäsivulla näkyy virhe uloskuittauksen yhteydessä

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa on vianmääritysohjeita, jotka voivat auttaa silloin, kun **Maksutapa**-osaa ei ladata, ja näyttöön tulee virhesanoma.

## <a name="description"></a>kuvaus

Kun avaat online-myymälän kassasivun,**Maksutapa**-osaa ei ladata, ja näyttöön tulee seuraava virhesanoma: "Jokin meni vikaan. Yritä myöhemmin uudelleen."

![Maksumoduulin virhe.](media/payment-module-error.jpg)

## <a name="resolution"></a>Ratkaisu

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Odota Commerce Scale Unit -välimuistin vanhentumista

Verkkokaupan kassasivun maksupalvelun asetukset tallennetaan välimuistiin Commerce Scale Unitissa, ja niiden näkyminen sähköisen kaupan sivustossa voi kestää 15 minuuttia. Nämä maksupalvelun asetukset sisältävät muutoksia myyjätilin tunnukseen, pilvipalvelun API-avaimeen ja erilaisiin maksutapaan liittyviin konfigurointiasetuksiin.

## <a name="additional-resources"></a>Lisäresurssit

[Online-kanavan määrittäminen](../channel-setup-online.md)
