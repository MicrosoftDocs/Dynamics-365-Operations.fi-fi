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
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: f317b22f2794dc71093068a51c8e9d4e6d7d55ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231149"
---
# <a name="retail-price-reports"></a><span data-ttu-id="0de37-103">Vähittäismyyntihintaraportit</span><span class="sxs-lookup"><span data-stu-id="0de37-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="0de37-104">Jotta hinnat olisivat kilpailukykyisiä, vähittäismyyjät muuttavat usein tuotteiden hintoja.</span><span class="sxs-lookup"><span data-stu-id="0de37-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="0de37-105">Myymäläpäälliköt haluavat, että pääsevät helposti käsiksi äskettäisiin tau tuleviin hintamuutoksiin, jotta he voivat suunnitella tarvittavat resurssit myymälän hyllyissä näkyvien hintalappujen päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="0de37-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="0de37-106">Retailin versiossa 10.0 myymäläpäällikkö voi avata **Hinta**-raportin valitsemalla **Kaikki vähittäismyymälät \> Myymälä \> Hintaraportti** ja tarkastelemalla myymälään liitettyjen tuotteiden päivitettyjä hintoja.</span><span class="sxs-lookup"><span data-stu-id="0de37-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="0de37-107">Hintaraportti voidaan ottaa käyttöön, kun **Ota myymälän hintaraportti käyttöön** -parametrin on oltava käytössä.</span><span class="sxs-lookup"><span data-stu-id="0de37-107">To enable the price report, the **Enable price report for store** parameter must be turned on.</span></span> <span data-ttu-id="0de37-108">Tämä parametri sijaitsee **Commercen parametrit \> Alennukset \> Muut**-välilehdessä. Kun **Hintaraportti**-sivu avataan, avautuvassa valintaikkunassa on useita määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="0de37-108">This parameter is located on the **Commerce parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="0de37-109">Käytettävissä olevat määritykset on lueteltu seuraavaksi.</span><span class="sxs-lookup"><span data-stu-id="0de37-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="0de37-110">Konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="0de37-110">Configuration</span></span> | <span data-ttu-id="0de37-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="0de37-111">Description</span></span> |
|---|---|
| <span data-ttu-id="0de37-112">Päivämäärästä/Päivämäärään</span><span class="sxs-lookup"><span data-stu-id="0de37-112">From date / To date</span></span>| <span data-ttu-id="0de37-113">Päivämääräalue, jolle hintaraportti luodaan.</span><span class="sxs-lookup"><span data-stu-id="0de37-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="0de37-114">Kesto on tällä hetkellä enintään 7 päivää.</span><span class="sxs-lookup"><span data-stu-id="0de37-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="0de37-115">Kanava</span><span class="sxs-lookup"><span data-stu-id="0de37-115">Channel</span></span>| <span data-ttu-id="0de37-116">Myymälä, jolle hintaraportti luodaan.</span><span class="sxs-lookup"><span data-stu-id="0de37-116">The store for which the price report should be generated.</span></span> |
| <span data-ttu-id="0de37-117">Näytä tuotteet, joita on varastossa</span><span class="sxs-lookup"><span data-stu-id="0de37-117">Display products with available inventory</span></span>| <span data-ttu-id="0de37-118">Kun asetukseksi valitaan **Kyllä**, vain niiden tuotteiden hinnat näytetään, joita on tällä hetkellä myymälän fyysisessä varastossa.</span><span class="sxs-lookup"><span data-stu-id="0de37-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="0de37-119">Näytä versioiden hinnat</span><span class="sxs-lookup"><span data-stu-id="0de37-119">Display prices for variants</span></span> | <span data-ttu-id="0de37-120">Kun asetukseksi valitaan **Kyllä**, versioiden hinnat näytetään päätuotteiden ohella.</span><span class="sxs-lookup"><span data-stu-id="0de37-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="0de37-121">Tämä asetus **otetaan käyttöön** vain, jos käytössä versiokohtaisia hintoja, koska muutoin rivejä on erittäin paljon.</span><span class="sxs-lookup"><span data-stu-id="0de37-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="0de37-122">Tulevissa versioissa otetaan käyttöön dimensiopohjaiset hinnat, jolloin myymäläpäällikkö voi valita dimensiot, joiden hinnat näytetään.</span><span class="sxs-lookup"><span data-stu-id="0de37-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="0de37-123">Näytä tuotteet, joilla on hintamuutoksia</span><span class="sxs-lookup"><span data-stu-id="0de37-123">Display products with price changes</span></span> | <span data-ttu-id="0de37-124">Kun asetukseksi valitaan **Kyllä**, vain niiden päivämäärien hinnat näytetään, jolloin hintaa on muutettu.</span><span class="sxs-lookup"><span data-stu-id="0de37-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="0de37-125">Valitun **Päivämäärästä**-kentän *yhtä päivää aikaisempi* hinta on aina näkyvissä, jotta myymäläpäällikön on helppo havaita tuotteet, joiden hinta ei ole muuttunut koko valittuna ajanjaksona. Tällä tavoin hän näkee myös nykyisen hinnan.</span><span class="sxs-lookup"><span data-stu-id="0de37-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="0de37-126">Raportin luonnin jälkeen Excel-tiedosto voidaan ladata mahdollista lisäsuodatusta varten.</span><span class="sxs-lookup"><span data-stu-id="0de37-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="0de37-127">Hintaraportin avulla voidaan tarkistaa myös tuotteiden aiempien päivämäärien historialliset hinnat.</span><span class="sxs-lookup"><span data-stu-id="0de37-127">The price report can also be used to check the historical prices of products for past dates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]