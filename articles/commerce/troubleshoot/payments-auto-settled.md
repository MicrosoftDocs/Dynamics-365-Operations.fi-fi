---
title: Maksut selvitetään automaattisesti, ennen kuin tilaukset laskutetaan tai lähetetään
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun maksu selvitetään Adyen-portaalissa heti tilauksen tekemisen jälkeen, vaikka myyntitilausta ei ole laskutettu eikä lähetetty.
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
ms.openlocfilehash: cc5167be43cccfd024ffdc65eb5f4dcac7e187288522d95be2385f8e7fdf106e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718644"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Maksut selvitetään automaattisesti, ennen kuin tilaukset laskutetaan tai lähetetään

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun maksu selvitetään Adyen-portaalissa heti tilauksen tekemisen jälkeen, vaikka myyntitilausta ei ole laskutettu eikä lähetetty.

## <a name="description"></a>kuvaus

Maksu selvitetään Adyen-portaalissa heti tilauksen tekemisen jälkeen, vaikka myyntitilausta ei ole laskutettu eikä lähetetty.

## <a name="resolution"></a>Ratkaisu

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Sähköisen kaupankäynnin maksujen manuaalisen sieppauksen konfiguroiminen Adyen-portaalissa

Voit konfiguroida sähköisen kaupankäynnin maksujen manuaalisen sieppauksen Adyen-portaalissa seuraavasti.

1. Kirjaudu Adyen-portaaliin.
1. Valitse oikeasta yläkulmasta sähköisen kaupankäynnin kanavan myyjätilisi.
1. Valitse yläreunan siirtymispalkissa **Tili** ja valitse sitten **Asetukset**.
1. Valitse **Siepausviive**-kentästä **manuaalinen**.

    ![Sieppausviive-asetus Adyen-portaalissa.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Lisäresurssit

[Adyen-maksun sieppaus](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector Adyenia varten](../dev-itpro/adyen-connector.md)

[Dynamics 365:n Adyen-maksuyhdistimen määritys](https://docs.adyen.com/plugins/microsoft-dynamics)
