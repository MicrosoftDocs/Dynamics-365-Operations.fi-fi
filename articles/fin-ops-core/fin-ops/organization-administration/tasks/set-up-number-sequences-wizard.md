---
title: Numerosarjojen määrittäminen ohjatulla toiminnolla
description: Tässä aiheessa selvitetään, miten kaikki pakolliset numerosarjat voidaan määrittää samanaikaisesti ohjatulla toiminnolla.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76dc32f2254ffd2a2e33eef594d6e602092bcb6f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140492"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="d403d-103">Numerosarjojen määrittäminen ohjatulla toiminnolla</span><span class="sxs-lookup"><span data-stu-id="d403d-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d403d-104">Numerosarjoja käytetään muodostamaan päätietotietueille ja niitä tarvitsevilla tapahtumatietueille luettavia, yksilöllisiä tunnisteita.</span><span class="sxs-lookup"><span data-stu-id="d403d-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="d403d-105">Tunnisteen vaativaa päätietoa tai tapahtumatietuetta kutsutaan numellä viite.</span><span class="sxs-lookup"><span data-stu-id="d403d-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="d403d-106">Ennen kuin voit luoda viitteelle uusia tietueita, määritä numerosarja ja kohdista se viitteeseen.</span><span class="sxs-lookup"><span data-stu-id="d403d-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="d403d-107">Tässä aiheessa selvitetään, miten kaikki pakolliset numerosarjat voidaan määrittää samanaikaisesti ohjatulla toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="d403d-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="d403d-108">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="d403d-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d403d-109">Siirry kohtaan **Siirtymisruutu > Moduulit > Organisaation hallinta > Numerosarjat > Numerosarjat**.</span><span class="sxs-lookup"><span data-stu-id="d403d-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="d403d-110">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="d403d-110">Select **Generate**.</span></span>
3. <span data-ttu-id="d403d-111">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="d403d-111">Select **Next**.</span></span>

   - <span data-ttu-id="d403d-112">Tällä sivulla voit muokata tunnuskoodia, pienintä arvoa ja suurinta arvoa.</span><span class="sxs-lookup"><span data-stu-id="d403d-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="d403d-113">Lisäksi voit määrittää, onko numerosarjan oltava jatkuva.</span><span class="sxs-lookup"><span data-stu-id="d403d-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="d403d-114">Älä valitse **Jatkuva**-vaihtoehtoa, jos numerosarjan numerot on esijaettava.</span><span class="sxs-lookup"><span data-stu-id="d403d-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="d403d-115">Lisää vaikutusaluesegmentti numerosarjan muotoon valitsemalla luettelosta muoto ja valitsemalla sitten **Sisällytä vaikutusalue muotoon**.</span><span class="sxs-lookup"><span data-stu-id="d403d-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="d403d-116">Poista vaikutusaluesegmentti numerosarjan muodosta valitsemalla muoto luettelosta ja valitsemalla sitten **Poista vaikutusalue muodosta**.</span><span class="sxs-lookup"><span data-stu-id="d403d-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="d403d-117">Sulje numerosarja pois automaattisesta luonnista valitsemalla numerosarja luettelosta ja valitsemalla sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="d403d-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="d403d-118">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="d403d-118">Select **Next**.</span></span>
5. <span data-ttu-id="d403d-119">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="d403d-119">Select **Finish**.</span></span>

