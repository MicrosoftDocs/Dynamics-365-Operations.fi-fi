---
title: Mukautetun tallennustilan sijaintien määrittäminen luoduille asiakirjoille
description: Tässä aiheessa käsitellään sähköisten raportointimuotojen (ER) muodostamien asiakirjojen tallennussijaintien luettelon laajentamista.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 362ac7f10cc61e26be89dfbae0e84745d42588a3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680755"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="c97ab-103">Mukautetun tallennustilan sijaintien määrittäminen luoduille asiakirjoille</span><span class="sxs-lookup"><span data-stu-id="c97ab-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c97ab-104">Sähköisen raportoinnin (ER) kehyksen ohjelmointirajapinnan avulla voit laajentaa ER-muotojen muodostamien asiakirjojen tallennussijaintien luetteloa.</span><span class="sxs-lookup"><span data-stu-id="c97ab-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="c97ab-105">Tässä aiheessa selitetään, kuinka voit lisätä mukautetun tallennussijainnin muodostetuille tiedostoille delegoimalla ER-sijaintien luontitehtävän oletusarvoiselle kohdetehtaalle ja toteuttamalla sen jälkeen mukautetun luokan, jolla on oma kohdelogiikkansa.</span><span class="sxs-lookup"><span data-stu-id="c97ab-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c97ab-106">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="c97ab-106">Prerequisites</span></span>

<span data-ttu-id="c97ab-107">Jatkuvaa koontia tukevan topologian ottaminen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="c97ab-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="c97ab-108">Lisätietoja on kohdassa [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="c97ab-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="c97ab-109">Sinulla on oltava tämän topologian käyttöoikeus yhdelle seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="c97ab-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="c97ab-110">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="c97ab-110">Electronic reporting developer</span></span>
- <span data-ttu-id="c97ab-111">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="c97ab-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="c97ab-112">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="c97ab-112">System administrator</span></span>

<span data-ttu-id="c97ab-113">Tarvitset myös tämän topologian kehitysympäristön käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="c97ab-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="c97ab-114">Kaikki tämän aiheen tehtävät voidaan suorittaa **USMF**-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="c97ab-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="c97ab-115">Tuo Kiinteiden resurssien eteenpäin siirtyvä ER-muoto</span><span class="sxs-lookup"><span data-stu-id="c97ab-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="c97ab-116">Voit luoda asiakirjat, jotka aiot lisätä mukautettuun varastosijaintiin [tuomalla](er-download-configurations-global-repo.md) **Kiinteiden resurssien eteenpäin siirtyvän** ER-muotomäärityksen nykyiseen topologiaan.</span><span class="sxs-lookup"><span data-stu-id="c97ab-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Konfiguraatiosäilön sivu](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="c97ab-118">Suorita Kiinteiden resurssien eteenpäin siirtyvä raportti</span><span class="sxs-lookup"><span data-stu-id="c97ab-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="c97ab-119">Siirry kohtaan **Kiinteät resurssit** \> **Tiedustelut ja raportit** \> **Tapahtumaraportit** \> **Kiinteiden resurssien eteenpäin siirtyvä**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="c97ab-120">Syötä **Alkamispäivä**-kenttään **1/1/2017** (1. tammikuuta 2017).</span><span class="sxs-lookup"><span data-stu-id="c97ab-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="c97ab-121">Syötä **Päättymispäivä**-kenttään **31/1/2017** (31. tammikuuta 2017).</span><span class="sxs-lookup"><span data-stu-id="c97ab-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="c97ab-122">Valitse **Valuuttakentässä** **Kirjanpitovaluutta**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="c97ab-123">Valitse **Muodon yhdistämismääritys**-kentässä **Kiinteiden resurssien eteenpäin siirtyvä**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="c97ab-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-124">Select **OK**.</span></span>

![Ajonaikainen dialogiruutu Kiinteiden resurssien eteenpäin siirtyvälle raportille](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="c97ab-126">Tarkista Microsoft Excelissä asiakirja, joka on luotu ja ladattavissa.</span><span class="sxs-lookup"><span data-stu-id="c97ab-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="c97ab-127">Tämä on [oletusarvoinen toimintatapa](electronic-reporting-destinations.md#default-behavior) ER-muodolle, jolle ei ole määritetty [kohteita](electronic-reporting-destinations.md) ja jota suoritetaan vuorovaikutteisessa tilassa.</span><span class="sxs-lookup"><span data-stu-id="c97ab-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="c97ab-128">Lähdekoodin tarkastelu</span><span class="sxs-lookup"><span data-stu-id="c97ab-128">Review the source code</span></span>

<span data-ttu-id="c97ab-129">Tarkastele `generateReportByGER()`-metodin koodia luokassa `AssetRollForwardService`.</span><span class="sxs-lookup"><span data-stu-id="c97ab-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="c97ab-130">Huomaa, että `Run()`-metodia käytetään ER-kehyksen kutsumiseen ja **Kiinteiden resurssien eteenpäin siirtyvän** raportin luomiseen.</span><span class="sxs-lookup"><span data-stu-id="c97ab-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="c97ab-131">Lähdekoodin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="c97ab-131">Modify the source code</span></span>

1. <span data-ttu-id="c97ab-132">Lisää Visual Studio -projektiisi uusi luokka (`AssetRollForwardDestination` tässä esimerkissä) ja kirjoita koodia toteuttaaksesi mukautetun kohteesi luoduille **Kiinteiden resurssien eteenpäin siirtyville** raporteille.</span><span class="sxs-lookup"><span data-stu-id="c97ab-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="c97ab-133">`new()`-metodi on suunniteltu hakemaan alkuperäinen ER-kohdeobjekti ja sovelluslogiikkavetoinen parametri, joka määrittää mukautetun kohteen, jonne luodut raportit tulisi tallentaa.</span><span class="sxs-lookup"><span data-stu-id="c97ab-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="c97ab-134">Tässä esimerkissä mukautettu sijainti on sen palvelimen paikallisen tiedostojärjestelmän kansion nimi, joka suorittaa Application Object Server (AOS)-palvelun.</span><span class="sxs-lookup"><span data-stu-id="c97ab-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="c97ab-135">`saveFile()`-metodi on suunniteltu tallentamaan luotu tiedosto AOS-palvelua suorittavan palvelimen paikallisen tiedostojärjestelmän kansioon.</span><span class="sxs-lookup"><span data-stu-id="c97ab-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="c97ab-136">Lisää Visual Studio -projektiisi uusi luokka (`AssetRollForwardDestinationFactory` tässä esimerkissä), ja kirjoita koodi määrittääksesi mukautetun kohdetehtaan, joka delegoi kohteen luomisen oletusarvoiselle kohdetehtaalle ja paketoidaksesi tiedostokohteen omalla kohteellasi.</span><span class="sxs-lookup"><span data-stu-id="c97ab-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="c97ab-137">Muokkaa aiemmin luotua `AssetRollForwardService`-luokkaa ja kirjoita koodi määrittääksesi mukautetun kohdetehtaan raportin suorittajalle.</span><span class="sxs-lookup"><span data-stu-id="c97ab-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="c97ab-138">Huomaa, että kun mukautettu kohdetehdas on muodostettu, kohdekansion määrittävä sovellusvetoinen parametri välitetään.</span><span class="sxs-lookup"><span data-stu-id="c97ab-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="c97ab-139">Näin kohd kansiota käytetään luotujen tiedostojen tallentamiseen.</span><span class="sxs-lookup"><span data-stu-id="c97ab-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="c97ab-140">Varmista, että määritetty kansio (**c:\\0** tässä esimerkissä) esiintyy AOS-palvelua suorittavan palvelimen paikallisessa tiedostojärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="c97ab-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="c97ab-141">Muussa tapauksessa suorituksen aikana ilmenee [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1)-poikkeus.</span><span class="sxs-lookup"><span data-stu-id="c97ab-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="c97ab-142">Muodosta projekti uudelleen.</span><span class="sxs-lookup"><span data-stu-id="c97ab-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="c97ab-143">Suorita Kiinteiden resurssien eteenpäin siirtyvä raportti uudelleen</span><span class="sxs-lookup"><span data-stu-id="c97ab-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="c97ab-144">Siirry kohtaan **Kiinteät resurssit** \> **Tiedustelut ja raportit** \> **Tapahtumaraportit** \> **Kiinteiden resurssien eteenpäin siirtyvä**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="c97ab-145">Syötä **Alkamispäivä**-kenttään arvo **1/1/2017**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="c97ab-146">Syötä **Päättymispäivä**-kenttään arvo **31/1/2017**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="c97ab-147">Valitse **Valuuttakentässä** **Kirjanpitovaluutta**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="c97ab-148">Valitse **Muodon yhdistämismääritys**-kentässä **Kiinteiden resurssien eteenpäin siirtyvä**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="c97ab-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c97ab-149">Select **OK**.</span></span>
7. <span data-ttu-id="c97ab-150">Selaa paikallista **C:\\0**-kansiota löytääksesi muodostetun tiedoston.</span><span class="sxs-lookup"><span data-stu-id="c97ab-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="c97ab-151">Koska `originDestination`-objektia ei käytetä `AssetRollForwardDestination`-objektissa tässä esimerkissä, ER-muoto [kohteet](electronic-reporting-destinations.md) ohitetaan suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="c97ab-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c97ab-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c97ab-152">Additional resources</span></span>

- [<span data-ttu-id="c97ab-153">Sähköisen raportoinnin (ER) kohteet</span><span class="sxs-lookup"><span data-stu-id="c97ab-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="c97ab-154">Laajennettavuuden kotisivu</span><span class="sxs-lookup"><span data-stu-id="c97ab-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
