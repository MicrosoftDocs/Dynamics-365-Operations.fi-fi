---
title: Suhteellisen polun käyttäminen ER-mallien ja-muotojen tietojen sidonnoissa
description: Sähköisellä raportointityökalun (ER) avulla käyttäjät voivat määrittää sähköisen muodon rakenteita ja kuvailla sitten, miten kyseiset rakenteet täytetään sovelluksessa olevilla tiedoilla ja algoritmeilla.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c08e81b6e2983a8f16104698944820e93ba3852d
ms.sourcegitcommit: 139c8007e68d279d7ca9aa302598217522abb8cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331321"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="6a285-103">Suhteellisen polun käyttäminen ER-mallien ja-muotojen tietojen sidonnoissa</span><span class="sxs-lookup"><span data-stu-id="6a285-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6a285-104">Sähköisellä raportointityökalun (ER) avulla käyttäjät voivat määrittää sähköisen muodon rakenteita ja kuvailla sitten, miten kyseiset rakenteet täytetään sovelluksessa olevilla tiedoilla ja algoritmeilla.</span><span class="sxs-lookup"><span data-stu-id="6a285-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in the application.</span></span> <span data-ttu-id="6a285-105">Lisätietoja on kohdassa [Sähköisen raportoinnin konfiguraatioiden luominen](electronic-reporting-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="6a285-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="6a285-106">Voit määrittää Finance and Operations -tietojen noutamiseen tarvittavan tietovirran ja sen avulla luotavan sähköisen asiakirjan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6a285-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="6a285-107">Sido määritetyt tietolähteet suunnitellun toimialuekohtaisen [tietomallin](general-electronic-reporting.md#data-model-and-model-mapping-components) elementteihin.</span><span class="sxs-lookup"><span data-stu-id="6a285-107">Bind configured data sources to elements of the designed domain-specific [data model](general-electronic-reporting.md#data-model-and-model-mapping-components).</span></span> <span data-ttu-id="6a285-108">Mallin rakenne ja valitut tietolähteet voivat olla osa monimutkaista hierarkkista rakennetta.</span><span class="sxs-lookup"><span data-stu-id="6a285-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="6a285-109">Tämän vuoksi lopulliset sidonnat voivat olla suuria ja niissä voi olla useita erityyppisiä elementtejä (kuten suhteita, tauluja ja menetelmiä).</span><span class="sxs-lookup"><span data-stu-id="6a285-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="6a285-110">Sidontojen luettavuus heikkenee ja niiden tarkistaminen ja ymmärtäminen voi olla hankalaa etenkin muille kuin omistajille.</span><span class="sxs-lookup"><span data-stu-id="6a285-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="6a285-111">Sitomalla tietomallin elementit [muodon](general-electronic-reporting.md#FormatComponentOutbound) osiin voit määrittää, mitkä tiedot täytetään tietomallista luodun muodon tulokseen.</span><span class="sxs-lookup"><span data-stu-id="6a285-111">Bind data model elements with [format](general-electronic-reporting.md#FormatComponentOutbound) components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="6a285-112">ER-yhdistämismääritysten suunnitteluohjelmien käytettävyyttä parantamaan on julkaistu [suhteellisen polun](er-formula-language.md#relative-path) ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="6a285-112">To improve usability of ER mapping designers, the [relative path](er-formula-language.md#relative-path) feature has been released.</span></span> <span data-ttu-id="6a285-113">Suhteellisen polun esitysvaihtoehto on oletusarvoisesti otettu käyttöön sovelluksen kaikissa uusissa esiintymissä, joissa ER-suunnittelukokemus on otettu käyttöön (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="6a285-113">By default, the relative path representation option is turned on for any new instance of the application where ER design experience is enabled (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="6a285-114">Suhteellisen polun parametri on toteutettu, jotta käyttäjät voivat jatkaa täydellisen polun käyttämistä, kun he käsittelevät ER-sidontojen tätä esitystä.</span><span class="sxs-lookup"><span data-stu-id="6a285-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="6a285-115">[![Käyttäjän parametrit](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="6a285-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="6a285-116">Kun suhteellisen polun käyttöparametri on otettu käyttöön, yksi @-merkki korvaa polun päänimikkeeseen nykyisen mallielementin sidonnassa.</span><span class="sxs-lookup"><span data-stu-id="6a285-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="6a285-117">Koko sidontapolku lyhenee, mikä selkeyttää koko yhdistämismääritystä ja helpottaa ymmärtämistä.</span><span class="sxs-lookup"><span data-stu-id="6a285-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="6a285-118">Useimmissa tapauksissa ER-suunnitteluohjelmassa ei tarvita erillistä vieritystä kaikkien tietomallin sidontojen näyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="6a285-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="6a285-119">[![Mallin yhdistämismäärityksen suunnitteluohjelma](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="6a285-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="6a285-120">Kun aloitat uuden ER-lausekkeen suunnittelun, tarvitset sidonnan määrittämiseen päänimikkeen kenttään vain yhden merkin.</span><span class="sxs-lookup"><span data-stu-id="6a285-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="6a285-121">[![Reseptien suunnittelu](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="6a285-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="6a285-122">Jos päätät muuttaa päämallinimikkeen tietolähdettä, absoluuttisessa polussa tämä mallinimike ja kaikki sisäkkäiset nimikkeet on sidottava uudelleen manuaalisesti uuteen tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="6a285-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="6a285-123">Kun suhteellisen polun käyttö on otettu käyttöön ja valitset uuden päänimikkeeseen sidottavan tietolähteen, saat mahdollisuuden sitoa kaikki päänimikkeen sisäkkäiset elementit automaattisesti uudelleen yhdellä napsautuksella.</span><span class="sxs-lookup"><span data-stu-id="6a285-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="6a285-124">[![Aiemmin luodun polun sanoman korvaaminen](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="6a285-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="6a285-125">Jos vahvistat sisäkkäisten nimikkeiden uudelleensidonnan, uusi päänimike sijoitetaan kunkin aiemmin luodun päänimikkeen sisältävän sisäkkäisen nimikkeen polkuun.</span><span class="sxs-lookup"><span data-stu-id="6a285-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="6a285-126">Tämä toiminto ei katkaise ER-kehyksen yhteensopivuutta aiempien versioiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="6a285-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="6a285-127">Kaikkia aiemmin suunniteltuja ER-määrityksiä voi käyttää tämän uuden toiminnon kanssa eikä päivityksiä tai muuntoja tarvita.</span><span class="sxs-lookup"><span data-stu-id="6a285-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="6a285-128">Kaikki muutokset, jotka otettiin käyttöön mallin yhdistämismääritysten sisäkkäisten elementtien sidontojen joukkomuokkauksella, tallennetaan oikein määrityksen muutostiedostoon (muutosten seurantaan).</span><span class="sxs-lookup"><span data-stu-id="6a285-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="6a285-129">Tällä tavoin asiakkaat voivat pohjustaa mallin yhdistämismääritysten johdetut versiot sen mihin tahansa uuteen perusversioon, jota on muokattu tällä uudella toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="6a285-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a285-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6a285-130">Additional resources</span></span>

[<span data-ttu-id="6a285-131">ER-kaavan kieli</span><span class="sxs-lookup"><span data-stu-id="6a285-131">ER formula language</span></span>](er-formula-language.md)
