---
title: Poista Talent-ympäristöt
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin testi- tai tuotantoympäristön poistoprosessista.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 904c8eb1254a65e1627c33f14488a1a8e12f7c2b
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "858879"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="edd52-103">Talent-ympäristöjen poistaminen</span><span class="sxs-lookup"><span data-stu-id="edd52-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="edd52-104">Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin testi- tai tuotantoympäristön poistoprosessista.</span><span class="sxs-lookup"><span data-stu-id="edd52-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="edd52-105">Testiympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="edd52-105">Removing a test drive environment</span></span>

<span data-ttu-id="edd52-106">Talentin testauksen valmistelussa on 60 päivän vanhentumiskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="edd52-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="edd52-107">Testiympäristöjen omistajat voivat kuitenkin lopettaa kokeiluversion käytön aikaisemmin seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="edd52-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="edd52-108">Siirry [PowerApps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="edd52-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="edd52-109">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="edd52-109">Select **Environments**.</span></span>
3. <span data-ttu-id="edd52-110">Valitse testiympäristö, jonka nimeämiskäytäntö on seuraavanlainen: TestDrive – alias@toimialue</span><span class="sxs-lookup"><span data-stu-id="edd52-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="edd52-111">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="edd52-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="edd52-112">Aiemmin luotu testausympäristö poistetaan.</span><span class="sxs-lookup"><span data-stu-id="edd52-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="edd52-113">Kun se on poistettu, voit tilata uuden testiympäristön</span><span class="sxs-lookup"><span data-stu-id="edd52-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="edd52-114">Tuotantoympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="edd52-114">Removing a production environment</span></span>

<span data-ttu-id="edd52-115">Ohjeaiheessa oletetaan, että olet ostanut Talentin pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="edd52-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="edd52-116">Koska yksi Talent-ympäristö toimii yhden PowerApps-ympäristön sisällä, huomioon on otettava kaksi vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="edd52-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="edd52-117">Ensimmäinen vaihtoehto poistaa koko PowerApps-ympäristön ja toinen vaihtoehto vain Talent-sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="edd52-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="edd52-118">Ensimmäinen vaihtoehto on ensisijainen, jos olet luonut PowerApps-ympäristön nimenomaan Talentin valmistelua varten ja olet vasta aloittanut käyttöönoton tai sinulla ei ole muodostettuja integraatioita.</span><span class="sxs-lookup"><span data-stu-id="edd52-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="edd52-119">Toista vaihtoehtoa voi käyttää silloin, kun olet muodostanut PowerApps-ympäristön, johon täytettyjä monipuolisia tietoja hyödynnetään PowerApps- ja Flow-ratkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="edd52-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="edd52-120">Varmista ennen PowerApps-ympäristön poistamista, että sitä ei käytetä monipuolisissa tietojen integroinneissa Talent-sovelluksen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="edd52-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="edd52-121">Huomaa myös, että PowerApps-oletusympäristöjä ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="edd52-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="edd52-122">Koko PowerApps-ympäristön sekä Talentin että siihen liittyvät sovellukset ja työnkulut:</span><span class="sxs-lookup"><span data-stu-id="edd52-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="edd52-123">Siirry [PowerApps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="edd52-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="edd52-124">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="edd52-124">Select **Environments**.</span></span>
3. <span data-ttu-id="edd52-125">Valitse poistettava ympäristö.</span><span class="sxs-lookup"><span data-stu-id="edd52-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="edd52-126">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="edd52-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="edd52-127">Odota, kunnes poisto on valmis.</span><span class="sxs-lookup"><span data-stu-id="edd52-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="edd52-128">Kirjaudu sisään [Lifecycle Servicesiin](https://lcs.dynamics.com/Logon/Index) (LSC) samalla tilillä, jota käytit tilatessasi Talent-sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="edd52-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="edd52-129">Valitse ympäristön sisältävä Talent-projekti.</span><span class="sxs-lookup"><span data-stu-id="edd52-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="edd52-130">Valitse LCS-projektin **Talent-sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="edd52-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="edd52-131">Valitse poistettava esiintymä.</span><span class="sxs-lookup"><span data-stu-id="edd52-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="edd52-132">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="edd52-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="edd52-133">Voit poistaa Talent-ympäristön aiemmin luodusta PowerApps-ympäristöstä suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="edd52-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="edd52-134">Huomaa, että Talent DevOps -ryhmän tuki ja yhteydenottomahdollisuus on käytössä väliaikaisesti siihen asti, kunnes tämä toiminto on käytössä suoraan LCS-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="edd52-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="edd52-135">Aloita poistopyyntö ottamalla yhteyttä tukeen.</span><span class="sxs-lookup"><span data-stu-id="edd52-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="edd52-136">Tukiryhmä tekee poistopyynnön Talent DevOps -ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="edd52-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="edd52-137">Jatka, kun saat tiedon ympäristön poistamisesta.</span><span class="sxs-lookup"><span data-stu-id="edd52-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="edd52-138">Kirjaudu sisään LCS:ään samalla tilillä, jota käytit tilatessasi Talent-sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="edd52-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="edd52-139">Valitse ympäristön sisältävä Talent-projekti.</span><span class="sxs-lookup"><span data-stu-id="edd52-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="edd52-140">Valitse LCS-projektin **Talent-sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="edd52-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="edd52-141">Valitse poistettava esiintymä, jonka käyttöottotilan merkintänä on oltava **Epäonnistui**.</span><span class="sxs-lookup"><span data-stu-id="edd52-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="edd52-142">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="edd52-142">Select **Remove instance** and confirm your decision.</span></span> 

