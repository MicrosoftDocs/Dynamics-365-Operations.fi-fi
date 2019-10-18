---
title: Ylläpitoaikataulun kustannus
description: Tässä ohjeaiheessa kerrotaan ylläpitoaikataulun kustannuksista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b2f53a4a64b06efc9269c607bfe1fc3a41c90cdd
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922065"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="2b7cf-103">Ylläpitoaikataulun kustannus</span><span class="sxs-lookup"><span data-stu-id="2b7cf-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="2b7cf-104">Käyttöomaisuuden hallinnassa voit laskea ylläpitoaikataulurivien budjetoidut kustannukset.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="2b7cf-105">Tästä on hyötyä, jos haluat saada yleiskuvan odotetuista kustannuksista, esimerkiksi kustannukset, jotka liittyvät suunniteltuihin ennaltaehkäiseviin kunnossapitotöihin ensi vuodelle.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="2b7cf-106">Laskelmat perustuvat olemassa oleviin ylläpitoaikatauluriveihin, joiden tyyppi on "huoltosuunnitelmat" ja "ylläpitokierrokset" ja "ylläpitopyynnöt".</span><span class="sxs-lookup"><span data-stu-id="2b7cf-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="2b7cf-107">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Ylläpitoaikataulun kustannus**.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="2b7cf-108">**Ylläpitoaikataulun kustannus** -valintaikkunassa voit valita **Taloushallinnon dimensioyhdistelmä** -kohdan, jos haluat tarkastella taloushallinnon dimensioihin ryhmiteltyjä kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="2b7cf-109">Taloushallinnon dimensioyhdistelmät määritetään kohdassa **Kirjanpito** > **Tilikartta** > **Dimensiot** > **Taloushallinnon dimensioyhdistelmät.**</span><span class="sxs-lookup"><span data-stu-id="2b7cf-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="2b7cf-110">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia ylläpitoaikataulun riveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="2b7cf-111">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitoaikataulun rivit työtilaukset näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="2b7cf-112">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki ylläpitoaikataulun rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="2b7cf-113">Jos haluat määrittää tiettyjen resurssien laskennat, valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja valitse sitten haluamasi käyttöomaisuudet.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="2b7cf-114">Tarvittaessa voit myös määrittää kustannuslaskennalle **Odotettu alkamispäivämäärä** -kentän tai valita kustannuslaskennalle toisen **Tila**-kentän arvon.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="2b7cf-115">Aloita ksustannuslaskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="2b7cf-116">Valitse **Ylläpitoaikataulun kustannus** -välilehden toimintoruudun **Ryhmittely ...**  -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-116">On the **Maintenance schedule cost** tab > in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="2b7cf-117">Valitut toimintoruuturyhmän painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-117">The selected action pane group buttons are highlighted.</span></span> <span data-ttu-id="2b7cf-118">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="2b7cf-119">Valitse **Laske kustannus** -painike, jos haluat tehdä uuden kustannuslaskennan.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="2b7cf-120">Alla oleva kuva näyttää ylläpitoaikataulun kustannusten laskemisen tulokset.</span><span class="sxs-lookup"><span data-stu-id="2b7cf-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Kuva 1](media/17-preventive-maintenance.png)

