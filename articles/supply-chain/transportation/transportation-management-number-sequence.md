---
title: Kuljetustenhallinnan numerosarja
description: Tässä aiheessa käsitellään kuljetustenhallinnan numerosarjojen määrittämistä.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3da757cbf47e0e1af781b720d17a673e19aeb3b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807677"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="d584a-103">Kuljetustenhallinnan numerosarja</span><span class="sxs-lookup"><span data-stu-id="d584a-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d584a-104">Määritä erilaiset tuotenumerot kuljetustenhallintamoduulin **Numerosarjat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d584a-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="d584a-105">Rahdinkuljettajat käyttävät tuotenumeroita kunkin lähetyksen organisointiin ja seurantaan.</span><span class="sxs-lookup"><span data-stu-id="d584a-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="d584a-106">Valmistenumeron numerosarjan luominen</span><span class="sxs-lookup"><span data-stu-id="d584a-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="d584a-107">Valmistenumeron numerosarja luodaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d584a-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="d584a-108">Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Numerosarjat**.</span><span class="sxs-lookup"><span data-stu-id="d584a-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="d584a-109">Luo uusi numerosarja valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d584a-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="d584a-110">Anna numerosarjalle yksilöivä tunnus ja kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="d584a-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="d584a-111">**Numerosarjan tyyppi** -kentän ainoa vaihtoehto on *Tuotenumero*.</span><span class="sxs-lookup"><span data-stu-id="d584a-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="d584a-112">**Tarkistusnumero**-kentän ainoa vaihtoehto on *Tarkistusnumero*, ja se on määritetty yleisenä laskentana.</span><span class="sxs-lookup"><span data-stu-id="d584a-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="d584a-113">Anna järjestyksen tiedot **Järjestys**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d584a-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="d584a-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d584a-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="d584a-115">Numerosarjan linkittäminen lähetyksen rahdinkuljettajaan</span><span class="sxs-lookup"><span data-stu-id="d584a-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="d584a-116">Numerosarja linkitetään rahdinkuljettajaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d584a-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="d584a-117">Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Lähetyksen rahdinkuljettajat**.</span><span class="sxs-lookup"><span data-stu-id="d584a-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="d584a-118">Valitse lähetyksen rahdinkuljettaja.</span><span class="sxs-lookup"><span data-stu-id="d584a-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="d584a-119">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="d584a-119">Select **Edit**.</span></span>
1. <span data-ttu-id="d584a-120">Valitse **Yleiskatsaus**-pikavälilehdessä **Tuotenumerosarja**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="d584a-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="d584a-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d584a-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]