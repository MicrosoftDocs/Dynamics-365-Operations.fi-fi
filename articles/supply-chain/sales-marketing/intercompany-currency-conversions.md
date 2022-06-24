---
title: Konsernin sisäiset valuuttamuunnokset
description: Tässä artikkelissa käsitellään konsernin sisäisten tapahtumien valuuttamuunnoksia.
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
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851475"
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
