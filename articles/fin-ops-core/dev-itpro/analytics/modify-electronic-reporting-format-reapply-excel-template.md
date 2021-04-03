---
title: Sähköisen raportoinnin muotojen muokkaaminen käyttämällä Excel-malleja
description: Tässä aiheessa käsitellään sellaisen sähköisen raportoinnin (ER) muodon muokkaamista, jota käytetään liiketoiminta-asiakirjojen luomiseen muokatun Excel-mallin avulla.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f28760f42d16b6ffcd301f121e583542bce0fac0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559287"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="3f31c-103">Sähköisen raportoinnin muotojen muokkaaminen käyttämällä Excel-malleja uudelleen</span><span class="sxs-lookup"><span data-stu-id="3f31c-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f31c-104">Sähköistä raportointityökalua (ER) käytetään luotaessa liiketoiminta-asiakirjoja sähköisessä muodossa.</span><span class="sxs-lookup"><span data-stu-id="3f31c-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="3f31c-105">Voit luoda liiketoiminta-asiakirjan, kun luot ensin ER-muodon ja käytät ER-suunnitteluohjelmaa liiketoiminta-asiakirjan asettelun ja asiakirjan sisällön määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="3f31c-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="3f31c-106">Tämän jälkeen voit suorittaa ER-muodon ja luoda liiketoiminta-asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="3f31c-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="3f31c-107">ER-työkalun avulla voi luoda liiketoiminta-asiakirjoja, kuten Microsoft Excel -tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="3f31c-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="3f31c-108">Voit käyttää Excel-asiakirjaa näiden asiakirjojen mallina.</span><span class="sxs-lookup"><span data-stu-id="3f31c-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="3f31c-109">Voit määrittää asiakirjan asettelun ER-suunnitteluohjelmassa tuomalla sen Excel-asiakirjan sisällön, jota haluat käyttää mallina määritetyssä ER-muodossa.</span><span class="sxs-lookup"><span data-stu-id="3f31c-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="3f31c-110">Voit toistaa tämän tehtäväoppaan **OPENXML-muotoisten raporttimääritysten suunnittelu -tehtäväopas** (7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677) -liiketoimintaprosessin osa), kun haluat lisätietoja tai harjoitella toimintoja.</span><span class="sxs-lookup"><span data-stu-id="3f31c-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="3f31c-111">Jos muokkaat liiketoiminta-asiakirjan mallina käytettävää Excel-asiakirjaa, uusi ER-toiminto auttaa päivitetyn mallin kohdistamisessa uudelleen ER-muotoon.</span><span class="sxs-lookup"><span data-stu-id="3f31c-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="3f31c-112">Tämän jälkeen ER-muoto päivitetään, jotta se on päivitetyn mallin mukainen.</span><span class="sxs-lookup"><span data-stu-id="3f31c-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="3f31c-113">Saat lisätietoja toiminnoista toistamalla tehtäväoppaan **ER-muodon muokkaaminen käyttämällä Excel-mallia uudelleen** (7.5.5.3 IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen (10683) -liiketoimintaprosessin osa).</span><span class="sxs-lookup"><span data-stu-id="3f31c-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="3f31c-114">Käytä mallina tehtäväoppaan päivitetyn mallin tuontivaiheen maksuraportin Excel-tiedoston muokattua mallia SampleVendPaymWsReport2.</span><span class="sxs-lookup"><span data-stu-id="3f31c-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]