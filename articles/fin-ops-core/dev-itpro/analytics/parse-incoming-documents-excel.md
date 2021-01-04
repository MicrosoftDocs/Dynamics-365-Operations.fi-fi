---
title: Saapuvien asiakirjojen jäsentäminen Excel-muodossa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) muotojen suunnittelusta, jotta se voi jäsentää sisältöä saapuvissa Microsoft Excel -tiedostoissa.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 6e27806d3b94eb485705cec539a4849b81fbba91
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685784"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="ace0e-103">Saapuvien asiakirjojen jäsentäminen Excel-muodossa</span><span class="sxs-lookup"><span data-stu-id="ace0e-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ace0e-104">Voit suunnitella sähköisen raportoinnin (ER) muodot jäsentämään saapuvia Microsoft Excel -tiedostoja, jotka edustavat tietoja Microsoft Excel -työkirjoissa (XLSX-tiedostot).</span><span class="sxs-lookup"><span data-stu-id="ace0e-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="ace0e-105">Sitten voit käyttää näiden tiedostojen sisältöä sovelluksen tietojen päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="ace0e-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="ace0e-106">Tämä on hyödyllistä, kun esimerkiksi:</span><span class="sxs-lookup"><span data-stu-id="ace0e-106">This is useful if you:</span></span>

- <span data-ttu-id="ace0e-107">Suunnittelet uutta mallia ja muotoa ja haluat testata niitä suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="ace0e-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="ace0e-108">Tässä tapauksessa Excel simuloi todellisia sovellustietoja.</span><span class="sxs-lookup"><span data-stu-id="ace0e-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="ace0e-109">Hallita soveluksen ulkopuolisia tietoja Excelissä ja tuoda nämä tiedot lähettäksesi tietyn raportin.</span><span class="sxs-lookup"><span data-stu-id="ace0e-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="ace0e-110">Saat lisätietoja tästä ominaisuudesta toistamalla tehtäväoppaat **ER - Tuo tiedot Microsoft Excel -tiedostosta (osa 1: Muodon suunnittelu)** ja **ER - Tuo tiedot Microsoft Excel -tiedostosta (osa 2: tietojen tuominen)** (osia 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677) -liiketoimintaprosessissa).</span><span class="sxs-lookup"><span data-stu-id="ace0e-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="ace0e-111">Nämä tehtäväoppaat käyvät läpi, kuinka saapuva Excel-tiedosto voidaan jäsentää käyttäen ER-muotoa, jotta voidaan tuoda tietoja saapuvista asiakirjoista ja päivittää sovellustiedot.</span><span class="sxs-lookup"><span data-stu-id="ace0e-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="ace0e-112">Voit ladata tehtäväoppaan tiedostot [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="ace0e-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="ace0e-113">Lataa seuraavat tiedostot suorittaaksesi yo. tehtäväoppaat:</span><span class="sxs-lookup"><span data-stu-id="ace0e-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="ace0e-114">Sisällön kuvaus</span><span class="sxs-lookup"><span data-stu-id="ace0e-114">Content description</span></span>                         | <span data-ttu-id="ace0e-115">Tiedosto</span><span class="sxs-lookup"><span data-stu-id="ace0e-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="ace0e-116">Saapuva tiedosto .XLSX-muodossa - malli</span><span class="sxs-lookup"><span data-stu-id="ace0e-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="ace0e-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="ace0e-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="ace0e-118">Saapuva tiedosto .XLSX-muodossa - näytetiedot</span><span class="sxs-lookup"><span data-stu-id="ace0e-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="ace0e-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="ace0e-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="ace0e-120">Jos et ole vielä toistanut tehtäväopasta [ER Luo vaaditut konfiguraatiot tietojen tuomiseksi ulkoisesta tiedostosta](./tasks/er-required-configurations-import-data.md) nykyisessä Finance and Operations -sovelluksessa, lataa seuraava tiedosto.</span><span class="sxs-lookup"><span data-stu-id="ace0e-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="ace0e-121">Sisällön kuvaus</span><span class="sxs-lookup"><span data-stu-id="ace0e-121">Content description</span></span>    | <span data-ttu-id="ace0e-122">Tiedosto</span><span class="sxs-lookup"><span data-stu-id="ace0e-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ace0e-123">ER_mallin määritys</span><span class="sxs-lookup"><span data-stu-id="ace0e-123">ER model configuration</span></span> | [<span data-ttu-id="ace0e-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="ace0e-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
