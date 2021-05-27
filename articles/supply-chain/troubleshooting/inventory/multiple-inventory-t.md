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
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="dbea2-103">Eränumeroiden useat varastotapahtumat, kun Fyysisen päivityksen yhteydessä on poistettu käytöstä</span><span class="sxs-lookup"><span data-stu-id="dbea2-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="dbea2-104">Tietopankin numero: 4613390</span><span class="sxs-lookup"><span data-stu-id="dbea2-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="dbea2-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="dbea2-105">Symptoms</span></span>

<span data-ttu-id="dbea2-106">Useita varastotapahtumia luodaan sen jälkeen, kun olet oikaissut ostotilausrivin nimikkeille, joilla eränumeroryhmän **Fyysisen päivityksen yhteydessä** -vaihtoehdon arvoksi on määritetty *Ei*.</span><span class="sxs-lookup"><span data-stu-id="dbea2-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="dbea2-107">Kun luot nimikkeen, jossa eränumeroryhmän **Fyysisen päivityksen yhteydessä** -asetuksena on *Ei*, järjestelmä luo automaattisesti uuden eränumeron, jos muokkaat ostorivin määrää ja tallennat ostotilaussivun.</span><span class="sxs-lookup"><span data-stu-id="dbea2-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="dbea2-108">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="dbea2-108">Resolution</span></span>

<span data-ttu-id="dbea2-109">Eränumeroryhmien **Fyysisen päivityksen yhteydessä** -asetus toimii seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="dbea2-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="dbea2-110">Kun asetus on *Kyllä*, uudet eränumerot luodaan vasta fyysisen päivityksen jälkeen (esimerkiksi silloin, kun nimikkeet lähetetään tai vastaanotetaan).</span><span class="sxs-lookup"><span data-stu-id="dbea2-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="dbea2-111">Kun asetuksena on *Ei*, uusi eränumero luodaan aina, kun sovellettava päivitys tapahtuu (esimerkiksi kun ostotilaukseen lisätään uusi määrä).</span><span class="sxs-lookup"><span data-stu-id="dbea2-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
