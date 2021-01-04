---
title: Tietojen integrointiprojektin luominen (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten tietojen integrointiprojekti luodaan.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: fb17d5e82709a34ff088774d9e9034adb714b58c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646250"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="51fc2-103">Tietojen integrointiprojektin luominen (esiversio)</span><span class="sxs-lookup"><span data-stu-id="51fc2-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="51fc2-104">Tässä ohjeaiheessa kerrotaan, miten tietojen integrointiprojekti luodaan.</span><span class="sxs-lookup"><span data-stu-id="51fc2-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="51fc2-105">Kirjaudu Microsoft Dynamics 365 Financeiin.</span><span class="sxs-lookup"><span data-stu-id="51fc2-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="51fc2-106">Siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Tietoyksiköt**.</span><span class="sxs-lookup"><span data-stu-id="51fc2-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="51fc2-107">Odota, kunnes kaikki tietoyksiköt on päivitetty, ennen kuin siirryt seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="51fc2-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="51fc2-108">Avaa [Power Apps -portaali](https://make.powerapps.com/) ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="51fc2-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="51fc2-109">Valitse sopiva ympäristö.</span><span class="sxs-lookup"><span data-stu-id="51fc2-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="51fc2-110">Valitse vasemmassa siirtymisruudussa **Tiedot \> Yhteydet**.</span><span class="sxs-lookup"><span data-stu-id="51fc2-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="51fc2-111">Muodosta yhteys soveltuviin esiintymiin seuraavissa kohteissa:</span><span class="sxs-lookup"><span data-stu-id="51fc2-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="51fc2-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="51fc2-112">Dynamics 365</span></span>
        - <span data-ttu-id="51fc2-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="51fc2-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="51fc2-114">Avaa [Power Apps -ympäristöt](https://admin.powerapps.com/environments) ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="51fc2-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="51fc2-115">Valitse **Tietojen integrointiohjelma**.</span><span class="sxs-lookup"><span data-stu-id="51fc2-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="51fc2-116">Valitse **Yhteysjoukot**.</span><span class="sxs-lookup"><span data-stu-id="51fc2-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="51fc2-117">Valitse **Uusi yhteysjoukko**.</span><span class="sxs-lookup"><span data-stu-id="51fc2-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="51fc2-118">Kirjoita yhteyden nimi.</span><span class="sxs-lookup"><span data-stu-id="51fc2-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="51fc2-119">Valitse sopivat yhteydet seuraaville kohteille:</span><span class="sxs-lookup"><span data-stu-id="51fc2-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="51fc2-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="51fc2-120">Dynamics 365</span></span>
        - <span data-ttu-id="51fc2-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="51fc2-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="51fc2-122">Valitse sopiva organisaation yhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="51fc2-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="51fc2-123">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="51fc2-123">Select **Create**.</span></span>

5. <span data-ttu-id="51fc2-124">Avaa [Power Apps -ympäristöt](https://admin.powerapps.com/environments) ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="51fc2-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="51fc2-125">Luo seuraavien mallien tietojen integrointiprojektit käyttämällä juuri luomaasi yhteysjoukkoa:</span><span class="sxs-lookup"><span data-stu-id="51fc2-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="51fc2-126">Asiakasmaksujen tietojen tulokset kävijä tietojen tulokset (CDS:stä Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="51fc2-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="51fc2-127">Kassavirran aikasarjojen tulokset (CDS:stä Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="51fc2-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="51fc2-128">Budjetin aikasarjojen tulokset (CDS:stä Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="51fc2-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="51fc2-129">Määritä kunkin projektin oikea ajoittaminen.</span><span class="sxs-lookup"><span data-stu-id="51fc2-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="51fc2-130">Jos pakolliset entiteetit eivät näy CDS:ssä, siirry kohtaan **Luotonvalvonta > Asetukset > Finance Insights > Finance Insights -parametrit**. Ota käyttöön Asiakasmaksun ennusteet -toiminto ja ja valitse **Luo ennustemalli**-painike.</span><span class="sxs-lookup"><span data-stu-id="51fc2-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="51fc2-131">Kun tekoälymallin käyttöönotto on päättynyt (onnistunut tai epäonnistunut), integroinnin luomiseen tarvittavat CDS-entiteetit otetaan käyttöön CDS:ssä.</span><span class="sxs-lookup"><span data-stu-id="51fc2-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="51fc2-132">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="51fc2-132">Privacy notice</span></span>

<span data-ttu-id="51fc2-133">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="51fc2-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
