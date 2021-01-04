---
title: Saapuvien asiakirjojen jäsentäminen JSON-muodossa
description: Tässä ohjeaiheessa käsitellään tapaa, jolla sähköisen raportoinnin (ER) muodot jäsentävät saapuvat asiakirjat JavaScript Object Notation (JSON) -muodossa.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
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
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b4ed81bb5527ea8e02caaa1262a57960dd7cdf29
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685760"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="4a6b5-103">Saapuvien asiakirjojen jäsentäminen JSON-muodossa</span><span class="sxs-lookup"><span data-stu-id="4a6b5-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4a6b5-104">Voit suunnitella sähköisen raportoinnin (ER) muodot jäsentämään saapuvat sähköiset asiakirjat, jotka viittaavat JavaScriptiin perustuviin tekstimuotoisiin tietoihin (eli JavaScript Object Notation \[JSON\] -muotoisiin tiedostoihin).</span><span class="sxs-lookup"><span data-stu-id="4a6b5-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="4a6b5-105">Saat lisätietoja tästä toiminnosta lataamalla seuraavan taulukon tiedostot ja toistamalla sitten tehtäväoppaan ER Muotokonfiguraation luominen tietojen ulkoisesta JSON-tiedostosta tuontia varten.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="4a6b5-106">Tämä tehtäväopas osoittaa, miten ER-muodon avulla saapuva JSON-tiedosto voidaan jäsentää päivittämään sovellustiedot.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="4a6b5-107">Titteli</span><span class="sxs-lookup"><span data-stu-id="4a6b5-107">Title</span></span>                                  | <span data-ttu-id="4a6b5-108">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="4a6b5-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="4a6b5-109">ER-muodon konfigurointi</span><span class="sxs-lookup"><span data-stu-id="4a6b5-109">ER format configuration</span></span>                | [<span data-ttu-id="4a6b5-110">Toimittajien trans_JSON.xml-tiedoston tuonnin muoto</span><span class="sxs-lookup"><span data-stu-id="4a6b5-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="4a6b5-111">Saapuvan .csv-muotoinen näytetiedosto</span><span class="sxs-lookup"><span data-stu-id="4a6b5-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="4a6b5-112">1099entries_JSON. txt</span><span class="sxs-lookup"><span data-stu-id="4a6b5-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="4a6b5-113">Tarpeet</span><span class="sxs-lookup"><span data-stu-id="4a6b5-113">Requirements</span></span>

<span data-ttu-id="4a6b5-114">Seuraava vaatimus on toteutettava ennen ER Muotokonfiguraation luominen tietojen ulkoisesta JSON-tiedostosta tuontia varten -tehtäväoppaan suorittamista:</span><span class="sxs-lookup"><span data-stu-id="4a6b5-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="4a6b5-115">JSON-tiedoston pääelementit voivat olla vain objektielementtejä.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="4a6b5-116">Objektin sisäkkäisten elementtien on oltava ominaisuuselementtejä, jotta kelvollinen JSON-rakenne voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="4a6b5-117">JSON-taulukot voivat olla vain objektin ominaisuuselementtien sisäkkäisiä elementtejä.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="4a6b5-118">JSON-taulukot voivat sisältää vain JSON-objekteja.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="4a6b5-119">Ne eivät voi sisältää suoria merkkijonoja tai numeroarvoja eivätkä sisäkkäisiä taulukoita.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="4a6b5-120">Näiden taulukoiden elementit jäsennetään muodossa määritetyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="4a6b5-121">Kunkin JSON-objektin monimuotoisuusasetukset otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="4a6b5-122">Lisäksi on suoritettava [ER Luo vaaditut konfiguraatiot tietojen tuomiseksi ulkoisesta tiedostosta](tasks/er-required-configurations-import-data.md) -tehtäväopas, jos sitä ei ole vielä suoritettu.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="4a6b5-123">Suorita tehtäväopas lataamalla seuraava tiedosto.</span><span class="sxs-lookup"><span data-stu-id="4a6b5-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="4a6b5-124">Titteli</span><span class="sxs-lookup"><span data-stu-id="4a6b5-124">Title</span></span>                  | <span data-ttu-id="4a6b5-125">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="4a6b5-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="4a6b5-126">ER_mallin määritys</span><span class="sxs-lookup"><span data-stu-id="4a6b5-126">ER model configuration</span></span> | [<span data-ttu-id="4a6b5-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="4a6b5-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
