---
title: Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten
description: Tässä aiheessa kerrotaan, miten Excel-työkirja luodaan niin, että vähittäismyyntitapahtumia voidaan muokata Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a2d41dd0470a4abae1a8238be8f1549fb094a026
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795736"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="2669c-103">Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="2669c-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2669c-104">Tässä aiheessa kerrotaan, miten Excel-työkirja luodaan niin, että vähittäismyyntitapahtumia voidaan muokata Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="2669c-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2669c-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2669c-105">Overview</span></span>

<span data-ttu-id="2669c-106">Asiakkaat voivat käyttää tätä esimääritettyä Excel-mallia järjestelmän eri osissa ja muokata ja tarkistaa sen avulla vähittäismyyntitapahtumia.</span><span class="sxs-lookup"><span data-stu-id="2669c-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="2669c-107">Asiakkaat voivat luoda myös mukautetun Excel-työkirjan tätä tarkoitusta varten.</span><span class="sxs-lookup"><span data-stu-id="2669c-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="2669c-108">Excel-työkirjan luominen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2669c-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="2669c-109">Alla olevien ohjeiden avulla voit luoda ja määrittää Excel-työkirjan niin, että vähittäismyyntitapahtumia on mahdollista muokata.</span><span class="sxs-lookup"><span data-stu-id="2669c-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="2669c-110">Avaa Excel ja luo tyhjä työkirja.</span><span class="sxs-lookup"><span data-stu-id="2669c-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="2669c-111">Valitse **Lisää**-välilehdessä **Omat apuohjelmat**.</span><span class="sxs-lookup"><span data-stu-id="2669c-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="2669c-112">Valitse oikeanpuoleisessa ruudussa **Lisää palvelimen tiedot** -linkki.</span><span class="sxs-lookup"><span data-stu-id="2669c-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="2669c-113">Syötä palvelimen URL-osoite ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2669c-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="2669c-114">Jos näyttöön tulee Sovelman rekisteröintejä ei löytynyt -virhesanoma, ratkaise ongelma seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="2669c-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="2669c-115">Siirry Commerce-sovelluksessa kohtaan **Järjestelmän hallinta \> Asetukset \> Office-sovelluksen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="2669c-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="2669c-116">Valitse **Sovellusparametrit**-pikavälilehdessä **Käynnistä sovellusparametrit**.</span><span class="sxs-lookup"><span data-stu-id="2669c-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="2669c-117">Valitse vahvistussanomaruudussa **OK**.</span><span class="sxs-lookup"><span data-stu-id="2669c-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="2669c-118">Valitse **Rekisteröidyt sovelmat** -pikavälilehdessä **Käynnistä sovelman rekisteröinti**.</span><span class="sxs-lookup"><span data-stu-id="2669c-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="2669c-119">Toista nämä kolme vaihetta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="2669c-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="2669c-120">Valitse **Rakenne** ja valitse sitten **Lisää taulukko**.</span><span class="sxs-lookup"><span data-stu-id="2669c-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="2669c-121">Valitse muokattavien tietojen perusteella entiteetit, jotka on lisättävä Excel-työkirjaan muokkausta varten.</span><span class="sxs-lookup"><span data-stu-id="2669c-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="2669c-122">Käytä seuraavaa taulukkoa viitteenä.</span><span class="sxs-lookup"><span data-stu-id="2669c-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="2669c-123">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="2669c-123">Transaction type</span></span> | <span data-ttu-id="2669c-124">Käytettävät tietoentiteetit</span><span class="sxs-lookup"><span data-stu-id="2669c-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="2669c-125">Itsepalvelutukkutapahtumat, Online-tilaukset, Asynkroniset asiakastilaukset, Asynkroniset asiakastarjoukset</span><span class="sxs-lookup"><span data-stu-id="2669c-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="2669c-126">Tapahtuma (tarkistettavissa), Myyntitapahtuma (tarkistettavissa), Maksutapahtumat (tarkistettavissa), Verotapahtumat (tarkistettavissa), Alennustapahtumat (tarkistettavissa), Muutostapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="2669c-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="2669c-127">Toimitus pankkiin</span><span class="sxs-lookup"><span data-stu-id="2669c-127">Bank drop</span></span> | <span data-ttu-id="2669c-128">Tapahtuma (tarkistettavissa), Pankkiin toimitetut maksuvälinetapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="2669c-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="2669c-129">Toimitus kassakaappiin</span><span class="sxs-lookup"><span data-stu-id="2669c-129">Safe drop</span></span> | <span data-ttu-id="2669c-130">Tapahtuma (tarkistettavissa), Kassakaapin maksuvälinetapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="2669c-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="2669c-131">Kassan laskeminen maksuvälineittäin</span><span class="sxs-lookup"><span data-stu-id="2669c-131">Tender declaration</span></span> | <span data-ttu-id="2669c-132">Tapahtuma (tarkistettavissa), Kassan laskeminen maksuvälineittäin -tapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="2669c-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="2669c-133">Tulot, kulut</span><span class="sxs-lookup"><span data-stu-id="2669c-133">Income, Expense</span></span> | <span data-ttu-id="2669c-134">Tapahtuma (tarkistettavissa), Tulo-/kulutapahtumat (tarkistettavissa), Maksutapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="2669c-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="2669c-135">Ilmoita aloitussumma, Maksuvälineen poisto, Liukuva merkintä, Maksuvälineen vaihto, Laskun maksu, Asiakkaan talletus</span><span class="sxs-lookup"><span data-stu-id="2669c-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="2669c-136">Tapahtuma (tarkistettavissa), Maksutapahtumat (tarkistettavissa)</span><span class="sxs-lookup"><span data-stu-id="2669c-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="2669c-137">Excel-työkirjaan tulee lisätä vain yksi tietoentiteetti.</span><span class="sxs-lookup"><span data-stu-id="2669c-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="2669c-138">Lisäksi kaikki kentät, jotka on merkitty avainsymbolilla, on lisättävä soveltuvaan työkirjaan.</span><span class="sxs-lookup"><span data-stu-id="2669c-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="2669c-139">Kun työkirja on määritetty, ota tarvittavat suodattimet käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2669c-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="2669c-140">Varmista, että kohdistat samat suodattimet tiedoston kaikkiin laskentataulukoihin.</span><span class="sxs-lookup"><span data-stu-id="2669c-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="2669c-141">Vältä suurten tietomäärien lataamista Excel-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="2669c-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="2669c-142">Muussa tapauksessa suorituskyky voi alentua, ja Excelin ja järjestelmän toiminta hidastuu.</span><span class="sxs-lookup"><span data-stu-id="2669c-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="2669c-143">Tiedoston suodattimina kannattaa aina käyttää Yritys-suodatinta ja joko Laskelmanumero- tai Tapahtumanumero-suodatinta.</span><span class="sxs-lookup"><span data-stu-id="2669c-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="2669c-144">Kun suodattimet on määritetty, päivitä tiedot valitsemalla **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="2669c-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="2669c-145">Muokkaa vaadittuja tietoja ja julkaise ne.</span><span class="sxs-lookup"><span data-stu-id="2669c-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="2669c-146">Jos **Julkaise**-painike ei ole käytettävissä, joitakin kenttiä ei todennäköisesti ole lisätty Excel-työkirjaan.</span><span class="sxs-lookup"><span data-stu-id="2669c-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2669c-147">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2669c-147">Additional resources</span></span>

[<span data-ttu-id="2669c-148">Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen</span><span class="sxs-lookup"><span data-stu-id="2669c-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="2669c-149">Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="2669c-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="2669c-150">Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="2669c-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="2669c-151">Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="2669c-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]