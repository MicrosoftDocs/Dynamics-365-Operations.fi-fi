---
title: "Poistokirjan päivityksen yleiskatsaus"
description: "Aiemmissa julkaisuversioissa oli kaksi käyttöomaisuuserien arviointikäsitettä: arvomallit ja poistokirjat. Microsoft Dynamics 365 for Operationsissa (1611) arvomallin toiminnot ja poistokirjatoiminnot on yhdistetty yhdeksi käsitteeksi, jota kutsutaan kirjaksi. Tämä aihe käsittelee päivityksessä huomioitavia seikkoja."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7093023713a81980010b8254708801b58bc68475
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="462b6-105">Poistokirjan päivityksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="462b6-105">Depreciation book upgrade overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="462b6-106">Aiemmissa julkaisuversioissa oli kaksi käyttöomaisuuserien arviointikäsitettä: arvomallit ja poistokirjat.</span><span class="sxs-lookup"><span data-stu-id="462b6-106">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="462b6-107">Microsoft Dynamics 365 for Operationsissa (1611) arvomallin toiminnot ja poistokirjatoiminnot on yhdistetty yhdeksi käsitteeksi, jota kutsutaan kirjaksi.</span><span class="sxs-lookup"><span data-stu-id="462b6-107">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="462b6-108">Tämä aihe käsittelee päivityksessä huomioitavia seikkoja.</span><span class="sxs-lookup"><span data-stu-id="462b6-108">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="462b6-109">Päivitysprosessi siirtää aiemmin määritetyt asetukset ja kaikki olemassa olevat tapahtumat uuden kirjan rakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="462b6-109">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="462b6-110">Arvomallit säilyvät nykyisellään, kirjana joka tekee kirjauksia kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="462b6-110">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="462b6-111">Poistokirjat siirretään kirjaan, jonka **Kirjaa kirjanpitoon** -asetus on **Ei**.</span><span class="sxs-lookup"><span data-stu-id="462b6-111">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="462b6-112">Poistokirjan kirjauskansioiden nimet siirretään kirjanpidon kirjauskansion nimeen, jonka kirjanpitotasoksi on määritetty **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="462b6-112">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="462b6-113">Poistokirjatapahtumat siirretään käyttöomaisuustapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="462b6-113">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="462b6-114">Ennen tietojen päivityksen suorittamista sinun on hyvä ymmärtää käytettävissä olevat kaksi vaihtoehtoa poistokirjan kirjauskansion rivien päivittämiseksi tapahtumatositteisiin, ja numerosarja, jota käytetään tositesarjaan.</span><span class="sxs-lookup"><span data-stu-id="462b6-114">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="462b6-115">Vaihtoehto 1: **Järjestelmän määrittämä numerosarjan**: tämä on oletusasetus päivityksen suorituskyvyn parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="462b6-115">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="462b6-116">Päivitys ei käytä numerosarjojen kehystä, mutta sen sijaan kohdistaa tositteet joukkoon perustuvan mallin pohjalta.</span><span class="sxs-lookup"><span data-stu-id="462b6-116">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="462b6-117">Päivityksen jälkeen uusi numerosarjan luodaan **Seuraava numerosarja** asianmukaisesti päivitettyjen tapahtumien perusteella.</span><span class="sxs-lookup"><span data-stu-id="462b6-117">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="462b6-118">Oletuksena käytettävä numerosarjan muoto on FADBUpgr\#\#\#\#\#\#\#\#\#.</span><span class="sxs-lookup"><span data-stu-id="462b6-118">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="462b6-119">Voit muuttaa muotoa muutamien parametrien avulla käyttäen tätä menetelmää:</span><span class="sxs-lookup"><span data-stu-id="462b6-119">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="462b6-120">**Numerosarjan koodi**: koodi numerosarjan tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="462b6-120">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="462b6-121">Tätä numerosarjan koodia ei ole olemassa, sillä koodi luodaan päivityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="462b6-121">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="462b6-122">Vakion nimi: **NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="462b6-122">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="462b6-123">Oletusarvo: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="462b6-123">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="462b6-124">**Etuliite**: kiinteä merkkijonon arvo, jota käytetään etuliitteenä tositenumeroissa.</span><span class="sxs-lookup"><span data-stu-id="462b6-124">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="462b6-125">Vakion nimi: **NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="462b6-125">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="462b6-126">Oletusarvo: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="462b6-126">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="462b6-127">**Aakkosnumeerinen pituus**: aakkosnumeerisen segmentin numerosarjan pituus.</span><span class="sxs-lookup"><span data-stu-id="462b6-127">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="462b6-128">Vakion nimi: **NumberSequenceDefaultParameterAlpanumericLength**</span><span class="sxs-lookup"><span data-stu-id="462b6-128">Constant name: **NumberSequenceDefaultParameterAlpanumericLength **</span></span>
    -   <span data-ttu-id="462b6-129">Oletusarvo: 9</span><span class="sxs-lookup"><span data-stu-id="462b6-129">Default value: 9</span></span>
-   <span data-ttu-id="462b6-130">**Ensimmäinen numero**: numerosarjan ensimmäinen numero.</span><span class="sxs-lookup"><span data-stu-id="462b6-130">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="462b6-131">Vakion nimi: **NumberSequenceDefaultParameterStartNumber**</span><span class="sxs-lookup"><span data-stu-id="462b6-131">Constant name: **NumberSequenceDefaultParameterStartNumber  **</span></span>
    -   <span data-ttu-id="462b6-132">Oletusarvo: 1</span><span class="sxs-lookup"><span data-stu-id="462b6-132">Default value: 1</span></span>

<span data-ttu-id="462b6-133">Vaihtoehto 2: **Aiemmin käyttäjän luoma numerosarja**: tämän vaihtoehdon avulla voit määrittää päivitystä varten käytettävän numerosarjan.</span><span class="sxs-lookup"><span data-stu-id="462b6-133">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="462b6-134">Tämä vaihtoehto kannattaa, jos tarvitaan edistynyttä numerosarjan konfigurointia.</span><span class="sxs-lookup"><span data-stu-id="462b6-134">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="462b6-135">Numerosarjan käyttöä varten on muokattava päivitysluokkaa ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans seuraavilla tiedoilla:</span><span class="sxs-lookup"><span data-stu-id="462b6-135">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="462b6-136">**Numerosarjan koodi**: Numerosarjan koodi.</span><span class="sxs-lookup"><span data-stu-id="462b6-136">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="462b6-137">Vakion nimi: **NumberSequenceExistingCode**</span><span class="sxs-lookup"><span data-stu-id="462b6-137">Constant name: **NumberSequenceExistingCode **</span></span>
    -   <span data-ttu-id="462b6-138">Oletusarvo: Ei oletusarvoa, tämä on päivitettävä numerosarjan koodiksi.</span><span class="sxs-lookup"><span data-stu-id="462b6-138">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="462b6-139">**Jaettu numerosarja**: totuusarvo, jolla tunnistetaan numerosarjan vaikutusalue.</span><span class="sxs-lookup"><span data-stu-id="462b6-139">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="462b6-140">Käytä jaetun numerosarjan arvoa "tosi" kaikissa yrityksissä ja arvoa "false" yrityskohtaisella alueella.</span><span class="sxs-lookup"><span data-stu-id="462b6-140">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="462b6-141">Käytettäessä "false"-arvoa samanniminen numerosarja on oltava kaikissa yrityksissä, joissa on poistokirjatapahtumia.</span><span class="sxs-lookup"><span data-stu-id="462b6-141">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="462b6-142">Jaettuja numerosarjoja on jokaisessa osiossa, joka sisältää poistokirjatapahtumia.</span><span class="sxs-lookup"><span data-stu-id="462b6-142">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="462b6-143">Vakion nimi: **NumberSequenceExistingIsShared**</span><span class="sxs-lookup"><span data-stu-id="462b6-143">Constant name: **NumberSequenceExistingIsShared **</span></span>
    -   <span data-ttu-id="462b6-144">Oletusarvo: tosi</span><span class="sxs-lookup"><span data-stu-id="462b6-144">Default value: true</span></span>

<span data-ttu-id="462b6-145">Parametrit ovat ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans -luokan alussa.</span><span class="sxs-lookup"><span data-stu-id="462b6-145">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="462b6-146">*// Tositteiden kohdistuksen ensisijaisen menetelmän määrittäminen* 
 *// tosi, jos haluat käyttää aiemmin luotua numerosarjan koodia* 
 *// epätosi, jos aiot käyttää järjestelmän määrittämää numerosarjaa (oletus)* const boolean NumberSequenceUseExistingCode = false;</span><span class="sxs-lookup"><span data-stu-id="462b6-146">*// Specify a preferable approach of vouchers allocation* 
 *// true, if you want to use an existing number sequence code* 
 *// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="462b6-147">*// Jos käytetään järjestelmän määrittämää numerosarjaa, määritä numerosarjan parametrit.*
 *// Näillä parametreilla luodaan uusi numerosarja.*</span><span class="sxs-lookup"><span data-stu-id="462b6-147">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
 *// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="462b6-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="462b6-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="462b6-149">*// Jos käytetään aiemmin luotua numerosarjaa, anna nykyinen numerosarjan koodi* 
 *// Tositteen kohdistus siirtyy riveittäin käyttämään aiemmin luotua numerosarjaa.*</span><span class="sxs-lookup"><span data-stu-id="462b6-149">*// If using the existing number sequence approach, specify the existing number sequence code.* 
 *// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="462b6-150">const str NumberSequenceExistingCode = ''; *// Määritä aiemmin luodun numerosarjan koodin vaikutusalue* 
 *// tosi, jos annettu numerosarja on jaettu* 
 *// epätosi, jos annettu numerosarja on yrityskohtainen* 
 *// Järjestelmän määrittämää oletusnumerosarjaa käytetään, jos määritetyllä alueella olevaa numerosarjaa ei löydy.*</span><span class="sxs-lookup"><span data-stu-id="462b6-150">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
 *// true, if the specified number sequence is shared* 
 *// false, if the specified number sequence is per-company* 
 *// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="462b6-151">const boolean NumberSequenceExistingIsShared = true;</span><span class="sxs-lookup"><span data-stu-id="462b6-151">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="462b6-152">Muodosta uudelleen projekti, joka sisältää luokan vakioiden muuttamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="462b6-152">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="462b6-153">Käytettäessä järjestelmän luomaa numerosarjaa (vaihtoehto 1) päivitys käyttää joukkoon perustuvaa käsittelyä kohdistaessaan tositenumerot päivityskomentosarjan parametrien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="462b6-153">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="462b6-154">Se luo myös uuden numerosarjan määritetyillä parametreilla kohdistuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="462b6-154">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="462b6-155">Käytettäessä käyttäjän määrittämää numerosarjaa (vaihtoehto 2) tietopäivitys tarkistaa, esiintyykö määritetyllä alueella vaikuttava numerosarja jokaisen osion tietokannassa ja yrityksessä, jolla on poistokirjatapahtumia.</span><span class="sxs-lookup"><span data-stu-id="462b6-155">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="462b6-156">Jos se esiintyy, päivitys kohdistaa tositenumerot riveittäin numerosarjan määrittämällä tavalla käyttäen numerosarjan kehystä.</span><span class="sxs-lookup"><span data-stu-id="462b6-156">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="462b6-157">Jos numerosarjaa ei ole olemassa määritetyllä alueella, päivitys käyttää oletusarvona olevaa järjestelmän määrittämää numerosarjaa tositenumeroiden kohdistamiseen ja luo uuden numerosarjan määritetyillä oletusparametreilla kohdistuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="462b6-157">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="462b6-158">Kummassakin menetelmässä tietojen päivityskomentosarja käyttää myös numerosarjaa **Tositesarja**-kentässä uusissa kirjauskansion nimissä, jotka luotiin vanhan poistokirjan kirjauskansion nimiä varten.</span><span class="sxs-lookup"><span data-stu-id="462b6-158">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>




