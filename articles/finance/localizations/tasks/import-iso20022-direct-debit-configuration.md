---
title: Tuo ISO20022-suoraveloituksen konfiguraatio
description: Näiden ohjeiden avuilla voit tuoda asiakkaan maksun sähköisen raportointikonfiguraation.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d0358c414af20558e7e5aaadad5d9844f7853bf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840886"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="b44b7-103">Tuo ISO20022-suoraveloituksen konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="b44b7-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b44b7-104">Näiden ohjeiden avuilla voit tuoda asiakkaan maksun sähköisen raportointikonfiguraation.</span><span class="sxs-lookup"><span data-stu-id="b44b7-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="b44b7-105">Näissä ohjeissa käytetään esimerkkinä ISO 20022 -suoraveloitusmuotoa.</span><span class="sxs-lookup"><span data-stu-id="b44b7-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="b44b7-106">Tämä ohje on luotu DEMF-yrityksen esittelytiedoilla, mutta sen voi suorittaa minkä tahansa esittely-yrityksen tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="b44b7-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="b44b7-107">Tämä on ensimmäinen viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="b44b7-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="b44b7-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="b44b7-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b44b7-109">Valitse konfiguraation lähdeluettelossa Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b44b7-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="b44b7-110">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="b44b7-110">Click Set active.</span></span>
4. <span data-ttu-id="b44b7-111">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="b44b7-111">Click Repositories.</span></span>
5. <span data-ttu-id="b44b7-112">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="b44b7-112">Click Open.</span></span>
6. <span data-ttu-id="b44b7-113">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="b44b7-113">Click Show filters.</span></span>
7. <span data-ttu-id="b44b7-114">Käytä seuraavaa suodatinta Kirjoita suodattimen arvoksi "ISO20022 Direct debit (DE)" Konfiguraation nimi -kenttään niin, että suodatinoperaattori on Alkaa.</span><span class="sxs-lookup"><span data-stu-id="b44b7-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="b44b7-115">Voit halutessasi etsiä konfiguraation luettelosta, valita sen ja ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="b44b7-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="b44b7-116">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="b44b7-116">Click Import.</span></span>
    * <span data-ttu-id="b44b7-117">Jos Tuo-painike ei ole näkyvissä, tämä konfiguraatio on jo tuotu.</span><span class="sxs-lookup"><span data-stu-id="b44b7-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="b44b7-118">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b44b7-118">Click Yes.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]