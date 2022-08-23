---
title: Maksut selvitetään automaattisesti, ennen kuin tilaukset laskutetaan tai lähetetään
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, kun maksu selvitetään Adyen-portaalissa heti tilauksen tekemisen jälkeen, vaikka myyntitilausta ei ole laskutettu eikä lähetetty.
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
ms.openlocfilehash: 6fdaf48600edc22b5423e0167177616758e2dc6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282704"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Maksut selvitetään automaattisesti, ennen kuin tilaukset laskutetaan tai lähetetään

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, kun maksu selvitetään Adyen-portaalissa heti tilauksen tekemisen jälkeen, vaikka myyntitilausta ei ole laskutettu eikä lähetetty.

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
