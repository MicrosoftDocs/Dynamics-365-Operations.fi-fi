---
title: Ehdota käyttöomaisuuden hankintaa
description: Näiden ohjeiden avulla voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9259c9bbf52c1c09a7092db6976fc3fabca6601
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990436"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="ce61d-103">Ehdota käyttöomaisuuden hankintaa</span><span class="sxs-lookup"><span data-stu-id="ce61d-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce61d-104">Näiden ohjeiden avulla voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="ce61d-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="ce61d-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="ce61d-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="ce61d-106">Jos aiot hankkia käyttöomaisuuden käyttöomaisuuden ehdotuskirjauskansion avulla, ensin on luotava käyttöomaisuustietue ja sitten määritettävä hankintahinta käyttöomaisuuskirjassa.</span><span class="sxs-lookup"><span data-stu-id="ce61d-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="ce61d-107">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="ce61d-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="ce61d-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ce61d-108">Select **New**.</span></span>
3. <span data-ttu-id="ce61d-109">Anna tai valitse arvo **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce61d-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="ce61d-110">Valitse toimintoruudussa **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="ce61d-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="ce61d-111">Valitse **Ehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="ce61d-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="ce61d-112">Valitse **Hankintaehdotus**.</span><span class="sxs-lookup"><span data-stu-id="ce61d-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="ce61d-113">Valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="ce61d-113">Select **Filter**.</span></span> <span data-ttu-id="ce61d-114">Tyhjennä aiemmat arvot valitsemalla **Palauta**.</span><span class="sxs-lookup"><span data-stu-id="ce61d-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="ce61d-115">Valitse **Käyttöomaisuuserän numero** -rivi.</span><span class="sxs-lookup"><span data-stu-id="ce61d-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="ce61d-116">Anna tai valitse arvo **Ehdot**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce61d-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="ce61d-117">Määritä muut ehdot käyttöomaisuuserille, jotka haluat hakea tämän ehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="ce61d-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="ce61d-118">Poistu ruudusta valitsemalla **OK** kahdesti.</span><span class="sxs-lookup"><span data-stu-id="ce61d-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="ce61d-119">Tarkista luodut tapahtumarivit.</span><span class="sxs-lookup"><span data-stu-id="ce61d-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="ce61d-120">Hankintaehdotukseen sisällytetään vain se käyttöomaisuuserä, jonka hankintapäivämäärä ja -hinta on määritetty kirjassa.</span><span class="sxs-lookup"><span data-stu-id="ce61d-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="ce61d-121">Valitse sivulla **Kirjat**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="ce61d-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="ce61d-122">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="ce61d-122">Select **Post**.</span></span>
