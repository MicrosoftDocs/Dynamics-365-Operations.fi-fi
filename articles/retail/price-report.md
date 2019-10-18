---
title: Vähittäismyyntihintaraportit
description: Tässä ohjeaiheessa on hintaraporttitoiminnon yleiskatsaus. Tämän toiminnon avulla voidaan tarkastella lajiteltujen tuotteiden tulevia hintamuutoksia.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 4fb02bdeca2d71d84ebdddfd16d471a532823e42
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025192"
---
# <a name="retail-price-reports"></a><span data-ttu-id="cc6d9-103">Vähittäismyyntihintaraportit</span><span class="sxs-lookup"><span data-stu-id="cc6d9-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="cc6d9-104">Jotta hinnat olisivat kilpailukykyisiä, vähittäismyyjät muuttavat usein tuotteiden hintoja.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="cc6d9-105">Myymäläpäälliköt haluavat, että pääsevät helposti käsiksi äskettäisiin tau tuleviin hintamuutoksiin, jotta he voivat suunnitella tarvittavat resurssit myymälän hyllyissä näkyvien hintalappujen päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="cc6d9-106">Retailin versiossa 10.0 myymäläpäällikkö voi avata **Hinta**-raportin valitsemalla **Kaikki vähittäismyymälät \> Myymälä \> Hintaraportti ja** tarkastelemalla myymälään liitettyjen tuotteiden päivitettyjä hintoja.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All retail stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="cc6d9-107">Hintaraportti voidaan ottaa käyttöön, kun **Ota vähittäismyymälän hintaraportti käyttöön** -parametrin on oltava käytössä.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-107">To enable the price report, the **Enable price report for Retail store** parameter must be turned on.</span></span> <span data-ttu-id="cc6d9-108">Tämä parametri sijaitsee **Vähittäismyynnin parametrit \> Alennukset \> Muut**-välilehdessä. Kun **Hintaraportti**-sivu avataan, avautuvassa valintaikkunassa on useita määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-108">This parameter is located on the **Retail parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="cc6d9-109">Käytettävissä olevat määritykset on lueteltu seuraavaksi.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="cc6d9-110">Konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="cc6d9-110">Configuration</span></span> | <span data-ttu-id="cc6d9-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="cc6d9-111">Description</span></span> |
|---|---|
| <span data-ttu-id="cc6d9-112">Päivämäärästä/Päivämäärään</span><span class="sxs-lookup"><span data-stu-id="cc6d9-112">From date / To date</span></span>| <span data-ttu-id="cc6d9-113">Päivämääräalue, jolle hintaraportti luodaan.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="cc6d9-114">Kesto on tällä hetkellä enintään 7 päivää.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="cc6d9-115">Kanava</span><span class="sxs-lookup"><span data-stu-id="cc6d9-115">Channel</span></span>| <span data-ttu-id="cc6d9-116">Vähittäismyymälä, jolle hintaraportti luodaan.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-116">The retail store for which the price report should be generated.</span></span> |
| <span data-ttu-id="cc6d9-117">Näytä tuotteet, joita on varastossa</span><span class="sxs-lookup"><span data-stu-id="cc6d9-117">Display products with available inventory</span></span>| <span data-ttu-id="cc6d9-118">Kun asetukseksi valitaan **Kyllä**, vain niiden tuotteiden hinnat näytetään, joita on tällä hetkellä myymälän fyysisessä varastossa.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="cc6d9-119">Näytä versioiden hinnat</span><span class="sxs-lookup"><span data-stu-id="cc6d9-119">Display prices for variants</span></span> | <span data-ttu-id="cc6d9-120">Kun asetukseksi valitaan **Kyllä**, versioiden hinnat näytetään päätuotteiden ohella.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="cc6d9-121">Tämä asetus **otetaan käyttöön** vain, jos käytössä versiokohtaisia hintoja, koska muutoin rivejä on erittäin paljon.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="cc6d9-122">Tulevissa versioissa otetaan käyttöön dimensiopohjaiset hinnat, jolloin myymäläpäällikkö voi valita dimensiot, joiden hinnat näytetään.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="cc6d9-123">Näytä tuotteet, joilla on hintamuutoksia</span><span class="sxs-lookup"><span data-stu-id="cc6d9-123">Display products with price changes</span></span> | <span data-ttu-id="cc6d9-124">Kun asetukseksi valitaan **Kyllä**, vain niiden päivämäärien hinnat näytetään, jolloin hintaa on muutettu.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="cc6d9-125">Valitun **Päivämäärästä**-kentän *yhtä päivää aikaisempi* hinta on aina näkyvissä, jotta myymäläpäällikön on helppo havaita tuotteet, joiden hinta ei ole muuttunut koko valittuna ajanjaksona. Tällä tavoin hän näkee myös nykyisen hinnan.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="cc6d9-126">Raportin luonnin jälkeen Excel-tiedosto voidaan ladata mahdollista lisäsuodatusta varten.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="cc6d9-127">Hintaraportin avulla voidaan tarkistaa myös tuotteiden aiempien päivämäärien historialliset hinnat.</span><span class="sxs-lookup"><span data-stu-id="cc6d9-127">The price report can also be used to check the historical prices of products for past dates.</span></span>
