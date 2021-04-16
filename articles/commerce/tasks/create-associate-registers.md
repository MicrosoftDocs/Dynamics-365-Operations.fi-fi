---
title: Luo ja liitä rekisterit
description: Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan.
author: rubencdelgado
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba978a3d895394760687386197dbb3512c62ef98
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798558"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="cb281-103">Luo ja liitä rekisterit</span><span class="sxs-lookup"><span data-stu-id="cb281-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb281-104">Tässä menettelyssä esitellään, miten myyntipisteen (POS) kassakone luodaan.</span><span class="sxs-lookup"><span data-stu-id="cb281-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="cb281-105">Menettely käyttää USRT-demotietoyritystä.</span><span class="sxs-lookup"><span data-stu-id="cb281-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="cb281-106">Siirry kohtaan Retail ja Commerce > Kanavan asetukset > Myyntipisteen asetukset > Kassakoneet.</span><span class="sxs-lookup"><span data-stu-id="cb281-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="cb281-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="cb281-107">Click New.</span></span>
3. <span data-ttu-id="cb281-108">Kirjoita Kassakoneen numero -kenttään uuden kassakoneen tunnus.</span><span class="sxs-lookup"><span data-stu-id="cb281-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="cb281-109">Kassakoneen tunnus sisältää yleensä koodeja, joiden avulla kassakone yhdistetään myymälään, johon se kuuluu sekä sijaintiin myymälässä.</span><span class="sxs-lookup"><span data-stu-id="cb281-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="cb281-110">Kirjoita Nimi-kenttään kassakonetta kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="cb281-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="cb281-111">Syötä tai valitse arvo Myymälän numero -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cb281-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="cb281-112">Syötä tai valitse arvo Laiteprofiili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="cb281-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="cb281-113">Laiteprofiileilla määritetään oheislaitteet, jotka liitetään kassakoneeseen, kuten käteislokero ja kuittitulostin.</span><span class="sxs-lookup"><span data-stu-id="cb281-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="cb281-114">Anna tai valitse Visuaalinen profiili -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="cb281-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="cb281-115">Visuaalisten profiilien avulla määritetään kuvat, joita käytetään myyntipisteen taustalla ja kirjautumissivulla. Niillä määritetään myös myyntipisteen teema.</span><span class="sxs-lookup"><span data-stu-id="cb281-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="cb281-116">Kirjoita arvo EFT:n POS-kassakoneen numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="cb281-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="cb281-117">EFT:n POS-kassakoneen numeroa käytetään ilmoittamaan maksun käsittelijälle, miltä maksupäätteeltä varmennuspyyntö on lähetetty.</span><span class="sxs-lookup"><span data-stu-id="cb281-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="cb281-118">Tätä arvoa kutsutaan usein nimellä "päätteen tunnus" tai "TID".</span><span class="sxs-lookup"><span data-stu-id="cb281-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="cb281-119">TID löytyy yleensä maksupäätteen tarrasta.</span><span class="sxs-lookup"><span data-stu-id="cb281-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="cb281-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="cb281-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]