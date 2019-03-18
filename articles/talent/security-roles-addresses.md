---
title: Yksityisten osoitteiden käyttöoikeudet käyttöoikeusroolin mukaan
description: Tässä ohjeaiheessa kerrotaan, miten ratkaista ongelma, jossa asiakas ei voi käyttää yksityisiä osoitteita.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304161"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="41421-103">Yksityisten osoitteiden käyttöoikeudet käyttöoikeusroolin mukaan</span><span class="sxs-lookup"><span data-stu-id="41421-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="41421-104">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="41421-104">**Issue**</span></span>

<span data-ttu-id="41421-105">Kun asiakas tekee kaksoiskappaleen käyttöoikeusroolista ja kirjautuu tänä uutena roolia, asiakas ei näe yksityiseksi merkittyjä osoitteita.</span><span class="sxs-lookup"><span data-stu-id="41421-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="41421-106">**Tarkkuus**</span><span class="sxs-lookup"><span data-stu-id="41421-106">**Resolution**</span></span>

<span data-ttu-id="41421-107">Asiakas voi ratkaista ongelman noudattamalla käyttöoikeusroolin kaksoiskappaletta koskevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="41421-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="41421-108">Valitse **Organisaation hallinto \> Yleinen osoitekirja \> Yleisen osoitekirjan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="41421-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="41421-109">Siirrä uusi käyttöoikeusrooli **Yksityisen sijainnin suojaus** -välilehdessä **Käytettävissä olevat roolit** -luettelosta **Valitut roolit** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="41421-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="41421-110">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="41421-110">Select **Save**.</span></span>

![Yleisen osoitekirjan parametrit -sivu](media/GAD-parameters.png)