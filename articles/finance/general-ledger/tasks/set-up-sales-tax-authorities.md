---
title: Arvonlisäveroviranomaisten määrittäminen
description: Arvonlisäveroviranomaiset ovat yksiköitä, joille on raportoitava kerättävästä arvonlisäverosta ja joille arvonlisävero maksetaan.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb0b30be91e33cb50af0ae5c2e4dcd75bd12599b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175401"
---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="08326-103">Arvonlisäveroviranomaisten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="08326-103">Set up sales tax authorities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08326-104">Arvonlisäveroviranomaiset ovat yksiköitä, joille on raportoitava kerättävästä arvonlisäverosta ja joille arvonlisävero maksetaan.</span><span class="sxs-lookup"><span data-stu-id="08326-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="08326-105">Yritys voi maksaa arvonlisäverot suoraan viranomaiselle tai arvonlisäveroviranomaiselle luodun toimittajatilin kautta.</span><span class="sxs-lookup"><span data-stu-id="08326-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="08326-106">Jos valitset tämän vaihtoehdon, yritys voi maksaa arvonlisäveroviranomaiselle ajoissa tavanomaista maksurutiinia käyttäen.</span><span class="sxs-lookup"><span data-stu-id="08326-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="08326-107">Jos veroviranomaista ei määritetä toimittajaksi, jonkun on laadittava maksut veroviranomaiselle manuaalisesti asianmukaisena eräpäivänä.</span><span class="sxs-lookup"><span data-stu-id="08326-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="08326-108">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="08326-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="08326-109">Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroviranomaiset.</span><span class="sxs-lookup"><span data-stu-id="08326-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="08326-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="08326-110">Click New.</span></span>
3. <span data-ttu-id="08326-111">Kirjoita arvo Viranomainen-kenttään.</span><span class="sxs-lookup"><span data-stu-id="08326-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="08326-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="08326-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="08326-113">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="08326-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="08326-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="08326-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="08326-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="08326-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="08326-116">Valitse maasi/alueesi raportin asettelu, jos sellainen on valittavissa.</span><span class="sxs-lookup"><span data-stu-id="08326-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="08326-117">Jos raportin asettelut eivät vastaa arvonlisäveroviranomaisen vaatimuksia, käytä oletusasettelua.</span><span class="sxs-lookup"><span data-stu-id="08326-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="08326-118">Määritä, miten veron maksettava kokonaissumma on pyöristettävä, syöttämällä arvo Pyöristystapa- ja Pyöristys-kenttään.</span><span class="sxs-lookup"><span data-stu-id="08326-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="08326-119">Pyöristyserot kirjataan tileille kirjanpidolle määritettyjä automaattisia tapahtumia varten.</span><span class="sxs-lookup"><span data-stu-id="08326-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="08326-120">Syötä Pyöristys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="08326-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="08326-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="08326-121">Click Save.</span></span>

