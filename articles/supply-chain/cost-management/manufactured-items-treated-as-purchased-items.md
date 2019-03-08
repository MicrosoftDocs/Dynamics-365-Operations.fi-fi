---
title: Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen
description: 'Tuotteita voi hankkia eri tavoin: ne voivat olla tuotettuja ja hankittuja (ostettuja). Tässä artikkelissa kuvataan joitakin seikkoja, jotka on otettava huomioon määritettäessä tuotteita monitasoista hankintaa varten.'
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a910b5782c8f15cfdd4cf93ea883bc28a5ce8e1a
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2019
ms.locfileid: "338449"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="f58e5-104">Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f58e5-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f58e5-105">Tuotteita voi hankkia eri tavoin: ne voivat olla tuotettuja ja hankittuja (ostettuja).</span><span class="sxs-lookup"><span data-stu-id="f58e5-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="f58e5-106">Tässä artikkelissa kuvataan joitakin seikkoja, jotka on otettava huomioon määritettäessä tuotteita monitasoista hankintaa varten.</span><span class="sxs-lookup"><span data-stu-id="f58e5-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="f58e5-107">Monitasoista hankintaa käytetään yleensä ostettuun nimikkeeseen, jota valmistetaan satunnaisesti tai kun nimike, joka oli ensisijaisesti valmistettu nimike, muuttuu siten, että se on nyt ensisijaisesti ostettu nimike.</span><span class="sxs-lookup"><span data-stu-id="f58e5-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="f58e5-108">Nimike määritetään ensin valmistetuksi nimikkeeksi, jotta tuoterakenne- ja reititystiedot voidaan määrittää, sekä nimikkeen tuotantotilauksien tueksi.</span><span class="sxs-lookup"><span data-stu-id="f58e5-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="f58e5-109">Tuotantotyypiksi on määritettävä **Tuoterakenne** (tai prosessivalmistuksessa **Resepti** tai **Oheistuote**).</span><span class="sxs-lookup"><span data-stu-id="f58e5-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="f58e5-110">Standardikustannuksia käytettäessä nimikkeen kustannustietueen voi laskea valmistetulle nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="f58e5-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="f58e5-111">Nimikkeen kustannustietue ei kuitenkaan välttämättä vastaa hankintatarkoituksissa tarvittavaa vakiokustannusta.</span><span class="sxs-lookup"><span data-stu-id="f58e5-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="f58e5-112">Tällöin vakiokustannus on kirjoitettava manuaalisesti ja aktivoitava nimikkeen kustannustietuetta varten.</span><span class="sxs-lookup"><span data-stu-id="f58e5-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="f58e5-113">Kustannusten laskennassa kannattaa valita erityinen tuoterakenne ja reititys, joka vastaa tuotteen toimitusmiksiä tilikaudella. Näin varianssit voidaan minimoida.</span><span class="sxs-lookup"><span data-stu-id="f58e5-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="f58e5-114">Lisäksi yhdessä toimipaikassa valmistettu nimike voidaan siirtää toiseen toimipaikkaan.</span><span class="sxs-lookup"><span data-stu-id="f58e5-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="f58e5-115">Siksi nimikkeen kustannus on syötettävä manuaalisesti ja aktivoitava toimipaikalle, johon nimike siirretään.</span><span class="sxs-lookup"><span data-stu-id="f58e5-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="f58e5-116">Kun valmistettua nimikettä käytetään komponenttina korkeamman tason tuotteissa, komponentin kustannuksia tulee käsitellä ostettuna nimikkeenä.</span><span class="sxs-lookup"><span data-stu-id="f58e5-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="f58e5-117">Tämän ohje pätee riippumatta siitä, onko komponentin kustannukset laskettu vai syötetty manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="f58e5-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="f58e5-118">Toisin sanoen tuoterakennelaskennassa nimikkeen kustannuksia on käsiteltävä ostettuna komponenttina sen sijaan, että kustannukset laskettaisiin käyttämällä nimikkeen tuoterakennetta ja reititystietoja.</span><span class="sxs-lookup"><span data-stu-id="f58e5-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="f58e5-119">Voit estää laskennan valitsemalla **Lopeta hajotus** -merkin, joka on sisällytetty nimikkeelle määritettyyn tuoterakenteen laskentaryhmään.</span><span class="sxs-lookup"><span data-stu-id="f58e5-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="f58e5-120">Voit estää pääajoituksen laskentaa hajottamasta tarpeita nimikkeen kautta asettamalla hajotuksen lopetusrajaksi 0 (nolla) päivää nimikkeen kattavuudessa tai kattavuusryhmässä.</span><span class="sxs-lookup"><span data-stu-id="f58e5-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="f58e5-121">Pääajoituksen laskenta käsittelee tämän jälkeen nimikkeen ostettuna nimikkeenä eikä suorita lisää laskutoimituksia nimikkeen tuoterakenne- ja reititystiedoille.</span><span class="sxs-lookup"><span data-stu-id="f58e5-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>





