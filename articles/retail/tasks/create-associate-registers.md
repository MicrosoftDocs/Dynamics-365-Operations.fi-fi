--- 
title: "Luo ja liitä rekisterit"
description: "Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6a95019e50bcc060165dab3e6aa2b3ca8a897bf3
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="7bfad-103">Luo ja liitä rekisterit</span><span class="sxs-lookup"><span data-stu-id="7bfad-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7bfad-104">Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan.</span><span class="sxs-lookup"><span data-stu-id="7bfad-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="7bfad-105">Menettely käyttää USRT-demotietoyritystä.</span><span class="sxs-lookup"><span data-stu-id="7bfad-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="7bfad-106">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavan asetukset > Myyntipisteen asetukset > Kassakoneet.</span><span class="sxs-lookup"><span data-stu-id="7bfad-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="7bfad-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7bfad-107">Click New.</span></span>
3. <span data-ttu-id="7bfad-108">Kirjoita Kassakoneen numero -kenttään uuden kassakoneen tunnus.</span><span class="sxs-lookup"><span data-stu-id="7bfad-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="7bfad-109">Kassakoneen tunnus sisältää yleensä koodeja, joiden avulla kassakone yhdistetään myymälään, johon se kuuluu sekä sijaintiin myymälässä.</span><span class="sxs-lookup"><span data-stu-id="7bfad-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="7bfad-110">Kirjoita Nimi-kenttään kassakonetta kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="7bfad-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="7bfad-111">Syötä tai valitse arvo Myymälän numero -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7bfad-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="7bfad-112">Syötä tai valitse arvo Laiteprofiili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7bfad-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="7bfad-113">Laiteprofiileilla määritetään vähittäismyynnin oheislaitteet, jotka liitetään kassakoneeseen, kuten käteislokero ja kuittitulostin.</span><span class="sxs-lookup"><span data-stu-id="7bfad-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="7bfad-114">Anna tai valitse Visuaalinen profiili -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="7bfad-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="7bfad-115">Visuaalisten profiilien avulla määritetään kuvat, joita käytetään myyntipisteen taustalla ja kirjautumissivulla. Niillä määritetään myös myyntipisteen teema.</span><span class="sxs-lookup"><span data-stu-id="7bfad-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="7bfad-116">Kirjoita arvo EFT:n POS-kassakoneen numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7bfad-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="7bfad-117">EFT:n POS-kassakoneen numeroa käytetään ilmoittamaan maksun käsittelijälle, miltä maksupäätteeltä varmennuspyyntö on lähetetty.</span><span class="sxs-lookup"><span data-stu-id="7bfad-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="7bfad-118">Tätä arvoa kutsutaan usein nimellä "päätteen tunnus" tai "TID".</span><span class="sxs-lookup"><span data-stu-id="7bfad-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="7bfad-119">TID löytyy yleensä maksupäätteen tarrasta.</span><span class="sxs-lookup"><span data-stu-id="7bfad-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="7bfad-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7bfad-120">Click Save.</span></span>


