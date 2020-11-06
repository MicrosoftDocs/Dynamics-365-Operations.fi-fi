---
title: Kaksoiskirjoituksen määrittämisen ohjeet
description: Tässä ohjeaiheessa kuvataan skenaariot, joita tuetaan kaksoiskirjoituksen asetuksia varten.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088503"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="39d11-103">Kaksoiskirjoituksen määrittämisen ohjeet</span><span class="sxs-lookup"><span data-stu-id="39d11-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="39d11-104">Voit määrittää kaksoiskirjoitusyhteyden Finance and Operations -ympäristön ja Common Data Service -ympäristön välille.</span><span class="sxs-lookup"><span data-stu-id="39d11-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="39d11-105">**Finance and Operations -ympäristö** muodostaa **Finance and Operations -sovellusten** (kuten Microsoft Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin ja Dynamics 365 Retailin) taustaympäristön.</span><span class="sxs-lookup"><span data-stu-id="39d11-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="39d11-106">**Common Data Service -ympäristö** muodostaa **asiakkaan osallistamisovellusten** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation) taustaympäristön.</span><span class="sxs-lookup"><span data-stu-id="39d11-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="39d11-107">Finance and Operationsin Human Resources tukee kaksoiskirjoitusyhteyksiä, mutta Dynamics 365 Human Resources -sovellus ei.</span><span class="sxs-lookup"><span data-stu-id="39d11-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="39d11-108">Asennusmekanismi vaihtelee tilauksen ja ympäristön mukaan.</span><span class="sxs-lookup"><span data-stu-id="39d11-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="39d11-109">Muutamissa Finance and Operations -sovellusten ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="39d11-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="39d11-110">Jos sinulla on Power Platformin käyttöoikeus, saat uuden Common Data Service -ympäristön, jos vuokraajalla ei ole sellaista.</span><span class="sxs-lookup"><span data-stu-id="39d11-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="39d11-111">Finance and Operations -sovellusten olemassa olevissa ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Finance and Operations -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="39d11-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="39d11-112">Ennen kaksoiskirjoituksen aloittamista entiteetissä voidaan tehdä ensimmäinen synkronointi, joka käsittelee Finance and Operations -sovellusten ja asiakkaan osallistamissovellusten kummankin puolen aiemmin luodut tiedot.</span><span class="sxs-lookup"><span data-stu-id="39d11-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="39d11-113">Voit ohittaa ensimmäisen synkronoinnin, jos tietoja ei tarvitse synkronoida ympäristöjen välillä.</span><span class="sxs-lookup"><span data-stu-id="39d11-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="39d11-114">Ensimmäisessä synkronoinnissa aiemmin luodut tiedot voivaan kopioida sovelluksesta toiseen kaksisuuntaisesti.</span><span class="sxs-lookup"><span data-stu-id="39d11-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="39d11-115">Määritysskenaarioita on useita, ja ne määräytyvät käytössä jo olevien ympäristöjen ja niissä olevien tietotyyppien perusteella.</span><span class="sxs-lookup"><span data-stu-id="39d11-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="39d11-116">Seuraavia asetusskenaarioita tuetaan:</span><span class="sxs-lookup"><span data-stu-id="39d11-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="39d11-117">Uusi Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="39d11-118">Uusi Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="39d11-119">Uusi Finance and Operations -sovelluksen esiintymä, jolla on tietoja, ja uusi asiakkaan osallistamissovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="39d11-120">Uusi Finance and Operations -sovelluksen esiintymä, jossa on tietoja, ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="39d11-121">Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="39d11-122">Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="39d11-123">Uusi Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="39d11-124">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymä (jossa ei ole tietoja) ja asiakkaan osallistamissovelluksen esiintymän välille, noudata kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="39d11-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="39d11-125">Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="39d11-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="39d11-126">Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="39d11-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="39d11-127">Valmistellaan uusi, tyhjä asiakkaan osallistamissovelluksen esiintymä, johon on asennettu ensisijainen CRM-ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="39d11-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="39d11-128">Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.</span><span class="sxs-lookup"><span data-stu-id="39d11-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="39d11-129">Yksikkökartat otetaan käyttöön reaaliaikaista synkronointia varten.</span><span class="sxs-lookup"><span data-stu-id="39d11-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="39d11-130">Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="39d11-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="39d11-131">Uusi Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="39d11-132">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymän (jossa ei ole tietoja) ja asiakkaan osallistamissovelluksen aiemmin luodun esiintymän välille, noudata kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="39d11-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="39d11-133">Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="39d11-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="39d11-134">Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="39d11-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="39d11-135">Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.</span><span class="sxs-lookup"><span data-stu-id="39d11-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="39d11-136">Yksikkökartat otetaan käyttöön reaaliaikaista synkronointia varten.</span><span class="sxs-lookup"><span data-stu-id="39d11-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="39d11-137">Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="39d11-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="39d11-138">Voit synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="39d11-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="39d11-139">Luo Finance and Operations -sovellukseen uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="39d11-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="39d11-140">Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="39d11-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="39d11-141">[Käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="39d11-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="39d11-142">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="39d11-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="39d11-143">Esimerkki ja vaihtoehtoinen toimintatapa on kohdassa [Esimerkki](#example).</span><span class="sxs-lookup"><span data-stu-id="39d11-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="39d11-144">Uusi Finance and Operations -sovelluksen esiintymä, jossa on tietoja, ja uusi asiakkaan osallistamissovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="39d11-145">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymän ja asiakkaan osallistamissovelluksen uuden esiintymän välille, seuraa ohjeita, jotka tämän ohjeaiheen osassa [Uusi Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamissovelluksen esiintymä](#new-new).</span><span class="sxs-lookup"><span data-stu-id="39d11-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="39d11-146">Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="39d11-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="39d11-147">Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="39d11-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="39d11-148">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="39d11-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="39d11-149">Esimerkki ja vaihtoehtoinen toimintatapa on kohdassa [Esimerkki](#example).</span><span class="sxs-lookup"><span data-stu-id="39d11-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="39d11-150">Uusi Finance and Operations -sovelluksen esiintymä, jossa on tietoja, ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="39d11-151">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymän ja asiakkaan aiemmin luodun osallistamissovelluksen esiintymän välille, noudata ohjeita, jotka ovat tämän ohjeaiheen osassa [Uusi Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä](#new-existing).</span><span class="sxs-lookup"><span data-stu-id="39d11-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="39d11-152">Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="39d11-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="39d11-153">Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="39d11-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="39d11-154">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="39d11-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="39d11-155">Voit synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="39d11-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="39d11-156">Luo Finance and Operations -sovellukseen uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="39d11-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="39d11-157">Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="39d11-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="39d11-158">[Käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="39d11-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="39d11-159">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="39d11-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="39d11-160">Esimerkki ja vaihtoehtoinen toimintatapa on kohdassa [Esimerkki](#example).</span><span class="sxs-lookup"><span data-stu-id="39d11-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="39d11-161">Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="39d11-162">Kaksoiskirjoitusyhteyden määrittäminen Finance and Operations -sovelluksen aiemmin luodun esiintymän ja asiakkaan osallistamissovelluksen uuden esiintymän välille Finance and Operation -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="39d11-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="39d11-163">[Yhteyden määrittäminen Finance and Operations -sovelluksessa](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="39d11-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="39d11-164">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="39d11-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="39d11-165">Esimerkki ja vaihtoehtoinen toimintatapa on kohdassa [Esimerkki](#example).</span><span class="sxs-lookup"><span data-stu-id="39d11-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="39d11-166">Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="39d11-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="39d11-167">Kaksoiskirjoitusyhteyden määrittäminen Finance and Operations -sovelluksen aiemmin luodun esiintymän ja asiakkaan osallistamissovelluksen aiemmin luodun esiintymän välille Finance and Operation -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="39d11-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="39d11-168">Määritä yhteys Finance and Operations -sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="39d11-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="39d11-169">Jos haluat synkronoida olemassa olevat Common Data Service -tiedot Finance and Operations -sovellukseen, [käynnistä](bootstrap-company-data.md) Common Data Service -tiedot käyttämällä kolmen kirjaimen ISO-yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="39d11-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="39d11-170">Suorita **Alkuperäinen synkronointi** -toiminto yksiköille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="39d11-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="39d11-171">Esimerkki ja vaihtoehtoinen toimintatapa on kohdassa [Esimerkki](#example).</span><span class="sxs-lookup"><span data-stu-id="39d11-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="39d11-172">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="39d11-172">Example</span></span>

<span data-ttu-id="39d11-173">Esimerkkiin voi tutustua kohdassa [Asiakkaiden V3 ottaminen käyttöön – yhteyshenkilöiden entiteetin yhdistämismääritys](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="39d11-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="39d11-174">Lisätietoja vaihtoehtoisesta tavasta, joka perustuu kunkin entiteetin tietomääriin, kun niissä on suoritettava ensimmäinen synkronointi, on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="39d11-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
