---
title: "Viivakoodien lukeminen kameralla Dynamics 365 for Finance and Operations – Warehousingissa"
description: "Tässä ohjeaiheessa käsitellään Dynamics 365 for Finance and Operations – Warehousingin määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 36378f0a8a87bb89c7e143d571c625904772bf1c
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a><span data-ttu-id="f2e10-103">Viivakoodien lukeminen kameralla Dynamics 365 for Finance and Operations – Warehousingissa</span><span class="sxs-lookup"><span data-stu-id="f2e10-103">Scan bar codes using a camera in Dynamics 365 for Finance and Operations – Warehousing</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f2e10-104">Tässä ohjeaiheessa käsitellään Dynamics 365 for Finance and Operations – Warehousingin määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten.</span><span class="sxs-lookup"><span data-stu-id="f2e10-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="f2e10-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="f2e10-105">Prerequisites</span></span>
<span data-ttu-id="f2e10-106">Tämän toiminnon käyttämiseen tarvitaan Warehousing 1.2.0.0, ja laitteessa on oltava kamera.</span><span class="sxs-lookup"><span data-stu-id="f2e10-106">To use this feature, you need to have version 1.2.0.0 of Warehousing installed, and your device must have a camera.</span></span> <span data-ttu-id="f2e10-107">Kun avaat sovelluksen päivityksen jälkeen, sinua pyydetään sallimaan kameran käyttö Dynamics 365 for Finance and Operations – Warehousing -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f2e10-107">When you open the app after updating, you will be prompted to allow the Dynamics 365 for Finance and Operations – Warehousing application to use the camera.</span></span> <span data-ttu-id="f2e10-108">Jos laiteessa ei ole kameraa, lupaa ei kysytä etkä voi käyttää kameraa skannerina.</span><span class="sxs-lookup"><span data-stu-id="f2e10-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="f2e10-109">Määritys</span><span class="sxs-lookup"><span data-stu-id="f2e10-109">Setup</span></span>
<span data-ttu-id="f2e10-110">Voit valita Warehousing-sovelluksen näyttöasetuksissa, käytetäänkö kameraa viivakoodin lukemiseen.</span><span class="sxs-lookup"><span data-stu-id="f2e10-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="f2e10-111">Jos otat **kameran käytön skannerina** käyttöön, voit käyttää kameraa jokaisessa syöttömenetelmäksi, jonka ensisijaiseksi syötetilaksi on määritetty **Luetaan**.</span><span class="sxs-lookup"><span data-stu-id="f2e10-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="f2e10-112">Voit määrittää, voiko syötekentän lukea, valitsemalla Dynamics 365 for Finance and Operationsin **Varastosovelluksen kenttänimet** -sivulla **Ensisijainen syöttömenetelmä** -asetukseksi **Luetaan**.</span><span class="sxs-lookup"><span data-stu-id="f2e10-112">To control whether an input field should be scannable, on the **Warehouse app field names** page in Dynamics 365 for Finance and Operations, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="f2e10-113">Kun tämä asetus on valittu, kameraa voidaan käyttää skannaukseen Warehousing-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f2e10-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="f2e10-114">Lisätietoja sovelluskenttien nimien määrittämisestä Warehousing-sovelluksessa on kohdassa [Warehousing-sovelluksen kenttien nimien määrittäminen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="f2e10-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="f2e10-115">Tuetut viivakoodimuodot</span><span class="sxs-lookup"><span data-stu-id="f2e10-115">Supported bar code formats</span></span>
<span data-ttu-id="f2e10-116">Eniten käytettyjä viivakoodimuotoja tuetaan. Niitä ovat esimerkiksi Koodi 128, Koodi 39, Koodi 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodit.</span><span class="sxs-lookup"><span data-stu-id="f2e10-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="f2e10-117">Siirtyminen</span><span class="sxs-lookup"><span data-stu-id="f2e10-117">Navigation</span></span>
<span data-ttu-id="f2e10-118">Kamerasivu käynnistetään jokaisella sivulla, jonka syötekentän ensisijaiseksi syöttömenetelmäksi on valittu Luetaan. Voit liikkua Kamera-sivulla seuraavien asetusten avulla:</span><span class="sxs-lookup"><span data-stu-id="f2e10-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="f2e10-119">Voit palata Tehtävät ja tiedot -sivulle napsauttamalla Takaisin-painiketta.</span><span class="sxs-lookup"><span data-stu-id="f2e10-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="f2e10-120">Kun napsautat kynäkuvaketta Tehtävät ja tiedot -sivulla, voit siirtyä sivulle, jossa voit kirjoittaa tiedot manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="f2e10-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="f2e10-121">Voit palata Kamera-sivulle napsauttamalla kamerakuvaketta Tehtävät ja tiedot -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f2e10-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="f2e10-122">Tehtävät ja tiedot -sivu</span><span class="sxs-lookup"><span data-stu-id="f2e10-122">Task and details page</span></span> | <span data-ttu-id="f2e10-123">Kamera-sivu</span><span class="sxs-lookup"><span data-stu-id="f2e10-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![kamera-luetaan-esimerkki-tehtävä-tiedot-sivu](./media/camera-scanning-example-task-detail-page50.png)          | ![kamera-luetaan-esimerkki-kamera-sivu-pieni](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="f2e10-126">Kun napsautat Kamera-sivulla kamerapainiketta, se näkyy himmeänä viivakoodin tunnistusyrityksen ajan.</span><span class="sxs-lookup"><span data-stu-id="f2e10-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="f2e10-127">Jos viivakoodia ei tunnisteta 5 sekunnin kuluessa, prosessi aikakatkaistaan ja kamerapainiketta voi taas käyttää.</span><span class="sxs-lookup"><span data-stu-id="f2e10-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="f2e10-128">Voit sitten yrittää lukea viivakoodin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f2e10-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="f2e10-129">Kun osoitat viivakoodia kameralla, saat parhaan tuloksen, kun viivakoodi on kohdistettu viivojen sisälle.</span><span class="sxs-lookup"><span data-stu-id="f2e10-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="f2e10-130">Kun viivakoodi on luettu, tulos käsitellään ja siirryt seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="f2e10-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="f2e10-131">Jos seuraavassa vaiheessa on toinen syötekenttä, jonka ensisijaiseksi syöttömenetelmäksi on valittu Luetaan, kamerasivu käynnistyy uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f2e10-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="f2e10-132">Jos seuraava vaihe ei ole luettava kenttä, kamerasivu ei käynnisty.</span><span class="sxs-lookup"><span data-stu-id="f2e10-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

