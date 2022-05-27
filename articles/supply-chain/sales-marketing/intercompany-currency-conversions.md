---
title: Konsernin sisäiset valuuttamuunnokset
description: Tässä aiheessa käsitellään konsernin sisäisten tapahtumien valuuttamuunnoksia.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f0af05c324bb67744ba6650e3d7a4ba8b958040e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671895"
---
# <a name="intercompany-currency-conversions"></a>Konsernin sisäiset valuuttamuunnokset

[!include [banner](../../includes/banner.md)]

Kun alkuperäisen myyntitilauksen ja konsernin sisäisen ostotilauksen valuuttakoodi poikkeaa toisistaan, seuraavien kenttien valuutta muunnetaan, jos synkronointi on otettu käyttöön:

- **Yksikköhinta**
- **Myynnin kulut** tai **Ostojen kulut**
- **Alennus**
- **Monirivialennus**

Nämä kentät synkronoidaan sitten konsernin sisäisen myyntitilauksen rivin kanssa.

Koska konsernin sisäisen ostotilauksen ja konsernin sisäisen ostotilauksen valuutta synkronoidaan aina, seuraavat kentät synkronoidaan ilman valuuttamuunnosta:

- **Yksikköhinta**
- **Myynnin kulut** tai **Ostojen kulut**
- **Alennus**
- **Alennusprosentti**
- **Monirivialennus**
- **Monirivialennusprosentti**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
