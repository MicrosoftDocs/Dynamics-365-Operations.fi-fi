---
title: Käyttäjän työn peruuttaminen ei onnistu
description: Käyttäjän työn peruuttaminen ei onnistu
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924398"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="1a54e-103">Käyttäjän työn peruuttaminen ei onnistu</span><span class="sxs-lookup"><span data-stu-id="1a54e-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="1a54e-104">Virhekoodi: WAX708</span><span class="sxs-lookup"><span data-stu-id="1a54e-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="1a54e-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="1a54e-105">Symptoms</span></span>

<span data-ttu-id="1a54e-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="1a54e-106">The system shows the following error message:</span></span>

> <span data-ttu-id="1a54e-107">Et voi peruuttaa työtä, joka on käyttäjällä.</span><span class="sxs-lookup"><span data-stu-id="1a54e-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="1a54e-108">Syy</span><span class="sxs-lookup"><span data-stu-id="1a54e-108">Cause</span></span>

<span data-ttu-id="1a54e-109">Työ on käyttäjän lukitsema eikä sitä voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="1a54e-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="1a54e-110">Voit vahvistaa tämän avaamalla työtunnuksen ja avaamalla sitten **Yleiset**-välilehden. Jos työ on lukittu, **Työn tila** -kentän arvoksi määritetään *Käsittelyssä* ja **Lukitsija**-kenttään määritetään käyttäjätunnus.</span><span class="sxs-lookup"><span data-stu-id="1a54e-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="1a54e-111">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="1a54e-111">Resolution</span></span>

<span data-ttu-id="1a54e-112">Voit peruuttaa työn seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1a54e-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="1a54e-113">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Tyhjennä \> Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="1a54e-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="1a54e-114">Määritä **Työtunnus**-kenttään peruutettavan työn tunnus.</span><span class="sxs-lookup"><span data-stu-id="1a54e-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="1a54e-115">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a54e-115">Select **OK**.</span></span>
1. <span data-ttu-id="1a54e-116">Vahvista, että haluat peruuttaa työn valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="1a54e-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="1a54e-117">Lisätietoja on kohdassa [Varastotyön peruuttaminen poikkeuksen käsittelyä varten](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="1a54e-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
