--- 
title: "Määritä taloushallinnon dimensiot"
description: "Tässä tehtäväopastuksessa selvitetään yksikön tukeman taloushallinnon dimension ja mukautetun taloushallinnon dimension lisääminen."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 20a7781486c6e0612c27af02a1bccbc48c55a932
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="define-financial-dimensions"></a><span data-ttu-id="3636c-103">Määritä taloushallinnon dimensiot</span><span class="sxs-lookup"><span data-stu-id="3636c-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3636c-104">Tässä tehtäväopastuksessa selvitetään yksikön tukeman taloushallinnon dimension ja mukautetun taloushallinnon dimension lisääminen.</span><span class="sxs-lookup"><span data-stu-id="3636c-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="3636c-105">Opastuksessa käytetään USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="3636c-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="3636c-106">Luo yksikön tukema taloushallinnon dimensio</span><span class="sxs-lookup"><span data-stu-id="3636c-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="3636c-107">Valitse Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="3636c-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="3636c-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3636c-108">Click New.</span></span>
3. <span data-ttu-id="3636c-109">Valitse Käytä arvoja -kentässä järjestelmän määrittämä yksikkö, johon taloushallinnon dimensio perustuu.</span><span class="sxs-lookup"><span data-stu-id="3636c-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="3636c-110">Kirjoita Dimension nimi -kenttään taloushallinnon dimensiota kuvaava arvo.</span><span class="sxs-lookup"><span data-stu-id="3636c-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="3636c-111">Nimi voi olla jokin muu kuin järjestelmän määrittämä yksikkö, mutta siinä ei saa olla välilyöntejä eikä erikoismerkkejä.</span><span class="sxs-lookup"><span data-stu-id="3636c-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="3636c-112">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="3636c-112">Click Activate.</span></span>
    * <span data-ttu-id="3636c-113">Taloushallinnon dimension aktivointi päivittää taulun taloushallinnon dimension nimellä ja poistaa poistetut dimensiot.</span><span class="sxs-lookup"><span data-stu-id="3636c-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="3636c-114">Voit antaa dimensioarvot ennen aktivoit taloushallinnon dimension aktivointia, mutta taloushallinnon dimensiota ei voi käyttää, ennen kuin se on aktivoitu.</span><span class="sxs-lookup"><span data-stu-id="3636c-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="3636c-115">Valitse aktivointisanoman sulkeminen.</span><span class="sxs-lookup"><span data-stu-id="3636c-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="3636c-116">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="3636c-116">Click Activate.</span></span>
    * <span data-ttu-id="3636c-117">Dimension aktivointi voidaan ajoittaa suoritettavaksi erätyönä tiettynä päivämääränä ja kellonaikana.</span><span class="sxs-lookup"><span data-stu-id="3636c-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="3636c-118">Valitse Dimensioarvot.</span><span class="sxs-lookup"><span data-stu-id="3636c-118">Click Dimension values.</span></span>
    * <span data-ttu-id="3636c-119">Jotkin dimensioarvot ovat yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="3636c-119">Some dimension values are company specific.</span></span> <span data-ttu-id="3636c-120">Voit tarkistaa, ovatko ne yrityskohtaisia sen perusteella, näkyykö yrityksen nimi dimensioarvoluettelossa.</span><span class="sxs-lookup"><span data-stu-id="3636c-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="3636c-121">Luo mukautettu taloushallinnon dimensio</span><span class="sxs-lookup"><span data-stu-id="3636c-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="3636c-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3636c-122">Close the page.</span></span>
2. <span data-ttu-id="3636c-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3636c-123">Click New.</span></span>
3. <span data-ttu-id="3636c-124">Valitse Käytä arvoja kohteesta -kentässä <Custom dimension>.</span><span class="sxs-lookup"><span data-stu-id="3636c-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="3636c-125">Kirjoita Dimension nimi -kenttään taloushallinnon dimensiota kuvaava arvo.</span><span class="sxs-lookup"><span data-stu-id="3636c-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="3636c-126">Nimi ei voi sisältää välilyöntejä eikä erikoismerkkejä.</span><span class="sxs-lookup"><span data-stu-id="3636c-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="3636c-127">Voit määrittää myös tilipeitteen rajoittamaan dimensioarvoille annettavaa summaa ja tietojen tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="3636c-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="3636c-128">Voit syöttää merkkejä, jotka pysyvät samana jokaisessa dimensioarvossa, kuten kirjaimia tai yhdysviivan.</span><span class="sxs-lookup"><span data-stu-id="3636c-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="3636c-129">Voit myös syöttää numeromerkkejä (#) ja et-merkkejä (&) paikkamerkkeinä kirjaimille ja numeroille, jotka muuttuvat aina, kun dimensioarvo luodaan.</span><span class="sxs-lookup"><span data-stu-id="3636c-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="3636c-130">Käytä numeromerkkiä (#) numeron paikkamerkkinä ja et-merkkiä (&) kirjaimen paikkamerkkinä.</span><span class="sxs-lookup"><span data-stu-id="3636c-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="3636c-131">Esimerkki: jos haluat rajoittaa dimensioarvon kirjaimiin CC ja kolmeen numeroon, anna muotoilupeitteeksi CC-###.</span><span class="sxs-lookup"><span data-stu-id="3636c-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="3636c-132">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="3636c-132">Click Activate.</span></span>
    * <span data-ttu-id="3636c-133">Taloushallinnon dimension aktivointi päivittää taulun taloushallinnon dimension nimellä ja poistaa poistetut dimensiot.</span><span class="sxs-lookup"><span data-stu-id="3636c-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="3636c-134">Voit antaa dimensioarvot ennen aktivoit taloushallinnon dimension aktivointia, mutta taloushallinnon dimensiota ei voi käyttää, ennen kuin se on aktivoitu.</span><span class="sxs-lookup"><span data-stu-id="3636c-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="3636c-135">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="3636c-135">Click Activate.</span></span>
    * <span data-ttu-id="3636c-136">Dimension aktivointi voidaan ajoittaa suoritettavaksi erätyönä tiettynä päivämääränä ja kellonaikana.</span><span class="sxs-lookup"><span data-stu-id="3636c-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="3636c-137">Valitse Dimensioarvot.</span><span class="sxs-lookup"><span data-stu-id="3636c-137">Click Dimension values.</span></span>
8. <span data-ttu-id="3636c-138">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3636c-138">Click New.</span></span>
9. <span data-ttu-id="3636c-139">Kirjoita Dimension arvo -kenttään taloushallinnon dimension arvoa kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="3636c-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="3636c-140">Kirjoita Kuvaus-kenttään taloushallinnon dimension arvon kuvaus.</span><span class="sxs-lookup"><span data-stu-id="3636c-140">In the Description field, type a description that describes your financial dimension value.</span></span>


