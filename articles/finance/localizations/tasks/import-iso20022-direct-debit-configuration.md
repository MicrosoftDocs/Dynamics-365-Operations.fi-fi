---
title: Tuo ISO20022-suoraveloituksen konfiguraatio
description: Näiden ohjeiden avuilla voit tuoda asiakkaan maksun sähköisen raportointikonfiguraation.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d4256b155d3e06d63e425fab63b4025ef2577f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140015"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="e18ab-103">Tuo ISO20022-suoraveloituksen konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="e18ab-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e18ab-104">Näiden ohjeiden avuilla voit tuoda asiakkaan maksun sähköisen raportointikonfiguraation.</span><span class="sxs-lookup"><span data-stu-id="e18ab-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="e18ab-105">Näissä ohjeissa käytetään esimerkkinä ISO 20022 -suoraveloitusmuotoa.</span><span class="sxs-lookup"><span data-stu-id="e18ab-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="e18ab-106">Tämä ohje on luotu DEMF-yrityksen esittelytiedoilla, mutta sen voi suorittaa minkä tahansa esittely-yrityksen tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="e18ab-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="e18ab-107">Tämä on ensimmäinen viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="e18ab-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="e18ab-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="e18ab-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e18ab-109">Valitse konfiguraation lähdeluettelossa Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e18ab-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="e18ab-110">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="e18ab-110">Click Set active.</span></span>
4. <span data-ttu-id="e18ab-111">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="e18ab-111">Click Repositories.</span></span>
5. <span data-ttu-id="e18ab-112">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="e18ab-112">Click Open.</span></span>
6. <span data-ttu-id="e18ab-113">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="e18ab-113">Click Show filters.</span></span>
7. <span data-ttu-id="e18ab-114">Käytä seuraavaa suodatinta Kirjoita suodattimen arvoksi "ISO20022 Direct debit (DE)" Konfiguraation nimi -kenttään niin, että suodatinoperaattori on Alkaa.</span><span class="sxs-lookup"><span data-stu-id="e18ab-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="e18ab-115">Voit halutessasi etsiä konfiguraation luettelosta, valita sen ja ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="e18ab-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="e18ab-116">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="e18ab-116">Click Import.</span></span>
    * <span data-ttu-id="e18ab-117">Jos Tuo-painike ei ole näkyvissä, tämä konfiguraatio on jo tuotu.</span><span class="sxs-lookup"><span data-stu-id="e18ab-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="e18ab-118">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e18ab-118">Click Yes.</span></span>

