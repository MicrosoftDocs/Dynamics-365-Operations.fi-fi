---
title: "Kirjanpidon kohdistussäännöt"
description: "Tässä artikkelissa on tietoja kirjanpidon kohdistussäännöistä. Artikkelissa kuvataan kohdistussääntöjen eri osia sekä käytettävissä olevia kohdistussääntöjä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 87b98811dabb6a8593cd4a75ad9c5a028f653867
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="3aab1-104">Kirjanpidon kohdistussäännöt</span><span class="sxs-lookup"><span data-stu-id="3aab1-104">Ledger allocation rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3aab1-105">Tässä artikkelissa on tietoja kirjanpidon kohdistussäännöistä.</span><span class="sxs-lookup"><span data-stu-id="3aab1-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="3aab1-106">Artikkelissa kuvataan kohdistussääntöjen eri osia sekä käytettävissä olevia kohdistussääntöjä.</span><span class="sxs-lookup"><span data-stu-id="3aab1-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="3aab1-107">Kirjanpidon kohdistussääntöjen avulla voidaan automaattisesti laskea ja luoda kohdistuskirjauskansioita ja kirjanpitomerkintöjä kirjanpitosaldojen tai kiinteiden summien kohdistusta varten.</span><span class="sxs-lookup"><span data-stu-id="3aab1-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="3aab1-108">Kohdistusmenetelmät voivat olla muuttuvia tai kiinteitä.</span><span class="sxs-lookup"><span data-stu-id="3aab1-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="3aab1-109">Kirjanpidon kohdistussäännöissä voidaan käyttää seuraavia kohdistusmenetelmiä:</span><span class="sxs-lookup"><span data-stu-id="3aab1-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="3aab1-110">**Peruste** – Tätä muuttuvaa menetelmää käytetään, kun kohdistus riippuu todellisesta kirjanpitosaldosta suodatusehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="3aab1-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="3aab1-111">Esimerkiksi mainoskulut voidaan kohdistaa sen mukaan, mikä on kunkin osaston myynti suhteessa osastojen kokonaismyyntiin.</span><span class="sxs-lookup"><span data-stu-id="3aab1-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="3aab1-112">**Kiinteä prosentti** ja **kiinteä paino** – Näissä menetelmissä kohdistusprosentti tai paino on määritetty suoraan säännölle.</span><span class="sxs-lookup"><span data-stu-id="3aab1-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="3aab1-113">Esimerkiksi mainontakulut voidaan kohdistaa siten, että osasto A saa 70 prosenttia mainoskuluista ja osasto B 30 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="3aab1-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="3aab1-114">**Tasaisesti** – Tämä menetelmä jakaa summan tasan kunkin määritetyn kohteen kesken.</span><span class="sxs-lookup"><span data-stu-id="3aab1-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="3aab1-115">Jos esimerkiksi kohteita määritetään osastolle A ja B, mainoskulut voidaan jakaa siten, että osastot A ja B saavat kumpikin 50 prosenttia mainoskuluista.</span><span class="sxs-lookup"><span data-stu-id="3aab1-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="3aab1-116">Jos kohdistussäännön kohdistusmenetelmä on Peruste, myös erilliset kirjanpidon kohdistusperustesäännöt täytyy määrittää.</span><span class="sxs-lookup"><span data-stu-id="3aab1-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="3aab1-117">Käsittele kohdistuspyyntö -prosessin avulla käyttäjät voivat käsitellä kirjanpidon kohdistussäännön ja esikatsella tuloksena muodostuvia kohdistuksen kirjauskansiovientejä, ennen kuin he joko kirjaavat tai poistavat lasketut kohdistukset.</span><span class="sxs-lookup"><span data-stu-id="3aab1-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="3aab1-118">Kirjanpidon kohdistussääntöjen osat</span><span class="sxs-lookup"><span data-stu-id="3aab1-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="3aab1-119">Jokaisella kohdistussäännöllä on neljä komponenttia: yleinen, lähde, kohde ja vastakirjaus.</span><span class="sxs-lookup"><span data-stu-id="3aab1-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="3aab1-120">Lisäkomponenttina tarvitaan kirjanpidon kohdistusperustesäännöt, jos kohdistusmenetelmänä on Peruste.</span><span class="sxs-lookup"><span data-stu-id="3aab1-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="3aab1-121">Jokainen komponentti tarjoaa tärkeitä tietoja, jotka tarvitaan kohdistusten käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="3aab1-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="3aab1-122">**Yleinen** – Tässä komponentissa käyttäjä määrittää vaihtoehdot, kuten kohdistusmenetelmän, konsernin sisäisten sääntöjen asetukset ja sen, onko sääntö aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="3aab1-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="3aab1-123">**Lähde** – Tässä komponentissa käyttäjä määrittää kohdistuksen lähdetiedot.</span><span class="sxs-lookup"><span data-stu-id="3aab1-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="3aab1-124">Varaus voi perustua kirjanpitosaldoihin (**Tietolähde**  =  **Kirjanpito**) tai kiinteisiin summiin (**Tietolähde**  =  **Kiinteä arvo**).</span><span class="sxs-lookup"><span data-stu-id="3aab1-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="3aab1-125">Kun **Tietolähde** -asetukseksi valitaan **Kirjanpito**, kirjanpidon kohdistussäännölle (esimerkiksi mainoskuluille) on määritettävä lähteen suodatusehdot.</span><span class="sxs-lookup"><span data-stu-id="3aab1-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="3aab1-126">**Kohde** – Tämä komponentti määrittää, miten kohdistuksen laskennan tulos jaetaan ja kirjataan.</span><span class="sxs-lookup"><span data-stu-id="3aab1-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="3aab1-127">Kullekin osastolle voi esimerkiksi olla yksi kohderivi.</span><span class="sxs-lookup"><span data-stu-id="3aab1-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="3aab1-128">**Vastakirjaus** – Tämä komponentti määrittää, miten päätilit ja dimensiot pitää määritellä vastakirjauksille, joilla kohdekirjaukset täsmätään.</span><span class="sxs-lookup"><span data-stu-id="3aab1-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="3aab1-129">Käyttäjän määrittämiä vaihtoehtoja käytetään tavallisesti lähteeseen perustuvien tilien ja dimensioiden sijasta.</span><span class="sxs-lookup"><span data-stu-id="3aab1-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="3aab1-130">Kun **Tietolähde**-asetuksena on **Kiinteä arvo**, **Lähde**-vaihtoehtoa ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="3aab1-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="3aab1-131">**Kirjanpidon kohdistusperustesäännöt** – Näillä säännöillä on omat lähteen suodatusehdot, jotka määrittävät, mitä kirjanpitosaldoja käytetään kohdistuksessa (esimerkiksi tuotto osastoittain).</span><span class="sxs-lookup"><span data-stu-id="3aab1-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="3aab1-132">Kutakin kohdistusperusteen sääntöä voi käyttää useiden kohdistussääntöjen kanssa.</span><span class="sxs-lookup"><span data-stu-id="3aab1-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>





