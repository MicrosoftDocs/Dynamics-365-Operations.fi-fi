---
title: Konsernin sisäiset valuuttamuunnokset
description: Tässä aiheessa käsitellään konsernin sisäisten tapahtumien valuuttamuunnoksia.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548249"
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
