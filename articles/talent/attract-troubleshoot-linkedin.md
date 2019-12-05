---
title: LinkedInin ja Microsoft Dynamics 365 Talent – Attractin integroinnin vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien vianmääritystä, jotka koskevat työpaikkojen julkaisua LinkedIniin Microsoft Dynamics 365 Talent – Attractista.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 42065f3d6b7ae9e7ad99b26c7692e41f8c36934d
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832974"
---
# <a name="troubleshoot-integration-with-linkedin-and-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="7bca6-103">LinkedInin ja Microsoft Dynamics 365 Talent – Attractin integroinnin vianmääritys</span><span class="sxs-lookup"><span data-stu-id="7bca6-103">Troubleshoot integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7bca6-104">Tee seuraavien tietojen avulla sellaisten ongelmien vianmääritys, joita voi esiintyä, kun yrität julkaista työpaikkoja LinkedIniin Microsoft Dynamics 365 Talent: Attractista.</span><span class="sxs-lookup"><span data-stu-id="7bca6-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="7bca6-105">Kirjautuminen LinkedIniin Attractista ei onnistu</span><span class="sxs-lookup"><span data-stu-id="7bca6-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="7bca6-106">Jos kirjautumisessa LinkedIniin Attractista on ongelmia, yritä seuraavia toimenpiteitä:</span><span class="sxs-lookup"><span data-stu-id="7bca6-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="7bca6-107">Varmista, että LinkedIn-tunnistetiedot, jotka olet määrittänyt Attractissa, ovat voimassa ja oikeat.</span><span class="sxs-lookup"><span data-stu-id="7bca6-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="7bca6-108">Jos tunnistetiedot ovat voimassa ja oikein, ota yhteyttä [LinkedInin tukeen](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="7bca6-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="7bca6-109">Jos ongelma ei ratkea, ota yhteyttä [Microsoftin tukeen](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="7bca6-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="7bca6-110">Attractista julkaistut työpaikat eivät näy LinkedInissä</span><span class="sxs-lookup"><span data-stu-id="7bca6-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="7bca6-111">Jos työpaikka ei näy LinkedInissä 24 tunnin jälkeen, kokeile seuraavia toimenpiteitä:</span><span class="sxs-lookup"><span data-stu-id="7bca6-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="7bca6-112">Varmista, että LinkedIn-yritystunnus yhdistetään LinkedIn-yrityssivulle ja että se on annettu oikein Attractin hallintakeskukseen.</span><span class="sxs-lookup"><span data-stu-id="7bca6-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="7bca6-113">Lisätietoja LinkedIn-asetusten muuttamisesta hallintakeskuksessa on kohdassa [Microsoft Dynamics 365 Talent – Attractin LinkedIn-integraation määrittäminen](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="7bca6-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md).</span></span> <span data-ttu-id="7bca6-114">Lisätietoja LinkedIn-yritystunnuksista on kohdassa [LinkedIn-yritystunnuksen liittäminen LinkedIn-työpaikkailmoitussivulle – usein kysyttyjä kysymyksiä](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="7bca6-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="7bca6-115">Tarkista työpaikan tiedot LinkedInissä ja varmista, että osoite on täydellinen.</span><span class="sxs-lookup"><span data-stu-id="7bca6-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="7bca6-116">Työpaikan onnistunut julkaisu edellyttää, että LinkedInissä on ainakin työpaikan kaupunki ja maa tai alue.</span><span class="sxs-lookup"><span data-stu-id="7bca6-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="7bca6-117">Varmista, että työpaikka ei ole toisen LinkedInissä julkaistun työpaikan kaksoiskappale.</span><span class="sxs-lookup"><span data-stu-id="7bca6-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="7bca6-118">LinkedIn ei julkaise työpaikkoja, jotka ovat toisen rekrytoijan LinkedInin Premium-työpaikkojen tai rajoitettujen listausten kaksoiskappaleita.</span><span class="sxs-lookup"><span data-stu-id="7bca6-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="7bca6-119">Varmista, ettei joku muu yrityksen työntekijä ole jo julkaissut työpaikkaa manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="7bca6-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bca6-120">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="7bca6-120">See also</span></span>

[<span data-ttu-id="7bca6-121">Attractin LinkedIn-integraation usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="7bca6-121">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="7bca6-122">Työpaikkojen julkaiseminen LinkedInissä Microsoft Dynamics 365 Talent – Attractista</span><span class="sxs-lookup"><span data-stu-id="7bca6-122">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="7bca6-123">Ehdokkaiden rekrytointi LinkedIn Recruiterilla Microsoft Dynamics 365 Talent – Attractissa</span><span class="sxs-lookup"><span data-stu-id="7bca6-123">Source candidates with LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="7bca6-124">Työpaikkojen luominen, hyväksyminen ja julkaiseminen Attractissa</span><span class="sxs-lookup"><span data-stu-id="7bca6-124">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="7bca6-125">LinkedInin ja Microsoft Dynamics 365 Talent – Attractin integroinnin vianmääritys</span><span class="sxs-lookup"><span data-stu-id="7bca6-125">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
