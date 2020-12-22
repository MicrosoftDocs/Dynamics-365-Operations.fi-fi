---
title: Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten
description: Tässä aiheessa kerrotaan, miten Excel-työkirja luodaan niin, että vähittäismyyntitapahtumia voidaan muokata Microsoft Dynamics 365 Commercessa.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458965"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="59c58-103">Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="59c58-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59c58-104">Tässä aiheessa kerrotaan, miten Excel-työkirja luodaan niin, että vähittäismyyntitapahtumia voidaan muokata Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="59c58-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="59c58-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="59c58-105">Overview</span></span>

<span data-ttu-id="59c58-106">Asiakkaat voivat käyttää tätä esimääritettyä Excel-mallia järjestelmän eri osissa ja muokata ja tarkistaa sen avulla vähittäismyyntitapahtumia.</span><span class="sxs-lookup"><span data-stu-id="59c58-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="59c58-107">Asiakkaat voivat luoda myös mukautetun Excel-työkirjan tätä tarkoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="59c58-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="59c58-108">Excel-työkirjan luominen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="59c58-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="59c58-109">Alla olevien ohjeiden avulla voit luoda ja määrittää Excel-työkirjan niin, että vähittäismyyntitapahtumia on mahdollista muokata.</span><span class="sxs-lookup"><span data-stu-id="59c58-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="59c58-110">Avaa Excel ja luo tyhjä työkirja.</span><span class="sxs-lookup"><span data-stu-id="59c58-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="59c58-111">Valitse **Lisää**-välilehdessä **Omat apuohjelmat**.</span><span class="sxs-lookup"><span data-stu-id="59c58-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="59c58-112">Valitse oikeanpuoleisessa ruudussa **Lisää palvelimen tiedot** -linkki.</span><span class="sxs-lookup"><span data-stu-id="59c58-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="59c58-113">Syötä palvelimen URL-osoite ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="59c58-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="59c58-114">Jos näyttöön tulee Sovelman rekisteröintejä ei löytynyt -virhesanoma, ratkaise ongelma seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="59c58-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="59c58-115">Siirry Commerce-sovelluksessa kohtaan **Järjestelmän hallinta \> Asetukset \> Office-sovelluksen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="59c58-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="59c58-116">Valitse **Sovellusparametrit**-pikavälilehdessä **Käynnistä sovellusparametrit**.</span><span class="sxs-lookup"><span data-stu-id="59c58-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="59c58-117">Valitse vahvistussanomaruudussa **OK**.</span><span class="sxs-lookup"><span data-stu-id="59c58-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="59c58-118">Valitse **Rekisteröidyt sovelmat** -pikavälilehdessä **Käynnistä sovelman rekisteröinti**.</span><span class="sxs-lookup"><span data-stu-id="59c58-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="59c58-119">Toista nämä kolme vaihetta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="59c58-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="59c58-120">Valitse **Rakenne** ja valitse sitten **Lisää taulukko**.</span><span class="sxs-lookup"><span data-stu-id="59c58-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="59c58-121">Valitse muokattavien tietojen perusteella entiteetit, jotka on lisättävä Excel-työkirjaan muokkausta varten.</span><span class="sxs-lookup"><span data-stu-id="59c58-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="59c58-122">Käytä seuraavaa taulukkoa viitteenä.</span><span class="sxs-lookup"><span data-stu-id="59c58-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="59c58-123">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="59c58-123">Transaction type</span></span> | <span data-ttu-id="59c58-124">Käytettävät tietoentiteetit</span><span class="sxs-lookup"><span data-stu-id="59c58-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="59c58-125">Itsepalvelutukkutapahtumat, Online-tilaukset, Asynkroniset asiakastilaukset, Asynkroniset asiakastarjoukset</span><span class="sxs-lookup"><span data-stu-id="59c58-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="59c58-126">Tapahtuma (tarkistettavissa), Myyntitapahtuma (tarkistettavissa), Maksutapahtumat (tarkistettavissa), Verotapahtumat (tarkistettavissa), Alennustapahtumat (tarkistettavissa), Muutostapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="59c58-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="59c58-127">Toimitus pankkiin</span><span class="sxs-lookup"><span data-stu-id="59c58-127">Bank drop</span></span> | <span data-ttu-id="59c58-128">Tapahtuma (tarkistettavissa), Pankkiin toimitetut maksuvälinetapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="59c58-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="59c58-129">Toimitus kassakaappiin</span><span class="sxs-lookup"><span data-stu-id="59c58-129">Safe drop</span></span> | <span data-ttu-id="59c58-130">Tapahtuma (tarkistettavissa), Kassakaapin maksuvälinetapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="59c58-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="59c58-131">Kassan laskeminen maksuvälineittäin</span><span class="sxs-lookup"><span data-stu-id="59c58-131">Tender declaration</span></span> | <span data-ttu-id="59c58-132">Tapahtuma (tarkistettavissa), Kassan laskeminen maksuvälineittäin -tapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="59c58-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="59c58-133">Tulot, kulut</span><span class="sxs-lookup"><span data-stu-id="59c58-133">Income, Expense</span></span> | <span data-ttu-id="59c58-134">Tapahtuma (tarkistettavissa), Tulo-/kulutapahtumat (tarkistettavissa), Maksutapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="59c58-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="59c58-135">Ilmoita aloitussumma, Maksuvälineen poisto, Liukuva merkintä, Maksuvälineen vaihto, Laskun maksu, Asiakkaan talletus</span><span class="sxs-lookup"><span data-stu-id="59c58-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="59c58-136">Tapahtuma (tarkistettavissa), Maksutapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="59c58-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="59c58-137">Excel-työkirjaan tulee lisätä vain yksi tietoentiteetti.</span><span class="sxs-lookup"><span data-stu-id="59c58-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="59c58-138">Lisäksi kaikki kentät, jotka on merkitty avainsymbolilla, on lisättävä soveltuvaan työkirjaan.</span><span class="sxs-lookup"><span data-stu-id="59c58-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="59c58-139">Kun työkirja on määritetty, ota tarvittavat suodattimet käyttöön.</span><span class="sxs-lookup"><span data-stu-id="59c58-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="59c58-140">Varmista, että kohdistat samat suodattimet tiedoston kaikkiin laskentataulukoihin.</span><span class="sxs-lookup"><span data-stu-id="59c58-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="59c58-141">Vältä suurten tietomäärien lataamista Excel-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="59c58-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="59c58-142">Muussa tapauksessa suorituskyky voi alentua, ja Excelin ja järjestelmän toiminta hidastuu.</span><span class="sxs-lookup"><span data-stu-id="59c58-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="59c58-143">Tiedoston suodattimina kannattaa aina käyttää Yritys-suodatinta ja joko Laskelmanumero- tai Tapahtumanumero-suodatinta.</span><span class="sxs-lookup"><span data-stu-id="59c58-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="59c58-144">Kun suodattimet on määritetty, päivitä tiedot valitsemalla **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="59c58-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="59c58-145">Muokkaa vaadittuja tietoja ja julkaise ne.</span><span class="sxs-lookup"><span data-stu-id="59c58-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="59c58-146">Jos **Julkaise**-painike ei ole käytettävissä, joitakin kenttiä ei todennäköisesti ole lisätty Excel-työkirjaan.</span><span class="sxs-lookup"><span data-stu-id="59c58-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59c58-147">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="59c58-147">Additional resources</span></span>

[<span data-ttu-id="59c58-148">Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen</span><span class="sxs-lookup"><span data-stu-id="59c58-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="59c58-149">Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="59c58-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="59c58-150">Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="59c58-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="59c58-151">Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="59c58-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
