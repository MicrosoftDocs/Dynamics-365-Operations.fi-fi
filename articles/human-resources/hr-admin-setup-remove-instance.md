---
title: Poista esiintymä
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Human Resourcesin testi- tai tuotantoympäristön poistoprosessista.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17f299f81d1326dfb06c11a6125acc54b8ef2a6e
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431196"
---
# <a name="remove-an-instance"></a><span data-ttu-id="cce65-103">Poista esiintymä</span><span class="sxs-lookup"><span data-stu-id="cce65-103">Remove an instance</span></span>

<span data-ttu-id="cce65-104">Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Human Resourcesin testi- tai tuotantoympäristön poistoprosessista.</span><span class="sxs-lookup"><span data-stu-id="cce65-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="cce65-105">Testiympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="cce65-105">Remove a test drive environment</span></span>

<span data-ttu-id="cce65-106">Human Resourcesin testauksen valmistelussa on 60 päivän vanhentumiskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="cce65-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="cce65-107">Testiympäristöjen omistajat voivat kuitenkin lopettaa kokeiluversion käytön aikaisemmin seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="cce65-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="cce65-108">Siirry [Power Apps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="cce65-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="cce65-109">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="cce65-109">Select **Environments**.</span></span>
3. <span data-ttu-id="cce65-110">Valitse testiympäristö, jonka nimeämiskäytäntö on seuraavanlainen: TestDrive – alias@toimialue</span><span class="sxs-lookup"><span data-stu-id="cce65-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="cce65-111">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="cce65-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="cce65-112">Aiemmin luotu testausympäristö poistetaan.</span><span class="sxs-lookup"><span data-stu-id="cce65-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="cce65-113">Kun se on poistettu, voit tilata uuden testiympäristön</span><span class="sxs-lookup"><span data-stu-id="cce65-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="cce65-114">Tuotantoympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="cce65-114">Remove a production environment</span></span>

<span data-ttu-id="cce65-115">Artikkelissa oletetaan, että olet ostanut Human Resourcesin pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="cce65-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="cce65-116">Koska yksi Human Resources -ympäristö toimii yhden Power Apps-ympäristön sisällä, huomioon on otettava kaksi vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="cce65-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="cce65-117">Ensimmäinen vaihtoehto poistaa koko Power Apps-ympäristön, ja toinen vaihtoehto vain Human Resources -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="cce65-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="cce65-118">Ensimmäinen vaihtoehto on parempi, jos olet luonut Power Apps-ympäristön nimenomaan Human Resourcesin valmistelua varten ja olet vasta aloittanut käyttöönoton tai sinulla ei ole muodostettuja integraatioita.</span><span class="sxs-lookup"><span data-stu-id="cce65-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="cce65-119">Toinen vaihtoehto on parempi, kun olet muodostanut Power Apps -ympäristön, johon täytettyjä monipuolisia tietoja hyödynnetään Power Apps- ja Power Automate -ratkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="cce65-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="cce65-120">Varmista ennen Power Apps-ympäristön poistamista, että sitä ei käytetä monipuolisissa tietojen integroinneissa Human Resources -sovelluksen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="cce65-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="cce65-121">Huomaa myös, että Power Apps-oletusympäristöjä ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="cce65-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="cce65-122">Koko Power Apps-ympäristön poistaminen, mukaan lukien Human Resources ja siihen liittyvät sovellukset ja työnkulut:</span><span class="sxs-lookup"><span data-stu-id="cce65-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="cce65-123">Siirry [Power Apps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="cce65-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="cce65-124">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="cce65-124">Select **Environments**.</span></span>
3. <span data-ttu-id="cce65-125">Valitse poistettava ympäristö.</span><span class="sxs-lookup"><span data-stu-id="cce65-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="cce65-126">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="cce65-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="cce65-127">Odota, kunnes poisto on valmis.</span><span class="sxs-lookup"><span data-stu-id="cce65-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="cce65-128">Kirjaudu sisään [Lifecycle Servicesiin](https://lcs.dynamics.com/Logon/Index) (LSC) samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="cce65-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="cce65-129">Valitse ympäristön sisältävä Human Resources -projekti.</span><span class="sxs-lookup"><span data-stu-id="cce65-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="cce65-130">Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="cce65-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="cce65-131">Valitse poistettava esiintymä.</span><span class="sxs-lookup"><span data-stu-id="cce65-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="cce65-132">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="cce65-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="cce65-133">Voit poistaa Human Resources -ympäristön aiemmin luodusta Power Apps-ympäristöstä suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="cce65-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="cce65-134">Huomaa, että Human Resources DevOps -ryhmän tuki ja yhteydenottomahdollisuus on käytössä väliaikaisesti siihen asti, kunnes tämä toiminto on käytössä suoraan LCS-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cce65-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="cce65-135">Aloita poistopyyntö ottamalla yhteyttä tukeen.</span><span class="sxs-lookup"><span data-stu-id="cce65-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="cce65-136">Tukiryhmä tekee poistopyynnön Human Resources DevOps -ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="cce65-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="cce65-137">Jatka, kun saat tiedon ympäristön poistamisesta.</span><span class="sxs-lookup"><span data-stu-id="cce65-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="cce65-138">Kirjaudu sisään LCS:ään samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="cce65-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="cce65-139">Valitse ympäristön sisältävä Human Resources -projekti.</span><span class="sxs-lookup"><span data-stu-id="cce65-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="cce65-140">Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="cce65-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="cce65-141">Valitse poistettava esiintymä, jonka käyttöottotilan merkintänä on oltava **Epäonnistui**.</span><span class="sxs-lookup"><span data-stu-id="cce65-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="cce65-142">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="cce65-142">Select **Remove instance** and confirm your decision.</span></span> 
