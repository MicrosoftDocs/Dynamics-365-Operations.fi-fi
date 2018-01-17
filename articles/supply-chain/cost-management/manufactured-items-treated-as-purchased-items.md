---
title: "Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen"
description: "Tuotteita voi hankkia eri tavoin: ne voivat olla tuotettuja ja hankittuja (ostettuja). Tässä artikkelissa kuvataan joitakin seikkoja, jotka on otettava huomioon määritettäessä tuotteita monitasoista hankintaa varten."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 87a6fd8ad05e460b9620855da4bcb587ad3ac3ae
ms.openlocfilehash: 2ebe639b039e58c3173e0bf3eda5ff2f0351dbeb
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="012c4-104">Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="012c4-104">Set up products that can be produced or procured</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="012c4-105">Tuotteita voi hankkia eri tavoin: ne voivat olla tuotettuja ja hankittuja (ostettuja).</span><span class="sxs-lookup"><span data-stu-id="012c4-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="012c4-106">Tässä artikkelissa kuvataan joitakin seikkoja, jotka on otettava huomioon määritettäessä tuotteita monitasoista hankintaa varten.</span><span class="sxs-lookup"><span data-stu-id="012c4-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="012c4-107">Monitasoista hankintaa käytetään yleensä ostettuun nimikkeeseen, jota valmistetaan satunnaisesti tai kun nimike, joka oli ensisijaisesti valmistettu nimike, muuttuu siten, että se on nyt ensisijaisesti ostettu nimike.</span><span class="sxs-lookup"><span data-stu-id="012c4-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="012c4-108">Nimike määritetään ensin valmistetuksi nimikkeeksi, jotta tuoterakenne- ja reititystiedot voidaan määrittää, sekä nimikkeen tuotantotilauksien tueksi.</span><span class="sxs-lookup"><span data-stu-id="012c4-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="012c4-109">Tuotantotyypiksi on määritettävä **Tuoterakenne** (tai prosessivalmistuksessa **Resepti** tai **Oheistuote**).</span><span class="sxs-lookup"><span data-stu-id="012c4-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="012c4-110">Standardikustannuksia käytettäessä nimikkeen kustannustietueen voi laskea valmistetulle nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="012c4-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="012c4-111">Nimikkeen kustannustietue ei kuitenkaan välttämättä vastaa hankintatarkoituksissa tarvittavaa vakiokustannusta.</span><span class="sxs-lookup"><span data-stu-id="012c4-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="012c4-112">Tällöin vakiokustannus on kirjoitettava manuaalisesti ja aktivoitava nimikkeen kustannustietuetta varten.</span><span class="sxs-lookup"><span data-stu-id="012c4-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="012c4-113">Kustannusten laskennassa kannattaa valita erityinen tuoterakenne ja reititys, joka vastaa tuotteen toimitusmiksiä tilikaudella. Näin varianssit voidaan minimoida.</span><span class="sxs-lookup"><span data-stu-id="012c4-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="012c4-114">Lisäksi yhdessä toimipaikassa valmistettu nimike voidaan siirtää toiseen toimipaikkaan.</span><span class="sxs-lookup"><span data-stu-id="012c4-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="012c4-115">Siksi nimikkeen kustannus on syötettävä manuaalisesti ja aktivoitava toimipaikalle, johon nimike siirretään.</span><span class="sxs-lookup"><span data-stu-id="012c4-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="012c4-116">Kun valmistettua nimikettä käytetään komponenttina korkeamman tason tuotteissa, komponentin kustannuksia tulee käsitellä ostettuna nimikkeenä.</span><span class="sxs-lookup"><span data-stu-id="012c4-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="012c4-117">Tämän ohje pätee riippumatta siitä, onko komponentin kustannukset laskettu vai syötetty manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="012c4-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="012c4-118">Toisin sanoen tuoterakennelaskennassa nimikkeen kustannuksia on käsiteltävä ostettuna komponenttina sen sijaan, että kustannukset laskettaisiin käyttämällä nimikkeen tuoterakennetta ja reititystietoja.</span><span class="sxs-lookup"><span data-stu-id="012c4-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="012c4-119">Voit estää laskennan valitsemalla **Lopeta hajotus** -merkin, joka on sisällytetty nimikkeelle määritettyyn tuoterakenteen laskentaryhmään.</span><span class="sxs-lookup"><span data-stu-id="012c4-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="012c4-120">Voit estää pääajoituksen laskentaa hajottamasta tarpeita nimikkeen kautta asettamalla hajotuksen lopetusrajaksi 0 (nolla) päivää nimikkeen kattavuudessa tai kattavuusryhmässä.</span><span class="sxs-lookup"><span data-stu-id="012c4-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="012c4-121">Pääajoituksen laskenta käsittelee tämän jälkeen nimikkeen ostettuna nimikkeenä eikä suorita lisää laskutoimituksia nimikkeen tuoterakenne- ja reititystiedoille.</span><span class="sxs-lookup"><span data-stu-id="012c4-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






