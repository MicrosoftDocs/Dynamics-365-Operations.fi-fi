---
title: Poista esiintymä
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Human Resourcesin testi- tai tuotantoympäristön poistoprosessista.
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
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
ms.openlocfilehash: 0a8eac74f0d840251ab56445dd5af4d19d3c0490
ms.sourcegitcommit: f759d361fa505323b8b171a98024dca9cc9fa0f0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/07/2020
ms.locfileid: "3668322"
---
# <a name="remove-an-instance"></a><span data-ttu-id="54952-103">Poista esiintymä</span><span class="sxs-lookup"><span data-stu-id="54952-103">Remove an instance</span></span>

<span data-ttu-id="54952-104">Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Human Resourcesin testi- tai tuotantoympäristön poistoprosessista.</span><span class="sxs-lookup"><span data-stu-id="54952-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="54952-105">Testiympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="54952-105">Remove a test drive environment</span></span>

<span data-ttu-id="54952-106">Human Resourcesin testauksen valmistelussa on 60 päivän vanhentumiskäytäntö.</span><span class="sxs-lookup"><span data-stu-id="54952-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="54952-107">Testiympäristöjen omistajat voivat kuitenkin lopettaa kokeiluversion käytön aikaisemmin seuraavien vaiheiden avulla.</span><span class="sxs-lookup"><span data-stu-id="54952-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="54952-108">Siirry [Power Apps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="54952-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="54952-109">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="54952-109">Select **Environments**.</span></span>
3. <span data-ttu-id="54952-110">Valitse testiympäristö, jonka nimeämiskäytäntö on seuraavanlainen: TestDrive – alias@toimialue</span><span class="sxs-lookup"><span data-stu-id="54952-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="54952-111">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="54952-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="54952-112">Aiemmin luotu testausympäristö poistetaan.</span><span class="sxs-lookup"><span data-stu-id="54952-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="54952-113">Kun se on poistettu, voit tilata uuden testiympäristön</span><span class="sxs-lookup"><span data-stu-id="54952-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="54952-114">Tuotantoympäristön poistaminen</span><span class="sxs-lookup"><span data-stu-id="54952-114">Remove a production environment</span></span>

<span data-ttu-id="54952-115">Artikkelissa oletetaan, että olet ostanut Human Resourcesin pilvipalveluratkaisujen toimittajalta tai yritysarkkitehtuurisopimuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="54952-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="54952-116">Koska yksi Human Resources -ympäristö toimii yhden Power Apps-ympäristön sisällä, huomioon on otettava kaksi vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="54952-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="54952-117">Ensimmäinen vaihtoehto poistaa koko Power Apps-ympäristön, ja toinen vaihtoehto vain Human Resources -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="54952-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="54952-118">Ensimmäinen vaihtoehto on parempi, jos olet luonut Power Apps-ympäristön nimenomaan Human Resourcesin valmistelua varten ja olet vasta aloittanut käyttöönoton tai sinulla ei ole muodostettuja integraatioita.</span><span class="sxs-lookup"><span data-stu-id="54952-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="54952-119">Toinen vaihtoehto on parempi, kun olet muodostanut Power Apps -ympäristön, johon täytettyjä monipuolisia tietoja hyödynnetään Power Apps- ja Power Automate -ratkaisuissa.</span><span class="sxs-lookup"><span data-stu-id="54952-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="54952-120">Varmista ennen Power Apps-ympäristön poistamista, että sitä ei käytetä monipuolisissa tietojen integroinneissa Human Resources -sovelluksen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="54952-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="54952-121">Huomaa myös, että Power Apps-oletusympäristöjä ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="54952-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="54952-122">Koko Power Apps-ympäristön poistaminen, mukaan lukien Human Resources ja siihen liittyvät sovellukset ja työnkulut:</span><span class="sxs-lookup"><span data-stu-id="54952-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="54952-123">Siirry [Power Apps-hallintakeskukseen](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="54952-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="54952-124">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="54952-124">Select **Environments**.</span></span>
3. <span data-ttu-id="54952-125">Valitse poistettava ympäristö.</span><span class="sxs-lookup"><span data-stu-id="54952-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="54952-126">Valitse **Poista** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="54952-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="54952-127">Odota, kunnes poisto on valmis.</span><span class="sxs-lookup"><span data-stu-id="54952-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="54952-128">Kirjaudu sisään [Lifecycle Servicesiin](https://lcs.dynamics.com/Logon/Index) (LSC) samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="54952-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="54952-129">Valitse ympäristön sisältävä Human Resources -projekti.</span><span class="sxs-lookup"><span data-stu-id="54952-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="54952-130">Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="54952-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="54952-131">Valitse poistettava esiintymä.</span><span class="sxs-lookup"><span data-stu-id="54952-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="54952-132">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="54952-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="54952-133">Voit poistaa Human Resources -ympäristön aiemmin luodusta Power Apps-ympäristöstä suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="54952-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="54952-134">Huomaa, että Human Resources DevOps -ryhmän tuki ja yhteydenottomahdollisuus on käytössä väliaikaisesti siihen asti, kunnes tämä toiminto on käytössä suoraan LCS-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="54952-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="54952-135">Aloita poistopyyntö ottamalla yhteyttä tukeen.</span><span class="sxs-lookup"><span data-stu-id="54952-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="54952-136">Tukiryhmä tekee poistopyynnön Human Resources DevOps -ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="54952-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="54952-137">Jatka, kun saat tiedon ympäristön poistamisesta.</span><span class="sxs-lookup"><span data-stu-id="54952-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="54952-138">Kirjaudu sisään LCS:ään samalla tilillä, jota käytit tilatessasi Human Resources -sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="54952-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="54952-139">Valitse ympäristön sisältävä Human Resources -projekti.</span><span class="sxs-lookup"><span data-stu-id="54952-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="54952-140">Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="54952-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="54952-141">Valitse poistettava esiintymä, jonka käyttöottotilan merkintänä on oltava **Poistettu**.</span><span class="sxs-lookup"><span data-stu-id="54952-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="54952-142">Valitse **Poista esiintymä** ja vahvista valinta.</span><span class="sxs-lookup"><span data-stu-id="54952-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="54952-143">Alustavasti poistetun ympäristön palauttaminen</span><span class="sxs-lookup"><span data-stu-id="54952-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="54952-144">Jos poistat Power Apps -ympäristön, johon Human Resources -ympäristö on yhdistetty, Human Resources -ympäristön tila Lifecycle Services -sovelluksessa on **Alustavasti poistettu**.</span><span class="sxs-lookup"><span data-stu-id="54952-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="54952-145">Tässä tapauksessa käyttäjät eivät voi muodostaa yhteyttä Human Resources -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="54952-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="54952-146">Voit palauttaa ympäristön seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="54952-146">To restore the environment:</span></span>

1. <span data-ttu-id="54952-147">Seuraa ohjeita kohdassa [Power Apps -ympäristön palauttaminen](/power-platform/admin/recover-environment.md).</span><span class="sxs-lookup"><span data-stu-id="54952-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="54952-148">Ota yhteyttä tukeen, jos haluat palauttaa Human Resources -ympäristön.</span><span class="sxs-lookup"><span data-stu-id="54952-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="54952-149">Lisätietoja on kohdassa [Pyydä tukea](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="54952-149">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="54952-150">Power Apps -ympäristöjä säilytetään vain seitsemän päivää poiston jälkeen.</span><span class="sxs-lookup"><span data-stu-id="54952-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="54952-151">Ympäristö on palautettava seitsemän päivän kuluessa.</span><span class="sxs-lookup"><span data-stu-id="54952-151">You must recover the environment within the seven day period.</span></span>
