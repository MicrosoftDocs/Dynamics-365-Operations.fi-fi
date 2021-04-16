---
title: Määritä tehtävien eriyttäminen
description: Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745738"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="a1a01-103">Määritä tehtävien eriyttäminen</span><span class="sxs-lookup"><span data-stu-id="a1a01-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1a01-104">Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="a1a01-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="a1a01-105">Tätä kutsutaan tehtävien eriyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="a1a01-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="a1a01-106">Et ehkä esimerkiksi halua, että sama henkilö kuittaa tavaroiden vastaanottamisen ja käsittelee maksua toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="a1a01-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="a1a01-107">Tehtävien eriyttäminen auttaa vähentämään petosriskiä. Lisäksi se auttaa havaitsemaan virheet tai väärinkäytökset.</span><span class="sxs-lookup"><span data-stu-id="a1a01-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="a1a01-108">Voit myös varmistaa tehtävien eriyttämisen avulla, että sisäisiä valvontakäytäntöjä noudatetaan.</span><span class="sxs-lookup"><span data-stu-id="a1a01-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="a1a01-109">Lue sääntö seuraavalla menettelyllä.</span><span class="sxs-lookup"><span data-stu-id="a1a01-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="a1a01-110">Sinun on oltava järjestelmänvalvoja, jotta voit suorittaa menettelyn.</span><span class="sxs-lookup"><span data-stu-id="a1a01-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="a1a01-111">Valitse **Järjestelmänhallinta** > **Suojaus** > **Tehtävien eriyttäminen** > **Tehtävien eriyttämisen säännöt**.</span><span class="sxs-lookup"><span data-stu-id="a1a01-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="a1a01-112">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a1a01-112">Click **New**.</span></span>
3. <span data-ttu-id="a1a01-113">Kirjoita säännön arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a1a01-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="a1a01-114">Avaa haku napsauttamalla **Ensimmäinen tehtävä** -kentästä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a1a01-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a1a01-115">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a1a01-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="a1a01-116">Valitse ensimmäinen säännön ohjaama tehtävä.</span><span class="sxs-lookup"><span data-stu-id="a1a01-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="a1a01-117">Avaa haku napsauttamalla **Toinen tehtävä** -kentästä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="a1a01-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="a1a01-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a1a01-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="a1a01-119">Valitse toinen säännön ohjaama tehtävä.</span><span class="sxs-lookup"><span data-stu-id="a1a01-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="a1a01-120">Valitse vaihtoehto **Vakavuusaste**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="a1a01-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="a1a01-121">Valitse riskin vakavuustaso, jos sama käyttäjä tai rooli suorittaa molemmat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="a1a01-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="a1a01-122">Kirjoita **Suojausriski**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a1a01-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="a1a01-123">Anna turvallisuusriskin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="a1a01-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="a1a01-124">Kirjoita **Suojauksen mitätöinti** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a1a01-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="a1a01-125">Anna kuvaus toiminnoista, joilla lievennät turvallisuusriskiä.</span><span class="sxs-lookup"><span data-stu-id="a1a01-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="a1a01-126">Voit lieventää riskiä esimerkiksi arvioimalla prosessin tarkasti, suorittamalla esimiestason arvioinnin kerran kuukaudessa tai jakamalla resurssit muiden osastojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="a1a01-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="a1a01-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a1a01-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="a1a01-128">Tehtävien eriyttämisen sääntöjen noudattamista ei ole tarkistettu sääntöä luotaessa.</span><span class="sxs-lookup"><span data-stu-id="a1a01-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="a1a01-129">Voit luoda säännön, joka luo ristiriidan aiemmin luoduille rooleille.</span><span class="sxs-lookup"><span data-stu-id="a1a01-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="a1a01-130">Myös aiemmin luodut käyttäjän roolimääritykset voivat olla ristiriidassa uuden säännön kanssa.</span><span class="sxs-lookup"><span data-stu-id="a1a01-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="a1a01-131">Vaatimustenmukaisuus on tarkistettava, kun sääntö luodaan tai sitä muokataan.</span><span class="sxs-lookup"><span data-stu-id="a1a01-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="a1a01-132">Lisätietoja on kohdassa [Tehtävien eriyttämisen ristiriitojen tunnistaminen ja ratkaiseminen](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="a1a01-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]