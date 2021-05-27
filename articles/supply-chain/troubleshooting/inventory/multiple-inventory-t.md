---
title: Eränumeroiden useat varastotapahtumat, kun Fyysisen päivityksen yhteydessä on poistettu käytöstä
description: Useita varastotapahtumia luodaan sen jälkeen, kun olet oikaissut ostotilausrivin nimikkeille, joilla eränumeroryhmän Fyysisen päivityksen yhteydessä -vaihtoehdon arvoksi on määritetty Ei.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026487"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Eränumeroiden useat varastotapahtumat, kun Fyysisen päivityksen yhteydessä on poistettu käytöstä

Tietopankin numero: 4613390

## <a name="symptoms"></a>Oireet

Useita varastotapahtumia luodaan sen jälkeen, kun olet oikaissut ostotilausrivin nimikkeille, joilla eränumeroryhmän **Fyysisen päivityksen yhteydessä** -vaihtoehdon arvoksi on määritetty *Ei*.

Kun luot nimikkeen, jossa eränumeroryhmän **Fyysisen päivityksen yhteydessä** -asetuksena on *Ei*, järjestelmä luo automaattisesti uuden eränumeron, jos muokkaat ostorivin määrää ja tallennat ostotilaussivun.

## <a name="resolution"></a>Ratkaisu

Eränumeroryhmien **Fyysisen päivityksen yhteydessä** -asetus toimii seuraavasti:

- Kun asetus on *Kyllä*, uudet eränumerot luodaan vasta fyysisen päivityksen jälkeen (esimerkiksi silloin, kun nimikkeet lähetetään tai vastaanotetaan).
- Kun asetuksena on *Ei*, uusi eränumero luodaan aina, kun sovellettava päivitys tapahtuu (esimerkiksi kun ostotilaukseen lisätään uusi määrä).
