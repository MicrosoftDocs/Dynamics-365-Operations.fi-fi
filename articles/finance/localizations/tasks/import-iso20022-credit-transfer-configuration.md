---
title: Tuo ISO20022-tilisiirron konfiguraatio
description: Näiden ohjeiden avuilla voit tuoda toimittajan maksun sähköisen raportointikonfiguraation.
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
ms.openlocfilehash: 01f44c49b6623cbcc2f08cfd6e4978c9a1676b83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442814"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="2244e-103">Tuo ISO20022-tilisiirron konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="2244e-103">Import ISO20022 credit transfer configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2244e-104">Näiden ohjeiden avuilla voit tuoda toimittajan maksun sähköisen raportointikonfiguraation.</span><span class="sxs-lookup"><span data-stu-id="2244e-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="2244e-105">Esimerkkinä on käytetty saksalaista ISO 20022 -hyvityssiirtomuotoa.</span><span class="sxs-lookup"><span data-stu-id="2244e-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="2244e-106">Nämä ohjeet soveltuvat myös muihin, saatavilla oleviin sähköisiin raportointimuotoihin.</span><span class="sxs-lookup"><span data-stu-id="2244e-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="2244e-107">Tämä tehtävä on luotu DEMF-yrityksen esittelytiedoilla, mutta tehtävän voi suorittaa minkä tahansa esittely-yrityksen tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="2244e-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="2244e-108">Tämä on ensimmäinen viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="2244e-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="2244e-109">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="2244e-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="2244e-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="2244e-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2244e-111">Valitse konfiguraation lähdeluettelossa Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2244e-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="2244e-112">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="2244e-112">Click Set active.</span></span>
4. <span data-ttu-id="2244e-113">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="2244e-113">Click Repositories.</span></span>
5. <span data-ttu-id="2244e-114">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="2244e-114">Click Open.</span></span>
6. <span data-ttu-id="2244e-115">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="2244e-115">Click Show filters.</span></span>
7. <span data-ttu-id="2244e-116">Käytä seuraavaa suodatinta Kirjoita suodattimen arvoksi "ISO20022 Credit transfer (DE)" Konfiguraation nimi -kenttään niin, että suodatinoperaattori on Alkaa.</span><span class="sxs-lookup"><span data-stu-id="2244e-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="2244e-117">Voit vaihtoehtoisesti myös etsiä konfiguraation luettelosta, valita sen ja siirtää konfiguraation Tuo tehtävä -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="2244e-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="2244e-118">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="2244e-118">Click Import.</span></span>
    * <span data-ttu-id="2244e-119">Jos Tuo-painike ei ole näkyvissä, tämä konfiguraatio on jo tuotu.</span><span class="sxs-lookup"><span data-stu-id="2244e-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="2244e-120">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2244e-120">Click Yes.</span></span>

