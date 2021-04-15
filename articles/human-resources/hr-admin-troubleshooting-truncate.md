---
title: Tekstin katkaisun välttäminen toimihierarkiassa ja Visio-viennissä
description: Tässä artikkelissa kerrotaan, miten voi ratkaista henkilöiden ja toimien nimien katkaisemisongelman, kun asiakkaat tarkastelevat toimihierarkiaa Microsoft Dynamics 365 Human Resourcesissa. Tekstin katkaisemisen voi vaikeuttaa näyttökuvan ottamista hierarkiasta tai sen tulostamista.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f8310def6f33b807f7f749e659432e482245d007
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803870"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="f1057-104">Tekstin katkaisemisen välttäminen toimihierarkiassa ja vienti Visioon</span><span class="sxs-lookup"><span data-stu-id="f1057-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f1057-105">**Varasto-otto**</span><span class="sxs-lookup"><span data-stu-id="f1057-105">**Issue**</span></span>

<span data-ttu-id="f1057-106">Kun asiakas tarkastelee, toimihierarkiaa Microsoft Dynamics 365 Human Resourcesissa, henkilöiden ja toimien nimet on katkaistu.</span><span class="sxs-lookup"><span data-stu-id="f1057-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="f1057-107">Tämän vuoksi näyttökuvan ottaminen hierarkiasta tai hierarkian tulostaminen jakamista varten voi olla hankalaa.</span><span class="sxs-lookup"><span data-stu-id="f1057-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Toimihierarkia](media/position-h.png)

<span data-ttu-id="f1057-109">**Syy**</span><span class="sxs-lookup"><span data-stu-id="f1057-109">**Cause**</span></span>

<span data-ttu-id="f1057-110">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="f1057-110">This behavior is by design.</span></span>

<span data-ttu-id="f1057-111">**Tarkkuus**</span><span class="sxs-lookup"><span data-stu-id="f1057-111">**Resolution**</span></span>

<span data-ttu-id="f1057-112">Tekstin koon muuttaminen ei valitettavasti ole yksinkertaista.</span><span class="sxs-lookup"><span data-stu-id="f1057-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="f1057-113">Voit kuitenkin viedä toimihierarkian Human Resourcesista ja tuoda sen Microsoft Visioon.</span><span class="sxs-lookup"><span data-stu-id="f1057-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="f1057-114">Vaikka seuraava artikkeli kirjoitettiin Microsoft Dynamics AX 2012:ta varten, samaa prosessia käytetään Human Resourcesissa: [Toimihierarkian vieminen Microsoft Visioon](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="f1057-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="f1057-115">Vie hierarkia Visioon seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f1057-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="f1057-116">Avaa Human Resourcesissa **Toimet**-luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="f1057-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="f1057-117">Jos haluat sisällyttää muita tietoja organisaation rakennekaavioon, lisää kenttiä **Toimet**-luetteloon. jotta ne ovat käytettävissä, kun käytät ohjattua toimintoa myöhemmin tämän menettelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="f1057-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="f1057-118">Valitse toimintoruudussa ensin **Avaa Microsoft Officessa** -painike ja sitten **Vie Exceliin** -kohdassa **Toimet**.</span><span class="sxs-lookup"><span data-stu-id="f1057-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="f1057-119">Voit vaihtoehtoisesti painaa näppäinyhdistelmää Ctrl+T.</span><span class="sxs-lookup"><span data-stu-id="f1057-119">Alternatively, press Ctrl+T.</span></span>

    ![Toimet-luettelosivun vieminen Exceliin](media/org-admin.png)

3. <span data-ttu-id="f1057-121">Tallenna viety Excel-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="f1057-121">Save the Excel file that is exported.</span></span>

    ![Vie Exceliin -valintaikkuna](media/export-excel.png)

4. <span data-ttu-id="f1057-123">Valitse Visiossa ensin **Visio - Luo uusi** ja sitten **Yritys**-malliluokka.</span><span class="sxs-lookup"><span data-stu-id="f1057-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Uusi kaavio](media/new.png)

5. <span data-ttu-id="f1057-125">Valitse ensin **organisaatiokaavion ohjattu toiminto** ja sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="f1057-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Organisaatiokaavion ohjatun toiminnon valintaikkuna](media/orgchart-wizard.png)

6. <span data-ttu-id="f1057-127">Valitse ensin **Tiedostoon tai tietokantaan jo tallennetut tiedot** ja sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="f1057-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Organisaatiokaavion ohjattu toiminto 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="f1057-129">Valitse ensin **Teksti-, Org Plus (\*.txt)- tai Excel-tiedosto** ja sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="f1057-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Organisaatiokaavion ohjattu toiminto 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="f1057-131">Siirry toimihierarkian sisältävään Excel-tiedostoon, valitse se ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="f1057-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Organisaatiokaavion ohjattu toiminto 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="f1057-133">Määritä **Nimi**-kentän arvoksi **Toimi** ja **Raportoi:**-kentän arvoksi **Raportoi toimella**. Valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="f1057-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Organisaatiokaavion ohjattu toiminto 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="f1057-135">Valitse kussakin solmussa näytettävät kentät ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="f1057-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Organisaatiokaavion ohjattu toiminto 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="f1057-137">Lisää **Toimi**-sarake **Muokkaa tietokenttien muotoa** -luetteloon ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="f1057-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Organisaatiokaavion ohjattu toiminto 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="f1057-139">Kuvia ei ole tällä hetkellä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f1057-139">Pictures aren't currently available.</span></span> <span data-ttu-id="f1057-140">Valitse tämän vuoksi seuraavalla sivulla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="f1057-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="f1057-141">Valitse **Haluan, että ohjattu toiminto jakaa organisaatiokaavio automaattisesti sivuille**.</span><span class="sxs-lookup"><span data-stu-id="f1057-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Organisaatiokaavion ohjattu toiminto 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="f1057-143">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="f1057-143">Select **Finish**.</span></span>

    <span data-ttu-id="f1057-144">Jos jotkin toimet eivät ole rakenteessa, sinua pyydetään sisällyttämään ne kaavioon.</span><span class="sxs-lookup"><span data-stu-id="f1057-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="f1057-145">Visiossa muodostettavassa kaaviossa jokainen esimies näkyy erillisessä laskentataulukossa.</span><span class="sxs-lookup"><span data-stu-id="f1057-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="f1057-146">Kun Visio-tiedosto luodaan, kussakin solmussa näkyvät ne tiedot, jotka perustuvat kaavioon sisällytettäväksi valittuihin kenttiin.</span><span class="sxs-lookup"><span data-stu-id="f1057-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hierarkiakaavio](media/hierarchy.png)

<span data-ttu-id="f1057-148">**Lisäasetus**</span><span class="sxs-lookup"><span data-stu-id="f1057-148">**Additional option**</span></span>

<span data-ttu-id="f1057-149">Human Resourcesissa joitakin hierarkiaan liittyviä tietoja voi olla mahdollista katsoa **Ihmiset**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="f1057-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]