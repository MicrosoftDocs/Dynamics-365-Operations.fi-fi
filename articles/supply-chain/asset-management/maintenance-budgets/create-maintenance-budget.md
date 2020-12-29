---
title: Luo ylläpitobudjetit
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitobudjetti luodaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2aaba8794bf0025f0449509752e4f197d3bf3db4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427138"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="a4277-103">Luo ylläpitobudjetit</span><span class="sxs-lookup"><span data-stu-id="a4277-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="a4277-104">Kunnossapitobudjettien avulla luodaan yleiskatsaus ennakoivaan kunnossapitoon liittyvistä odotetuista kustannuksista.</span><span class="sxs-lookup"><span data-stu-id="a4277-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="a4277-105">Budjettirivit lasketaan niiden kunnossapitoaikataulurivien perusteella, joiden odotettu alkamispäivämäärä on budjettikauden aikana.</span><span class="sxs-lookup"><span data-stu-id="a4277-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="a4277-106">Kunnossapitobudjetit perustuvat käyttöomaisuuden hallinnassa käytettyihin kustannustyyppeihin: **Ennaltaehkäisevä**, **Korjaava** ja **Investointi**.</span><span class="sxs-lookup"><span data-stu-id="a4277-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="a4277-107">Investointi-ylläpidon budjetoidut kustannukset sisältyvät aktiivisiin käyttökohteisiin, joilla on korvauspäivä budjettikauden aikana sekä siihen liittyvä korvaava arvo.</span><span class="sxs-lookup"><span data-stu-id="a4277-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="a4277-108">Korjaavan huollon budjetoidut kustannukset sisällytetään, jos edellinen oikaisupäivämäärä sisällytetään budjetin laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="a4277-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="a4277-109">Tällöin aiemman kauden korjaavat kustannukset lasketaan samalle tulevalle kaudelle, jolle ylläpitobudjettia lasketaan.</span><span class="sxs-lookup"><span data-stu-id="a4277-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="a4277-110">Luo ylläpitobudjetti</span><span class="sxs-lookup"><span data-stu-id="a4277-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="a4277-111">Valitse **Resurssien hallinta**\>**Kyselyt**\> **Ylläpitobudjetti** \> **Budjetti**.</span><span class="sxs-lookup"><span data-stu-id="a4277-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="a4277-112">Valitse **Luo budjetti**.</span><span class="sxs-lookup"><span data-stu-id="a4277-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="a4277-113">Kirjoita budjetin tunnus **Ylläpitobudjetti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a4277-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="a4277-114">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="a4277-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="a4277-115">Määritä **Kausi**-pikavälilehden **Alkupäivämäärä** -ja **Päättymispäivämäärä**-kenttiin budjettikauden alkamis- ja päättymispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="a4277-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="a4277-116">Jos haluat sisällyttää korjattavat budjetti kustannukset, jotka lasketaan edellisen kauden todellisten kustannusten perusteella, määritä **Korjaus päivämäärästä** -kenttään sen kauden alkamispäivämäärä, josta nämä kustannukset sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="a4277-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="a4277-117">Määritä viidessä **Ryhmittely**-pikavälilehdessä asetukset sen mukaan, miten yksityiskohtaisia tietoja budjetti edellyttää.</span><span class="sxs-lookup"><span data-stu-id="a4277-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="a4277-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4277-118">Select **OK**.</span></span>
8. <span data-ttu-id="a4277-119">Valitsemalla **Budjettirivit** voit avata **Ylläpitobudjettirivit**-sivun, jossa voit tarkastella kaikkia kaudelle luotuja budjettirivejä.</span><span class="sxs-lookup"><span data-stu-id="a4277-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="a4277-120">Voit hyväksyä budjetin valitsemalla sen **Ylläpitobudjetit** -sivulta ja valitsemalla sitten **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="a4277-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="a4277-121">Valitse sitten **Hyväksy budjetti** -valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4277-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="a4277-122">Nimesi lisätään **Ylläpitobudjetit**-sivun **Hyväksynyt-** kenttään.</span><span class="sxs-lookup"><span data-stu-id="a4277-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4277-123">Kun olet hyväksynyt ylläpitobudjetin, et voi laskea uudelleen tai muuttaa **Ylläpitobudjetin rivit** -sivun liittyviä rivejä, ellet ensin poista hyväksyntää.</span><span class="sxs-lookup"><span data-stu-id="a4277-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="a4277-124">Voit poistaa ylläpitobudjetin hyväksynnän valitsemalla sen **Ylläpitobudjetit** -sivulta ja valitsemalla sitten **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="a4277-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="a4277-125">Valitse sitten **Hyväksy budjetti** -valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4277-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Ylläpitobudjetit](media/01-maintenance-budgets.png)

<span data-ttu-id="a4277-127">Voit myös luoda uuden ylläpitobudjetin kopioimalla aiemmin luodun budjetin.</span><span class="sxs-lookup"><span data-stu-id="a4277-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="a4277-128">Valitse **Ylläpitobudjetit** -sivulla kopioitava budjetti ja valitse sitten **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="a4277-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="a4277-129">Tästä lähestymistavasta on hyötyä, jos olet esimerkiksi luonut yhden kuukauden budjetin ja haluat kopioida sen muihin kuukausiin.</span><span class="sxs-lookup"><span data-stu-id="a4277-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="a4277-130">Kunnossapitobudjetissa lasketaan vain kunnossapitoaikatauluriveihin perustuvia budjettikustannuksia.</span><span class="sxs-lookup"><span data-stu-id="a4277-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="a4277-131">Voit laskea saman kauden todelliset kustannukset käyttämällä **Resurssien kustannusten hallinta** -sivulla olevaa laskentaa.</span><span class="sxs-lookup"><span data-stu-id="a4277-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
