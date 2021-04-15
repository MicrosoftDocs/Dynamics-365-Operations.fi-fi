---
title: Kaksoiskirjoituksen määrittämisen ohjeet
description: Tässä ohjeaiheessa kuvataan skenaariot, joita tuetaan kaksoiskirjoituksen asetuksia varten.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 999b37970be1c10fd5e78c3d8ac6c1fb25cad367
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751383"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="4e0af-103">Kaksoiskirjoituksen määrittämisen ohjeet</span><span class="sxs-lookup"><span data-stu-id="4e0af-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4e0af-104">Voit määrittää kaksoiskirjoitusyhteyden Finance and Operations -ympäristön ja Dataverse -ympäristön välille.</span><span class="sxs-lookup"><span data-stu-id="4e0af-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="4e0af-105">**Finance and Operations -ympäristö** tarjoaa **Finance and Operations -sovelluksille** (esimerkiksi Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Human Resources) taustaympäristön.</span><span class="sxs-lookup"><span data-stu-id="4e0af-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="4e0af-106">**Dataverse-ympäristö** on **asiakkaiden aktivointisovellusten** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation) pohjaympäristö.</span><span class="sxs-lookup"><span data-stu-id="4e0af-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e0af-107">Dynamics 365 Financen Human Resources -moduuli tukee kaksoiskirjoitusyhteyksiä, mutta Dynamics 365 Human Resources -sovellus ei.</span><span class="sxs-lookup"><span data-stu-id="4e0af-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="4e0af-108">Asennusmekanismi vaihtelee tilauksen ja ympäristön mukaan:</span><span class="sxs-lookup"><span data-stu-id="4e0af-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="4e0af-109">Muutamissa Finance and Operations -sovellusten ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Microsoft Dynamics Lifecycle Services (LCS) -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="4e0af-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4e0af-110">Jos sinulla on Microsoft Power Platformin käyttöoikeus, saat uuden Dataverse -ympäristön, jos vuokraajalla ei ole sellaista.</span><span class="sxs-lookup"><span data-stu-id="4e0af-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="4e0af-111">Finance and Operations -sovellusten olemassa olevissa ilmentymissä kaksoiskirjoitusyhteyden asetus alkaa Finance and Operations -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="4e0af-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="4e0af-112">Ennen kaksoiskirjoituksen aloittamista entiteetissä voidaan tehdä ensimmäinen synkronointi, joka käsittelee Finance and Operations -sovellusten ja asiakkaan osallistamissovellusten kummankin puolen aiemmin luodut tiedot.</span><span class="sxs-lookup"><span data-stu-id="4e0af-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="4e0af-113">Voit ohittaa ensimmäisen synkronoinnin, jos tietoja ei tarvitse synkronoida ympäristöjen välillä.</span><span class="sxs-lookup"><span data-stu-id="4e0af-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="4e0af-114">Ensimmäisessä synkronoinnissa aiemmin luodut tiedot voivaan kopioida sovelluksesta toiseen kaksisuuntaisesti.</span><span class="sxs-lookup"><span data-stu-id="4e0af-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="4e0af-115">Määritysskenaarioita on useita, ja ne määräytyvät käytössä jo olevien ympäristöjen ja niissä olevien tietotyyppien perusteella.</span><span class="sxs-lookup"><span data-stu-id="4e0af-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="4e0af-116">Seuraavia asetusskenaarioita tuetaan:</span><span class="sxs-lookup"><span data-stu-id="4e0af-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="4e0af-117">Uusi Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="4e0af-118">Uusi Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="4e0af-119">Uusi Finance and Operations -sovelluksen esiintymä, jolla on tietoja, ja uusi asiakkaan osallistamissovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="4e0af-120">Uusi Finance and Operations -sovelluksen esiintymä, jossa on tietoja, ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="4e0af-121">Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="4e0af-122">Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="4e0af-123">Uusi Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="4e0af-124">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymä (jossa ei ole tietoja) ja asiakkaan osallistamissovelluksen esiintymän välille, noudata kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="4e0af-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="4e0af-125">Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="4e0af-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="4e0af-126">Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="4e0af-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="4e0af-127">Valmistellaan uusi, tyhjä asiakkaan osallistamissovelluksen esiintymä, johon on asennettu ensisijainen CRM-ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="4e0af-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="4e0af-128">Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.</span><span class="sxs-lookup"><span data-stu-id="4e0af-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="4e0af-129">Taulukartat otetaan käyttöön reaaliaikaista synkronointia varten.</span><span class="sxs-lookup"><span data-stu-id="4e0af-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="4e0af-130">Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="4e0af-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="4e0af-131">Uusi Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="4e0af-132">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymän (jossa ei ole tietoja) ja asiakkaan osallistamissovelluksen aiemmin luodun esiintymän välille, noudata kohdan [Kaksoiskirjoituksen määritys Lifecycle Services -sovelluksesta](lcs-setup.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="4e0af-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="4e0af-133">Kun yhteyden määritys on valmis, seuraavat toiminnot tapahtuvat automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="4e0af-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="4e0af-134">Uusi, tyhjä Finance and Operations -ympäristö valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="4e0af-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="4e0af-135">Kaksoiskirjoitusyhteys muodostetaan DAT-yritystiedoille.</span><span class="sxs-lookup"><span data-stu-id="4e0af-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="4e0af-136">Taulukartat otetaan käyttöön reaaliaikaista synkronointia varten.</span><span class="sxs-lookup"><span data-stu-id="4e0af-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="4e0af-137">Molemmat ympäristöt ovat nyt valmiita reaaliaikaisten tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="4e0af-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="4e0af-138">Voit synkronoida olemassa olevat Dataverse -tiedot Finance and Operations -sovellukseen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4e0af-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="4e0af-139">Luo Finance and Operations -sovellukseen uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="4e0af-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="4e0af-140">Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="4e0af-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="4e0af-141">[Käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="4e0af-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="4e0af-142">Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="4e0af-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="4e0af-143">Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on jäljempänä tässä aiheessa olevassa [Esimerkissä](#example).</span><span class="sxs-lookup"><span data-stu-id="4e0af-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="4e0af-144">Uusi Finance and Operations -sovelluksen esiintymä, jossa on tietoja, ja uusi asiakkaan osallistamissovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="4e0af-145">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymän ja asiakkaan osallistamissovelluksen uuden esiintymän välille, seuraa ohjeita, jotka tämän ohjeaiheen osassa [Uusi Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamissovelluksen esiintymä](#new-new).</span><span class="sxs-lookup"><span data-stu-id="4e0af-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="4e0af-146">Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="4e0af-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="4e0af-147">Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="4e0af-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="4e0af-148">Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="4e0af-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="4e0af-149">Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).</span><span class="sxs-lookup"><span data-stu-id="4e0af-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="4e0af-150">Uusi Finance and Operations -sovelluksen esiintymä, jossa on tietoja, ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="4e0af-151">Jos haluat määrittää kaksoiskirjoitusyhteyden Finance and Operations -sovelluksen uuden esiintymän ja asiakkaan aiemmin luodun osallistamissovelluksen esiintymän välille, noudata ohjeita, jotka ovat tämän ohjeaiheen osassa [Uusi Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamissovelluksen esiintymä](#new-existing).</span><span class="sxs-lookup"><span data-stu-id="4e0af-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="4e0af-152">Kun yhteyden määritys on valmis, voit synkronoida tiedot asiakkaan osallistamissovelluksen kanssa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="4e0af-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="4e0af-153">Avaa Finance and Operations -sovellus LCS-sivulla, kirjaudu sisään ja siirry kohtaan **Tiedonhallinta \> Kaksoiskirjoitus**.</span><span class="sxs-lookup"><span data-stu-id="4e0af-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="4e0af-154">Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="4e0af-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="4e0af-155">Voit synkronoida olemassa olevat Dataverse -tiedot Finance and Operations -sovellukseen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="4e0af-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="4e0af-156">Luo Finance and Operations -sovellukseen uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="4e0af-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="4e0af-157">Lisää yritys kaksoiskirjoitusyhteyden asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="4e0af-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="4e0af-158">[Käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO (International Organization for Standardization) -yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="4e0af-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="4e0af-159">Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="4e0af-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="4e0af-160">Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).</span><span class="sxs-lookup"><span data-stu-id="4e0af-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="4e0af-161">Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja uusi asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="4e0af-162">Kaksoiskirjoitusyhteyden määrittäminen Finance and Operations -sovelluksen aiemmin luodun esiintymän ja asiakkaan osallistamissovelluksen uuden esiintymän välille Finance and Operation -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="4e0af-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="4e0af-163">[Yhteyden määrittäminen Finance and Operations -sovelluksessa](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="4e0af-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="4e0af-164">Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="4e0af-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="4e0af-165">Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).</span><span class="sxs-lookup"><span data-stu-id="4e0af-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="4e0af-166">Aiemmin luotu Finance and Operations -sovelluksen esiintymä ja aiemmin luotu asiakkaan osallistamisovelluksen esiintymä</span><span class="sxs-lookup"><span data-stu-id="4e0af-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="4e0af-167">Kaksoiskirjoitusyhteyden määrittäminen Finance and Operations -sovelluksen aiemmin luodun esiintymän ja asiakkaan osallistamissovelluksen aiemmin luodun esiintymän välille Finance and Operation -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="4e0af-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="4e0af-168">[Yhteyden määrittäminen Finance and Operations -sovelluksessa](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="4e0af-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="4e0af-169">Jos haluat synkronoida olemassa olevat Dataverse -tiedot Finance and Operations -sovellukseen, [käynnistä](bootstrap-company-data.md) Dataverse -tiedot käyttämällä kolmen kirjaimen ISO-yrityskoodia.</span><span class="sxs-lookup"><span data-stu-id="4e0af-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="4e0af-170">Suorita **Alkuperäinen synkronointi** -toiminto tauluille, joiden tiedot haluat synkronoida.</span><span class="sxs-lookup"><span data-stu-id="4e0af-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="4e0af-171">Esimerkkejä linkeistä ja vaihtoehtoinen lähestymistapa on osassa [Esimerkki](#example).</span><span class="sxs-lookup"><span data-stu-id="4e0af-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="4e0af-172">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="4e0af-172">Example</span></span>

<span data-ttu-id="4e0af-173">Esimerkkiin voi tutustua kohdassa [Asiakkaiden V3 ottaminen käyttöön – yhteyshenkilöiden taulun yhdistämismääritys](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="4e0af-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="4e0af-174">Lisätietoja vaihtoehtoisesta tavasta, joka perustuu kunkin entiteetin tietomääriin, kun niissä on suoritettava ensimmäinen synkronointi, on kohdassa [Alustavaa synkronointia koskevia huomautuksia](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="4e0af-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]