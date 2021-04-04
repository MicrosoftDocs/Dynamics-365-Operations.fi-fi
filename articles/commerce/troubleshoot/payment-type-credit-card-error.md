---
title: Maksutyypin pitää olla luottokortti -virhe myyntitilaussivulla
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun myyntitilaussivulla näkyy virhesanoma tilauksen synkronoinnin jälkeen.
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
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585304"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Maksutyypin pitää olla luottokortti -virhe myyntitilaussivulla

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun myyntitilaussivulla näkyy virhesanoma tilauksen synkronoinnin jälkeen.

## <a name="description"></a>kuvaus

Kun avaat myyntitilaussivun tilauksen synkronoinnin jälkeen, näkyviin tulee seuraava virhesanoma: "Maksutyypin on oltava luottokortti, koska luottokortin numero on määritetty."

![Maksutyypin on oltava luottokortti -virhe](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Ratkaisu

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Maksutyypin asetus Commerce headquarters -sovelluksessa

1. Siirry kohtaan **Myyntireskontra \> Maksujen asetukset \> Maksuehdot**.
1. Valitse maksuehdot vasemmanpuoleista siirtymispalkista.
1. Varmista **Maksutyyppi**-kentässä, että **Luottokortti** on valittu.

## <a name="additional-resources"></a>Lisäresurssit

[Online-myyntien ja -maksujen kirjaaminen](../tasks/posting-online-sales-payments.md)
