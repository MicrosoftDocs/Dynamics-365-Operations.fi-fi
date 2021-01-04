---
title: Määritä tehtävien eriyttäminen
description: Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688170"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="e8a79-103">Määritä tehtävien eriyttäminen</span><span class="sxs-lookup"><span data-stu-id="e8a79-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8a79-104">Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="e8a79-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="e8a79-105">Tätä kutsutaan tehtävien eriyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="e8a79-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="e8a79-106">Et ehkä esimerkiksi halua, että sama henkilö kuittaa tavaroiden vastaanottamisen ja käsittelee maksua toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="e8a79-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="e8a79-107">Tehtävien eriyttäminen auttaa vähentämään petosriskiä. Lisäksi se auttaa havaitsemaan virheet tai väärinkäytökset.</span><span class="sxs-lookup"><span data-stu-id="e8a79-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="e8a79-108">Voit myös varmistaa tehtävien eriyttämisen avulla, että sisäisiä valvontakäytäntöjä noudatetaan.</span><span class="sxs-lookup"><span data-stu-id="e8a79-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="e8a79-109">Lue sääntö seuraavalla menettelyllä.</span><span class="sxs-lookup"><span data-stu-id="e8a79-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="e8a79-110">Sinun on oltava järjestelmänvalvoja, jotta voit suorittaa menettelyn.</span><span class="sxs-lookup"><span data-stu-id="e8a79-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="e8a79-111">Tämän menettelyn luomisessa käytetty esittely-yritys on DAT.</span><span class="sxs-lookup"><span data-stu-id="e8a79-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="e8a79-112">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen säännöt**.</span><span class="sxs-lookup"><span data-stu-id="e8a79-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="e8a79-113">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e8a79-113">Click **New**.</span></span>
3. <span data-ttu-id="e8a79-114">Kirjoita säännön arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e8a79-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="e8a79-115">Avaa haku napsauttamalla **Ensimmäinen tehtävä** -kentästä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="e8a79-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e8a79-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e8a79-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="e8a79-117">Valitse ensimmäinen säännön ohjaama tehtävä.</span><span class="sxs-lookup"><span data-stu-id="e8a79-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="e8a79-118">Avaa haku napsauttamalla **Toinen tehtävä** -kentästä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="e8a79-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="e8a79-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e8a79-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="e8a79-120">Valitse toinen säännön ohjaama tehtävä.</span><span class="sxs-lookup"><span data-stu-id="e8a79-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="e8a79-121">Valitse vaihtoehto **Vakavuusaste**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="e8a79-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="e8a79-122">Valitse riskin vakavuustaso, jos sama käyttäjä tai rooli suorittaa molemmat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="e8a79-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="e8a79-123">Kirjoita **Suojausriski**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e8a79-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="e8a79-124">Anna turvallisuusriskin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="e8a79-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="e8a79-125">Kirjoita **Suojauksen mitätöinti** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e8a79-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="e8a79-126">Anna kuvaus toiminnoista, joilla lievennät turvallisuusriskiä.</span><span class="sxs-lookup"><span data-stu-id="e8a79-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="e8a79-127">Voit lieventää riskiä esimerkiksi arvioimalla prosessin tarkasti, suorittamalla esimiestason arvioinnin kerran kuukaudessa tai jakamalla resurssit muiden osastojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="e8a79-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="e8a79-128">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e8a79-128">Click **Save**.</span></span>

