---
title: Päivitä ylläpitobudjetit
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitobudjetti päivitetään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f3b771319eeb602a371500fdc69c68f88afe341
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571734"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="ff484-103">Päivitä ylläpitobudjetit</span><span class="sxs-lookup"><span data-stu-id="ff484-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ff484-104">**Ylläpitobudjetin rivit** -sivulla näkyvät kaikki budjettirivit, jotka on luotu **Ylläpitobudjetit**-sivulla valitulle budjetille.</span><span class="sxs-lookup"><span data-stu-id="ff484-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="ff484-105">(Lisätietoja on kohdassa [Luo ylläpitobudjetit](create-maintenance-budget.md)luominen.) Voit laskea uudelleen ja oikaista kunnossapitobudjetin rivejä, kunnes ylläpitobudjetti on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="ff484-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="ff484-106">Kun budjettikausi on kulunut ja kustannukset on kirjattu käyttöomaisuuden hallinnassa, voit myös päivittää todelliset kustannukset budjettiriveille.</span><span class="sxs-lookup"><span data-stu-id="ff484-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="ff484-107">Laske ylläpitobudjetti uudelleen</span><span class="sxs-lookup"><span data-stu-id="ff484-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="ff484-108">Kunnossapitobudjetin voi laskea uudelleen **Ylläpitobudjetin rivit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ff484-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="ff484-109">Kun huoltobudjetti lasketaan uudelleen, olemassa olevat budjettirivit poistetaan ja uusi laskenta tehdään.</span><span class="sxs-lookup"><span data-stu-id="ff484-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="ff484-110">Valitse **Ylläpitobudjetin rivit** -sivulla **Laske uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="ff484-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="ff484-111">Tee uuden laskennan edellyttämät muutokset **Laske budjetti uudelleen** -valintaikkunassa ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff484-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="ff484-112">Uudet budjettirivit luodaan määrittämiesi arvojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="ff484-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="ff484-113">Budjettirivien oikaisu</span><span class="sxs-lookup"><span data-stu-id="ff484-113">Adjust budget lines</span></span>

<span data-ttu-id="ff484-114">Koko kunnossapitobudjetin uudelleenlaskemisen asemesta voit oikaista valittuja budjettikustannuksiin liittyviä rivejä.</span><span class="sxs-lookup"><span data-stu-id="ff484-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="ff484-115">Valitse **Ylläpitobudjetin rivit** -sivulla rivit, joille haluat päivittää budjetin kustannukset.</span><span class="sxs-lookup"><span data-stu-id="ff484-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="ff484-116">Valitse **Oikaise**.</span><span class="sxs-lookup"><span data-stu-id="ff484-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="ff484-117">Jos haluat lisätä summan valittuihin riveihin, valitse **Lisää kustannus** -valintaruutu ja kirjoita sitten arvo **Lisää arvo** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ff484-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="ff484-118">Jos haluat kertoa valittujen budjettirivien budjetoidut kustannukset kertoimella, valitse **Kerro kustannukset** -valintaruutu ja kirjoita kerroin **Kertoimen arvo** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ff484-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="ff484-119">Jos esimerkiksi kirjoitat **1,2**-arvon **Kertoimen arvo** -kenttään, korotat valittujen rivien budjetin kustannuksia 20 prosentilla.</span><span class="sxs-lookup"><span data-stu-id="ff484-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="ff484-120">Jos syötät **0,7**, vähennät valittujen rivien budjetin kustannuksia 30 prosentilla.</span><span class="sxs-lookup"><span data-stu-id="ff484-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="ff484-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff484-121">Select **OK**.</span></span>

<span data-ttu-id="ff484-122">Valitut budjettirivit päivitetään vaiheessa 3 tai 4 määritettyjen arvojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ff484-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="ff484-123">Päivitä toteutuneet kustannukset</span><span class="sxs-lookup"><span data-stu-id="ff484-123">Update actual costs</span></span>

<span data-ttu-id="ff484-124">Kun budjettirivien päivämäärät ovat ohi ja toteutuneet kustannukset on kirjattu käyttöomaisuuden hallinnassa, voit myös päivittää todelliset kustannukset ylläpitobudjettiin.</span><span class="sxs-lookup"><span data-stu-id="ff484-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="ff484-125">Valitse **Ylläpitobudjetin rivit** -sivulla **Päivitä kustannukset**.</span><span class="sxs-lookup"><span data-stu-id="ff484-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="ff484-126">Valitse **Laske toteutunut kustannus** -valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff484-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="ff484-127">Budjettirivien **Toteutunut kustannus** -kentät päivitetään, jos todelliset kustannukset on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="ff484-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="ff484-128">Uusia budjetti rivejä voidaan luoda, jos uusia käyttöomaisuustyyppejä on luotu sen jälkeen, kun olet luonut budjetin, ja jos näitä käyttöomaisuuslajeja on käytetty sellaisten omaisuuserien osalta, joille on luotu työtilauksia ja joihin liittyvät kustannukset on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="ff484-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="ff484-129">Uusilla budjettiriveillä näkyvät vain todelliset kustannukset, koska niille ei laskettu budjettikustannuksia.</span><span class="sxs-lookup"><span data-stu-id="ff484-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="ff484-130">Jos haluat nähdä yhteenvedon todellisista kustannuksista, jotka on jaettu ennaltaehkäiseviin, korjaaviin ja investointikustannuksiin, voit tehdä saman kauden laskun **Resurssien kustannusten hallinta** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ff484-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="ff484-131">Budjettirivien lisääminen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="ff484-131">Manually add budget lines</span></span>

<span data-ttu-id="ff484-132">**Ylläpitobudjetin rivit** -sivulla voit lisätä uuden budjettirivin manuaalisesti valitsemalla **Uusi** ja tekemällä sitten valintoja rivillä.</span><span class="sxs-lookup"><span data-stu-id="ff484-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="ff484-133">Seuraavassa on esimerkkejä tilanteista, joissa tästä lähestymistavasta voi olla hyötyä:</span><span class="sxs-lookup"><span data-stu-id="ff484-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="ff484-134">Tiedät, että joidenkin käyttöomaisuuserien kunnostus on parhaillaan suunnitteluvaiheessa, mutta siihen liittyviä töitä ei ole vielä luotu omaisuuden hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="ff484-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="ff484-135">Haluat kuitenkin, että näiden töiden budjettikustannukset sisällytetään ylläpitobudjettiin.</span><span class="sxs-lookup"><span data-stu-id="ff484-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="ff484-136">Uusia resursseja tai resurssityyppejä on luotu ylläpitobudjetin luomisen jälkeen, mutta ylläpitosuunnitelmia ei ole vielä määritetty näille käyttöomaisuuserille tai -tyypeille.</span><span class="sxs-lookup"><span data-stu-id="ff484-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="ff484-137">Haluat kuitenkin, että näiden resurssityyppien budjettikustannukset sisällytetään ylläpitobudjettiin.</span><span class="sxs-lookup"><span data-stu-id="ff484-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
