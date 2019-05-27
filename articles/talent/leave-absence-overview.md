---
title: Lomien ja poissaolojen hallinta
description: Tässä ohjeaiheessa on loman ja poissaolojen hallintamoduulin yleiskatsaus.
author: andreabichsel
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebfaeb0696d7200ddf3c715f96a259b91db08e7a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517880"
---
# <a name="leave-and-absence-management"></a><span data-ttu-id="fb7ff-103">Lomien ja poissaolojen hallinta</span><span class="sxs-lookup"><span data-stu-id="fb7ff-103">Leave and absence management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb7ff-104">**Loman ja poissaolojen hallinta** -moduuli on joustava kehys poissaolojen hallintaprosessin määrittämiselle.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-104">The **Leave and absence management** module offers a flexible framework for defining the absence management process.</span></span> <span data-ttu-id="fb7ff-105">Loma- ja poissaolosuunnitelmat voidaan luoda määrittämään, miten työntekijöiden lomat jaksotetaan tai miten niitä heille myönnetään.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-105">Leave and absence plans can be created to determine how employees accrue or are granted time off.</span></span> <span data-ttu-id="fb7ff-106">Kun työntekijät ovat rekisteröityneet suunnitelmaan, työntekijät voivat lähettää lomapyyntöjä esimiesten hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-106">After employees are enrolled in a plan, they can submit time-off requests for approval by managers.</span></span> <span data-ttu-id="fb7ff-107">Loman seurannan avulla sekä ensimmäisen tason esimiehet että henkilöstöpäälliköt voivat nähdä, ketkä ovat parhaillaan lomalla ja kuinka paljon heillä on lomaa jäljellä.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-107">Leave tracking lets both first-level managers and Human Resources (HR) managers see who is taking time off and how much time off each employee still has.</span></span>  

<span data-ttu-id="fb7ff-108">Loman ja poissaolojen hallinta sisältää seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="fb7ff-108">Leave and absence management provides the following features:</span></span> 

- <span data-ttu-id="fb7ff-109">**Määritä loma- ja poissaolotyyppi.**</span><span class="sxs-lookup"><span data-stu-id="fb7ff-109">**Define leave and absence types.**</span></span>

    <span data-ttu-id="fb7ff-110">Lomatyypit määrittävät erilaiset poissaolotyypit, joita työntekijät voivat ilmoittaa.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-110">Leave types define the various types of absences that employees can report.</span></span> <span data-ttu-id="fb7ff-111">Koska nämä tyypit ovat käyttäjän määrittämiä, ne voidaan räätälöidä organisaation tarpeita vastaaviksi.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-111">Because these types are user-defined, they can be tailored to your organization.</span></span> <span data-ttu-id="fb7ff-112">Tyypillisiä lomatyyppejä ovat palkallinen vapaa (PTO), loma, lyhytaikainen vamma, jury-velvollisuus (tämä lomatyyppi koskee vain Yhdysvaltoja) ja kuolemantapaus.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-112">Some typical leave types include paid time off (PTO), leave, short-term disability, jury duty (this leave type is specific to the United States), and bereavement.</span></span> 

- <span data-ttu-id="fb7ff-113">**Määritä yritykseen sopivat loma- ja poissaolosuunnitelmat.**</span><span class="sxs-lookup"><span data-stu-id="fb7ff-113">**Define leave and absence plans that are tiered to fit your business.**</span></span>

    <span data-ttu-id="fb7ff-114">Loma- ja poissaolosuunnitelmat voidaan määrittää siten, että lomat jaksotetaan tietyin välein, kuten vuosittain, kuukausittain tai kaksi kertaa kuukaudessa.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-114">Leave and absence plans can be defined so that accrual occurs at specific frequencies, such as annually, monthly, or semimonthly.</span></span> <span data-ttu-id="fb7ff-115">Suunnitelmat voidaan myös määrittää myönnettynä, jolloin yksi jaksotus tapahtuu tiettynä päivämääränä.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-115">Plans can also be defined as a grant, where a single accrual occurs on a specific date.</span></span> 

    <span data-ttu-id="fb7ff-116">Lomasuunnitelmissa on usein tasoja, joilla osa työntekijäryhmistä saa lisäetuja sen mukaan, kuinka kauan he ovat olleet organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-116">Leave plans often contain tiers, where some groups of employees receive additional benefits, based on the amount of time that they have been with the organization.</span></span> <span data-ttu-id="fb7ff-117">Näiden käyttäjän määrittämien tasojen avulla voidaan tehdä automaattinen rekisteröityminen lisäetuihin määritettyjen päivämääräehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-117">These user-defined tiers enable automatic enrollment in additional benefit hours, based on the date criteria that are defined.</span></span> <span data-ttu-id="fb7ff-118">Lomasuunnitelmat voidaan myös määrittää pakottamaan suurin siirrettävä määrä tai minimisaldo, jotta työntekijät eivät voi käyttää enemmän etutunteja kuin heille on jaksotettu.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-118">Leave plans can also be configured to enforce a maximum carry-over amount or a minimum balance, to prevent employees from using more benefit hours than they have accrued.</span></span> 

    <span data-ttu-id="fb7ff-119">Tyypillisissä lomasuunnitelmissa on tasokohtaisia suunnitelmia, jotka myöntävät uusille työntekijöille 80 tunnin palkallisen vapaan. 60 kuukauden työsuhteen jälkeen etu on 120 tuntia.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-119">Typical leave plans include tiered plans that grant a benefit of 80 hours of PTO to new employees but a benefit of 120 hours after 60 months of service.</span></span> <span data-ttu-id="fb7ff-120">Lisäsuunnitelmat voivat myöntää liikkuvia lomia tai toimeen perustuvia etuja, kun vain johtotehtäviä koskevia etutunteja.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-120">Additional plans might grant floating holidays or position-based benefits, such as executive-only benefit hours.</span></span>

- <span data-ttu-id="fb7ff-121">**Rekisteröi loma- ja poissaolosuunnitelmat yksittäin tai työehtoihin perustuvana joukkomäärityksenä.**</span><span class="sxs-lookup"><span data-stu-id="fb7ff-121">**Enroll employees in leave and absence plans individually or through mass assignment that is based on job criteria.**</span></span>

    <span data-ttu-id="fb7ff-122">Erilaisia työhön liittyviä suodattamia voidaan käyttää määrittämään työntekijäryhmä lomasuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-122">Several job-related filters can be used to assign a group of employees to a leave plan.</span></span> <span data-ttu-id="fb7ff-123">Henkilöstöpäälliköt voivat tarkastella työntekijöitä ja tarkistaa, mihin loma- ja poissaolosuunnitelmiin työntekijä on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-123">HR managers can view an employee to see what leave and absence plans the employee is enrolled in.</span></span> <span data-ttu-id="fb7ff-124">Vaihtoehtoisesti henkilöstöjohtajat voivat myös tarkastella kaikkia suunnitelmia ja liittyvistä työtekijöiden rekisteröinnistä.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-124">Alternatively, HR managers can view all plans and the related employee enrollments.</span></span>

- <span data-ttu-id="fb7ff-125">**Keskeytä loma- ja poissaolosuunnitelmia.**</span><span class="sxs-lookup"><span data-stu-id="fb7ff-125">**Suspend leave and absence plans.**</span></span>

    <span data-ttu-id="fb7ff-126">Loma- ja poissaolosuunnitelmat voidaan keskeyttää, joilla ne poistuvat käytöstä eikä niiden mukainen jaksotus estetään.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-126">Leave and absence plans can be suspended to make them inactive and prevent additional accruals.</span></span> <span data-ttu-id="fb7ff-127">Työntekijöiden jaksotus keskeytetään, jos työsuhde päättyy.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-127">Accruals are suspended for employees if their employment ends.</span></span>  

- <span data-ttu-id="fb7ff-128">**Säädä oikeutuksia ja palkkioita.**</span><span class="sxs-lookup"><span data-stu-id="fb7ff-128">**Adjust entitlements and grants.**</span></span>

    <span data-ttu-id="fb7ff-129">Työntekijä voidaan rekisteröidä ylemmän tason suunnitelmaan käyttämällä työntekijäkohtaista päivämäärää työntekijän oletussuunnitelman ohittamiseen.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-129">An employee can be enrolled in a higher plan tier by using a worker-specific date to override the employee's default plan offering.</span></span> <span data-ttu-id="fb7ff-130">Työntekijöiden rekisteröinnin aikaista loma- ja poissaolosaldoa voidaan oikaista manuaalisesti, tai henkilöstöpäällikkö voi tehdä manuaalisen oikaisun koska tahansa.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-130">Employees can receive a manual adjustment to their leave and absence balance at the time of plan enrollment, or HR can make a manual adjustment at any time.</span></span> 

- <span data-ttu-id="fb7ff-131">**Käsittele lomapyynnöt työnkulun avulla.**</span><span class="sxs-lookup"><span data-stu-id="fb7ff-131">**Apply a workflow to time-off requests.**</span></span>

     <span data-ttu-id="fb7ff-132">Työnkulku voidaan mukauttaa ja sitä voidaan käyttää poissaolopyynnöissä organisaation tarpeiden edellyttämällä tavalla.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-132">A workflow can be customized and applied to time-off requests to meet the organization’s requirements.</span></span>  

- <span data-ttu-id="fb7ff-133">**Seuraa työtekijöiden poissaolosaldoja.**</span><span class="sxs-lookup"><span data-stu-id="fb7ff-133">**Track employee absence balances.**</span></span>

    <span data-ttu-id="fb7ff-134">Työntekijät, heidän esimiehensä ja henkilöstöpäällikkö voivat tarkastella loma- ja poissaolosaldoja.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-134">Employees, their manager, and HR can view leave and absence balances.</span></span> <span data-ttu-id="fb7ff-135">Henkilöstöpäällikkö voi seurata suunnitelmaan rekisteröitymisiä ja poissaolosaldoja tyypeittäin vuorovaikutteisten raporttien avulla.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-135">HR can use interactive reports to track plan enrollments and time-off balances by type.</span></span> 

- <span data-ttu-id="fb7ff-136">**Lähetä poissaolopyynnöt.**</span><span class="sxs-lookup"><span data-stu-id="fb7ff-136">**Submit time-off requests.**</span></span>

    <span data-ttu-id="fb7ff-137">Työntekijät voivat poissaolopyyntöjen käytettävissä olevien tuntien perusteella.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-137">Employees can submit time-off requests against their available hours.</span></span> <span data-ttu-id="fb7ff-138">Pyynnöt voivat olla yksinkertaisia yhden päivän pyyntöjä tai useasta päivästä koostuvia pyyntöjä, joihin voi sisältyä useita loma- ja poissaolotyyppejä.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-138">Requests can be simple single-day requests or multiple-day requests that include multiple leave and absence types.</span></span> <span data-ttu-id="fb7ff-139">Jos työnkulkua ei ole otettu käyttöön, pyynnöt hyväksytään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-139">If a workflow isn't enabled, the requests are automatically approved.</span></span> <span data-ttu-id="fb7ff-140">Jos työnkulku on otettu käyttöön, hyväksyminen voi olla työnkulun määrityksen mukaan automaattinen tai se voi edellyttää kuittausta.</span><span class="sxs-lookup"><span data-stu-id="fb7ff-140">If a workflow is enabled, the approval can be automatic, or it can require sign-off, depending on the workflow configuration.</span></span>
