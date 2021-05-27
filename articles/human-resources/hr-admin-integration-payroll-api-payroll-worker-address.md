---
title: Palkanlaskennan työntekijän osoite
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan työntekijän osoite -yksikölle Dynamics 365 Human Resourcesissa.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020702"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="6360f-103">Palkanlaskennan työntekijän osoite</span><span class="sxs-lookup"><span data-stu-id="6360f-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6360f-104">Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan työntekijän osoite -yksikölle Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="6360f-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="6360f-105">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="6360f-105">Properties</span></span>

| <span data-ttu-id="6360f-106">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="6360f-106">Property</span></span><br><span data-ttu-id="6360f-107">**Fyysinen nimi**</span><span class="sxs-lookup"><span data-stu-id="6360f-107">**Physical name**</span></span><br><span data-ttu-id="6360f-108">**_Laji_**</span><span class="sxs-lookup"><span data-stu-id="6360f-108">**_Type_**</span></span> | <span data-ttu-id="6360f-109">Käytä</span><span class="sxs-lookup"><span data-stu-id="6360f-109">Use</span></span> | <span data-ttu-id="6360f-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="6360f-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6360f-111">**Paikkakunta**</span><span class="sxs-lookup"><span data-stu-id="6360f-111">**City**</span></span><br><span data-ttu-id="6360f-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="6360f-112">mshr_city</span></span><br><span data-ttu-id="6360f-113">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-113">*String*</span></span> | <span data-ttu-id="6360f-114">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-114">Read-only</span></span><br><span data-ttu-id="6360f-115">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-115">Required</span></span> | <span data-ttu-id="6360f-116">Osoitteessa määritetty paikkakunta.</span><span class="sxs-lookup"><span data-stu-id="6360f-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="6360f-117">**Henkilöstönumero**</span><span class="sxs-lookup"><span data-stu-id="6360f-117">**Personnel number**</span></span><br><span data-ttu-id="6360f-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="6360f-118">mshr_personnelnumber</span></span><br><span data-ttu-id="6360f-119">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-119">*String*</span></span> | <span data-ttu-id="6360f-120">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-120">Read-only</span></span><br><span data-ttu-id="6360f-121">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-121">Required</span></span> | <span data-ttu-id="6360f-122">Työntekijän yksilöivä henkilökuntanumero.</span><span class="sxs-lookup"><span data-stu-id="6360f-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="6360f-123">**Maa alue**</span><span class="sxs-lookup"><span data-stu-id="6360f-123">**Country region**</span></span><br><span data-ttu-id="6360f-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="6360f-124">mshr_countryregionid</span></span><br><span data-ttu-id="6360f-125">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-125">*String*</span></span> | <span data-ttu-id="6360f-126">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-126">Read-only</span></span><br><span data-ttu-id="6360f-127">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-127">Required</span></span> | <span data-ttu-id="6360f-128">Osoitteeseen määritetty maa tai alue</span><span class="sxs-lookup"><span data-stu-id="6360f-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="6360f-129">**Voimassaolo alkaa**</span><span class="sxs-lookup"><span data-stu-id="6360f-129">**Valid from**</span></span><br><span data-ttu-id="6360f-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="6360f-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="6360f-131">*Päivämäärä aika siirros*</span><span class="sxs-lookup"><span data-stu-id="6360f-131">*Date Time Offset*</span></span> | <span data-ttu-id="6360f-132">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-132">Read-only</span></span> <br><span data-ttu-id="6360f-133">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-133">Required</span></span> | <span data-ttu-id="6360f-134">Päivämäärä, josta alkaen osoite on voimassa.</span><span class="sxs-lookup"><span data-stu-id="6360f-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="6360f-135">**Työskenteli osoitteessa**</span><span class="sxs-lookup"><span data-stu-id="6360f-135">**Worked in address**</span></span><br><span data-ttu-id="6360f-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="6360f-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="6360f-137">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-137">Read-only</span></span><br><span data-ttu-id="6360f-138">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-138">Required</span></span> | <span data-ttu-id="6360f-139">Osoittaa, onko osoite se, jossa työntekijä työskentelee.</span><span class="sxs-lookup"><span data-stu-id="6360f-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="6360f-140">**Lääni**</span><span class="sxs-lookup"><span data-stu-id="6360f-140">**County**</span></span><br><span data-ttu-id="6360f-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="6360f-141">mshr_county</span></span><br><span data-ttu-id="6360f-142">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-142">*String*</span></span> | <span data-ttu-id="6360f-143">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-143">Read-only</span></span><br><span data-ttu-id="6360f-144">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-144">Required</span></span> | <span data-ttu-id="6360f-145">Osoitteessa määritetty maakunta.</span><span class="sxs-lookup"><span data-stu-id="6360f-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="6360f-146">**Palkanlaskennan työntekijän osoitteen tunnus**</span><span class="sxs-lookup"><span data-stu-id="6360f-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="6360f-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="6360f-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="6360f-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6360f-148">*GUID*</span></span> | <span data-ttu-id="6360f-149">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-149">Required</span></span><br><span data-ttu-id="6360f-150">Järjestelmän luoma</span><span class="sxs-lookup"><span data-stu-id="6360f-150">System generated</span></span> | <span data-ttu-id="6360f-151">Järjestelmän luoma GUID-arvo, jonka avulla osoite voidaan yksilöivästi tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="6360f-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="6360f-152">**Ensisijainen kenttä**</span><span class="sxs-lookup"><span data-stu-id="6360f-152">**Primary field**</span></span><br><span data-ttu-id="6360f-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="6360f-153">mshr_primaryfield</span></span><br><span data-ttu-id="6360f-154">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-154">*String*</span></span> | <span data-ttu-id="6360f-155">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-155">Read-only</span></span><br><span data-ttu-id="6360f-156">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-156">Required</span></span> |  |
| <span data-ttu-id="6360f-157">**Katu**</span><span class="sxs-lookup"><span data-stu-id="6360f-157">**Street**</span></span><br><span data-ttu-id="6360f-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="6360f-158">mshr_street</span></span><br><span data-ttu-id="6360f-159">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-159">*String*</span></span> | <span data-ttu-id="6360f-160">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-160">Read-only</span></span><br><span data-ttu-id="6360f-161">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-161">Required</span></span> | <span data-ttu-id="6360f-162">Osoitteessa määritetty katu.</span><span class="sxs-lookup"><span data-stu-id="6360f-162">The street defined for the address.</span></span> |
| <span data-ttu-id="6360f-163">**Voimassaolo päättyy**</span><span class="sxs-lookup"><span data-stu-id="6360f-163">**Valid to**</span></span><br><span data-ttu-id="6360f-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="6360f-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="6360f-165">*Päivämäärä aika siirros*</span><span class="sxs-lookup"><span data-stu-id="6360f-165">*Date Time Offset*</span></span> | <span data-ttu-id="6360f-166">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-166">Read-only</span></span> <br><span data-ttu-id="6360f-167">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-167">Required</span></span> | <span data-ttu-id="6360f-168">Päivämäärä, johon asti osoite on voimassa.</span><span class="sxs-lookup"><span data-stu-id="6360f-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="6360f-169">**Sijainnin tunnus**</span><span class="sxs-lookup"><span data-stu-id="6360f-169">**Location ID**</span></span><br><span data-ttu-id="6360f-170">mshr_locationidbr>*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="6360f-171">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-171">Read-only</span></span> <br><span data-ttu-id="6360f-172">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-172">Required</span></span> | <span data-ttu-id="6360f-173">Osoitteen tunnus.</span><span class="sxs-lookup"><span data-stu-id="6360f-173">The ID for the address.</span></span>  |
| <span data-ttu-id="6360f-174">**Postinumero**</span><span class="sxs-lookup"><span data-stu-id="6360f-174">**Postal code**</span></span><br><span data-ttu-id="6360f-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="6360f-175">mshr_zipcode</span></span><br><span data-ttu-id="6360f-176">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-176">*String*</span></span> | <span data-ttu-id="6360f-177">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-177">Read-only</span></span> <br><span data-ttu-id="6360f-178">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-178">Required</span></span> |<span data-ttu-id="6360f-179">Työntekijälle määritetty tunnusnumero.</span><span class="sxs-lookup"><span data-stu-id="6360f-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="6360f-180">**Asui osoitteessa**</span><span class="sxs-lookup"><span data-stu-id="6360f-180">**Lived in address**</span></span><br><span data-ttu-id="6360f-181">mshr_islivedinaddressbr>*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="6360f-182">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-182">Read-only</span></span><br><span data-ttu-id="6360f-183">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-183">Required</span></span> | <span data-ttu-id="6360f-184">Osoittaa, onko osoite se, jossa työntekijä asuu.</span><span class="sxs-lookup"><span data-stu-id="6360f-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="6360f-185">**Alue**</span><span class="sxs-lookup"><span data-stu-id="6360f-185">**State**</span></span><br><span data-ttu-id="6360f-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="6360f-186">mshr_state</span></span><br><span data-ttu-id="6360f-187">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="6360f-187">*String*</span></span> | <span data-ttu-id="6360f-188">Vain luku</span><span class="sxs-lookup"><span data-stu-id="6360f-188">Read-only</span></span><br><span data-ttu-id="6360f-189">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="6360f-189">Required</span></span> | <span data-ttu-id="6360f-190">Osoitteessa määritetty osavaltio.</span><span class="sxs-lookup"><span data-stu-id="6360f-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="6360f-191">Esimerkkikysely</span><span class="sxs-lookup"><span data-stu-id="6360f-191">Example query</span></span>

<span data-ttu-id="6360f-192">**Pyyntö**</span><span class="sxs-lookup"><span data-stu-id="6360f-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="6360f-193">**Vastaus**</span><span class="sxs-lookup"><span data-stu-id="6360f-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
