---
title: Et voi tuoda nimikettä käyttämällä Vapautetut tuotteet V2 -yksikköä
description: Et voi tuoda nimikettä käyttämällä Vapautetut tuotteet V2 -yksikköä.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026465"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="8e3a7-103">Et voi tuoda nimikettä käyttämällä Vapautetut tuotteet V2 -yksikköä</span><span class="sxs-lookup"><span data-stu-id="8e3a7-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="8e3a7-104">Tietopankin numero: 4611825</span><span class="sxs-lookup"><span data-stu-id="8e3a7-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="8e3a7-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="8e3a7-105">Symptoms</span></span>

<span data-ttu-id="8e3a7-106">Kun yrität tuoda nimikkeen käyttämällä *Vapautetut tuotteet V2* -yksikköä, näkyviin tulee seuraavaa esimerkkiä muistuttava virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="8e3a7-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="8e3a7-107">Tietuetta ei voi luoda Nimikkeet - seurantadimensioryhmät (EcoResTrackingDimensionGroupItem) -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="8e3a7-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="8e3a7-108">Nimikkeen numero: 2040663, erä.</span><span class="sxs-lookup"><span data-stu-id="8e3a7-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="8e3a7-109">Tietue on jo olemassa.</span><span class="sxs-lookup"><span data-stu-id="8e3a7-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="8e3a7-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8e3a7-110">Resolution</span></span>

<span data-ttu-id="8e3a7-111">Jotta voit tuoda uusia vapautettuja tuotteita, sinun on käytettävä *Vapautetun tuotteen luominen V2* -yksikköä *Vapautetut tuotteet V2* -yksikön asemesta.</span><span class="sxs-lookup"><span data-stu-id="8e3a7-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
