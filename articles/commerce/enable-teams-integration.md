---
title: Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön
description: Tässä aiheessa kuvataan, kuinka otetaan käyttöön Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointi.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019832"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="2b523-103">Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="2b523-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2b523-104">Tässä aiheessa kuvataan, kuinka otetaan käyttöön Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointi.</span><span class="sxs-lookup"><span data-stu-id="2b523-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="2b523-105">Jotta Teams voidaan valmistella Dynamics 365 Commercen tiedoilla ja Teams-sovelluksen ja myyntipisteen välinen tehtävänhallinta voidaan synkronoida, integrointitoiminnot on otettava käyttöön Commerce headquartersissa.</span><span class="sxs-lookup"><span data-stu-id="2b523-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="2b523-106">Kun otat Teams-integroinnin käyttöön, suostut jakamaan tietosi Teamsin kanssa.</span><span class="sxs-lookup"><span data-stu-id="2b523-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="2b523-107">Teamsin kanssa jaetut tiedot saattavat olla eri maassa kuin Commerce-tiedot, ja ne saattavat olla erilaisten yhteensopivuusvaatimusten mukaisia.</span><span class="sxs-lookup"><span data-stu-id="2b523-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="2b523-108">Lisätietoja: [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="2b523-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="2b523-109">Lisätietoja Microsoftin tietosuojakäytännöistä: [Microsoftin tietosuojalauseke](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="2b523-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="2b523-110">Ota Teams-integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="2b523-110">Enable Teams integration</span></span>

<span data-ttu-id="2b523-111">Ennen kuin voit ottaa Microsoft Teamsin ja Commercen integroinnin käyttöön, Teams-sovellus on rekisteröitävä vuokraajaa käyttäen Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="2b523-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="2b523-112">Noudattamalla seuraavia ohjeita voit rekisteröidä Teams-sovelluksen vuokraajaasi käyttäen Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="2b523-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="2b523-113">Noudata artikkelin [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](/azure/active-directory/develop/quickstart-register-app) ohjeita rekisteröidäksesi Teams-sovelluksen vuokraajasi kautta Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="2b523-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="2b523-114">Kopioi rekisteröidyn sovelluksen **Sovelluksen (asiakasohjelman) tunnus** -arvo **Yhteenveto**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="2b523-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="2b523-115">Tämän arvon avulla voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="2b523-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="2b523-116">Kopioi varmenteen arvo, joka on annettu, kun olet [lisännyt varmenteen](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) vaiheessa 1.</span><span class="sxs-lookup"><span data-stu-id="2b523-116">Copy the certificate value that was entered when you [added a certificate](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="2b523-117">Varmenne tunnetaan myös julkisena avaimena tai sovellusavaimena.</span><span class="sxs-lookup"><span data-stu-id="2b523-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="2b523-118">Tämän arvon avulla voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="2b523-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="2b523-119">Voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2b523-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2b523-120">Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integrointimääritys**.</span><span class="sxs-lookup"><span data-stu-id="2b523-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="2b523-121">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="2b523-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2b523-122">Määritä **Ota Microsoft Teams -integrointi käyttöön** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2b523-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="2b523-123">Kirjoita **Sovellustunnus**- ja **Sovellusavain**-kenttiin arvot, jotka sait rekisteröidessäsi Teams-sovelluksen Azure-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="2b523-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="2b523-124">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2b523-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="2b523-125">Seuraavassa kuvassa on esimerkki Teams-integroinnin konfiguroinnista Commerce headquartersissa.</span><span class="sxs-lookup"><span data-stu-id="2b523-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Teams-integroinnin konfiguraatio Commerce headquarters -sovelluksessa](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="2b523-127">Ota Teams-integraatio pois käytöstä</span><span class="sxs-lookup"><span data-stu-id="2b523-127">Disable Teams integration</span></span>

<span data-ttu-id="2b523-128">Voit ottaa Microsoft Teams -integroinnin pois käytöstä Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2b523-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2b523-129">Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integrointimääritys**.</span><span class="sxs-lookup"><span data-stu-id="2b523-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="2b523-130">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="2b523-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="2b523-131">Määritä **Ota Microsoft Teams -integrointi käyttöön** -asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="2b523-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="2b523-132">Tyhjennä arvot **Sovellustunnus**- ja **Sovellusavain**-kentistä.</span><span class="sxs-lookup"><span data-stu-id="2b523-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="2b523-133">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2b523-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="2b523-134">Kun olet poistanut Commercen Teams-integroinnin käytöstä, myyntipistepäätteet eivät enää näytä Teams-sovelluksella julkaistuja tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="2b523-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b523-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2b523-135">Additional resources</span></span>

[<span data-ttu-id="2b523-136">Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2b523-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="2b523-137">Microsoft Teamsin valmistelu Dynamics 365 Commercesta</span><span class="sxs-lookup"><span data-stu-id="2b523-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="2b523-138">Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä</span><span class="sxs-lookup"><span data-stu-id="2b523-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="2b523-139">Käyttäjäroolien hallinta Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="2b523-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="2b523-140">Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä</span><span class="sxs-lookup"><span data-stu-id="2b523-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="2b523-141">Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="2b523-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)