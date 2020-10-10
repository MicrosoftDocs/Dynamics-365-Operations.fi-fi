---
title: Kaksoiskirjoituksen asetusten tuetut skenaariot
description: Tässä ohjeaiheessa kuvataan skenaariot, joita tuetaan kaksoiskirjoituksen asetuksia varten.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
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
ms.openlocfilehash: b4f69e7933bc5a50cccad6911c99cf08d2768578
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818593"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="109b2-103">Kaksoiskirjoituksen asetusten tuetut skenaariot</span><span class="sxs-lookup"><span data-stu-id="109b2-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="109b2-104">Voit määrittää kaksoiskirjoitusyhteyden Finance and Operations -ympäristön ja Common Data Service -ympäristön välille.</span><span class="sxs-lookup"><span data-stu-id="109b2-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="109b2-105">**Finance and Operations -ympäristö** muodostaa **Finance and Operations -sovellusten** (kuten Microsoft Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin ja Dynamics 365 Retailin) taustaympäristön.</span><span class="sxs-lookup"><span data-stu-id="109b2-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="109b2-106">**Common Data Service -ympäristö** tarjoaa **Dynamics 365:n mallipohjaisille sovelluksille** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation) taustaympäristön.</span><span class="sxs-lookup"><span data-stu-id="109b2-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="109b2-107">Finance and Operationsin Human Resources tukee kaksoiskirjoitusyhteyksiä, mutta Dynamics 365 Human Resources -sovellus ei.</span><span class="sxs-lookup"><span data-stu-id="109b2-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="109b2-108">Asennusmekanismi vaihtelee tilauksen ja ympäristön mukaan.</span><span class="sxs-lookup"><span data-stu-id="109b2-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="109b2-109">Muutamissa Finance and Operations -sovellusten ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="109b2-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="109b2-110">Jos sinulla on Power Platformin käyttöoikeus, saat uuden Common Data Service -ympäristön, jos vuokraajalla ei ole sellaista.</span><span class="sxs-lookup"><span data-stu-id="109b2-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="109b2-111">Finance and Operations -sovellusten olemassa olevissa ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Finance and Operations -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="109b2-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="109b2-112">Seuraavia asetusskenaarioita tuetaan:</span><span class="sxs-lookup"><span data-stu-id="109b2-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="109b2-113">Uusi Finance and Operations -sovelluksen ilmentymä ja uusi mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="109b2-114">Uusi Finance and Operations -sovelluksen ilmentymä ja olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="109b2-115">Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja uusi mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="109b2-116">Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="109b2-117">Olemassa oleva Finance and Operations -sovelluksen ilmentymä ja uusi tai olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="109b2-118">Uusi Finance and Operations -sovelluksen ilmentymä ja uusi mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="109b2-119">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa ei ole tietoja) ja Dynamics 365:n uuden mallipohjaisen sovelluksen ilmentymän välille, seuraa kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="109b2-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="109b2-120">Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="109b2-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="109b2-121">Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="109b2-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="109b2-122">Valmistellaan uusi, tyhjä mallipohjaisen sovelluksen ilmentymä, johon on asennettu ensisijainen CRM-ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="109b2-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="109b2-123">Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.</span><span class="sxs-lookup"><span data-stu-id="109b2-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="109b2-124">Yksikkökartat otetaan käyttöön reaaliaikaista synkronointia varten.</span><span class="sxs-lookup"><span data-stu-id="109b2-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="109b2-125">Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="109b2-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="109b2-126">Uusi Finance and Operations -sovelluksen ilmentymä ja olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="109b2-127">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa ei ole tietoja) ja Dynamics 365:n olemassa olevan mallipohjaisen sovelluksen ilmentymän välille, seuraa kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="109b2-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="109b2-128">Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="109b2-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="109b2-129">Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="109b2-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="109b2-130">Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.</span><span class="sxs-lookup"><span data-stu-id="109b2-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="109b2-131">Yksikkökartat otetaan käyttöön reaaliaikaista synkronointia varten.</span><span class="sxs-lookup"><span data-stu-id="109b2-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="109b2-132">Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="109b2-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="109b2-133">Voit synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="109b2-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="109b2-134">Luo Finance and Operations -sovellukseen uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="109b2-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="109b2-135">Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="109b2-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="109b2-136">[Käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="109b2-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="109b2-137">Koska kaksoiskirjoitus on reaaliaikaisen synkronoinnin tilassa, Common Data Servicen tiedot alkavat siirtyä automaattisesti Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="109b2-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="109b2-138">Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja uusi mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="109b2-139">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa on esittelytietoja) ja Dynamics 365:n uuden mallipohjaisen sovelluksen ilmentymän välille, seuraa aiemmin tässä ohjeaiheessa olevan [Uusi Finance and Operations -sovelluksen ilmentymä ja uusi mallipohjaisen sovelluksen ilmentymä](#new-new) -osan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="109b2-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="109b2-140">Kun yhteyden määritys on valmis, voit synkronoida esittelytiedot mallipohjaisen sovelluksen kanssa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="109b2-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="109b2-141">Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="109b2-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="109b2-142">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="109b2-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="109b2-143">Uusi Finance and Operations -sovelluksen ilmentymä, jolla on esittelytietoja, ja olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-143">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="109b2-144">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden ilmentymän (jossa on esittelytietoja) ja Dynamics 365:n olemassa olevan mallipohjaisen sovelluksen ilmentymän välille, seuraa aiemmin tässä ohjeaiheessa olevan [Uusi Finance and Operations -sovelluksen ilmentymä ja olemassa oleva mallipohjaisen sovelluksen ilmentymä](#new-existing) -osan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="109b2-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="109b2-145">Kun yhteyden määritys on valmis, voit synkronoida esittelytiedot mallipohjaisen sovelluksen kanssa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="109b2-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="109b2-146">Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="109b2-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="109b2-147">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="109b2-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="109b2-148">Voit synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="109b2-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="109b2-149">Luo Finance and Operations -sovellukseen uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="109b2-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="109b2-150">Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="109b2-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="109b2-151">[Käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="109b2-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="109b2-152">Koska kaksoiskirjoitus on reaaliaikaisen synkronoinnin tilassa, Common Data Servicen tiedot alkavat siirtyä automaattisesti Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="109b2-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="109b2-153">Olemassa oleva Finance and Operations -sovelluksen ilmentymä ja uusi tai olemassa oleva mallipohjaisen sovelluksen ilmentymä</span><span class="sxs-lookup"><span data-stu-id="109b2-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="109b2-154">Kaksoiskirjoitusyhteyden määrittäminen Finance and Operations -sovelluksen olemassa olevan ilmentymän ja Dynamics 365:n uuden tai olemassa olevan mallipohjaisen sovelluksen ilmentymän välille Finance and Operation -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="109b2-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="109b2-155">Määritä yhteys Finance and Operations -sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="109b2-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="109b2-156">Jos haluat synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen, [käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO-yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="109b2-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="109b2-157">Koska kaksoiskirjoitus on reaaliaikaisen synkronoinnin tilassa, Common Data Servicen tiedot alkavat siirtyä automaattisesti Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="109b2-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
