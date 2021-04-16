---
title: Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön
description: Tässä aiheessa kuvataan, kuinka otetaan käyttöön Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointi.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842654"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="58f04-103">Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="58f04-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="58f04-104">Tässä aiheessa kuvataan, kuinka otetaan käyttöön Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointi.</span><span class="sxs-lookup"><span data-stu-id="58f04-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="58f04-105">Jotta Teams voidaan valmistella Dynamics 365 Commercen tiedoilla ja Teams-sovelluksen ja myyntipisteen välinen tehtävänhallinta voidaan synkronoida, integrointitoiminnot on otettava käyttöön Commerce headquartersissa.</span><span class="sxs-lookup"><span data-stu-id="58f04-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="58f04-106">Kun otat Teams-integroinnin käyttöön, suostut jakamaan tietosi Teamsin kanssa.</span><span class="sxs-lookup"><span data-stu-id="58f04-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="58f04-107">Teamsin kanssa jaetut tiedot saattavat olla eri maassa kuin Commerce-tiedot, ja ne saattavat olla erilaisten yhteensopivuusvaatimusten mukaisia.</span><span class="sxs-lookup"><span data-stu-id="58f04-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="58f04-108">Lisätietoja: [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="58f04-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="58f04-109">Lisätietoja Microsoftin tietosuojakäytännöistä: [Microsoftin tietosuojalauseke](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="58f04-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="58f04-110">Ota Teams-integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="58f04-110">Enable Teams integration</span></span>

<span data-ttu-id="58f04-111">Ennen kuin voit ottaa Microsoft Teamsin ja Commercen integroinnin käyttöön, Teams-sovellus on rekisteröitävä vuokraajaa käyttäen Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="58f04-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="58f04-112">Noudattamalla seuraavia ohjeita voit rekisteröidä Teams-sovelluksen vuokraajaasi käyttäen Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="58f04-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="58f04-113">Noudata artikkelin [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) ohjeita rekisteröidäksesi Teams-sovelluksen vuokraajasi kautta Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="58f04-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="58f04-114">Kopioi rekisteröidyn sovelluksen **Sovelluksen (asiakasohjelman) tunnus** -arvo **Yhteenveto**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="58f04-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="58f04-115">Tämän arvon avulla voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="58f04-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="58f04-116">Kopioi varmenteen arvo, joka on annettu, kun olet [lisännyt varmenteen](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) vaiheessa 1.</span><span class="sxs-lookup"><span data-stu-id="58f04-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="58f04-117">Varmenne tunnetaan myös julkisena avaimena tai sovellusavaimena.</span><span class="sxs-lookup"><span data-stu-id="58f04-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="58f04-118">Tämän arvon avulla voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="58f04-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="58f04-119">Voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="58f04-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="58f04-120">Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integrointimääritys**.</span><span class="sxs-lookup"><span data-stu-id="58f04-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="58f04-121">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="58f04-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="58f04-122">Määritä **Ota Microsoft Teams -integrointi käyttöön** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="58f04-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="58f04-123">Kirjoita **Sovellustunnus**- ja **Sovellusavain**-kenttiin arvot, jotka sait rekisteröidessäsi Teams-sovelluksen Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="58f04-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="58f04-124">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="58f04-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="58f04-125">Seuraavassa kuvassa on esimerkki Teams-integroinnin konfiguroinnista Commerce headquartersissa.</span><span class="sxs-lookup"><span data-stu-id="58f04-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Teams-integroinnin konfiguraatio Commerce headquarters -sovelluksessa](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="58f04-127">Ota Teams-integraatio pois käytöstä</span><span class="sxs-lookup"><span data-stu-id="58f04-127">Disable Teams integration</span></span>

<span data-ttu-id="58f04-128">Voit ottaa Microsoft Teams -integroinnin pois käytöstä Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="58f04-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="58f04-129">Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integrointimääritys**.</span><span class="sxs-lookup"><span data-stu-id="58f04-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="58f04-130">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="58f04-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="58f04-131">Määritä **Ota Microsoft Teams -integrointi käyttöön** -asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="58f04-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="58f04-132">Tyhjennä arvot **Sovellustunnus**- ja **Sovellusavain**-kentistä.</span><span class="sxs-lookup"><span data-stu-id="58f04-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="58f04-133">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="58f04-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="58f04-134">Kun olet poistanut Commercen Teams-integroinnin käytöstä, myyntipistepäätteet eivät enää näytä Teams-sovelluksella julkaistuja tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="58f04-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58f04-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="58f04-135">Additional resources</span></span>

[<span data-ttu-id="58f04-136">Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="58f04-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="58f04-137">Microsoft Teamsin valmistelu Dynamics 365 Commercesta</span><span class="sxs-lookup"><span data-stu-id="58f04-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="58f04-138">Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä</span><span class="sxs-lookup"><span data-stu-id="58f04-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="58f04-139">Käyttäjäroolien hallinta Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="58f04-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="58f04-140">Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä</span><span class="sxs-lookup"><span data-stu-id="58f04-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="58f04-141">Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="58f04-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
