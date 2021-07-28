---
title: Oletusmaksupalveluun liittyvä tilauksen synkronointivirhe
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa korjaamaan online-tilauksen synkronoinnin yhteydessä mahdollisesti tapahtuvat virheet.
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
ms.openlocfilehash: 647060635813ad7e680ea88be76668818ff606d3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350351"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Oletusmaksupalveluun liittyvä tilauksen synkronointivirhe

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa korjaamaan online-tilauksen synkronoinnin yhteydessä mahdollisesti tapahtuvat virheet.

## <a name="description"></a>kuvaus

Kun synkronoit online-tilauksen, näyttöön tulee seuraava virhesanoma: "Luottokorttitapahtumien käsittelemiseksi on oltava oletusmaksupalvelu."

![Puuttuva oletusmaksupalvelu -virhe.](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Ratkaisu

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Commerce headquarters -oletusmaksupalvelun vahvistus tai asetus

Voit vahvistaa tai määrittää Commerce headquarters -oletusmaksupalvelun seuraavasti.

1. Siirry kohtaan **Myyntireskontra \> Maksujen asetukset \> Maksupalvelut**.
1. Varmista, että **Uusien luottokorttien oletuskäsittelijä** -asetukseksi on määritetty **Kyllä** yhdelle maksupalvelulle.

## <a name="additional-resources"></a>Lisäresurssit

[Luottokorttien määrittäminen, varmennus ja tietojen tarkistus](../../finance/accounts-receivable/credit-card-authorizations.md)