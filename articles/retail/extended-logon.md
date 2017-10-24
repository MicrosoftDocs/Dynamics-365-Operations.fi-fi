---
title: "Jatketun sisäänkirjautumisen määrittäminen pilvimyyntipisteelle ja myyntipisteelle"
description: "Tässä aiheessa käsitellään Cloud POS:n ja Retail Modern POS:n (MPOS) laajennetun kirjautumisen määrittämistä."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e29aea4509dd323c295b02f289fbcfa46fab3392
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a><span data-ttu-id="cbd9c-103">Jatketun sisäänkirjautumisen määrittäminen pilvimyyntipisteelle ja myyntipisteelle</span><span class="sxs-lookup"><span data-stu-id="cbd9c-103">Set up extended logon functionality for Cloud POS and MPOS</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="cbd9c-104">Tässä aiheessa käsitellään Cloud POS:n ja Retail Modern POS:n (MPOS) laajennetun kirjautumisen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

<a name="setting-up-extended-logon"></a><span data-ttu-id="cbd9c-105">Jatketun sisäänkirjautumisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cbd9c-105">Setting up extended logon</span></span>
=========================

<span data-ttu-id="cbd9c-106">Viivakoodimuotojen asetukset ovat **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipisteen profiilit** &gt; **Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-106">You can find the setup for bar code masks at **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="cbd9c-107">**Toiminnot**-pikavälilehti sisältää seuraavat jatkettuun sisäänkirjautumiseen liittyvät asetukset.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="cbd9c-108">Henkilökunnan viivakoodisisäänkirjautuminen</span><span class="sxs-lookup"><span data-stu-id="cbd9c-108">Staff bar code logon</span></span>

<span data-ttu-id="cbd9c-109">Kun **Henkilökunnan viivakoodisisäänkirjautuminen** -asetus on käytössä, työntekijät, joiden myyntipisteen sisäänkirjautumisen tunnistetietoihin on määritetty jatkettu sisäänkirjautuminen, voivat kirjautua sisään viivakoodin avulla.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="cbd9c-110">Henkilökunnan viivakoodisisäänkirjautumisessa tarvitaan salasana</span><span class="sxs-lookup"><span data-stu-id="cbd9c-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="cbd9c-111">Kun **Henkilökunnan viivakoodisisäänkirjautumisessa tarvitaan salasana** -asetus on käytössä, henkilökunnan viivakoodisisäänkirjautuminen valitsee vain työntekijän, jolle on määritetty esitetty jatkettu sisäänkirjautuminen.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="cbd9c-112">Työntekijöiden on silti syötettävä salasanansa, kun tämä asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="cbd9c-113">Henkilökunnan korttisisäänkirjautuminen</span><span class="sxs-lookup"><span data-stu-id="cbd9c-113">Staff card logon</span></span>

<span data-ttu-id="cbd9c-114">Kun **Henkilökunnan korttisisäänkirjautuminen** -asetus on käytössä, työntekijät, joiden myyntipisteen sisäänkirjautumisen tunnistetietoihin on määritetty jatkettu sisäänkirjautuminen, voivat kirjautua sisään magneettinauhan avulla.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="cbd9c-115">Henkilökunnan korttisisäänkirjautumisessa tarvitaan salasana</span><span class="sxs-lookup"><span data-stu-id="cbd9c-115">Staff card logon requires password</span></span>

<span data-ttu-id="cbd9c-116">Kun **Henkilökunnan korttisisäänkirjautumisessa tarvitaan salasana** -asetus on käytössä, henkilökunnan korttisisäänkirjautuminen valitsee vain työntekijän, jolle on määritetty esitetty jatkettu sisäänkirjautuminen.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="cbd9c-117">Työntekijöiden on silti syötettävä salasanansa, kun tämä asetus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-117">Workers must still enter their password when this option is enabled.</span></span>

<a name="assigning-an-extended-logon"></a><span data-ttu-id="cbd9c-118">Jatketun sisäänkirjautumisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cbd9c-118">Assigning an extended logon</span></span>
===========================

<span data-ttu-id="cbd9c-119">Oletuksena vain päälliköt voivat määrittää työntekijöille jatketun sisäänkirjautumisen.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="cbd9c-120">Määritä laajennettu sisäänkirjautuminen, siirtymällä myyntipisteessä kohtaan **Jatkettu kirjautuminen**.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="cbd9c-121">Etsi sitten työntekijä syöttämällä hänen operaattorintunnus hakukenttään.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="cbd9c-122">Valitse työntekijä ja napsauta sitten **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="cbd9c-123">Lue tai skannaa työntekijälle määritettävä jatkettu sisäänkirjautuminen seuraavalla sivulla.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="cbd9c-124">Jos kortin luku tai skannaus luettiin onnistuneesti, **OK**-painike tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="cbd9c-125">Napsauta **OK** tallentaaksesi jatkettu sisäänkirjautuminen kyseiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-125">Click **OK** to save the extended logon for that worker.</span></span>

<a name="deleting-an-extended-logon"></a><span data-ttu-id="cbd9c-126">Jatketun sisäänkirjautumisen poistaminen</span><span class="sxs-lookup"><span data-stu-id="cbd9c-126">Deleting an extended logon</span></span>
==========================

<span data-ttu-id="cbd9c-127">Poista työntekijälle määritetty jatkettu sisäänkirjautuminen etsimällä työntekijä **Jatkettu kirjautuminen** -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="cbd9c-128">Valitse työntekijä ja napsauta sitten **Poista määritys**.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="cbd9c-129">Kaikki tälle käyttäjälle määritetyt jatketun kirjautumisen tunnistetiedot poistetaan.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-129">All extended logon credentials that are associated with that worker are removed.</span></span>

<a name="extending-extended-logon"></a><span data-ttu-id="cbd9c-130">Jatketun kirjautumisen laajentaminen</span><span class="sxs-lookup"><span data-stu-id="cbd9c-130">Extending extended logon</span></span>
========================

<span data-ttu-id="cbd9c-131">Kirjautumispalvelua voidaan laajentaa niin, että ne tukevat laajennettuja kirjautumislaitteita kuten käsiskannereita.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="cbd9c-132">Lisätietoja on POS-laajennettavuusdokumentaatiossa.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-132">For more information, see the POS extensibility documentation.</span></span>

<a name="using-extended-logon"></a><span data-ttu-id="cbd9c-133">Jatketun sisäänkirjautumisen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="cbd9c-133">Using extended logon</span></span>
====================

<span data-ttu-id="cbd9c-134">Kun jatkettu sisäänkirjautuminen on määritetty ja työntekijälle on määritetty viivakoodi tai magneettinauha, työntekijän tarvitsee vain lukea tai skannata korttinsa myyntipisteen kirjautumissivulla.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="cbd9c-135">Jos tarvitaan myös salasana ennen kuin kirjautuminen voi jatkua, työntekijää kehotetaan syöttämään salasanansa.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>




