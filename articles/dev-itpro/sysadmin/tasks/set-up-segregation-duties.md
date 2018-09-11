--- 
title: "Määritä tehtävien eriyttäminen"
description: "Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 0e20272f09cc8c75bdd93ebcc996cf58b98ccf67
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="320b4-103">Määritä tehtävien eriyttäminen</span><span class="sxs-lookup"><span data-stu-id="320b4-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="320b4-104">Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="320b4-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="320b4-105">Tätä kutsutaan tehtävien eriyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="320b4-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="320b4-106">Et ehkä esimerkiksi halua, että sama henkilö kuittaa tavaroiden vastaanottamisen ja käsittelee maksua toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="320b4-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="320b4-107">Tehtävien eriyttäminen auttaa vähentämään petosriskiä. Lisäksi se auttaa havaitsemaan virheet tai väärinkäytökset.</span><span class="sxs-lookup"><span data-stu-id="320b4-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="320b4-108">Voit myös varmistaa tehtävien eriyttämisen avulla, että sisäisiä valvontakäytäntöjä noudatetaan.</span><span class="sxs-lookup"><span data-stu-id="320b4-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="320b4-109">Lue sääntö seuraavalla menettelyllä.</span><span class="sxs-lookup"><span data-stu-id="320b4-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="320b4-110">Sinun on oltava järjestelmänvalvoja, jotta voit suorittaa menettelyn.</span><span class="sxs-lookup"><span data-stu-id="320b4-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="320b4-111">Tämän menettelyn luomisessa käytetty esittely-yritys on DAT.</span><span class="sxs-lookup"><span data-stu-id="320b4-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="320b4-112">Valitse Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen säännöt.</span><span class="sxs-lookup"><span data-stu-id="320b4-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="320b4-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="320b4-113">Click New.</span></span>
3. <span data-ttu-id="320b4-114">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="320b4-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="320b4-115">Anna säännön nimi.</span><span class="sxs-lookup"><span data-stu-id="320b4-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="320b4-116">Avaa haku napsauttamalla Ensimmäinen tehtävä -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="320b4-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="320b4-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="320b4-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="320b4-118">Valitse ensimmäinen säännön ohjaama tehtävä.</span><span class="sxs-lookup"><span data-stu-id="320b4-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="320b4-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="320b4-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="320b4-120">Avaa haku napsauttamalla Toinen tehtävä -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="320b4-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="320b4-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="320b4-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="320b4-122">Valitse toinen säännön ohjaama tehtävä.</span><span class="sxs-lookup"><span data-stu-id="320b4-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="320b4-123">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="320b4-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="320b4-124">Valitse vaihtoehto Vakavuusaste-kentässä.</span><span class="sxs-lookup"><span data-stu-id="320b4-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="320b4-125">Valitse riskin vakavuustaso, jos sama käyttäjä tai rooli suorittaa molemmat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="320b4-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="320b4-126">Kirjoita Suojausriski-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="320b4-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="320b4-127">Anna turvallisuusriskin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="320b4-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="320b4-128">Kirjoita Suojauksen mitätöinti -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="320b4-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="320b4-129">Anna kuvaus toiminnoista, joilla lievennät turvallisuusriskiä.</span><span class="sxs-lookup"><span data-stu-id="320b4-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="320b4-130">Voit lieventää riskiä esimerkiksi arvioimalla prosessin tarkasti, suorittamalla esimiestason arvioinnin kerran kuukaudessa tai jakamalla resurssit muiden osastojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="320b4-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="320b4-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="320b4-131">Click Save.</span></span>


