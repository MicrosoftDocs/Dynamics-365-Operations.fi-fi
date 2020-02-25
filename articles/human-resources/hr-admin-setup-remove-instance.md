---
title: Esiintymän poistaminen
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008835"
---
# <a name="remove-an-instance"></a><span data-ttu-id="28877-102">Esiintymän poistaminen</span><span class="sxs-lookup"><span data-stu-id="28877-102">Remove an instance</span></span>

<span data-ttu-id="28877-103">Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Human Resourcesin testi- tai tuotantoympäristön poistoprosessista.</span><span class="sxs-lookup"><span data-stu-id="28877-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="28877-104">Testiympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="28877-104">Remove a test drive environment</span></span>

<span data-ttu-id="28877-105">Human Resourcesin testauksen valmistelussa on 60 päivän vanhentumiskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="28877-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="28877-106">Testiympäristöjen omistajat voivat kuitenkin lopettaa kokeiluversion käytön aikaisemmin seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="28877-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="28877-107">Siirry [Power Apps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="28877-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="28877-108">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="28877-108">Select **Environments**.</span></span>
3. <span data-ttu-id="28877-109">Valitse testiympäristö, jonka nimeämiskäytäntö on seuraavanlainen: TestDrive – alias@toimialue</span><span class="sxs-lookup"><span data-stu-id="28877-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="28877-110">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="28877-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="28877-111">Aiemmin luotu testausympäristö poistetaan.</span><span class="sxs-lookup"><span data-stu-id="28877-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="28877-112">Kun se on poistettu, voit tilata uuden testiympäristön</span><span class="sxs-lookup"><span data-stu-id="28877-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="28877-113">Tuotantoympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="28877-113">Remove a production environment</span></span>

<span data-ttu-id="28877-114">Artikkelissa oletetaan, että olet ostanut Human Resourcesin pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="28877-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="28877-115">Koska yksi Human Resources -ympäristö toimii yhden Power Apps-ympäristön sisällä, huomioon on otettava kaksi vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="28877-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="28877-116">Ensimmäinen vaihtoehto poistaa koko Power Apps-ympäristön, ja toinen vaihtoehto vain Human Resources -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="28877-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="28877-117">Ensimmäinen vaihtoehto on parempi, jos olet luonut Power Apps-ympäristön nimenomaan Human Resourcesin valmistelua varten ja olet vasta aloittanut käyttöönoton tai sinulla ei ole muodostettuja integraatioita.</span><span class="sxs-lookup"><span data-stu-id="28877-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="28877-118">Toinen vaihtoehto on parempi, kun olet muodostanut Power Apps -ympäristön, johon täytettyjä monipuolisia tietoja hyödynnetään Power Apps- ja Power Automate -ratkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="28877-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="28877-119">Varmista ennen Power Apps-ympäristön poistamista, että sitä ei käytetä monipuolisissa tietojen integroinneissa Human Resources -sovelluksen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="28877-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="28877-120">Huomaa myös, että Power Apps-oletusympäristöjä ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="28877-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="28877-121">Koko Power Apps-ympäristön poistaminen, mukaan lukien Human Resources ja siihen liittyvät sovellukset ja työnkulut:</span><span class="sxs-lookup"><span data-stu-id="28877-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="28877-122">Siirry [Power Apps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="28877-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="28877-123">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="28877-123">Select **Environments**.</span></span>
3. <span data-ttu-id="28877-124">Valitse poistettava ympäristö.</span><span class="sxs-lookup"><span data-stu-id="28877-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="28877-125">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="28877-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="28877-126">Odota, kunnes poisto on valmis.</span><span class="sxs-lookup"><span data-stu-id="28877-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="28877-127">Kirjaudu sisään [Lifecycle Servicesiin](https://lcs.dynamics.com/Logon/Index) (LSC) samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="28877-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="28877-128">Valitse ympäristön sisältävä Human Resources -projekti.</span><span class="sxs-lookup"><span data-stu-id="28877-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="28877-129">Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="28877-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="28877-130">Valitse poistettava esiintymä.</span><span class="sxs-lookup"><span data-stu-id="28877-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="28877-131">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="28877-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="28877-132">Voit poistaa Human Resources -ympäristön aiemmin luodusta Power Apps-ympäristöstä suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="28877-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="28877-133">Huomaa, että Human Resources DevOps -ryhmän tuki ja yhteydenottomahdollisuus on käytössä väliaikaisesti siihen asti, kunnes tämä toiminto on käytössä suoraan LCS-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="28877-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="28877-134">Aloita poistopyyntö ottamalla yhteyttä tukeen.</span><span class="sxs-lookup"><span data-stu-id="28877-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="28877-135">Tukiryhmä tekee poistopyynnön Human Resources DevOps -ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="28877-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="28877-136">Jatka, kun saat tiedon ympäristön poistamisesta.</span><span class="sxs-lookup"><span data-stu-id="28877-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="28877-137">Kirjaudu sisään LCS:ään samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="28877-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="28877-138">Valitse ympäristön sisältävä Human Resources -projekti.</span><span class="sxs-lookup"><span data-stu-id="28877-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="28877-139">Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="28877-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="28877-140">Valitse poistettava esiintymä, jonka käyttöottotilan merkintänä on oltava **Epäonnistui**.</span><span class="sxs-lookup"><span data-stu-id="28877-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="28877-141">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="28877-141">Select **Remove instance** and confirm your decision.</span></span> 
