---
title: Määritä tehtävien eriyttäminen
description: Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40b40b77877680e28671b7a15ea8c8b58ce94417
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180872"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="5052f-103">Määritä tehtävien eriyttäminen</span><span class="sxs-lookup"><span data-stu-id="5052f-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5052f-104">Voit määrittää sääntöjä erottamaan tehtävät, joilla on oltava eri käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="5052f-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="5052f-105">Tätä kutsutaan tehtävien eriyttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="5052f-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="5052f-106">Et ehkä esimerkiksi halua, että sama henkilö kuittaa tavaroiden vastaanottamisen ja käsittelee maksua toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="5052f-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="5052f-107">Tehtävien eriyttäminen auttaa vähentämään petosriskiä. Lisäksi se auttaa havaitsemaan virheet tai väärinkäytökset.</span><span class="sxs-lookup"><span data-stu-id="5052f-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="5052f-108">Voit myös varmistaa tehtävien eriyttämisen avulla, että sisäisiä valvontakäytäntöjä noudatetaan.</span><span class="sxs-lookup"><span data-stu-id="5052f-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="5052f-109">Lue sääntö seuraavalla menettelyllä.</span><span class="sxs-lookup"><span data-stu-id="5052f-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="5052f-110">Sinun on oltava järjestelmänvalvoja, jotta voit suorittaa menettelyn.</span><span class="sxs-lookup"><span data-stu-id="5052f-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="5052f-111">Tämän menettelyn luomisessa käytetty esittely-yritys on DAT.</span><span class="sxs-lookup"><span data-stu-id="5052f-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="5052f-112">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Suojaus > Tehtävien eriyttäminen > Tehtävien eriyttämisen säännöt**.</span><span class="sxs-lookup"><span data-stu-id="5052f-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="5052f-113">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5052f-113">Click **New**.</span></span>
3. <span data-ttu-id="5052f-114">Kirjoita säännön arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5052f-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="5052f-115">Avaa haku napsauttamalla **Ensimmäinen tehtävä** -kentästä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="5052f-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5052f-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5052f-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="5052f-117">Valitse ensimmäinen säännön ohjaama tehtävä.</span><span class="sxs-lookup"><span data-stu-id="5052f-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="5052f-118">Avaa haku napsauttamalla **Toinen tehtävä** -kentästä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="5052f-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="5052f-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5052f-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="5052f-120">Valitse toinen säännön ohjaama tehtävä.</span><span class="sxs-lookup"><span data-stu-id="5052f-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="5052f-121">Valitse vaihtoehto **Vakavuusaste**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="5052f-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="5052f-122">Valitse riskin vakavuustaso, jos sama käyttäjä tai rooli suorittaa molemmat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="5052f-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="5052f-123">Kirjoita **Suojausriski**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5052f-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="5052f-124">Anna turvallisuusriskin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5052f-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="5052f-125">Kirjoita **Suojauksen mitätöinti** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5052f-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="5052f-126">Anna kuvaus toiminnoista, joilla lievennät turvallisuusriskiä.</span><span class="sxs-lookup"><span data-stu-id="5052f-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="5052f-127">Voit lieventää riskiä esimerkiksi arvioimalla prosessin tarkasti, suorittamalla esimiestason arvioinnin kerran kuukaudessa tai jakamalla resurssit muiden osastojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="5052f-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="5052f-128">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5052f-128">Click **Save**.</span></span>

