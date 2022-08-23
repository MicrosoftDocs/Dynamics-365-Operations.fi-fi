---
title: Maksutyypin pitää olla luottokortti -virhe myyntitilaussivulla
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, kun myyntitilaussivulla näkyy virhesanoma tilauksen synkronoinnin jälkeen.
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
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285629"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Maksutyypin pitää olla luottokortti -virhe myyntitilaussivulla

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, kun myyntitilaussivulla näkyy virhesanoma tilauksen synkronoinnin jälkeen.

## <a name="description"></a>kuvaus

Kun avaat myyntitilaussivun tilauksen synkronoinnin jälkeen, näkyviin tulee seuraava virhesanoma: "Maksutyypin on oltava luottokortti, koska luottokortin numero on määritetty."

![Maksutyypin on oltava luottokortti -virhe.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Ratkaisu

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Maksutyypin asetus Commerce headquarters -sovelluksessa

1. Siirry kohtaan **Myyntireskontra \> Maksujen asetukset \> Maksuehdot**.
1. Valitse maksuehdot vasemmanpuoleista siirtymispalkista.
1. Varmista **Maksutyyppi**-kentässä, että **Luottokortti** on valittu.

## <a name="additional-resources"></a>Lisäresurssit

[Online-myyntien ja -maksujen kirjaaminen](../tasks/posting-online-sales-payments.md)
