---
title: Luottokortin merkintäsivulla näkyy virhe uloskuittauksen yhteydessä
description: Tässä artikkelissa on vianmääritysohjeita, jotka voivat auttaa silloin, kun Maksutapa-osaa ei ladata, ja näyttöön tulee virhesanoma.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269752"
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
