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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d68e5a63ea3b037cc111d6732857f0aae1ce7e5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989948"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="6ec69-103">Tuo ISO20022-suoraveloituksen konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="6ec69-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ec69-104">Näiden ohjeiden avuilla voit tuoda asiakkaan maksun sähköisen raportointikonfiguraation.</span><span class="sxs-lookup"><span data-stu-id="6ec69-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="6ec69-105">Näissä ohjeissa käytetään esimerkkinä ISO 20022 -suoraveloitusmuotoa.</span><span class="sxs-lookup"><span data-stu-id="6ec69-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="6ec69-106">Tämä ohje on luotu DEMF-yrityksen esittelytiedoilla, mutta sen voi suorittaa minkä tahansa esittely-yrityksen tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="6ec69-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="6ec69-107">Tämä on ensimmäinen viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="6ec69-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="6ec69-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="6ec69-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6ec69-109">Valitse konfiguraation lähdeluettelossa Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6ec69-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="6ec69-110">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="6ec69-110">Click Set active.</span></span>
4. <span data-ttu-id="6ec69-111">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="6ec69-111">Click Repositories.</span></span>
5. <span data-ttu-id="6ec69-112">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="6ec69-112">Click Open.</span></span>
6. <span data-ttu-id="6ec69-113">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="6ec69-113">Click Show filters.</span></span>
7. <span data-ttu-id="6ec69-114">Käytä seuraavaa suodatinta Kirjoita suodattimen arvoksi "ISO20022 Direct debit (DE)" Konfiguraation nimi -kenttään niin, että suodatinoperaattori on Alkaa.</span><span class="sxs-lookup"><span data-stu-id="6ec69-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="6ec69-115">Voit halutessasi etsiä konfiguraation luettelosta, valita sen ja ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="6ec69-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="6ec69-116">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="6ec69-116">Click Import.</span></span>
    * <span data-ttu-id="6ec69-117">Jos Tuo-painike ei ole näkyvissä, tämä konfiguraatio on jo tuotu.</span><span class="sxs-lookup"><span data-stu-id="6ec69-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="6ec69-118">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="6ec69-118">Click Yes.</span></span>

