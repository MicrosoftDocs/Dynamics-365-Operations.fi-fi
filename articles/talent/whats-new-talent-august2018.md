---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (elokuu 2018)
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Talent - Core HR:n uusista ja muuttuneista ominaisuuksista.
author: andreabichsel
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
ms.author: anbichse
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: 30646de08bd5ea4b2da05bfc38da7edc320a3331
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690097"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-august-2018"></a><span data-ttu-id="f26a3-103">Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (elokuu 2018)</span><span class="sxs-lookup"><span data-stu-id="f26a3-103">What's new or changed in Dynamics 365 Talent - Core HR (August 2018)</span></span>

<span data-ttu-id="f26a3-104">**Koontiversio 8.1.104**</span><span class="sxs-lookup"><span data-stu-id="f26a3-104">**Build 8.1.104**</span></span>

<span data-ttu-id="f26a3-105">Tässä ohjeaiheessa käsitellään Dynamics 365 Talent: Core HRin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="f26a3-105">This topic describes features that are either new or changed in Dynamics 365 Talent: Core HR.</span></span>

## <a name="view-expiring-records-in-manager-self-service"></a><span data-ttu-id="f26a3-106">Vanhentuvien tietueiden näyttäminen esimiehen itsepalvelussa</span><span class="sxs-lookup"><span data-stu-id="f26a3-106">View expiring records in Manager self-service</span></span>

<span data-ttu-id="f26a3-107">Voit nyt tarkastella vanhentuvia tietueita esimiehen itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="f26a3-107">You can now view expiring records in Manager self-service.</span></span> <span data-ttu-id="f26a3-108">Voit määrittää uusilla asetuksilla, mitä tietoja esimiehet voivat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="f26a3-108">New options allow you to configure what information will be available for managers to view.</span></span> <span data-ttu-id="f26a3-109">Vaihtoehtoja ovat esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="f26a3-109">These options include:</span></span>

-   <span data-ttu-id="f26a3-110">Todistukset</span><span class="sxs-lookup"><span data-stu-id="f26a3-110">Certificates</span></span>

-   <span data-ttu-id="f26a3-111">Tunnusnumerot</span><span class="sxs-lookup"><span data-stu-id="f26a3-111">Identification numbers</span></span>

-   <span data-ttu-id="f26a3-112">Koeajat</span><span class="sxs-lookup"><span data-stu-id="f26a3-112">Probation periods</span></span>

-   <span data-ttu-id="f26a3-113">Seulonnat</span><span class="sxs-lookup"><span data-stu-id="f26a3-113">Screenings</span></span>

-   <span data-ttu-id="f26a3-114">Testit</span><span class="sxs-lookup"><span data-stu-id="f26a3-114">Tests</span></span>

<span data-ttu-id="f26a3-115">Voit määrittää tällä ominaisuudella päivämääräalueen, josta vanhenevia tietueita etsitään.</span><span class="sxs-lookup"><span data-stu-id="f26a3-115">This feature also gives you the ability to specify the range of days in which to look for expiring records.</span></span>

## <a name="configurable-transfer-actions"></a><span data-ttu-id="f26a3-116">Määritettävät siirtotoiminnot</span><span class="sxs-lookup"><span data-stu-id="f26a3-116">Configurable transfer actions</span></span>

<span data-ttu-id="f26a3-117">Voit määrittää rooliin asetuksilla, jotka tulevat käytettäviksi siirtopyynnön antamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="f26a3-117">You can configure by role the options that will be available during the entry of a transfer request.</span></span> <span data-ttu-id="f26a3-118">Tämä ominaisuus lisää joustavuutta organisaation rooleihin.</span><span class="sxs-lookup"><span data-stu-id="f26a3-118">This feature provides additional flexibility across the roles in an organization.</span></span>

<span data-ttu-id="f26a3-119">Työntekijöiden siirtoa pyytäneet esimiehillä ei esimerkiksi ehkä ole kompensaatiosummien ehdotus- tai antamisoikeutta tai he eivät voi valita tehtäväluetteloita, jotka liitetään siirtopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="f26a3-119">For example, managers requesting employee transfers may not have access to suggest or enter compensation amounts or select the task lists that will be associated with the transfer request.</span></span> <span data-ttu-id="f26a3-120">Esimiehet voivat luoda ja lähettää siirtopyyntöjä, mutta eivät voi syöttää kompensaatiota tai tehtäväluettelomäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="f26a3-120">Managers can create and submit transfer requests, but can't enter compensation or task list assignments.</span></span> <span data-ttu-id="f26a3-121">Henkilöstöhallinto voi tässä määrityksessä määrittää uudet kompensaatioarvot ja mahdolliset lisätarkistusluettelot, jotka on täytettävä siirron valmistuttua.</span><span class="sxs-lookup"><span data-stu-id="f26a3-121">In this same configuration, HR can assign the new compensation values and assign any additional checklists to be completed because of the transfer completing.</span></span>

<span data-ttu-id="f26a3-122">Uudet määritysasetukset on oletusarvoisesti määritetty olemaan muuttamatta ominaisuuksia ennen tätä päivitystä.</span><span class="sxs-lookup"><span data-stu-id="f26a3-122">By default, the new configuration options are set to not change the capabilities prior to this update.</span></span>

## <a name="leave-and-absence"></a><span data-ttu-id="f26a3-123">Loma ja poissaolo</span><span class="sxs-lookup"><span data-stu-id="f26a3-123">Leave and absence</span></span>

<span data-ttu-id="f26a3-124">Loma ja poissaolo -kohdassa on lisää päivämääräkenttiä.</span><span class="sxs-lookup"><span data-stu-id="f26a3-124">There are now additional Date fields available in Leave and Absence.</span></span>

<span data-ttu-id="f26a3-125">Voit määrittää tällä ominaisuudella jaksotuskausiperustan käyttämään suunnitelmatasolla tiettyjä työntekijäpäivämääriä.</span><span class="sxs-lookup"><span data-stu-id="f26a3-125">With this feature, you can set the accrual period basis at the plan level to use specific employee dates.</span></span> <span data-ttu-id="f26a3-126">Loman jaksotusprosessissa voidaan käyttää kaikkia päivämääriä suunnitelman aloituspäivämäärää lukuun ottamatta.</span><span class="sxs-lookup"><span data-stu-id="f26a3-126">Dates other than the plan start date can be used during the leave accrual process.</span></span> <span data-ttu-id="f26a3-127">Työntekijäkohtaisissa päivämääräasetuksissa on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="f26a3-127">Options for employee-specific dates include the following values:</span></span>

-   <span data-ttu-id="f26a3-128">Mukautettu (käytössä ennen tätä päivitystä)</span><span class="sxs-lookup"><span data-stu-id="f26a3-128">Custom (available prior to this update)</span></span>

-   <span data-ttu-id="f26a3-129">Vuosipäivän päivämäärä</span><span class="sxs-lookup"><span data-stu-id="f26a3-129">Anniversary date</span></span>

-   <span data-ttu-id="f26a3-130">Alkuperäinen työsuhteen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="f26a3-130">Original hire date</span></span>

-   <span data-ttu-id="f26a3-131">Ikälisäpäivä</span><span class="sxs-lookup"><span data-stu-id="f26a3-131">Seniority date</span></span>

-   <span data-ttu-id="f26a3-132">Työntekijän muutettu aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="f26a3-132">Worker’s adjusted start date</span></span>

-   <span data-ttu-id="f26a3-133">Työntekijän aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="f26a3-133">Worker’s start date</span></span>

<span data-ttu-id="f26a3-134">Kun määritetty käyttämään yhtä työntekijäkohtaista päivämäärää, rekisteröintiprosessi laskee jaksotuskaudet käyttämällä määritettyä päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="f26a3-134">When configured to use one of the employee-specific dates, the enrollment process will use the specified date to calculate the accrual periods.</span></span> <span data-ttu-id="f26a3-135">Myös jaksotuskausiperusta näytetään työntekijän suunnitelman rekisteröinnissä, mikä auttaa ymmärtämään, mitä käytetään jaksoprosessissa.</span><span class="sxs-lookup"><span data-stu-id="f26a3-135">The accrual period basis is also displayed on the employee’s plan enrollment to help you understand what’s being used during the accrual process.</span></span>

## <a name="microsoft-word-integration"></a><span data-ttu-id="f26a3-136">Microsoft Word -integrointi</span><span class="sxs-lookup"><span data-stu-id="f26a3-136">Microsoft Word integration</span></span>

<span data-ttu-id="f26a3-137">Asiakirjamallit on otettu käyttöön koko Core HR:ssä.</span><span class="sxs-lookup"><span data-stu-id="f26a3-137">Document templates have been enabled throughout Core HR.</span></span> <span data-ttu-id="f26a3-138">Voit luoda tällä ominaisuudella luotuihin Word-malleihin perustuvia kirjeitä ja raportteja.</span><span class="sxs-lookup"><span data-stu-id="f26a3-138">This feature allows you to create letters and reports based on Word templates that you create.</span></span>

<span data-ttu-id="f26a3-139">Lisätietoja tästä ominaisuudesta on [Office-integraation opetusohjelma](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span><span class="sxs-lookup"><span data-stu-id="f26a3-139">Additional information about this feature is available in the [Office integration tutorial](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span></span>


## <a name="other-fixes"></a><span data-ttu-id="f26a3-140">Muut korjaukset</span><span class="sxs-lookup"><span data-stu-id="f26a3-140">Other fixes</span></span>

<span data-ttu-id="f26a3-141">Tämä versio sisältää uusien yksiköiden lisäksi myös useita aiempien yksiköiden ohjelmavirhekorjauksia ja lokalisoituja otsikkomuutoksia.</span><span class="sxs-lookup"><span data-stu-id="f26a3-141">This release also includes a number of bug fixes, the addition of new entities, fixes to existing entities, and localized label changes.</span></span>
