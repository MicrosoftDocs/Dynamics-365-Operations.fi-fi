---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (7. tammikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974427"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="e422e-103">Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (7. tammikuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="e422e-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="e422e-104">Tässä artikkelissa käsitellään Dynamics 365 Talentin uusia tai muuttuneita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="e422e-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="e422e-105">Attractin muutokset</span><span class="sxs-lookup"><span data-stu-id="e422e-105">Changes in Attract</span></span>

<span data-ttu-id="e422e-106">Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="e422e-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="e422e-107">Onboardin muutokset</span><span class="sxs-lookup"><span data-stu-id="e422e-107">Changes in Onboard</span></span>

<span data-ttu-id="e422e-108">Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="e422e-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="e422e-109">Core HR:n muutokset</span><span class="sxs-lookup"><span data-stu-id="e422e-109">Changes in Core HR</span></span>

<span data-ttu-id="e422e-110">Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="e422e-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="e422e-111">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.</span><span class="sxs-lookup"><span data-stu-id="e422e-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="e422e-112">Työntekijöitä, joilla ei ole työtietoja, ei voi poistaa - (386157)</span><span class="sxs-lookup"><span data-stu-id="e422e-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="e422e-113">Tämä muutos lisää poistovaihtoehdon **Työntekijät, joilla ei ole työtä**-muotoa.</span><span class="sxs-lookup"><span data-stu-id="e422e-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="e422e-114">Työntekijät näkyvät tässä lomakkeessa, kun työntekijälle ei ole tulevia, aktiivisia tai historiallisia työtehtäviä.</span><span class="sxs-lookup"><span data-stu-id="e422e-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="e422e-115">Tässä versiossa Delete-toiminto on käytössä vain järjestelmänvalvojille.</span><span class="sxs-lookup"><span data-stu-id="e422e-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="e422e-116">Ensi viikon versiossa suojaus päivitetään kuitenkin siten, että kaikki käyttäjät, joilla on HR-assistenttirooli, voivat poistaa työntekijöitä ilman työtehtävää.</span><span class="sxs-lookup"><span data-stu-id="e422e-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="e422e-117">Voit tehdä nämä muutokset myös manuaalisesti noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e422e-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="e422e-118">Mene kohtaan **Suojauskonfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="e422e-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="e422e-119">Suodata**Oikeudet**-välilehdessä **Oikeudet**-luettelo ja **Ylläpidä työntekijöitä**.</span><span class="sxs-lookup"><span data-stu-id="e422e-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="e422e-120">Valitse **viitteet**-sarakkeesta **Näytä valikon vaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="e422e-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="e422e-121">Valitse **Näytä valikon vaihtoehdot**-sarakkeesta **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="e422e-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="e422e-122">Määritä **Poisto**-oikeuden myöntäminen.</span><span class="sxs-lookup"><span data-stu-id="e422e-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="e422e-123">Valitse **Julkaisemattomat objektit** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="e422e-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="e422e-124">Valitse **Julkaise kaikki**.</span><span class="sxs-lookup"><span data-stu-id="e422e-124">Select **Publish all**.</span></span>
