---
title: Konsernin sisäiset erä- ja sarjanumerot
description: Tässä artikkelissa käsitellään konsernin sisäisten tilausten erä- ja sarjanumeroiden rekisteröimistä
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
ms.openlocfilehash: 5c743c8eee8d27a2c2357523a11236eb247ec5be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851504"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Konsernin sisäiset erä- ja sarjanumerot

[!include [banner](../../includes/banner.md)]

Yritysten, jotka seuraavat nimikkeitä sarja- tai eränumeroiden avulla, on seurattava myös poimittujen nimikkeiden sarja- ja eränumeroita. Konsernin sisäinen toiminto vie tai tuo automaattisesti sarja- ja eränumerot yrityksestä toiseen. Kun rekisteröit konsernin sisäisen myyntitilauksen nimikkeiden sarja- ja eränumerot, voit määrittää ohjelman viemään nämä numerot automaattisesti konsernin sisäiseen ostotilaukseen ja alkuperäiseen myyntitilaukseen. Soveltuvat parametrit määritetään myyntitilauksen **Konsernin sisäinen** -sivulla:

- Jos **Eränumero**-kenttä valitaan **Myyntitilauskäytännöt**-sivulla, eränumero synkronoidaan konsernin sisäisen ostotilauksen rivien varastotapahtumiin, kun konsernin sisäisen myyntitilauksen pakkausluettelo kirjataan.
- Jos **Sarjanumero**-kenttä valitaan, sarjanumerot synkronoidaan konsernin sisäisen ostotilauksen rivien varastotapahtumiin, kun konsernin sisäisen myyntitilauksen pakkausluettelo kirjataan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
