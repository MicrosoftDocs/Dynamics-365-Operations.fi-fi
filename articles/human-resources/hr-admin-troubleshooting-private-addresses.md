---
title: Yksityisten osoitteiden käyttöoikeudet käyttöoikeusroolin mukaan
description: Tässä artikkelissa kerrotaan, miten ratkaista ongelma, jossa asiakas ei voi käyttää yksityisiä osoitteita.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6598094e7877a30c35e1b03794f82c8a4ec001a7
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112345"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="d8e34-103">Yksityisten osoitteiden käyttöoikeudet käyttöoikeusroolin mukaan</span><span class="sxs-lookup"><span data-stu-id="d8e34-103">Access to private addresses by security role</span></span>

<span data-ttu-id="d8e34-104">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="d8e34-104">**Issue**</span></span>

<span data-ttu-id="d8e34-105">Kun asiakas tekee kaksoiskappaleen käyttöoikeusroolista ja kirjautuu tänä uutena roolia, asiakas ei näe yksityiseksi merkittyjä osoitteita.</span><span class="sxs-lookup"><span data-stu-id="d8e34-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="d8e34-106">**Tarkkuus**</span><span class="sxs-lookup"><span data-stu-id="d8e34-106">**Resolution**</span></span>

<span data-ttu-id="d8e34-107">Asiakas voi ratkaista ongelman noudattamalla käyttöoikeusroolin kaksoiskappaletta koskevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d8e34-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="d8e34-108">Valitse **Organisaation hallinto \> Yleinen osoitekirja \> Yleisen osoitekirjan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="d8e34-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="d8e34-109">Siirrä uusi käyttöoikeusrooli **Yksityisen sijainnin suojaus** -välilehdessä **Käytettävissä olevat roolit** -luettelosta **Valitut roolit** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="d8e34-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="d8e34-110">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d8e34-110">Select **Save**.</span></span>

![Yleisen osoitekirjan parametrit -sivu](media/GAD-parameters.png)
