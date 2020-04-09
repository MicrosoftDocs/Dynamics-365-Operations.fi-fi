---
title: Kaksoiskirjoituksen asetusten tuetut skenaariot
description: Tässä ohjeaiheessa kuvataan skenaariot, joita tuetaan kaksoiskirjoituksen asetuksia varten.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d7ff514768ee8e4797b591da89e190a855385885
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172851"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="b82c2-103">Kaksoiskirjoituksen asetusten tuetut skenaariot</span><span class="sxs-lookup"><span data-stu-id="b82c2-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="b82c2-104">Voit määrittää kaksoiskirjoitusyhteyden Finance and Operations -ympäristön ja Common Data Service -ympäristön välille.</span><span class="sxs-lookup"><span data-stu-id="b82c2-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="b82c2-105">**Finance and Operations -ympäristö** tarjoaa **Finance and Operations -sovelluksille** (esimerkiksi Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail ja Dynamics 365 Human Resources) taustaympäristön.</span><span class="sxs-lookup"><span data-stu-id="b82c2-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="b82c2-106">**Common Data Service -ympäristö** tarjoaa **Dynamics 365:n mallipohjaisille sovelluksille** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation) taustaympäristön.</span><span class="sxs-lookup"><span data-stu-id="b82c2-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="b82c2-107">Asennusmekanismi vaihtelee tilauksen ja ympäristön mukaan.</span><span class="sxs-lookup"><span data-stu-id="b82c2-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="b82c2-108">Muutamissa Finance and Operations -sovellusten ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="b82c2-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b82c2-109">Jos sinulla on Microsoft Power Platformin käyttöoikeus, saat uuden Common Data Service -ympäristön, jos vuokraajalla ei ole sellaista.</span><span class="sxs-lookup"><span data-stu-id="b82c2-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="b82c2-110">Finance and Operations -sovellusten olemassa olevissa ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Finance and Operations -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="b82c2-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="b82c2-111">Seuraavia asetusskenaarioita tuetaan:</span><span class="sxs-lookup"><span data-stu-id="b82c2-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="b82c2-112">Uusi Finance and Operations -sovelluksen ilmentymä ja uusi mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="b82c2-113">Uusi Finance and Operations -sovelluksen ilmentymä ja olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="b82c2-114">Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja uusi mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="b82c2-115">Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="b82c2-116">Olemassa oleva Finance and Operations -sovelluksen ilmentymä ja uusi tai olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="b82c2-117">Uusi Finance and Operations -sovelluksen ilmentymä ja uusi mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="b82c2-118">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa ei ole tietoja) ja Dynamics 365:n uuden mallipohjaisen sovelluksen ilmentymän välille, seuraa kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b82c2-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="b82c2-119">Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="b82c2-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="b82c2-120">Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="b82c2-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="b82c2-121">Valmistellaan uusi, tyhjä mallipohjaisen sovelluksen ilmentymä, johon on asennettu ensisijainen CRM-ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="b82c2-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="b82c2-122">Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.</span><span class="sxs-lookup"><span data-stu-id="b82c2-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="b82c2-123">Yksikkökartat otetaan käyttöön reaaliaikaista synkronointia varten.</span><span class="sxs-lookup"><span data-stu-id="b82c2-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="b82c2-124">Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="b82c2-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="b82c2-125">Uusi Finance and Operations -sovelluksen ilmentymä ja olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="b82c2-126">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa ei ole tietoja) ja Dynamics 365:n olemassa olevan mallipohjaisen sovelluksen ilmentymän välille, seuraa kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b82c2-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="b82c2-127">Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="b82c2-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="b82c2-128">Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="b82c2-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="b82c2-129">Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.</span><span class="sxs-lookup"><span data-stu-id="b82c2-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="b82c2-130">Yksikkökartat otetaan käyttöön reaaliaikaista synkronointia varten.</span><span class="sxs-lookup"><span data-stu-id="b82c2-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="b82c2-131">Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="b82c2-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="b82c2-132">Voit synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b82c2-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b82c2-133">Luo Finance and Operations -sovellukseen uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="b82c2-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="b82c2-134">Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="b82c2-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="b82c2-135">[Käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="b82c2-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="b82c2-136">Koska kaksoiskirjoitus on reaaliaikaisen synkronoinnin tilassa, Common Data Servicen tiedot alkavat siirtyä automaattisesti Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="b82c2-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="b82c2-137">Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja uusi mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="b82c2-138">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa on esittelytietoja) ja Dynamics 365:n uuden mallipohjaisen sovelluksen ilmentymän välille, seuraa aiemmin tässä ohjeaiheessa olevan [Uusi Finance and Operations -sovelluksen ilmentymä ja uusi mallipohjaisen sovelluksen ilmentymä](#new-new) -osan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b82c2-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="b82c2-139">Kun yhteyden määritys on valmis, voit synkronoida esittelytiedot mallipohjaisen sovelluksen kanssa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b82c2-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="b82c2-140">Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="b82c2-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="b82c2-141">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="b82c2-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="b82c2-142">Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="b82c2-143">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa on esittelytietoja) ja Dynamics 365:n olemassa olevan mallipohjaisen sovelluksen ilmentymän välille, seuraa aiemmin tässä ohjeaiheessa olevan [Uusi Finance and Operations -sovelluksen ilmentymä ja olemassa oleva mallipohjaisen sovelluksen ilmentymä](#new-existing) -osan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b82c2-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="b82c2-144">Kun yhteyden määritys on valmis, voit synkronoida esittelytiedot mallipohjaisen sovelluksen kanssa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b82c2-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="b82c2-145">Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="b82c2-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="b82c2-146">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="b82c2-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="b82c2-147">Voit synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b82c2-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b82c2-148">Luo Finance and Operations -sovellukseen uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="b82c2-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="b82c2-149">Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="b82c2-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="b82c2-150">[Käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="b82c2-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="b82c2-151">Koska kaksoiskirjoitus on reaaliaikaisen synkronoinnin tilassa, Common Data Servicen tiedot alkavat siirtyä automaattisesti Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="b82c2-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="b82c2-152">Olemassa oleva Finance and Operations -sovelluksen ilmentymä ja uusi tai olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="b82c2-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="b82c2-153">Kaksoiskirjoitusyhteyden määrittäminen Finance and Operations -sovelluksen olemassa olevan ilmentymän ja Dynamics 365:n uuden tai olemassa olevan mallipohjaisen sovelluksen ilmentymän välille Finance and Operation -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="b82c2-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="b82c2-154">Määritä yhteys Finance and Operations -sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="b82c2-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="b82c2-155">Jos haluat synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen, [käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO-yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="b82c2-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="b82c2-156">Koska kaksoiskirjoitus on reaaliaikaisen synkronoinnin tilassa, Common Data Servicen tiedot alkavat siirtyä automaattisesti Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="b82c2-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
