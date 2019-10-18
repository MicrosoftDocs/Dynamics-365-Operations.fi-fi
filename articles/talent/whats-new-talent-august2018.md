---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (elokuu 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: db7c91ea6599bde7d4c589a021d2d3b262e57ec9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010449"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-august-2018"></a><span data-ttu-id="17472-103">Dynamics 365 Talent: Core HR:n uudet ja muuttuneet ominaisuudet (elokuu 2018)</span><span class="sxs-lookup"><span data-stu-id="17472-103">What's new or changed in Dynamics 365 Talent: Core HR (August 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17472-104">**Koontiversio 8.1.104**</span><span class="sxs-lookup"><span data-stu-id="17472-104">**Build 8.1.104**</span></span>

<span data-ttu-id="17472-105">Tässä ohjeaiheessa käsitellään Dynamics 365 Talent: Core HRin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="17472-105">This topic describes features that are either new or changed in Dynamics 365 Talent: Core HR.</span></span>

## <a name="view-expiring-records-in-manager-self-service"></a><span data-ttu-id="17472-106">Vanhentuvien tietueiden näyttäminen esimiehen itsepalvelussa</span><span class="sxs-lookup"><span data-stu-id="17472-106">View expiring records in Manager self service</span></span>

<span data-ttu-id="17472-107">Voit nyt tarkastella vanhentuvia tietueita esimiehen itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="17472-107">You can now view expiring records in Manager self-service.</span></span> <span data-ttu-id="17472-108">Voit määrittää uusilla asetuksilla, mitä tietoja esimiehet voivat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="17472-108">New options are allow you to configure what information will be available for managers to view.</span></span> <span data-ttu-id="17472-109">Näitä kenttiä ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="17472-109">These include:</span></span>

-   <span data-ttu-id="17472-110">Todistukset</span><span class="sxs-lookup"><span data-stu-id="17472-110">Certificates</span></span>

-   <span data-ttu-id="17472-111">Tunnusnumerot</span><span class="sxs-lookup"><span data-stu-id="17472-111">Identification numbers</span></span>

-   <span data-ttu-id="17472-112">Koeajat</span><span class="sxs-lookup"><span data-stu-id="17472-112">Probation periods</span></span>

-   <span data-ttu-id="17472-113">Seulonnat</span><span class="sxs-lookup"><span data-stu-id="17472-113">Screenings</span></span>

-   <span data-ttu-id="17472-114">Testit</span><span class="sxs-lookup"><span data-stu-id="17472-114">Tests</span></span>

<span data-ttu-id="17472-115">Voit määrittää tällä ominaisuudella päivämääräalueen, josta vanhenevia tietueita etsitään.</span><span class="sxs-lookup"><span data-stu-id="17472-115">This feature also gives you the ability to specify the range of days in which to look for expiring records.</span></span>

## <a name="configurable-transfer-actions"></a><span data-ttu-id="17472-116">Määritettävät siirtotoiminnot</span><span class="sxs-lookup"><span data-stu-id="17472-116">Configurable transfer actions</span></span>

<span data-ttu-id="17472-117">Voit määrittää rooliin asetuksilla, jotka tulevat käytettäviksi siirtopyynnön antamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="17472-117">You can configure by role the options that will be available during the entry of a transfer request.</span></span> <span data-ttu-id="17472-118">Tämä ominaisuus lisää joustavuutta organisaation rooleihin.</span><span class="sxs-lookup"><span data-stu-id="17472-118">This feature provides additional flexibility across the roles in an organization.</span></span>

<span data-ttu-id="17472-119">Työntekijöiden siirtoa pyytäneet esimiehillä ei esimerkiksi ehkä ole kompensaatiosummien ehdotus- tai antamisoikeutta tai he eivät voi valita tehtäväluetteloita, jotka liitetään siirtopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="17472-119">For example, managers requesting employee transfers may not have access to suggest or enter compensation amounts or select the task lists that will be associated with the transfer request.</span></span> <span data-ttu-id="17472-120">Esimiehet ovat tässä tapauksessa voineet luoda ja lähettää siirtopyyntöjä, mutta eivät ole voineet antaa kompensaatiota tai tehtäväluettelomäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="17472-120">In this case, managers can create and submit transfer requests but are not allowed to enter compensation or task list assignments.</span></span> <span data-ttu-id="17472-121">Henkilöstöhallinto voi tässä määrityksessä määrittää sekä uudet kompensaatioarvot että mahdolliset lisätarkistusluettelot, jotka on täytettävä siirron valmistuttua.</span><span class="sxs-lookup"><span data-stu-id="17472-121">In this same configuration, HR will be able to assign the new compensation values as well as assign any additional checklists to be completed as a result of the transfer completing.</span></span>

<span data-ttu-id="17472-122">Uudet määritysasetukset on oletusarvoisesti määritetty olemaan muuttamatta ominaisuuksia ennen tätä päivitystä.</span><span class="sxs-lookup"><span data-stu-id="17472-122">By default, the new configuration options are set to not change the capabilities prior to this update.</span></span>

## <a name="leave-and-absence"></a><span data-ttu-id="17472-123">Loma ja poissaolo</span><span class="sxs-lookup"><span data-stu-id="17472-123">Leave and absence</span></span>

<span data-ttu-id="17472-124">Loma ja poissaolo -kohdassa on lisää päivämääräkenttiä.</span><span class="sxs-lookup"><span data-stu-id="17472-124">There are now additional Date fields available in Leave and Absence.</span></span>

<span data-ttu-id="17472-125">Voit määrittää tällä ominaisuudella jaksotuskausiperustan käyttämään suunnitelmatasolla tiettyjä työntekijäpäivämääriä.</span><span class="sxs-lookup"><span data-stu-id="17472-125">With this feature you can set the accrual period basis at the plan level to use specific employee dates.</span></span> <span data-ttu-id="17472-126">Tällä tavoin muita päivämääriä kuin suunnitelman aloituspäivä käytettäväksi loman jaksotusprosessissa.</span><span class="sxs-lookup"><span data-stu-id="17472-126">This allows for dates other than the plan start date to be used during the leave accrual process.</span></span> <span data-ttu-id="17472-127">Työntekijäkohtaisissa päivämääräasetuksissa on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="17472-127">Options for employee specific dates include the following values:</span></span>

-   <span data-ttu-id="17472-128">Mukautettu (käytössä ennen tätä päivitystä)</span><span class="sxs-lookup"><span data-stu-id="17472-128">Custom (available prior to this update)</span></span>

-   <span data-ttu-id="17472-129">Vuosipäivän päivämäärä</span><span class="sxs-lookup"><span data-stu-id="17472-129">Anniversary date</span></span>

-   <span data-ttu-id="17472-130">Alkuperäinen työsuhteen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="17472-130">Original hire date</span></span>

-   <span data-ttu-id="17472-131">Ikälisäpäivä</span><span class="sxs-lookup"><span data-stu-id="17472-131">Seniority date</span></span>

-   <span data-ttu-id="17472-132">Työntekijän muutettu aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="17472-132">Worker’s adjusted start date</span></span>

-   <span data-ttu-id="17472-133">Työntekijän aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="17472-133">Worker’s start date</span></span>

<span data-ttu-id="17472-134">Kun määritetty käyttämään yhtä työntekijäkohtaista päivämäärää, rekisteröintiprosessi laskee jaksotuskaudet käyttämällä määritettyä päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="17472-134">When configured to use one of the employee specific dates, the enrollment process will use the specified date to calculate the accrual periods.</span></span> <span data-ttu-id="17472-135">Myös jaksotuskausiperusta näytetään työntekijän suunnitelman rekisteröinnissä, mikä auttaa ymmärtämään, mitä käytetään jaksoprosessissa.</span><span class="sxs-lookup"><span data-stu-id="17472-135">The accrual period basis is also displayed on the employee’s plan enrollment to help you understand what’s being used during the accrual process.</span></span>

## <a name="microsoft-word-integration"></a><span data-ttu-id="17472-136">Microsoft Word -integrointi</span><span class="sxs-lookup"><span data-stu-id="17472-136">Microsoft Word integration</span></span>

<span data-ttu-id="17472-137">Asiakirjamallit on otettu käyttöön koko Core HR:ssä.</span><span class="sxs-lookup"><span data-stu-id="17472-137">Document templates have been enabled throughout Core HR.</span></span> <span data-ttu-id="17472-138">Voit luoda tällä ominaisuudella luotuihin Word-malleihin perustuvia kirjeitä ja raportteja.</span><span class="sxs-lookup"><span data-stu-id="17472-138">This feature allows you to create letters and reports based on Word templates that you create.</span></span>

<span data-ttu-id="17472-139">Lisätietoja tästä ominaisuudesta on [Office-integraation opetusohjelma](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span><span class="sxs-lookup"><span data-stu-id="17472-139">Additional information about this feature is available in the [Office integration tutorial](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span></span>


## <a name="other-fixes"></a><span data-ttu-id="17472-140">Muut korjaukset</span><span class="sxs-lookup"><span data-stu-id="17472-140">Other fixes</span></span>

<span data-ttu-id="17472-141">Tämä versio sisältää uusien yksiköiden lisäksi myös useita aiempien yksiköiden ohjelmavirhekorjauksia ja lokalisoituja otsikkomuutoksia.</span><span class="sxs-lookup"><span data-stu-id="17472-141">This release also includes a number of bug fixes, the addition of new entities, fixes to existing entities, and localized label changes.</span></span>
