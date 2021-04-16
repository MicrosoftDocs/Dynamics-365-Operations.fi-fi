---
title: Myyntipistesovellus (POS) ja käyttäjän kielialueasetukset
description: Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Modern POS:ssa (MPOS) ja Cloud POS:ssa.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0c5087ee04030a76aef774871b88b7970391723c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804378"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="b7e2e-103">Myyntipistesovellus (POS) ja käyttäjän kielialueasetukset</span><span class="sxs-lookup"><span data-stu-id="b7e2e-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b7e2e-104">Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Modern POS:ssa (MPOS) ja Cloud POS:ssa.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="b7e2e-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b7e2e-105">Overview</span></span>
<span data-ttu-id="b7e2e-106">Modern POS (MPOS) ja Cloud POS tukevat ympäristöjä, joissa kielisetukset ja käännökset voivat vaihdella myymälän ja käyttäjäasetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="b7e2e-107">Esimerkiksi myymälä saattaa sijaita alueella, jossa englannin kieli on asiakkaiden yleisimmin käyttämä, mutta jotkut työntekijät käyttävät mieluummin sovellusta ranskankielisillä käännöksillä.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="b7e2e-108">Tietojen kieli</span><span class="sxs-lookup"><span data-stu-id="b7e2e-108">Data language</span></span>

<span data-ttu-id="b7e2e-109">Käyttäjän asetuksista riippumatta, MPOS ja Cloud POS käyttävät aina myymälän kieliasetuksia tietojen käännöksen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="b7e2e-110">Näin voidaan varmistaa, että kaikilla käyttäjillä ja asiakkailla on yhtenevä kokemus.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="b7e2e-111">Esimerkkejä tiedoista ovat:</span><span class="sxs-lookup"><span data-stu-id="b7e2e-111">Examples of data include:</span></span>

- <span data-ttu-id="b7e2e-112">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="b7e2e-112">Products</span></span>
- <span data-ttu-id="b7e2e-113">Määritteet ja arvot</span><span class="sxs-lookup"><span data-stu-id="b7e2e-113">Attributes and values</span></span>
- <span data-ttu-id="b7e2e-114">Luokkien nimet</span><span class="sxs-lookup"><span data-stu-id="b7e2e-114">Category names</span></span>
- <span data-ttu-id="b7e2e-115">Tulostetut tai sähköpostitse toimitetut tapahtumien kuitit</span><span class="sxs-lookup"><span data-stu-id="b7e2e-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="b7e2e-116">Maksutapojen nimet</span><span class="sxs-lookup"><span data-stu-id="b7e2e-116">Payment method names</span></span>
- <span data-ttu-id="b7e2e-117">Riveillä näytettävät sanomat</span><span class="sxs-lookup"><span data-stu-id="b7e2e-117">Line display messages</span></span>

<span data-ttu-id="b7e2e-118">Myymälän kieltä käytetään myös myyntipisteen pääkirjautumissivulla, koska käyttäjää ei tunneta ennen kirjautumista.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="b7e2e-119">Jos myymälän kielellä olevaa käännöstä ei ole saatavilla, myyntipiste palaa yrityksen kieleen.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="b7e2e-120">Myymälän kieliasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b7e2e-120">Configuring the store's language setting</span></span>

<span data-ttu-id="b7e2e-121">Myymälän kieliasetukset määritetään **Kaikki myymälät** -kohdassa **Myymälä**-sivulla valitsemalla **Yleinen &gt; Alueasetukset &gt; Kieli**.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="b7e2e-122">Valitse kunkin myymälän kieli avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="b7e2e-123">Käyttöliittymän kieli</span><span class="sxs-lookup"><span data-stu-id="b7e2e-123">User interface language</span></span>

<span data-ttu-id="b7e2e-124">Myyntipisteen käyttäjän kieliasetukset määrittävät sovelluksen käyttöliittymässä käytettävät käännökset.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="b7e2e-125">Tähän sisältyvät kaikki otsikot, valikot ja luettelot, joita ei pidetä tietoina.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="b7e2e-126">Yksi poikkeus tähän on teksti, joka näytetään myyntipisteen painikeruudukoissa.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="b7e2e-127">Ne eivät tue käännöksiä, joten ne näyttävät aina tekstin siten, kuin se on määritetty painikkeessa.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="b7e2e-128">Jos haluat, että ne tukevat käännettyjä painikkeita, sinun on kopioitava erilliset painikeruudukot ja ylläpidettävä niitä, ja määritettävä ne soveltuville käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="b7e2e-129">Käyttäjän kieliasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b7e2e-129">Configuring the user's language setting</span></span>

<span data-ttu-id="b7e2e-130">Myyntipisteen kieliasetukset määritetään kohdassa **Työntekijä**-sivun **Kaikki työntekijät** -kohdassa valitsemalla **Retail ja Commerce &gt; Kieli**.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="b7e2e-131">Sitä ei määritetä profiilin päävälilehdellä. Myyntipiste ei käytä tätä asetusta.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="b7e2e-132">Jos käyttäjän kieltä ei määritetä tai jos se on määritetty kielelle, jolla ei ole saatavilla käännöksiä, myyntipiste palaa myymälän kieleen.</span><span class="sxs-lookup"><span data-stu-id="b7e2e-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="b7e2e-133">Käyttöliittymän kieli   </span><span class="sxs-lookup"><span data-stu-id="b7e2e-133">UI language</span></span>                | <span data-ttu-id="b7e2e-134">Tietojen kieli (tuotteet, kuittimuodot, rivinäyttö, jne.)</span><span class="sxs-lookup"><span data-stu-id="b7e2e-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b7e2e-135">**Yritys**</span><span class="sxs-lookup"><span data-stu-id="b7e2e-135">**Company**</span></span> | <span data-ttu-id="b7e2e-136">Oletusarvo</span><span class="sxs-lookup"><span data-stu-id="b7e2e-136">Default</span></span>                    | <span data-ttu-id="b7e2e-137">Oletusarvo</span><span class="sxs-lookup"><span data-stu-id="b7e2e-137">Default</span></span>                                                       |
| <span data-ttu-id="b7e2e-138">**Myymälä**</span><span class="sxs-lookup"><span data-stu-id="b7e2e-138">**Store**</span></span>   | <span data-ttu-id="b7e2e-139">Ohittaa yrityksen</span><span class="sxs-lookup"><span data-stu-id="b7e2e-139">Overrides company</span></span>          | <span data-ttu-id="b7e2e-140">Ohittaa yrityksen</span><span class="sxs-lookup"><span data-stu-id="b7e2e-140">Overrides company</span></span>                                             |
| <span data-ttu-id="b7e2e-141">**Käyttäjä**</span><span class="sxs-lookup"><span data-stu-id="b7e2e-141">**User**</span></span>    | <span data-ttu-id="b7e2e-142">Ohittaa myymälän tai yrityksen</span><span class="sxs-lookup"><span data-stu-id="b7e2e-142">Overrides store or company</span></span> | <span data-ttu-id="b7e2e-143">En koskaan</span><span class="sxs-lookup"><span data-stu-id="b7e2e-143">Never</span></span>                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]