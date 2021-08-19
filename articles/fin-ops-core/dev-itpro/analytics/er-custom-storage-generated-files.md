---
title: Mukautetun tallennustilan sijaintien määrittäminen luoduille asiakirjoille
description: Tässä aiheessa käsitellään sähköisten raportointimuotojen (ER) muodostamien asiakirjojen tallennussijaintien luettelon laajentamista.
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 83b2d3c35e3e68aaad22bc03a46b17abc1526073895057717fd055dacdfbee5c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718474"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Mukautetun tallennustilan sijaintien määrittäminen luoduille asiakirjoille

[!include[banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) kehyksen ohjelmointirajapinnan avulla voit laajentaa ER-muotojen muodostamien asiakirjojen tallennussijaintien luetteloa. Tässä aiheessa selitetään, kuinka voit lisätä mukautetun tallennussijainnin muodostetuille tiedostoille delegoimalla ER-sijaintien luontitehtävän oletusarvoiselle kohdetehtaalle ja toteuttamalla sen jälkeen mukautetun luokan, jolla on oma kohdelogiikkansa.

## <a name="prerequisites"></a>Edellytykset

Jatkuvaa koontia tukevan topologian ottaminen käyttöön. Lisätietoja on kohdassa [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Sinulla on oltava tämän topologian käyttöoikeus yhdelle seuraavista rooleista:

- Sähköisen raportoinnin kehittäjä
- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

Tarvitset myös tämän topologian kehitysympäristön käyttöoikeuden.

Kaikki tämän aiheen tehtävät voidaan suorittaa **USMF**-yrityksessä.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Tuo Kiinteiden resurssien eteenpäin siirtyvä ER-muoto

Voit luoda asiakirjat, jotka aiot lisätä mukautettuun varastosijaintiin [tuomalla](er-download-configurations-global-repo.md) **Kiinteiden resurssien eteenpäin siirtyvän** ER-muotomäärityksen nykyiseen topologiaan.

![Konfiguraatiosäilön sivu.](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Suorita Kiinteiden resurssien eteenpäin siirtyvä raportti

1. Siirry kohtaan **Kiinteät resurssit** \> **Tiedustelut ja raportit** \> **Tapahtumaraportit** \> **Kiinteiden resurssien eteenpäin siirtyvä**.
2. Syötä **Alkamispäivä**-kenttään **1/1/2017** (1. tammikuuta 2017).
3. Syötä **Päättymispäivä**-kenttään **31/1/2017** (31. tammikuuta 2017).
4. Valitse **Valuuttakentässä** **Kirjanpitovaluutta**.
5. Valitse **Muodon yhdistämismääritys**-kentässä **Kiinteiden resurssien eteenpäin siirtyvä**.
6. Valitse **OK**.

![Ajonaikainen dialogiruutu Kiinteiden resurssien eteenpäin siirtyvä -raportille.](./media/er-custom-storage-generated-files-runtime-dialog.png)

Tarkista Microsoft Excelissä asiakirja, joka on luotu ja ladattavissa. Tämä on [oletusarvoinen toimintatapa](electronic-reporting-destinations.md#default-behavior) ER-muodolle, jolle ei ole määritetty [kohteita](electronic-reporting-destinations.md) ja jota suoritetaan vuorovaikutteisessa tilassa.

## <a name="review-the-source-code"></a>Lähdekoodin tarkastelu

Tarkastele `generateReportByGER()`-metodin koodia luokassa `AssetRollForwardService`. Huomaa, että `Run()`-metodia käytetään ER-kehyksen kutsumiseen ja **Kiinteiden resurssien eteenpäin siirtyvän** raportin luomiseen.

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

## <a name="modify-the-source-code"></a>Lähdekoodin muokkaaminen

1. Lisää Visual Studio -projektiisi uusi luokka (`AssetRollForwardDestination` tässä esimerkissä) ja kirjoita koodia toteuttaaksesi mukautetun kohteesi luoduille **Kiinteiden resurssien eteenpäin siirtyville** raporteille.

    - `new()`-metodi on suunniteltu hakemaan alkuperäinen ER-kohdeobjekti ja sovelluslogiikkavetoinen parametri, joka määrittää mukautetun kohteen, jonne luodut raportit tulisi tallentaa. Tässä esimerkissä mukautettu sijainti on sen palvelimen paikallisen tiedostojärjestelmän kansion nimi, joka suorittaa Application Object Server (AOS)-palvelun.
    - `saveFile()`-metodi on suunniteltu tallentamaan luotu tiedosto AOS-palvelua suorittavan palvelimen paikallisen tiedostojärjestelmän kansioon.

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

2. Lisää Visual Studio -projektiisi uusi luokka (`AssetRollForwardDestinationFactory` tässä esimerkissä), ja kirjoita koodi määrittääksesi mukautetun kohdetehtaan, joka delegoi kohteen luomisen oletusarvoiselle kohdetehtaalle ja paketoidaksesi tiedostokohteen omalla kohteellasi.

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

3. Muokkaa aiemmin luotua `AssetRollForwardService`-luokkaa ja kirjoita koodi määrittääksesi mukautetun kohdetehtaan raportin suorittajalle. Huomaa, että kun mukautettu kohdetehdas on muodostettu, kohdekansion määrittävä sovellusvetoinen parametri välitetään. Näin kohd kansiota käytetään luotujen tiedostojen tallentamiseen.

    > [!NOTE] 
    > Varmista, että määritetty kansio (**c:\\0** tässä esimerkissä) esiintyy AOS-palvelua suorittavan palvelimen paikallisessa tiedostojärjestelmässä. Muussa tapauksessa suorituksen aikana ilmenee [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1)-poikkeus.

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

4. Muodosta projekti uudelleen.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Suorita Kiinteiden resurssien eteenpäin siirtyvä raportti uudelleen

1. Siirry kohtaan **Kiinteät resurssit** \> **Tiedustelut ja raportit** \> **Tapahtumaraportit** \> **Kiinteiden resurssien eteenpäin siirtyvä**.
2. Syötä **Alkamispäivä**-kenttään arvo **1/1/2017**.
3. Syötä **Päättymispäivä**-kenttään arvo **31/1/2017**.
4. Valitse **Valuuttakentässä** **Kirjanpitovaluutta**.
5. Valitse **Muodon yhdistämismääritys**-kentässä **Kiinteiden resurssien eteenpäin siirtyvä**.
6. Valitse **OK**.
7. Selaa paikallista **C:\\0**-kansiota löytääksesi muodostetun tiedoston.

> [!NOTE]
> Koska `originDestination`-objektia ei käytetä `AssetRollForwardDestination`-objektissa tässä esimerkissä, ER-muoto [kohteet](electronic-reporting-destinations.md) ohitetaan suorituksen aikana.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)
- [Laajennettavuuden kotisivu](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]