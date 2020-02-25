---
title: Talentin laajentaminen Power Appsin ja Power Automaten avulla
description: Tässä artikkelissa käsitellään Microsoft Power Appsia ja Microsoft Power Automatea käyttäviä Microsoft Dynamics 365 Talent ‑ Attractin laajennusesimerkkejä.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029908"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="5eb6e-103">Talentin laajentaminen Power Appsin ja Power Automaten avulla</span><span class="sxs-lookup"><span data-stu-id="5eb6e-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="5eb6e-104">Tässä artikkelissa käsitellään Microsoft Power Appsia ja Microsoft Power Automatea käyttäviä Microsoft Dynamics 365 Talent: Attractin laajennusesimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="5eb6e-105">Voit tuoda kumpaankin esimerkkiin liitetyt ratkaisupaketin Power Apps-ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="5eb6e-106">Voit sitten käyttää paketteja joka ohjeena tai lähtökohtana, jonka avulla toteutat organisaatioon sopivia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5eb6e-107">Jos haluat käyttää tässä artikkelissa kuvattuja malleja ja sovellusta sellaisenaan, varmista testaamalla, että ne kattavat kaikki toteutukseen kuuluvat skenaariot.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="5eb6e-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="5eb6e-108">Prerequisites</span></span>

- <span data-ttu-id="5eb6e-109">Pakettien tuontia varten käyttäjät tarvitsevat **Ympäristön tekijä** -käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="5eb6e-110">Sovellusten vientiä ja tuontia varten käyttäjillä on oltava Power Apps-palvelupaketin 2 käyttöoikeus tai Power Apps -palvelupaketin 2 kokeiluversion käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="5eb6e-111">Power Automate – lomakeyhteys</span><span class="sxs-lookup"><span data-stu-id="5eb6e-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="5eb6e-112">**Power Automate – lomakeyhteys** -mallin avulla voi lukea tietoja Microsoft Formsista ja tallentaa ne Common Data Service -yksikköön.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="5eb6e-113">Mallia voidaan laajentaa siten, että sitä voidaan käyttää muissa skenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="5eb6e-114">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="5eb6e-114">Here are some examples:</span></span>

- <span data-ttu-id="5eb6e-115">Ehdokasarviointien taltiointi.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="5eb6e-116">Kurssin kyselylomakkeiden tulosten taltiointi.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="5eb6e-117">Haastattelukysymyskirjaston kokoaminen henkilöstöhallinnon järjestelmänvalvojille.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="5eb6e-118">Ehdokkaan haastatteluprosessin arvioinnin taltiointi.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="5eb6e-119">Microsoft Dynamics 365: Attractissa voit käyttää lomakkeita ehdokasportaalissa, jossa ehdokkaat täyttävät tiedot.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="5eb6e-120">Lomakkeet voidaan myös upottaa tehtävinä työmalliin.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="5eb6e-121">Kun ehdokas lähettää lomakkeen, Microsoft Power Automate taltioi lomakkeen lähetyksen, lukee tiedot ja tallentaa sen Common Data Service -yksikköön.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="5eb6e-122">Voit ladata **Power Automate – lomakeyhteys** -mallin ja mukautetun yksikkörakenteen siirtymällä Microsoft Download Centerissä kohtaan [Power Automate – lomakeyhteys](https://go.microsoft.com/fwlink/?linkid=2081988).</span><span class="sxs-lookup"><span data-stu-id="5eb6e-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="5eb6e-123">Power Automate – SharePoint -integraatio</span><span class="sxs-lookup"><span data-stu-id="5eb6e-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="5eb6e-124">**Power Automate – SharePoint-integrointi** -mallin avulla voi lukea tietoja Microsoft SharePoint -luettelosta, verrata luetteloa Common Data Service -yksikön kenttien arvoihin ja lähettää vertailun tulokset ilmoitussähköpostina.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="5eb6e-125">Organisaatio voi tarvita pikaisesti tiettyjä osaamisalueita.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="5eb6e-126">Nämä osaamisalueet voidaan tallentaa SharePointiin SharePoint-luettelona.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="5eb6e-127">Jos ehdokas hakee työtä, jossa on mainittu tarvittava osaamisaluejoukko, ja jos ehdokkaan osaamisalue ja SharePointiin tallennetut osaamisalueet vastaavat hyvin toisiaan, ilmoitussähköposti lähetetään.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="5eb6e-128">Tällä tavoin kiireellisesti täytettävä toimet voidaan täyttää nopeammin, sillä ilmoitukset auttavat työhönottajia palkkaamaan ehdokkaita koko organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="5eb6e-129">Tämä malli voidaan laajentaa käytettäväksi missä tahansa SharePoint-integraation sisältävässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="5eb6e-130">Voit ladata **Power Automate – SharePoint-integrointi** -mallin Microsoft Download Centerin kohdassa [Power Automate – SharePoint-integrointi](https://go.microsoft.com/fwlink/?linkid=2082109).</span><span class="sxs-lookup"><span data-stu-id="5eb6e-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="5eb6e-131">Suositussovellus</span><span class="sxs-lookup"><span data-stu-id="5eb6e-131">Referral App</span></span>

<span data-ttu-id="5eb6e-132">Voit lisätä ehdokkaita jaettuun kykypooliin suositussovelluksella.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="5eb6e-133">Suosittelija voi antaa **etunimen**, **sukunimen**, **sähköpostin** ja **LinkedInin URL-osoitteen**, kun ehdokas lähetetään.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="5eb6e-134">Ehdokkaan lähteen metatiedot täytetään sitten suosittelijan tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="5eb6e-135">Voit upottaa tämän sovelluksen työntekijän itsepalveluun suositusten lähettämistä varten tai voit käyttää sitä linkkinä yritysportaalissa ja suorittaa sen itsenäisenä sovelluksena.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="5eb6e-136">Lataa **suositussovellus** siirtymällä [Dynamics 365 Talent -laajennusratkaisu: suositussovellukseen](https://www.microsoft.com/download/details.aspx?id=58497) Microsoft Download Centerissä.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="5eb6e-137">Voit tuoda tämän sovelluksen ja mukauttaa sen lisäämään lisätoimintoja.</span><span class="sxs-lookup"><span data-stu-id="5eb6e-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5eb6e-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5eb6e-138">Additional resources</span></span>

[<span data-ttu-id="5eb6e-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="5eb6e-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="5eb6e-140">Sovelluksen siirtäminen vuokraajien ja ympäristöjen kesken</span><span class="sxs-lookup"><span data-stu-id="5eb6e-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
