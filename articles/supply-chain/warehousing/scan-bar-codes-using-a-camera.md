---
title: Viivakoodien lukeminen kameran avulla varastosovelluksessa
description: Tässä ohjeaiheessa käsitellään varastosovelluksen määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: fd4818ab936e1c93000793da756c97df6d05b2a9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426866"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a><span data-ttu-id="5c590-103">Viivakoodien lukeminen kameran avulla varastosovelluksessa</span><span class="sxs-lookup"><span data-stu-id="5c590-103">Scan bar codes using a camera in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c590-104">Tässä ohjeaiheessa käsitellään varastosovelluksen määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten.</span><span class="sxs-lookup"><span data-stu-id="5c590-104">This topic explains how to set up the warehouse app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="5c590-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="5c590-105">Prerequisites</span></span>
<span data-ttu-id="5c590-106">Tämän toiminnon käyttämiseen tarvitaan varastosovelluksen versio 1.2.0.0, ja laitteessa on oltava kamera.</span><span class="sxs-lookup"><span data-stu-id="5c590-106">To use this feature, you need to have version 1.2.0.0 of the warehouse app installed, and your device must have a camera.</span></span> <span data-ttu-id="5c590-107">Kun avaat sovelluksen päivityksen jälkeen, sovellus pyytää lupaasi käyttää kameraa.</span><span class="sxs-lookup"><span data-stu-id="5c590-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="5c590-108">Jos laiteessa ei ole kameraa, lupaa ei kysytä etkä voi käyttää kameraa skannerina.</span><span class="sxs-lookup"><span data-stu-id="5c590-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="5c590-109">Määritys</span><span class="sxs-lookup"><span data-stu-id="5c590-109">Setup</span></span>
<span data-ttu-id="5c590-110">Voit valita varastosovelluksen näyttöasetuksissa, käytetäänkö kameraa viivakoodin lukemiseen.</span><span class="sxs-lookup"><span data-stu-id="5c590-110">In the Display settings of the warehouse application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="5c590-111">Jos otat **kameran käytön skannerina** käyttöön, voit käyttää kameraa jokaisessa syöttömenetelmäksi, jonka ensisijaiseksi syötetilaksi on määritetty **Luetaan**.</span><span class="sxs-lookup"><span data-stu-id="5c590-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="5c590-112">Voit määrittää, voiko syötekentän lukea, valitsemalla **Varastosovelluksen kenttien nimet** -sivulla **Ensisijainen syöttömenetelmä** -asetukseksi **Luetaan**.</span><span class="sxs-lookup"><span data-stu-id="5c590-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="5c590-113">Kun tämä asetus on valittu, kameraa voidaan käyttää skannaukseen varastosovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="5c590-113">When this option is selected, a camera can be used for scanning in the warehouse app.</span></span> <span data-ttu-id="5c590-114">Lisätietoja sovelluskenttien nimien määrittämisestä varastosovelluksessa on kohdassa [Varastosovelluksen kenttien nimien määrittäminen](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="5c590-114">For information about how to configure app field names in Warehousing, see [Configure app field names in warehouse app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="5c590-115">Tuetut viivakoodimuodot</span><span class="sxs-lookup"><span data-stu-id="5c590-115">Supported bar code formats</span></span>
<span data-ttu-id="5c590-116">Eniten käytettyjä viivakoodimuotoja tuetaan. Niitä ovat esimerkiksi Koodi 128, Koodi 39, Koodi 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodit.</span><span class="sxs-lookup"><span data-stu-id="5c590-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="5c590-117">Siirtyminen</span><span class="sxs-lookup"><span data-stu-id="5c590-117">Navigation</span></span>
<span data-ttu-id="5c590-118">Kamerasivu käynnistetään jokaisella sivulla, jonka syötekentän ensisijaiseksi syöttömenetelmäksi on valittu Luetaan. Voit liikkua Kamera-sivulla seuraavien asetusten avulla:</span><span class="sxs-lookup"><span data-stu-id="5c590-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="5c590-119">Voit palata Tehtävät ja tiedot -sivulle napsauttamalla Takaisin-painiketta.</span><span class="sxs-lookup"><span data-stu-id="5c590-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="5c590-120">Kun napsautat kynäkuvaketta Tehtävät ja tiedot -sivulla, voit siirtyä sivulle, jossa voit kirjoittaa tiedot manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="5c590-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="5c590-121">Voit palata Kamera-sivulle napsauttamalla kamerakuvaketta Tehtävät ja tiedot -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5c590-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="5c590-122">Tehtävät ja tiedot -sivu</span><span class="sxs-lookup"><span data-stu-id="5c590-122">Task and details page</span></span> | <span data-ttu-id="5c590-123">Kamera-sivu</span><span class="sxs-lookup"><span data-stu-id="5c590-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Kameranluvun esimerkkitehtävän tietosivu](./media/camera-scanning-example-task-detail-page50.png)          | ![Kameranluvun esimerkkitehtävän pienempi tietosivu](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="5c590-126">Kun napsautat Kamera-sivulla kamerapainiketta, se näkyy himmeänä viivakoodin tunnistusyrityksen ajan.</span><span class="sxs-lookup"><span data-stu-id="5c590-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="5c590-127">Jos viivakoodia ei tunnisteta 5 sekunnin kuluessa, prosessi aikakatkaistaan ja kamerapainiketta voi taas käyttää.</span><span class="sxs-lookup"><span data-stu-id="5c590-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="5c590-128">Voit sitten yrittää lukea viivakoodin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="5c590-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="5c590-129">Kun osoitat viivakoodia kameralla, saat parhaan tuloksen, kun viivakoodi on kohdistettu viivojen sisälle.</span><span class="sxs-lookup"><span data-stu-id="5c590-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="5c590-130">Kun viivakoodi on luettu, tulos käsitellään ja siirryt seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="5c590-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="5c590-131">Jos seuraavassa vaiheessa on toinen syötekenttä, jonka ensisijaiseksi syöttömenetelmäksi on valittu Luetaan, kamerasivu käynnistyy uudelleen.</span><span class="sxs-lookup"><span data-stu-id="5c590-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="5c590-132">Jos seuraava vaihe ei ole luettava kenttä, kamerasivu ei käynnisty.</span><span class="sxs-lookup"><span data-stu-id="5c590-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

