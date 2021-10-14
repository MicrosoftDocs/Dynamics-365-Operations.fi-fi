---
title: Konsernin sisäiset erä- ja sarjanumerot
description: Tässä aiheessa käsitellään konsernin sisäisten tilausten erä- ja sarjanumeroiden rekisteröimistä
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
ms.openlocfilehash: 4da936263bb57c24eeb7021ac61b3945bb2777fb
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548251"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Konsernin sisäiset erä- ja sarjanumerot

[!include [banner](../../includes/banner.md)]

Yritysten, jotka seuraavat nimikkeitä sarja- tai eränumeroiden avulla, on seurattava myös poimittujen nimikkeiden sarja- ja eränumeroita. Konsernin sisäinen toiminto vie tai tuo automaattisesti sarja- ja eränumerot yrityksestä toiseen. Kun rekisteröit konsernin sisäisen myyntitilauksen nimikkeiden sarja- ja eränumerot, voit määrittää ohjelman viemään nämä numerot automaattisesti konsernin sisäiseen ostotilaukseen ja alkuperäiseen myyntitilaukseen. Soveltuvat parametrit määritetään myyntitilauksen **Konsernin sisäinen** -sivulla:

- Jos **Eränumero**-kenttä valitaan **Myyntitilauskäytännöt**-sivulla, eränumero synkronoidaan konsernin sisäisen ostotilauksen rivien varastotapahtumiin, kun konsernin sisäisen myyntitilauksen pakkausluettelo kirjataan.
- Jos **Sarjanumero**-kenttä valitaan, sarjanumerot synkronoidaan konsernin sisäisen ostotilauksen rivien varastotapahtumiin, kun konsernin sisäisen myyntitilauksen pakkausluettelo kirjataan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
