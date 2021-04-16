---
title: Viivakoodien lukeminen kameran avulla varastonhallinnan mobiilisovelluksessa
description: Tässä ohjeaiheessa käsitellään varastonhallinnan mobiilisovelluksen määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831215"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="554c0-103">Viivakoodien lukeminen kameran avulla varastonhallinnan mobiilisovelluksessa</span><span class="sxs-lookup"><span data-stu-id="554c0-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="554c0-104">Tässä ohjeaiheessa käsitellään varastonhallinnan mobiilisovelluksen määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten.</span><span class="sxs-lookup"><span data-stu-id="554c0-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="554c0-105">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="554c0-105">Setup</span></span>

<span data-ttu-id="554c0-106">Voit valita varastonhallinnan mobiilisovelluksen näyttöasetuksissa, käytetäänkö kameraa viivakoodin lukemiseen.</span><span class="sxs-lookup"><span data-stu-id="554c0-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="554c0-107">Jos otat **kameran käytön skannerina** käyttöön, voit käyttää kameraa jokaisessa syöttömenetelmäksi, jonka ensisijaiseksi syötetilaksi on määritetty **Luetaan**.</span><span class="sxs-lookup"><span data-stu-id="554c0-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="554c0-108">Voit määrittää, voiko syötekentän lukea, valitsemalla **Varastosovelluksen kenttien nimet** -sivulla **Ensisijainen syöttömenetelmä** -asetukseksi **Luetaan**.</span><span class="sxs-lookup"><span data-stu-id="554c0-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="554c0-109">Kun tämä asetus on valittu, kameraa voidaan käyttää skannaukseen varastonhallinnan mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="554c0-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="554c0-110">Lisätietoja: [Varastonhallinnan mobiilisovelluksen kenttien konfigurointi](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="554c0-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="554c0-111">Tuetut viivakoodimuodot</span><span class="sxs-lookup"><span data-stu-id="554c0-111">Supported bar code formats</span></span>

<span data-ttu-id="554c0-112">Eniten käytettyjä viivakoodimuotoja tuetaan. Niitä ovat esimerkiksi Koodi 128, Koodi 39, Koodi 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodit.</span><span class="sxs-lookup"><span data-stu-id="554c0-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="554c0-113">Siirtyminen</span><span class="sxs-lookup"><span data-stu-id="554c0-113">Navigation</span></span>

<span data-ttu-id="554c0-114">Kamerasivu käynnistetään jokaisella sivulla, jonka syötekentän **ensisijaiseksi syöttömenetelmäksi** on valittu *Skannaus*. Voit liikkua Kamera-sivulla seuraavien asetusten avulla:</span><span class="sxs-lookup"><span data-stu-id="554c0-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="554c0-115">Voit palata **Tehtävät ja tiedot** -sivulle napsauttamalla Takaisin-painiketta.</span><span class="sxs-lookup"><span data-stu-id="554c0-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="554c0-116">Kun valitset kynäkuvakkeen **Tehtävät ja tiedot** -sivulla, voit siirtyä sivulle, jossa voit kirjoittaa tiedot manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="554c0-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="554c0-117">Voit palata kamerasivulle valitsemalla kamerakuvakkeen **Tehtävät ja tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="554c0-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="554c0-118">Kun valitset Kamera-sivulla kamerapainikkeen, se näkyy himmeänä viivakoodin tunnistusyrityksen ajan.</span><span class="sxs-lookup"><span data-stu-id="554c0-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="554c0-119">Jos viivakoodia ei tunnisteta 5 sekunnin kuluessa, prosessi aikakatkaistaan ja kamerapainiketta voi taas käyttää.</span><span class="sxs-lookup"><span data-stu-id="554c0-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="554c0-120">Voit sitten yrittää lukea viivakoodin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="554c0-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="554c0-121">Kun osoitat viivakoodia kameralla, saat parhaan tuloksen, kun viivakoodi on kohdistettu viivojen sisälle.</span><span class="sxs-lookup"><span data-stu-id="554c0-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="554c0-122">Kun viivakoodi on luettu, tulos käsitellään ja siirryt seuraavaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="554c0-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="554c0-123">Jos seuraavassa vaiheessa on toinen syötekenttä, jonka ensisijaiseksi syöttömenetelmäksi on valittu Luetaan, kamerasivu käynnistyy uudelleen.</span><span class="sxs-lookup"><span data-stu-id="554c0-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="554c0-124">Jos seuraava vaihe ei ole luettava kenttä, kamerasivu ei käynnisty.</span><span class="sxs-lookup"><span data-stu-id="554c0-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]