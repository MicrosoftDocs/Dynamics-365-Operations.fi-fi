---
title: Projektibudjettien ennustemallien luominen
description: Tässä aiheessa kuvataan, miten jäljellä oleville budjeteille luodaan ennustemalli.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321776"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="10500-103">Projektibudjettien ennustemallien luominen</span><span class="sxs-lookup"><span data-stu-id="10500-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10500-104">Tässä aiheessa kuvataan, miten jäljellä oleville budjeteille luodaan ennustemalli.</span><span class="sxs-lookup"><span data-stu-id="10500-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="10500-105">Budjetin hallinnan alainen projekti käyttää kahta budjettia: alkuperäistä ja jäljellä olevaa.</span><span class="sxs-lookup"><span data-stu-id="10500-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="10500-106">Kun luot projektibudjetin, sinun on määritettävä alkuperäisen ja jäljellä olevan budjetin ennustemallit, jotka luotiin   **Ennustemallit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="10500-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="10500-107">Tiettyihin malleihin perustuvat projektibudjetit luodaan, kun toteutat projektibudjetin.</span><span class="sxs-lookup"><span data-stu-id="10500-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="10500-108">Budjetin hallinnassa käytettävällä ennustemallilla ei voi olla osamallia eikä sitä voi käyttää osamallina.</span><span class="sxs-lookup"><span data-stu-id="10500-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="10500-109">Valitse kohta **Projektinhallinta- ja kirjanpito** > **Määritys** > **Ennusteet**  > **Ennustemallit**.</span><span class="sxs-lookup"><span data-stu-id="10500-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="10500-110">Valitse **Uusi** luodaksesi uuden ennustemallin ja kirjoita sitten uuden mallin tunnusnumero ja nimi.</span><span class="sxs-lookup"><span data-stu-id="10500-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="10500-111">Voit estää ennustemallin ennusterivien muuttamisen määrittämällä **Pysäytetty** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="10500-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="10500-112">Jos malliin liitettyjen ennusterivien tulisi luoda kassavirtaennusteita kirjanpidossa, aseta **Sisällytä kassavirtaennusteisiin** -valinnan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="10500-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="10500-113">Jos haluat käyttää projektin päivää laskun päivämääränä, määritä **Ennustepäivämäärä**-valinnan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="10500-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="10500-114">Valitse  **Budjettityyppi**-kenttään jokin seuraavista mallityypeistä:</span><span class="sxs-lookup"><span data-stu-id="10500-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="10500-115">**Alkuperäinen budjetti**: Käytä alkuperäisiä budjettisummia, jotka on toteutettu, kun alkuperäinen budjetti on luotu ja hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="10500-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="10500-116">**Jäljellä oleva budjetti**: Käytä jäljellä olevia budjettisummia projektin elinkaaren aikana.</span><span class="sxs-lookup"><span data-stu-id="10500-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="10500-117">Tämän ennustemallin saldoja vähennetään todellisilla tapahtumilla ja kasvatetaan tai vähennetään budjetin versioilla.</span><span class="sxs-lookup"><span data-stu-id="10500-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="10500-118">**Tehtävä siirtokirjaus**: Käytä tehtävää siirtokirjausta projektin budjettisummien kirjausten siirtämiseen.</span><span class="sxs-lookup"><span data-stu-id="10500-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="10500-119">Kirjausten siirtäminen on valinnainen prosessi, joka voidaan suorittaa käyttämättömien budjettisummien siirtämiseksi tilikaudelta toiselle.</span><span class="sxs-lookup"><span data-stu-id="10500-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="10500-120">Määritä seuraavat asetukset tarvittaessa:</span><span class="sxs-lookup"><span data-stu-id="10500-120">Set the following options as required:</span></span>

   - <span data-ttu-id="10500-121">Ota käyttöön **Ennustepäivämäärä** käyttääksesi projektin päivää laskun päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="10500-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="10500-122">Ota käyttöön **Ennuste, jossa KET** ennustaaksesi keskeneräisten töiden (KET) perusteella, ja valitse sitten KET-tyyppi.</span><span class="sxs-lookup"><span data-stu-id="10500-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="10500-123">Voit säilyttää oletuksena olevan **budjettityypin** muodossa **Ei mitään** tai määrittää uuden tyypin.</span><span class="sxs-lookup"><span data-stu-id="10500-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="10500-124">Budjettityyppiä ei voi muuttaa, kun tietuetta on muutettu.</span><span class="sxs-lookup"><span data-stu-id="10500-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="10500-125">Jos muutat oletusbudjettityyppiä, kaikki muut asetukset eivät ole käytettävissä päivityksissä, eikä tätä ennustemallia voi käyttää uudelleen.</span><span class="sxs-lookup"><span data-stu-id="10500-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

