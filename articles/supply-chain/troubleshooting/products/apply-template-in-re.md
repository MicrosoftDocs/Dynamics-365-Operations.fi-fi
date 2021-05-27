---
title: Mallia ei voi käyttää vapautettuun tuotteeseen
description: Mallia ei voi käyttää vapautettuun tuotteeseen.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026466"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="20436-103">Mallia ei voi käyttää vapautetun tuotteen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="20436-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="20436-104">Tietopankin numero: 4612097</span><span class="sxs-lookup"><span data-stu-id="20436-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="20436-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="20436-105">Symptoms</span></span>

<span data-ttu-id="20436-106">Kun luot uuden vapautetun tuotteen käyttämällä **Uusi vapautettu tuote** -valintaikkunaa, voit valita mallin.</span><span class="sxs-lookup"><span data-stu-id="20436-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="20436-107">Mallin tulisi määrittää oletusasetukset monille uuden vapautetun tuotteen kentille.</span><span class="sxs-lookup"><span data-stu-id="20436-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="20436-108">Joitakin kenttiä tai kaikkia kenttiä ei kuitenkaan voi määrittää mallin valitsemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="20436-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="20436-109">Syy</span><span class="sxs-lookup"><span data-stu-id="20436-109">Cause</span></span>

<span data-ttu-id="20436-110">Monella Microsoft Dynamics 365 Supply Chain Managementin sivulla voit luoda mallin, jossa määritetään sivuilla näkyvien tietueiden alkuasetukset.</span><span class="sxs-lookup"><span data-stu-id="20436-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="20436-111">Voit luoda yhden näistä malleista valitsemalla **Tietueen tiedot** toimintoruudun **Asetukset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="20436-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="20436-112">Vapautetut tuotteet ovat kuitenkin paljon monimutkaisempia kuin useimmat muut tietueet.</span><span class="sxs-lookup"><span data-stu-id="20436-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="20436-113">Vaikka voitkin luoda mallin valitsemalla **Vapautetut tuotteet** -sivulla **Tietueen tiedot** ja voit valita tämän mallin vapautetun tuotteen luomiseen, malli ei tarjoa uuden vapautetun tuotteen odotettuja kenttäarvoja.</span><span class="sxs-lookup"><span data-stu-id="20436-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="20436-114">Siksi vapautettujen tuotteiden tietuetietomalleja ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="20436-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="20436-115">Sen sijaan on luotava erilliset tuotemallit.</span><span class="sxs-lookup"><span data-stu-id="20436-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="20436-116">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="20436-116">Resolution</span></span>

<span data-ttu-id="20436-117">Voit luoda tuotemallin käyttämällä toimintoruudun **Tuote**-välilehden **Malli**-valikkoa, ei **Asetukset**-välilehden **Tietueen tiedot** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="20436-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="20436-118">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="20436-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="20436-119">Valitse toimintoruudun **Tuote**-välilehden **Uusi**-ryhmästä **Malli** ja valitse sitten tarpeen mukaan joko **Luo henkilökohtainen malli** tai **Luo jaettu malli**.</span><span class="sxs-lookup"><span data-stu-id="20436-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
