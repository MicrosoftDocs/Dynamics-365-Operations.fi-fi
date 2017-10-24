---
title: "Yleisen osoitekirjan ja lisäosoitekirjojen määrittämissuunnitelma"
description: "Tässä artikkelissa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin Microsoft Dynamics 365 for Finance and Operationsin yleinen osoitekirja ja lisäosoitekirjat määritetään. Jotkin päätökset vaativat tuotteen muilla alueilla, esimerkiksi organisaatiohierarkiassa, tehtyjen päätösten vahvistamisen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a><span data-ttu-id="a15f4-104">Yleisen osoitekirjan ja lisäosoitekirjojen määrittämissuunnitelma</span><span class="sxs-lookup"><span data-stu-id="a15f4-104">Plan how to configure the global address book and additional address books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a15f4-105">Tässä artikkelissa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin Microsoft Dynamics 365 for Finance and Operationsin yleinen osoitekirja ja lisäosoitekirjat määritetään.</span><span class="sxs-lookup"><span data-stu-id="a15f4-105">This article describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a15f4-106">Jotkin päätökset vaativat tuotteen muilla alueilla, esimerkiksi organisaatiohierarkiassa, tehtyjen päätösten vahvistamisen.</span><span class="sxs-lookup"><span data-stu-id="a15f4-106">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

<a name="global-address-book"></a><span data-ttu-id="a15f4-107">Yleinen osoitekirja</span><span class="sxs-lookup"><span data-stu-id="a15f4-107">Global address book</span></span>
-------------------

<span data-ttu-id="a15f4-108">Ennen kuin aloita yleisen osoitekirjan käsittelyn, sille on määritettävä oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="a15f4-108">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="a15f4-109">Näitä oletusarvoja käytetään sitten mahdollisissa lisäosoitekirjoissa, jotka luot.</span><span class="sxs-lookup"><span data-stu-id="a15f4-109">These default values are then used for any additional address books that you create.</span></span> 

<span data-ttu-id="a15f4-110">**Päätökset:**</span><span class="sxs-lookup"><span data-stu-id="a15f4-110">**Decisions:**</span></span>

-   <span data-ttu-id="a15f4-111">Missä järjestyksessä nimet näytetään **Henkilö**-tyypin osapuolitietueissa?</span><span class="sxs-lookup"><span data-stu-id="a15f4-111">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="a15f4-112">Yksi järjestys on esimerkiksi sukunimi, toinen nimi, etunimi.</span><span class="sxs-lookup"><span data-stu-id="a15f4-112">For example, one sequence is last name, middle name, first name.</span></span>
-   <span data-ttu-id="a15f4-113">Poistetaanko osapuolitietueet osoitekirjasta, kun roolitietue poistetaan?</span><span class="sxs-lookup"><span data-stu-id="a15f4-113">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="a15f4-114">Jos esimerkiksi asiakastietue poistetaan, poistetaanko myös osapuolitietue?</span><span class="sxs-lookup"><span data-stu-id="a15f4-114">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
-   <span data-ttu-id="a15f4-115">Ilmoitetaanko käyttäjille uutta tietuetta luotaessa, jos yleisestä osoitekirjasta löytyy tietueen kaksoiskappale?</span><span class="sxs-lookup"><span data-stu-id="a15f4-115">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
-   <span data-ttu-id="a15f4-116">Sisällytetäänkö DUNS (Data Universal Numbering System) -numero osapuolitietueen tietoihin?</span><span class="sxs-lookup"><span data-stu-id="a15f4-116">Should the Data Universal Numbering System (DUNS) number be included in a party record’s information?</span></span>
-   <span data-ttu-id="a15f4-117">Jos DUNS-numero sisällytetään osapuolitietueeseen, tarkistetaanko, että numero on yksilöllinen?</span><span class="sxs-lookup"><span data-stu-id="a15f4-117">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
-   <span data-ttu-id="a15f4-118">Kun yleiseen osoitekirjaan luodaan osapuolitietue, haluatko oletusosapuolen tyypin, henkilön vai organisaation?</span><span class="sxs-lookup"><span data-stu-id="a15f4-118">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
-   <span data-ttu-id="a15f4-119">Mitkä käyttäjäroolit saavat osapuolitietueiden yksityisten osoitteiden ja yhteystietojen käyttöoikeudet?</span><span class="sxs-lookup"><span data-stu-id="a15f4-119">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="a15f4-120">Lisäosoitekirjat</span><span class="sxs-lookup"><span data-stu-id="a15f4-120">Additional address books</span></span>
<span data-ttu-id="a15f4-121">Kun olet luonut yleisen osoitekirjan, voit luoda tarvittavia lisäosoitekirjoja, kuten oman osoitekirjan organisaation kullekin yritykselle tai toimialalle.</span><span class="sxs-lookup"><span data-stu-id="a15f4-121">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="a15f4-122">Fabrikam on esimerkiksi kansainvälinen organisaatio, jolla on useita yrityksiä ja toimialoja.</span><span class="sxs-lookup"><span data-stu-id="a15f4-122">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="a15f4-123">Fabrikam suunnittelee toimialakohtaisten osoitekirjojen luontia.</span><span class="sxs-lookup"><span data-stu-id="a15f4-123">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="a15f4-124">Fabrikam suunnittelee useassa toimipaikassa toimiville toimialoille, kuten paineilmatyökalujen toimiala, oman osoitekirjan luontia kullekin toimipaikalle.</span><span class="sxs-lookup"><span data-stu-id="a15f4-124">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="a15f4-125">Fabrikamin IT-päällikkö Chris on luonut seuraavan luettelon tarvittavista osoitekirjoista.</span><span class="sxs-lookup"><span data-stu-id="a15f4-125">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="a15f4-126">Tässä luettelossa on myös kuvaus osapuolitietueista, joiden on sisällyttävä kuhunkin osoitekirjaan.</span><span class="sxs-lookup"><span data-stu-id="a15f4-126">This list also also describes the party records that each address book must include.</span></span>

-   <span data-ttu-id="a15f4-127">**Julkisen sektorin sopimukset (PubSC)** – kaikkien Fabrikamin julkisen sektorin sopimusten osapuolien osapuolitietueet.</span><span class="sxs-lookup"><span data-stu-id="a15f4-127">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="a15f4-128">**Yksityisen sektorin sopimukset (PriSC)** – kaikkien Fabrikamin yksityisen sektorin sopimusten osapuolien osapuolitietueet.</span><span class="sxs-lookup"><span data-stu-id="a15f4-128">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="a15f4-129">**Sähköiset työkalut (ET)** – kaikkien niiden osapuolien osapuolitietueet, jotka osallistuvat sähköisten työkalujen ostoon tai myyntiin tai jotka toimivat muutoin Fabrikamin Fabrikam-Japan-yrityksen toimittamien tai sille ostettujen sähköisten työkalujen parissa.</span><span class="sxs-lookup"><span data-stu-id="a15f4-129">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="a15f4-130">**Paineilmatyökalut (PTJPN)** – kaikkien niiden osapuolien osapuolitietueet, jotka osallistuvat paineilmatyökalujen ostoon tai myyntiin tai jotka toimivat muutoin Fabrikamin Fabrikam-Japan-yrityksen toimittamien tai sille ostettujen paineilmatyökalujen parissa.</span><span class="sxs-lookup"><span data-stu-id="a15f4-130">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="a15f4-131">**Paineilmatyökalut (PTUSA)** – kaikkien niiden osapuolien osapuolitietueet, jotka osallistuvat paineilmatyökalujen ostoon tai myyntiin tai jotka toimivat muutoin Fabrikamin Fabrikam-US-yrityksen toimittamien tai sille ostettujen paineilmatyökalujen parissa.</span><span class="sxs-lookup"><span data-stu-id="a15f4-131">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="a15f4-132">**Päätös:**</span><span class="sxs-lookup"><span data-stu-id="a15f4-132">**Decision:**</span></span>

-   <span data-ttu-id="a15f4-133">Kuinka monta lisäosoitekirjaa luot?</span><span class="sxs-lookup"><span data-stu-id="a15f4-133">How many additional address books will you create?</span></span>

### <a name="address-book-security"></a><span data-ttu-id="a15f4-134">Osoitekirjan suojaus</span><span class="sxs-lookup"><span data-stu-id="a15f4-134">Address book security</span></span>

<span data-ttu-id="a15f4-135">Voit luoda osoitekirjoja koska tahansa ja voit myös määrittää osoitekirjojen suojauksen parametrit koska tahansa.</span><span class="sxs-lookup"><span data-stu-id="a15f4-135">You can create address books at any time, and you can also set security parameters for the address books at any time.</span></span> <span data-ttu-id="a15f4-136">Sinun ei tarvitse määrittää osoitekirjan suojausoikeuksia, mutta jos et tee niin, organisaation kaikki työntekijät voivat tarkastella kaikkia kyseisen osoitekirjan osapuolitietueita.</span><span class="sxs-lookup"><span data-stu-id="a15f4-136">You aren't required to set security privileges for an address book, but if you don't, all workers in your organization can view all party records in that address book.</span></span> <span data-ttu-id="a15f4-137">Voit määrittää osapuolitietueiden suojausoikeudet osoitekirjojen kautta.</span><span class="sxs-lookup"><span data-stu-id="a15f4-137">You can set security privileges to party records through address books.</span></span> <span data-ttu-id="a15f4-138">Suojausoikeudet perustuvat ryhmiin.</span><span class="sxs-lookup"><span data-stu-id="a15f4-138">Security privileges are based on teams.</span></span> <span data-ttu-id="a15f4-139">Näin taataan, että vain siihen ryhmään määritetyt työntekijät, joilla on osoitekirjan käyttöoikeus, voivat tarkastella kyseisen osoitekirjan osapuolitietueita.</span><span class="sxs-lookup"><span data-stu-id="a15f4-139">This approach guarantees that only workers who are assigned to a team that has access to an address book can view the party records in that address book.</span></span> <span data-ttu-id="a15f4-140">Sinun on valittava ryhmät, joilla on kunkin osoitekirjan käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="a15f4-140">You must select the teams that have access to each address book.</span></span> <span data-ttu-id="a15f4-141">Määritä kullekin osoitekirjalle suojausoikeudet, jotka sallivat käytön tietyille ryhmille tai estävät käytön.</span><span class="sxs-lookup"><span data-stu-id="a15f4-141">For each address book, you can set security privileges that allow or deny access to specific teams.</span></span> <span data-ttu-id="a15f4-142">Kun myönnät ryhmälle osoitekirjan käyttöoikeuden, kyseisen ryhmän kaikki jäsenet voivat tarkastella osoitekirjan tietueita.</span><span class="sxs-lookup"><span data-stu-id="a15f4-142">If you grant a team privileges to an address book, all members of that team can view the records in the address book.</span></span> <span data-ttu-id="a15f4-143">Jos et myönnä ryhmälle osoitekirjan käyttöoikeutta, kyseisen ryhmän jäsenet eivät voivat tarkastella osoitekirjaa tai sen sisältöä.</span><span class="sxs-lookup"><span data-stu-id="a15f4-143">If you don't grant a team access to an address book, the members of that team can't view the address book or its contents.</span></span> 

<span data-ttu-id="a15f4-144">**Päätös:**</span><span class="sxs-lookup"><span data-stu-id="a15f4-144">**Decision:**</span></span>

-   <span data-ttu-id="a15f4-145">Mitkä ryhmät saavat kunkin luomasi uuden osoitekirjan käyttöoikeudet?</span><span class="sxs-lookup"><span data-stu-id="a15f4-145">Which teams should have access to each new address book that you will create?</span></span>





