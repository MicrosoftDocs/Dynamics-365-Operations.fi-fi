---
title: Yksityisten osoitteiden käyttöoikeudet käyttöoikeusroolin mukaan
description: Tässä ohjeaiheessa kerrotaan, miten ratkaista ongelma, jossa asiakas ei voi käyttää yksityisiä osoitteita.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517892"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="f9242-103">Yksityisten osoitteiden käyttöoikeudet käyttöoikeusroolin mukaan</span><span class="sxs-lookup"><span data-stu-id="f9242-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f9242-104">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="f9242-104">**Issue**</span></span>

<span data-ttu-id="f9242-105">Kun asiakas tekee kaksoiskappaleen käyttöoikeusroolista ja kirjautuu tänä uutena roolia, asiakas ei näe yksityiseksi merkittyjä osoitteita.</span><span class="sxs-lookup"><span data-stu-id="f9242-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="f9242-106">**Tarkkuus**</span><span class="sxs-lookup"><span data-stu-id="f9242-106">**Resolution**</span></span>

<span data-ttu-id="f9242-107">Asiakas voi ratkaista ongelman noudattamalla käyttöoikeusroolin kaksoiskappaletta koskevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f9242-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="f9242-108">Valitse **Organisaation hallinto \> Yleinen osoitekirja \> Yleisen osoitekirjan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f9242-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="f9242-109">Siirrä uusi käyttöoikeusrooli **Yksityisen sijainnin suojaus** -välilehdessä **Käytettävissä olevat roolit** -luettelosta **Valitut roolit** -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="f9242-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="f9242-110">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f9242-110">Select **Save**.</span></span>

![Yleisen osoitekirjan parametrit -sivu](media/GAD-parameters.png)
