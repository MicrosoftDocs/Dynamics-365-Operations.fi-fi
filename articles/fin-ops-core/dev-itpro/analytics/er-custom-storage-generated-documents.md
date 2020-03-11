---
title: Mukautetun tallennussijainnin määrittäminen luoduille asiakirjoille
description: Tässä ohjeaiheessa käsitellään sähköisten raportointimuotojen muodostamien asiakirjojen tallennussijaintiluettelon laajentamista.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 98c08ae2ab4c7cceadb6caaf98fa431e56be4b97
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042731"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="db797-103">Mukautetun tallennussijainnin määrittäminen luoduille asiakirjoille</span><span class="sxs-lookup"><span data-stu-id="db797-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="db797-104">Sähköisen raportoinnin (ER) kehyksen ohjelmointirajapinnan avulla voit laajentaa ER-muotojen muodostamien asiakirjojen tallennussijaintien luetteloa.</span><span class="sxs-lookup"><span data-stu-id="db797-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="db797-105">Tässä ohjeaiheessa on niiden päätehtävien yleiskatsaus, jotka on tehtävä, jotta mukautettu tallennussijainti voidaan lisätä.</span><span class="sxs-lookup"><span data-stu-id="db797-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="db797-106">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="db797-106">Prerequisites</span></span>

<span data-ttu-id="db797-107">Käyttöön on otettava jatkuvaa koontia tukeva topologia.</span><span class="sxs-lookup"><span data-stu-id="db797-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="db797-108">(Lisätietoja on kohdassa [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Sinulla on oltava tämän topologian käyttöoikeus jollakin seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="db797-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="db797-109">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="db797-109">Electronic reporting developer</span></span>
- <span data-ttu-id="db797-110">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="db797-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="db797-111">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="db797-111">System administrator</span></span>

<span data-ttu-id="db797-112">Tarvitset myös tämän topologian kehitysympäristön käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="db797-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="db797-113">ER-muotokokoonpanon luonti tai tuonti</span><span class="sxs-lookup"><span data-stu-id="db797-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="db797-114">[Luo uusi ER-muoto](tasks/er-format-configuration-2016-11.md) nykyisessä topologiassa ja muodosta asiakirjoja, joille aiot lisätä mukautetun tallennussijainnin.</span><span class="sxs-lookup"><span data-stu-id="db797-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="db797-115">Vaihtoehtoisesti voit [tuoda aiemmin luodun ER-muodon tähän topologiaan](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="db797-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Muodon suunnittelutoiminto -sivu](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="db797-117">Luotavassa tai tuotavassa ER-muodossa on oltava vähintään yksi seuraavista muotoelementeistä:</span><span class="sxs-lookup"><span data-stu-id="db797-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="db797-118">Tiedosto</span><span class="sxs-lookup"><span data-stu-id="db797-118">File</span></span>
> - <span data-ttu-id="db797-119">Kansio</span><span class="sxs-lookup"><span data-stu-id="db797-119">Folder</span></span>
> - <span data-ttu-id="db797-120">Yhdistystoiminto</span><span class="sxs-lookup"><span data-stu-id="db797-120">Merger</span></span>
> - <span data-ttu-id="db797-121">Liite</span><span class="sxs-lookup"><span data-stu-id="db797-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="db797-122">Uuden tiedostotyypin luominen</span><span class="sxs-lookup"><span data-stu-id="db797-122">Create a new document type</span></span>

<span data-ttu-id="db797-123">ER-muodon luomien asiakirjojen reitityksen määrittämistä varten on määritettävä [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="db797-123">To specify how documents that an ER format generates are routed, you must configure [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="db797-124">Jokaisessa ER-kohteessa, joka on määritetty tallentamaan muodostetut asiakirjat tiedostoina, on määritettävä tiedoston hallintakehyksen asiakirjatyyppi.</span><span class="sxs-lookup"><span data-stu-id="db797-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="db797-125">Eri asiakirjatyyppejä voidaan käyttää reitittämään eri ER-muotojen muodostamia asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="db797-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="db797-126">Lisää aiemmin luodulle tai tuodulle ER-muodolle uusi [asiakirjatyyppi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management).</span><span class="sxs-lookup"><span data-stu-id="db797-126">Add a new [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="db797-127">Seuraavassa kuvassa asiakirjan tyyppi on **FileX**.</span><span class="sxs-lookup"><span data-stu-id="db797-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="db797-128">Voit erottaa tämän asiakirjatyypin muista asiakirjatyypeistä sisällyttämällä tietyn avainsanan sen nimeen.</span><span class="sxs-lookup"><span data-stu-id="db797-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="db797-129">Esimerkiksi seuraavassa kuvassa nimi on **(PAIKALLINEN) kansio**.</span><span class="sxs-lookup"><span data-stu-id="db797-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="db797-130">Määritä **Luokka**-kentässä **Liitä tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="db797-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="db797-131">Määritä **Ryhmä**-kentässä **Tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="db797-131">In the **Group** field, specify **File**.</span></span>

![Asiakirjatyypit-sivu](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="db797-133">Asiakirjatyypit ovat yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="db797-133">Document types are company-specific.</span></span> <span data-ttu-id="db797-134">Jos haluat käyttää ER-muotoa, jossa on määritetty kohde, useissa yrityksissä, kullekin yritykselle on määritettävä oma asiakirjatyyppi.</span><span class="sxs-lookup"><span data-stu-id="db797-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="db797-135">Lähdekoodin tarkastelu</span><span class="sxs-lookup"><span data-stu-id="db797-135">Review source code</span></span>

<span data-ttu-id="db797-136">Tarkastele **ERDocuManagement**-luokan **insertFile()**-menetelmän koodia.</span><span class="sxs-lookup"><span data-stu-id="db797-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="db797-137">Huomaa, että **AttachingFile()**-tapahtuma muodostetaan, kun muodostettua tiedostoa liitetään tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="db797-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="db797-138">**AttachingFile()**-tapahtuma muodostetaan, kun seuraavat ER-kohteet käsitellään:</span><span class="sxs-lookup"><span data-stu-id="db797-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="db797-139">**Arkisto** – Kun tätä kohdetta käytetään, suoritettavan ER-muodon uusi tietue luodaan ERFormatMappingRunJobTable-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="db797-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="db797-140">Tämän tietueen **Arkistoitu**-kentän arvoksi määritetään **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="db797-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="db797-141">Jos ER-muodon suorittaminen onnistuu, muodostettu asiakirja liitetään tähän tietueeseen ja **AttachingFile()**-tapahtuma muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="db797-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="db797-142">Tässä ER-kohteessa valittu asiakirjatyyppi määrittää liitetyn tiedoston tallennussijainnin (Microsoft Azuren tallennus tai Microsoft SharePoint -kansio).</span><span class="sxs-lookup"><span data-stu-id="db797-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="db797-143">**Työarkisto** – Kun tätä kohdetta käytetään, suoritettavan ER-muodon uusi tietue luodaan ERFormatMappingRunJobTable-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="db797-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="db797-144">Tämän tietueen **Arkistoitu**-kentän arvoksi määritetään **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="db797-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="db797-145">Jos ER-muodon suorittaminen onnistuu, muodostettu asiakirja liitetään tähän tietueeseen ja **AttachingFile()**-tapahtuma muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="db797-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="db797-146">ER-parametreissa määritetty asiakirjatyyppi määrittää liitetyn tiedoston tallennussijainnin (Azuren tallennus tai SharePoint-kansio).</span><span class="sxs-lookup"><span data-stu-id="db797-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Sähköisen raportoinnin parametrit -sivu](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="db797-148">ER-kohteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="db797-148">Configure an ER destination</span></span>

1. <span data-ttu-id="db797-149">Määritä luodun tai tuodun ER-muodon yhden edellä mainitun elementin (tiedosto, kansio, yhdistämistoiminto tai liite) arkistokohde.</span><span class="sxs-lookup"><span data-stu-id="db797-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="db797-150">Lisätietoja on kohdassa [ER Kohteiden määrittäminen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="db797-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="db797-151">Käytä asiakirjatyyppiä, jonka lisäsit määritetylle kohteelle aiemmin.</span><span class="sxs-lookup"><span data-stu-id="db797-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="db797-152">(Tämä ohjeaiheen esimerkissä asiakirjatyyppi on **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="db797-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Kohdeasetukset-valintaikkuna](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="db797-154">Lähdekoodin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="db797-154">Modify source code</span></span>

1. <span data-ttu-id="db797-155">Lisää uusi luokka Microsoft Visual Studio -projektiin ja kirjoita koodi, joka tilaa aiemmin mainitun **AttachingFile()**-tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="db797-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="db797-156">(Lisätietoja käytettävästä laajennettavuusmallista on kohdassa [Vastaaminen käyttämällä kohdetta EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Kirjoita esimerkiksi uudessa luokassa koodia, joka suorittaa seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="db797-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="db797-157">Tallenna muodostetut tiedostot sen palvelimen paikallisen tiedostojärjestelmän kansioon, joka suorittaa Application Object Server (AOS) -palvelun.</span><span class="sxs-lookup"><span data-stu-id="db797-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="db797-158">Tallenna muodostetut tiedostot vain, kun uutta asiakirjatyyppiä (kuten **FileX**-tyyppi, jonka nimessä on avainsana (PAIKALLINEN)) käytetään liitettäessä tiedostoa tietueeseen ER-suoritustyölokissa.</span><span class="sxs-lookup"><span data-stu-id="db797-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="db797-159">Muodosta projekti uudelleen.</span><span class="sxs-lookup"><span data-stu-id="db797-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="db797-160">Luodun tai tuodun ER-muodon suorittaminen</span><span class="sxs-lookup"><span data-stu-id="db797-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="db797-161">Suorita luotu tai tuotu ER-muoto.</span><span class="sxs-lookup"><span data-stu-id="db797-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="db797-162">Valitse **Organisaation hallinto \> Sähköinen raportointi \> Sähköisen raportoinnin työt**.</span><span class="sxs-lookup"><span data-stu-id="db797-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="db797-163">Etsi tälle suoritustyölle luotu tietue, johon on liitetty muodostettu tiedosto.</span><span class="sxs-lookup"><span data-stu-id="db797-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="db797-164">Etsi sama muodostettu tiedosto paikallisesta **C:\\0**-kansiosta.</span><span class="sxs-lookup"><span data-stu-id="db797-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db797-165">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="db797-165">Additional resources</span></span>

- [<span data-ttu-id="db797-166">Sähköisen raportoinnin (ER) kohteet</span><span class="sxs-lookup"><span data-stu-id="db797-166">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="db797-167">Laajennettavuuden kotisivu</span><span class="sxs-lookup"><span data-stu-id="db797-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
