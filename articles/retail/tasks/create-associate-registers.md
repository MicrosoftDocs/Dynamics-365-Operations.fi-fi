---
title: Luo ja liitä rekisterit
description: Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07e4b9f32a3a74b273272bd0b759d35c2a963e2e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "360644"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="3c03d-103">Luo ja liitä rekisterit</span><span class="sxs-lookup"><span data-stu-id="3c03d-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3c03d-104">Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan.</span><span class="sxs-lookup"><span data-stu-id="3c03d-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="3c03d-105">Menettely käyttää USRT-demotietoyritystä.</span><span class="sxs-lookup"><span data-stu-id="3c03d-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="3c03d-106">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavan asetukset > Myyntipisteen asetukset > Kassakoneet.</span><span class="sxs-lookup"><span data-stu-id="3c03d-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="3c03d-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3c03d-107">Click New.</span></span>
3. <span data-ttu-id="3c03d-108">Kirjoita Kassakoneen numero -kenttään uuden kassakoneen tunnus.</span><span class="sxs-lookup"><span data-stu-id="3c03d-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="3c03d-109">Kassakoneen tunnus sisältää yleensä koodeja, joiden avulla kassakone yhdistetään myymälään, johon se kuuluu sekä sijaintiin myymälässä.</span><span class="sxs-lookup"><span data-stu-id="3c03d-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="3c03d-110">Kirjoita Nimi-kenttään kassakonetta kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="3c03d-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="3c03d-111">Syötä tai valitse arvo Myymälän numero -kentässä.</span><span class="sxs-lookup"><span data-stu-id="3c03d-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="3c03d-112">Syötä tai valitse arvo Laiteprofiili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3c03d-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="3c03d-113">Laiteprofiileilla määritetään vähittäismyynnin oheislaitteet, jotka liitetään kassakoneeseen, kuten käteislokero ja kuittitulostin.</span><span class="sxs-lookup"><span data-stu-id="3c03d-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="3c03d-114">Anna tai valitse Visuaalinen profiili -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="3c03d-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="3c03d-115">Visuaalisten profiilien avulla määritetään kuvat, joita käytetään myyntipisteen taustalla ja kirjautumissivulla. Niillä määritetään myös myyntipisteen teema.</span><span class="sxs-lookup"><span data-stu-id="3c03d-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="3c03d-116">Kirjoita arvo EFT:n POS-kassakoneen numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3c03d-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="3c03d-117">EFT:n POS-kassakoneen numeroa käytetään ilmoittamaan maksun käsittelijälle, miltä maksupäätteeltä varmennuspyyntö on lähetetty.</span><span class="sxs-lookup"><span data-stu-id="3c03d-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="3c03d-118">Tätä arvoa kutsutaan usein nimellä "päätteen tunnus" tai "TID".</span><span class="sxs-lookup"><span data-stu-id="3c03d-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="3c03d-119">TID löytyy yleensä maksupäätteen tarrasta.</span><span class="sxs-lookup"><span data-stu-id="3c03d-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="3c03d-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3c03d-120">Click Save.</span></span>

