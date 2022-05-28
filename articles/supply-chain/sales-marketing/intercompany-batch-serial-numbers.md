---
title: Konsernin sisäiset erä- ja sarjanumerot
description: Tässä aiheessa käsitellään konsernin sisäisten tilausten erä- ja sarjanumeroiden rekisteröimistä
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
ms.openlocfilehash: 9d5e6ddd0bf9ab9dd032e3ab8d1e11d53fba639e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672931"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Konsernin sisäiset erä- ja sarjanumerot

[!include [banner](../../includes/banner.md)]

Yritysten, jotka seuraavat nimikkeitä sarja- tai eränumeroiden avulla, on seurattava myös poimittujen nimikkeiden sarja- ja eränumeroita. Konsernin sisäinen toiminto vie tai tuo automaattisesti sarja- ja eränumerot yrityksestä toiseen. Kun rekisteröit konsernin sisäisen myyntitilauksen nimikkeiden sarja- ja eränumerot, voit määrittää ohjelman viemään nämä numerot automaattisesti konsernin sisäiseen ostotilaukseen ja alkuperäiseen myyntitilaukseen. Soveltuvat parametrit määritetään myyntitilauksen **Konsernin sisäinen** -sivulla:

- Jos **Eränumero**-kenttä valitaan **Myyntitilauskäytännöt**-sivulla, eränumero synkronoidaan konsernin sisäisen ostotilauksen rivien varastotapahtumiin, kun konsernin sisäisen myyntitilauksen pakkausluettelo kirjataan.
- Jos **Sarjanumero**-kenttä valitaan, sarjanumerot synkronoidaan konsernin sisäisen ostotilauksen rivien varastotapahtumiin, kun konsernin sisäisen myyntitilauksen pakkausluettelo kirjataan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
