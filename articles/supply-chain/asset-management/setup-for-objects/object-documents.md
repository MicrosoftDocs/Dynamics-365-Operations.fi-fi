---
title: Resurssin asiakirjat
description: Tässä ohjeaiheessa kerrotaan resurssien asiakirjoista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1c90788da7ad536fb9978db18160ccf6c158033
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783225"
---
# <a name="asset-documents"></a><span data-ttu-id="6cf6e-103">Resurssin asiakirjat</span><span class="sxs-lookup"><span data-stu-id="6cf6e-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6cf6e-104">Tässä ohjeaiheessa kerrotaan resurssien asiakirjoista resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="6cf6e-105">Resurssien hallinnassa voit määrittää asiakirjoja niin, että ne liittyvät automaattisesti esimerkiksi työtyyppeihin, resurssien valmistajiin, resurssityyppeihin tai resursseihin.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="6cf6e-106">Tämä toiminto on hyödyllinen, kun päivitetyt tiedostoversiot vapautetaan.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="6cf6e-107">Tällöin sinun on vain asetettava päivitetty asiakirja Microsoft Dynamics 365 for Finance and Operationsin asiakirjojen vakiosijaintiin ja liitettävä asiakirja luomaasi resurssin asiakirjatietueeseen.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-107">In that case, you just have to put the updated document in the standard location that you use for your Microsoft Dynamics 365 for Finance and Operations documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="6cf6e-108">Päivitettyä asiakirjaa voi sitten käyttää valikkokohteissa **Kaikki resurssit**, **Aktiiviset resurssit**, **Omat aktiiviset resurssit**, **Kaikki työtilaukset** ja **Aktiivisten työtilausten työt**.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="6cf6e-109">Prosessi, jossa asiakirjoja liitetään resurssin asiakirjatietueeseen, käyttää Finance and Operationsin asiakirjojen vakiokäsittelyjärjestelmää.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-109">The process for attaching documents to an asset document record uses the standard document handling system in Finance and Operations.</span></span>

<span data-ttu-id="6cf6e-110">**Esimerkki 1:** työtyyppiin liittyvä tiedosto voi kuvata kyseisen työlajin proseduurin.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="6cf6e-111">**Esimerkki 2:** resurssityypin, valmistajan ja mallin yhdistelmään liittyvä asiakirja voi olla valitun resurssin valmistajan mallin vakiokäsikirja.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="6cf6e-112">Luo resurssin ja asiakirjan suhde</span><span class="sxs-lookup"><span data-stu-id="6cf6e-112">Create asset document relation</span></span>

1. <span data-ttu-id="6cf6e-113">Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssin asiakirjat**.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="6cf6e-114">Luo resurssin asiakirjatietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="6cf6e-115">Tee tarvittavat valinnat seuraavista kentistä sen mukaan, miten tiedostosuhde halutaan määrittää: **resurssityyppi**, **valmistaja**, **malli**, **resurssi**, **Työtyypin luokka**, **Työtyyppi**, **Työtyypin variantti** ja **Työtarve**.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="6cf6e-116">**Työtyypin variantti**- ja **Työtarve**-kentissä käytettävissä olevat vaihtoehdot määräytyvät **Työtyyppi**-kentässä tehdyn valinnan mukaan.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6cf6e-117">Kun järjestelmä etsii asiakirjoja, jotka liittyvät resurssiiin tai työtilaukseen, resurssien hallinta käy läpi kaikki resurssiasiakirjan tietueet ja tarkistaa mahdollisen vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="6cf6e-118">Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="6cf6e-119">Toisin sanoen resurssien hallinta tarkistaa ensin **Työtarve**-kentän vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="6cf6e-120">Jos vastaavuutta ei löydy, se tarkistaa **Työtyypin variantti** -kentän vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="6cf6e-121">Jos vastaavuutta ei löydy, se tarkistaa **Työtyyppi** -kentän vastaavuuden ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="6cf6e-122">Kuten näet **Resurssin asiakirjat** -sivun asettelussa, tämä tarkoittaa sitä, että jos haluat löytää erityisen yhdistelmän, omaisuuden hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta se vastaa toisiaan.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="6cf6e-123">Useita asiakirjoja voi liittyä resurssiin tai työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="6cf6e-124">Voit muokata ylläpitopyynnössä tai työtilauksessa palvelutasoa.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="6cf6e-125">Valitse **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-125">Select **Attachments**.</span></span> <span data-ttu-id="6cf6e-126">Näkyviin tulee Finance and Operationsin tavanomainen **Tiedoston käsittely** -sivu.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-126">The standard **Document handling** page in Finance and Operations appears.</span></span>
5. <span data-ttu-id="6cf6e-127">Määritä asiakirjat tai huomautukset, jotka liitetään resurssin asiakirjatietueeseen.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="6cf6e-128">Kun olet liittänyt tiedostot, **Liitteet**-kentässä näkyy tietueeseen liittyvien tiedostojen määrä.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
