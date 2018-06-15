---
title: "Poista Talent-ympäristö"
description: "Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin testi- tai tuotantoympäristön poistoprosessista."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d1870c84d4d5e7402bae44d192ce7587c2f67fe7
ms.openlocfilehash: 0e7748b079b1cd5c069917d46e05cd281ea6aa01
ms.contentlocale: fi-fi
ms.lasthandoff: 04/05/2018

---
# <a name="remove-a-talent-environment"></a><span data-ttu-id="0a1b8-103">Poista Talent-ympäristö</span><span class="sxs-lookup"><span data-stu-id="0a1b8-103">Remove a Talent environment</span></span>

<span data-ttu-id="0a1b8-104">Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin testi- tai tuotantoympäristön poistoprosessista.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="0a1b8-105">Testiympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="0a1b8-105">Removing a test drive environment</span></span>

<span data-ttu-id="0a1b8-106">Talentin testauksen valmistelussa on 60 päivän vanhentumiskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="0a1b8-107">Testiympäristöjen omistajat voivat kuitenkin lopettaa kokeiluversion käytön aikaisemmin seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="0a1b8-108">Siirry [PowerApps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="0a1b8-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="0a1b8-109">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-109">Select **Environments**.</span></span>
3. <span data-ttu-id="0a1b8-110">Valitse testiympäristö, jonka nimeämiskäytäntö on seuraavanlainen: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="0a1b8-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="0a1b8-111">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="0a1b8-112">Aiemmin luotu testausympäristö poistetaan.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="0a1b8-113">Kun se on poistettu, voit tilata uuden testiympäristön</span><span class="sxs-lookup"><span data-stu-id="0a1b8-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="0a1b8-114">Tuotantoympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="0a1b8-114">Removing a production environment</span></span>

<span data-ttu-id="0a1b8-115">Ohjeaiheessa oletetaan, että olet ostanut Talentin pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="0a1b8-116">Koska yksi Talent-ympäristö toimii yhden PowerApps-ympäristön sisällä, huomioon on otettava kaksi vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="0a1b8-117">Ensimmäinen vaihtoehto poistaa koko PowerApps-ympäristön ja toinen vaihtoehto vain Talent-sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="0a1b8-118">Ensimmäinen vaihtoehto on ensisijainen, jos olet luonut PowerApps-ympäristön nimenomaan Talentin valmistelua varten ja olet vasta aloittanut käyttöönoton tai sinulla ei ole muodostettuja integraatioita.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="0a1b8-119">Toista vaihtoehtoa voi käyttää silloin, kun olet muodostanut PowerApps-ympäristön, johon täytettyjä monipuolisia tietoja hyödynnetään PowerApps- ja Flow-ratkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="0a1b8-120">Varmista ennen PowerApps-ympäristön poistamista, että sitä ei käytetä monipuolisissa tietojen integroinneissa Talent-sovelluksen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="0a1b8-121">Huomaa myös, että PowerApps-oletusympäristöjä ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="0a1b8-122">Koko PowerApps-ympäristön sekä Talentin että siihen liittyvät sovellukset ja työnkulut:</span><span class="sxs-lookup"><span data-stu-id="0a1b8-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="0a1b8-123">Siirry [PowerApps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="0a1b8-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="0a1b8-124">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-124">Select **Environments**.</span></span>
3. <span data-ttu-id="0a1b8-125">Valitse poistettava ympäristö.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="0a1b8-126">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="0a1b8-127">Odota, kunnes poisto on valmis.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="0a1b8-128">Kirjaudu sisään [Lifecycle Servicesiin](https://lcs.dynamics.com/Logon/Index) (LSC) samalla tilillä, jota käytit tilatessasi Talent-sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="0a1b8-129">Valitse ympäristön sisältävä Talent-projekti.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="0a1b8-130">Valitse LCS-projektin **Talent-sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="0a1b8-131">Valitse poistettava esiintymä.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="0a1b8-132">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="0a1b8-133">Voit poistaa Talent-ympäristön aiemmin luodusta PowerApps-ympäristöstä suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="0a1b8-134">Huomaa, että Talent DevOps -ryhmän tuki ja yhteydenottomahdollisuus on käytössä väliaikaisesti siihen asti, kunnes tämä toiminto on käytössä suoraan LCS-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="0a1b8-135">Aloita poistopyyntö ottamalla yhteyttä tukeen.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="0a1b8-136">Tukiryhmä tekee poistopyynnön Talent DevOps -ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="0a1b8-137">Jatka, kun saat tiedon ympäristön poistamisesta.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="0a1b8-138">Kirjaudu sisään LCS:ään samalla tilillä, jota käytit tilatessasi Talent-sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="0a1b8-139">Valitse ympäristön sisältävä Talent-projekti.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="0a1b8-140">Valitse LCS-projektin **Talent-sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="0a1b8-141">Valitse poistettava esiintymä, jonka käyttöottotilan merkintänä on oltava **Epäonnistui**.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="0a1b8-142">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="0a1b8-142">Select **Remove instance** and confirm your decision.</span></span> 

