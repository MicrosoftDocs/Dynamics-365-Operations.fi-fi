---
title: Toimittajan maksupidätysehtojen luominen ja käyttäminen
description: Tässä ohjeaiheessa on tietoja toimittajamaksuissa olevien säilytysehtojen määrittämisestä ja ylläpidosta.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410217"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="58f27-103">Toimittajan maksupidätysehtojen luominen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="58f27-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="58f27-104">Toimittajamaksun pidätysehtojen määrittäminen projektille on hyödyllistä, kun organisaatio haluaa säilyttää osan toimittajalle tehdyistä maksuista.</span><span class="sxs-lookup"><span data-stu-id="58f27-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="58f27-105">Jos esimerkiksi haluat pidättää maksuja toimittajalle, kunnes toimitetut tuotteet vastaavat odotuksiasi.</span><span class="sxs-lookup"><span data-stu-id="58f27-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="58f27-106">Toimittajan maksuehtojen pidätysehdot voidaan määrittää, kun neuvottelet toimittajan kanssa.</span><span class="sxs-lookup"><span data-stu-id="58f27-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="58f27-107">Toimittajan maksun pidättämisehtojen luominen</span><span class="sxs-lookup"><span data-stu-id="58f27-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="58f27-108">Voit syöttää toimittajamaksun prosenttiosuuden pidätettäväksi ja prosenttiosuuden aiemmin pidätetystä summasta vapautettavaksi.</span><span class="sxs-lookup"><span data-stu-id="58f27-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="58f27-109">Summat säilytetään automaattisesti toimittajan laskuissa, kunnes sopimus saavuttaa tietyn täyttymistilan.</span><span class="sxs-lookup"><span data-stu-id="58f27-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="58f27-110">Kun olet määrittänyt pidätysehdot, voit soveltaa niitä mihin tahansa projektiin tälle toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="58f27-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="58f27-111">Käytä seuraavia vaiheita määrittääksesi ja ylläpitääksesi toimittajamaksujen ehtoja.</span><span class="sxs-lookup"><span data-stu-id="58f27-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="58f27-112">Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Pidättäminen** > **Toimittajamaksujen pidätysehdot**.</span><span class="sxs-lookup"><span data-stu-id="58f27-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="58f27-113">Valitse **Uusi** lisätäksesi uudet toimittajan pidätysehdot.</span><span class="sxs-lookup"><span data-stu-id="58f27-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="58f27-114">**Säännön tunnus** -arvo uudelle termille lisätään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="58f27-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="58f27-115">Kirjoita lyhyt kuvaus **Kuvaus**-kenttään ja valitse **Ehdot**-pikavälilehdessä **Lisää rivi**, niin voit määrittää termin arvot seuraaville:</span><span class="sxs-lookup"><span data-stu-id="58f27-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="58f27-116">**Toimitettujen yksiköiden prosenttiosuus**: Syötä termin valmistumisprosentti.</span><span class="sxs-lookup"><span data-stu-id="58f27-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="58f27-117">Summat säilytetään automaattisesti toimittajalaskuissa, kunnes valmistumisprosentin vaihe vastaa määritettyä prosenttiosuutta.</span><span class="sxs-lookup"><span data-stu-id="58f27-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="58f27-118">Esimerkiksi jos kirjoitat 50,00, määrät säilytetään, kunnes projektista 50 prosenttia on valmiina.</span><span class="sxs-lookup"><span data-stu-id="58f27-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="58f27-119">**Pidätettävä prosenttiosuus**: Syötä toimittajan laskutussumman pidätettävä prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="58f27-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="58f27-120">Esimerkiksi jos syötät arvon 10,00, 10 prosenttia toimittajalaskun summasta pidätetään, kunnes projekti saavuttaa valmistumisprosentin, jonka olet asettanut **Toimitettujen yksiköiden prosenttiosuus** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="58f27-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="58f27-121">**Vapautettava prosenttiosuus**: Valitse **Lisää rivi** lisätäksesi prosenttiosuuden mistä tahansa aiemmin pidätetyistä summista vapautettavaksi projektin valmistumisen valitulla tasolla.</span><span class="sxs-lookup"><span data-stu-id="58f27-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="58f27-122">Jos sinulla on useita projektin eri tasojen valmistumisen välitavoitteita, syötä erillinen toimittajan pidätysehdon rivi kuhunkin pidätyssääntöön.</span><span class="sxs-lookup"><span data-stu-id="58f27-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="58f27-123">Kullekin riville voidaan määrittää eri pidätysprosenttiosuus ja eri vapautusprosenttiosuus kullekin nimetylle projektin valmistumisasteen tasolle.</span><span class="sxs-lookup"><span data-stu-id="58f27-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="58f27-124">Kun olet luonut toimittajan pidätysehdot toimittajalle, voit soveltaa ehtoja projektiin.</span><span class="sxs-lookup"><span data-stu-id="58f27-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="58f27-125">Sovella toimittajan pidätysehtoja projektiin</span><span class="sxs-lookup"><span data-stu-id="58f27-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="58f27-126">Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Projektit** > **Kaikki projektit** ja avaa projekti projektiluettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="58f27-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="58f27-127">Valitse **Toimittajasopimukset** -pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="58f27-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="58f27-128">Valitse **Tilikoodi**-kentästä jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="58f27-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="58f27-129">**Taulukko**: Toimittajan pidätysehtoja sovelletaan yhteen toimittajaan.</span><span class="sxs-lookup"><span data-stu-id="58f27-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="58f27-130">**Ryhmä**: Toimittajan pidätysehtoja sovelletaan kaikkiin toimittajaryhmän toimittajiin.</span><span class="sxs-lookup"><span data-stu-id="58f27-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="58f27-131">**Kaikki**: Toimittajan pidätysehtoja sovelletaan kaikkiin toimittajiin.</span><span class="sxs-lookup"><span data-stu-id="58f27-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="58f27-132">Valitse **Toimittaja tai toimittajaryhmä** -kentässä toimittaja tai toimittajaryhmä, johon toimittajan pidätysehtoja sovelletaan.</span><span class="sxs-lookup"><span data-stu-id="58f27-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="58f27-133">Jos olet valinnut **Kaikki** edellisessä vaiheessa, tämä kenttä ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="58f27-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="58f27-134">Valitse **Toimittajan pidätysehdot** -kentästä pidätysehdot, jotka loit edellisessä menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="58f27-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="58f27-135">Jos projektissa on toimittajalle myös määritetty Maksa, kun maksettu -ehdot (PWP), syötä kynnysprosenttiarvo projektille **PWP-kynnysprosenttiarvo**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="58f27-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="58f27-136">Toimittajan pidätysehdot näkyvät myös ostotilauksissa, jotka luot toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="58f27-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
