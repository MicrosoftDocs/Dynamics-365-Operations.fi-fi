---
title: Aiheutuneen kustannuksen Hankkiminen ja hankinta -parametrit
description: Tässä aiheessa kuvataan, miten määritetään tarvittavat Hankkiminen- ja hankintaparametrit, kun käytät Aiheutunut kustannus -moduulia.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833926"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="95324-103">Aiheutuneen kustannuksen Hankkiminen ja hankinta -parametrit</span><span class="sxs-lookup"><span data-stu-id="95324-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95324-104">**Hankkiminen ja hankinta -parametrien** sivulla on muutamia asetuksia, jotka ovat erityisen tärkeitä käytettäessä **Aiheutunut kustannus** -moduulia.</span><span class="sxs-lookup"><span data-stu-id="95324-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="95324-105">**Hankkiminen ja hankinta -parametrit** -sivulla avatun **Päivitä tilausrivit** -valintaikkunan avulla voit määrittää, päivitetäänkö ostotilausrivit automaattisesti, kun ostotilauksen otsikkoon tehdään muutoksia.</span><span class="sxs-lookup"><span data-stu-id="95324-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="95324-106">Viimeiste määritys noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="95324-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="95324-107">Siirry kohtaan **Hankkiminen ja hankinta \> Asetukset \> Hankkiminen ja hankinta -parametrit**.</span><span class="sxs-lookup"><span data-stu-id="95324-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="95324-108">Valitse **Yleiset**-välilehdestä **Päivitä tilausrivit** -linkki.</span><span class="sxs-lookup"><span data-stu-id="95324-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="95324-109">**Päivitä tilausrivit** -valintaikkunassa näkyvät tilausotsikon kentät, jotka voivat myös päivittää tilausrivien kenttiä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="95324-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="95324-110">Määritä luettelon kullekin kentälle jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="95324-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="95324-111">**Aina** – Tilausrivien pitäisi päivittyä automaattisesti, kun tilauksen otsikkotiedot päivitetään.</span><span class="sxs-lookup"><span data-stu-id="95324-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="95324-112">**Ei koskaan** – Tilausrivien ei pitäisi päivittyä koskaan, kun tilauksen otsikkotiedot päivitetään.</span><span class="sxs-lookup"><span data-stu-id="95324-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="95324-113">**Kehote** – Käyttäjää pyydetään valitsemaan, päivitetäänkö tilausrivit.</span><span class="sxs-lookup"><span data-stu-id="95324-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
