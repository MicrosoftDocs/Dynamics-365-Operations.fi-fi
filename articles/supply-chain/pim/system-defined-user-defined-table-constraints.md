---
title: Järjestelmän ja käyttäjän määrittämät taulurajoitukset
description: Tässä artikkelissa kuvataan käyttäjän ja järjestelmän määrittämiä taulurajoituksia tuotemääritysmallin komponenteille. Taulurajoitukset edustavat sallittujen määriteyhdistelmien matriiseja, joissa kukin rivi määrittää yhden mahdollisten määritearvojen joukon.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3fb1395859b5abd06539e07ada3d968b2e9c9147
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427089"
---
# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="82123-104">Järjestelmän ja käyttäjän määrittämät taulurajoitukset</span><span class="sxs-lookup"><span data-stu-id="82123-104">System-defined and user-defined table constraints</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82123-105">Tässä artikkelissa kuvataan käyttäjän ja järjestelmän määrittämiä taulurajoituksia tuotemääritysmallin komponenteille.</span><span class="sxs-lookup"><span data-stu-id="82123-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="82123-106">Taulurajoitukset edustavat sallittujen määriteyhdistelmien matriiseja, joissa kukin rivi määrittää yhden mahdollisten määritearvojen joukon.</span><span class="sxs-lookup"><span data-stu-id="82123-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="82123-107">Taulurajoitukset ovat matriiseja komponenteille tuotemääritysmallissa sallittujen määritteiden yhdistelmistä.</span><span class="sxs-lookup"><span data-stu-id="82123-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="82123-108">Taulun kukin rivi määrittää yhden mahdollisten määritearvojen joukon.</span><span class="sxs-lookup"><span data-stu-id="82123-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="82123-109">Tuotemääritysmallissa voi määrittää kahdentyyppisiä rajoituksia:</span><span class="sxs-lookup"><span data-stu-id="82123-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="82123-110">**Lausekerajoitus** – Luo lauseke, joka määrittää määritteiden väliset suhteet niin, että tuotetta määritettäessä voidaan valita vain yhteensopivia arvoja.</span><span class="sxs-lookup"><span data-stu-id="82123-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="82123-111">**Taulurajoitus** – Luo taulu, joka määrittää kaikki tietylle määritejoukolle sallitut yhdistelmät.</span><span class="sxs-lookup"><span data-stu-id="82123-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="82123-112">Käytettävissä on kahdenlaisia taulurajoituksia: käyttäjän määrittämiä ja järjestelmän määrittämiä.</span><span class="sxs-lookup"><span data-stu-id="82123-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="82123-113">Tässä artikkelissa on kuvattu käyttäjän ja järjestelmän määrittämiä taulurajoituksia tuotemääritysmallin komponenteille.</span><span class="sxs-lookup"><span data-stu-id="82123-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="82123-114">Käyttäjän määrittämät taulurajoitukset</span><span class="sxs-lookup"><span data-stu-id="82123-114">User-defined table constraints</span></span>
<span data-ttu-id="82123-115">Käyttäjän määrittämä taulurajoitus on matriisityyppi, jonka avulla voidaan kuvata määritetyyppien määrittämien määritearvojen yhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="82123-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="82123-116">Jos yrityksesi valmistaa esimerkiksi kaiuttimia, voit liittää käyttäjän määrittämään taulurajoitukseen sarakkeet kaapin viimeistelyä ja etusäleikköä varten.</span><span class="sxs-lookup"><span data-stu-id="82123-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="82123-117">Kaapin viimeistelyn määritetyypillä on neljä arvoa ja etusäleikön määritetyypillä on kolme arvoa.</span><span class="sxs-lookup"><span data-stu-id="82123-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="82123-118">Jos rajoituksia ei käytetä, mahdollisia yhdistelmiä on 4 × 3 = 12.</span><span class="sxs-lookup"><span data-stu-id="82123-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="82123-119">Tässä esimerkissä on kuitenkin sallittu vain kuusi yhdistelmää, kuten seuraavasta taulukosta käy ilmi.</span><span class="sxs-lookup"><span data-stu-id="82123-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="82123-120">Nämä tiedot näkyvät **Muokkaa taulurajoitusta** -sivun **Sallitut yhdistelmät** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="82123-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="82123-121">Kaapin viimeistely</span><span class="sxs-lookup"><span data-stu-id="82123-121">Cabinet finish</span></span> | <span data-ttu-id="82123-122">Etusäleikkö</span><span class="sxs-lookup"><span data-stu-id="82123-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="82123-123">Musta</span><span class="sxs-lookup"><span data-stu-id="82123-123">Black</span></span>          | <span data-ttu-id="82123-124">Musta</span><span class="sxs-lookup"><span data-stu-id="82123-124">Black</span></span>       |
| <span data-ttu-id="82123-125">Musta</span><span class="sxs-lookup"><span data-stu-id="82123-125">Black</span></span>          | <span data-ttu-id="82123-126">Metalli</span><span class="sxs-lookup"><span data-stu-id="82123-126">Metal</span></span>       |
| <span data-ttu-id="82123-127">Tammi</span><span class="sxs-lookup"><span data-stu-id="82123-127">Oak</span></span>            | <span data-ttu-id="82123-128">Musta</span><span class="sxs-lookup"><span data-stu-id="82123-128">Black</span></span>       |
| <span data-ttu-id="82123-129">Ruusupuu</span><span class="sxs-lookup"><span data-stu-id="82123-129">Rosewood</span></span>       | <span data-ttu-id="82123-130">Valkoinen</span><span class="sxs-lookup"><span data-stu-id="82123-130">White</span></span>       |
| <span data-ttu-id="82123-131">Valkoinen</span><span class="sxs-lookup"><span data-stu-id="82123-131">White</span></span>          | <span data-ttu-id="82123-132">Musta</span><span class="sxs-lookup"><span data-stu-id="82123-132">Black</span></span>       |
| <span data-ttu-id="82123-133">Valkoinen</span><span class="sxs-lookup"><span data-stu-id="82123-133">White</span></span>          | <span data-ttu-id="82123-134">Valkoinen</span><span class="sxs-lookup"><span data-stu-id="82123-134">White</span></span>       |

<span data-ttu-id="82123-135">Käyttäjän määrittämät taulurajoitukset määritetään staattisella taulusyötteellä, joka toimii samaan tapaan kuin lausekerajoitus.</span><span class="sxs-lookup"><span data-stu-id="82123-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="82123-136">Kun käytät käyttäjän määrittämää taulurajoitusta, etuna on se, että taulut on usein helpompi luoda, ne ovat selkeämpiä ja niiden ylläpitäminen on helpompaa kuin pitkien lausekerajoitteiden.</span><span class="sxs-lookup"><span data-stu-id="82123-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="82123-137">Järjestelmän määrittämät taulurajoitukset</span><span class="sxs-lookup"><span data-stu-id="82123-137">System-defined table constraints</span></span>
<span data-ttu-id="82123-138">Järjestelmän määrittämä taulurajoitus luo dynaamisen yhdistämismäärityksen taulussa olevan määritetyypin ja kentän välille.</span><span class="sxs-lookup"><span data-stu-id="82123-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="82123-139">Kun järjestelmän määrittämä taulurajoitus sisältyy tuotemääritysmalliin, yhdistämismääritys varmistaa, että taulun tiedot ovat näkyvissä määritetyypin arvojen sijaan.</span><span class="sxs-lookup"><span data-stu-id="82123-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="82123-140">Tuloksena on dynaaminen rajoitus, koska taulun sisältöä voi muokata (esimerkiksi muissa moduuleissa).</span><span class="sxs-lookup"><span data-stu-id="82123-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="82123-141">Kun luot järjestelmän määrittämän taulurajoituksen, valitse taulu, määritä halutessasi käytettävä kysely ja määritä sitten määritetyypit valitun taulun kenttiin.</span><span class="sxs-lookup"><span data-stu-id="82123-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="82123-142">Kenttätyyppien on vastattava määritetyyppejä.</span><span class="sxs-lookup"><span data-stu-id="82123-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="82123-143">Ennen kuin taulurajoitus voidaan ottaa käyttöön tuotemääritysmallissa, taulurajoitus on sisällytettävä mallin yhden komponentin rajoitukseen.</span><span class="sxs-lookup"><span data-stu-id="82123-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="82123-144">Tätä varten luodaan uusi rajoitus, valitaan taulurajoituksen tyyppi ja valitaan sitten käytettävä taulurajoitusmääritys.</span><span class="sxs-lookup"><span data-stu-id="82123-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="82123-145">Lopuksi kaikki taulurajoituksen kentät on yhdistettävä tuotemääritysmallin määritteisiin.</span><span class="sxs-lookup"><span data-stu-id="82123-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="additional-resources"></a><span data-ttu-id="82123-146">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="82123-146">Additional resources</span></span>
--------

[<span data-ttu-id="82123-147">Tuotekonfiguraatiomallien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="82123-147">Product configuration models overview</span></span>](product-configuration-models.md)



