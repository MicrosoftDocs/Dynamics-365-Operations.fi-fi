---
title: Tietojen tuonti useita laskentataulukkoja sisältävistä Excelin tietoyksikkömalleista
description: Tässä ohjeaiheessa käsitellään tietojen tuontia Finance and Operationsiin Excelin tietoyksikkömallien avulla.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 618b62364353f409f6971ddd9adc7d55297d09cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688076"
---
# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a><span data-ttu-id="980e1-103">Tietojen tuonti useita laskentataulukkoja sisältävistä Excelin tietoyksikkömalleista</span><span class="sxs-lookup"><span data-stu-id="980e1-103">Import data from Excel data entity templates that have multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="980e1-104">Sovelluksen tietojen hallinta tukee tietoyksiköiden Microsoft Excel -pohjaisia malleja.</span><span class="sxs-lookup"><span data-stu-id="980e1-104">Data management in the application supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="980e1-105">Näissä malleissa voi olla yksi laskentataulukko tai useita laskentataulukkoja.</span><span class="sxs-lookup"><span data-stu-id="980e1-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="980e1-106">Useita laskentataulukkoja sisältäviä malleja käytetään usein, kun tietoja halutaan hallita yhdessä tiedostossa, joka voidaan vielä useisiin tietoyksiköihin.</span><span class="sxs-lookup"><span data-stu-id="980e1-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="980e1-107">Esimerkki: toimipaikat ja varastot.</span><span class="sxs-lookup"><span data-stu-id="980e1-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="980e1-108">Kerran ladatun tiedoston yhdistämiseen kaikkiin yksiköihin</span><span class="sxs-lookup"><span data-stu-id="980e1-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="980e1-109">Esimerkkinä voisi olla tilanne, jossa yhdessä Excel-tiedostossa on **Toimipaikat**- ja **Varastot**-nimiset laskentataulukot.</span><span class="sxs-lookup"><span data-stu-id="980e1-109">Let's take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="980e1-110">Voit määrittää tietojen tuontiprojektin lisäämällä ensimmäisen tietoyksikön, **Toimipaikat**, lataamalla tiedosto sitten.</span><span class="sxs-lookup"><span data-stu-id="980e1-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="980e1-111">Voit valita **Toimipaikat** tässä yksikössä käytettäväksi laskentataulukoksi.</span><span class="sxs-lookup"><span data-stu-id="980e1-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="980e1-112">Jos lisäät toisen yksikön, **Varastot**, lähtemättä **Lisää tiedosto** -lomakkeesta, laskentataulukkohaku antaa valita **Varasto**-laskentataulukon ilman, että tiedosto on ladattava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="980e1-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="980e1-113">Uusi tiedosto tarvitsisi ladata vain, jos **Varastot**-tiedot olisivat eri tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="980e1-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Useita laskentataulukoita](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="980e1-115">Laskentataulukon korjaaminen yksikön yhdistämismääritykseen</span><span class="sxs-lookup"><span data-stu-id="980e1-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="980e1-116">Laskentataulukon yhdistämismääritys tuontityön tietoyksikköön voidaan korjata ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="980e1-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="980e1-117">Ruudukon **Laskentataulukko**-sarake sisältää yhdistetyn tiedoston laskentataulukot.</span><span class="sxs-lookup"><span data-stu-id="980e1-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="980e1-118">Voit valita toisen laskentataulukon avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="980e1-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="980e1-119">Jos valittu laskentataulukko on jo yhdistetty yksikköön tietoprojektissa, järjestelmä pyytää vahvistamaan muutoksen.</span><span class="sxs-lookup"><span data-stu-id="980e1-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="980e1-120">Kaikki yhdistämismääritykset kannattaa korjata ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="980e1-120">We recommend that you fix all mappings in the grid.</span></span>

![Laskentataulukon yhdistämispäivityksen päivitys](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="980e1-122">Uudelleenyhdistäminen uuteen tiedostoon</span><span class="sxs-lookup"><span data-stu-id="980e1-122">Re-map to a new file</span></span>

<span data-ttu-id="980e1-123">Jos saman tiedoston uusi versio tai täysin uusi tiedosto on ladattava tietoprojektin aiemmin luotuihin yksiköihin, on käytettävä **Lisää tiedosto** -vaihtoehtoa ja yksiköt on lisättävä uudelleen aivan kuin ne lisättäisiin ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="980e1-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="980e1-124">Järjestelmä vahvistaa ennen jatkamista, että haluat korvata tietoprojektin aiemmin luodut yksiköt.</span><span class="sxs-lookup"><span data-stu-id="980e1-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="980e1-125">Yksiköt, joita ei ole lisätty uudelleen (tai korjattu), sisältävät edelleen edellisestä tiedostosta tehdyt aiemmat yhdistämismääritykset.</span><span class="sxs-lookup"><span data-stu-id="980e1-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="980e1-126">Tiedoston lataaminen Suorita projekti -toiminnolla</span><span class="sxs-lookup"><span data-stu-id="980e1-126">Upload a file using Run project</span></span>

<span data-ttu-id="980e1-127">Voit ladata Excel-tiedoston samalla, kun tuot projektin **Suorita projektit** -asetuksella.</span><span class="sxs-lookup"><span data-stu-id="980e1-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="980e1-128">Ole huolellinen ja lataa vain tiedostot, joissa on samat laskentataulukot kuin tietoprojektin tietoyksiköiden aiemmin luoduissa yhdistämismäärityksissä.</span><span class="sxs-lookup"><span data-stu-id="980e1-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="980e1-129">Jos laskentataulukkoa ei ole juuri ladatussa tiedostossa, järjestelmä ilmoittaa virheestä ja lopettaa tuonnin.</span><span class="sxs-lookup"><span data-stu-id="980e1-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="980e1-130">Jos yhdistämistä laskentataulukkoon on muutettava yksikössä, tietoprojektin yhdistämismääritykset on ensin päivitettävä tietoprojektissa ennen **Suorita projekti** -toiminnon käyttöä tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="980e1-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>
