---
title: Talousraportoinnin tietovaraston osajoukon palauttaminen
description: "Tässä ohjeaiheessa kerrotaan, miten talousraportoinnin tietovaraston osajoukko palautetaan."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Talousraportoinnin tietovaraston osajoukon palauttaminen

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten seuraavien versioiden talousraportoinnin tietovaraston osajoukko palautetaan:

- Microsoft Dynamics 365 for Finance and Operations: Taloushallinnon raportoinnin versio 7.2.6.0 ja uudempi
- Microsoft Dynamics 365 for Finance and Operations: Taloushallinnon raportoinnin versio 7.0.10000.4 ja uudempi
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (paikallinen)

Saat Finance and Operationsin taloushallinnon raportoinnin version 7.2.6.0, kun lataat KB-artikkelin 4052514 osoitteesta <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Finance and Operationsin taloushallinnon raportoinnin version 7.2.6.0 ja uudemman version talousraportoinnin tietovaraston osajoukon palauttaminen

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Talousraportoinnin tietovaraston osajoukon palauttaminen raportin suunnittelutoiminnosta

> [!NOTE]
> Tämän prosessin vaiheita tuetaan Finance and Operationsin taloushallinnon raportoinnin versiossa 7.2.6.0 ja uudemmissa versioissa. Jos käytössä on aiempi versio, ota yhteys tukitiimiin.

Tietyissä skenaarioissa talousraportoinnin tietovaraston osajoukko on ehkä palautettava. Tämä tehtävä voidaan tehdä raportin suunnitteluohjelman käyttöliittymässä. Seuraavassa on joitakin skenaarioita, joissa tietovaraston osajoukko on ehkä palautettava:

- Finance and Operations -tietokanta on palautettu, mutta tietovaraston osajoukkoa ei.
- Kauden tiedot ovat virheelliset.
- Tuki kehottaa palauttamaan tietovaraston osajoukon vianmääritysvaiheen osana.

Tietovaraston osajoukon palautus on tehtävä ajankohtana, jona tietokannassa ei käsitellä paljon tietoja. Taloushallinnon raportointi ei ole käytettävissä palautusprosessin aikana.

#### <a name="reset-the-data-mart"></a>Tietovaraston osajoukon palauttaminen

Voit palauttaa tietovaraston osajoukon valitsemalla raportin suunnitteluohjelman **Työkalut**-valikossa **Palauta tietovaraston osajoukko**. Esiin tulevassa valintaikkunassa on kaksi osaa: **Tilastotiedot** ja **Palauta**.

[![Palauta tietovaraston osajoukko -valintaikkuna](./media/Reset-72.jpg)](./media/Reset-72.jpg)

##### <a name="integration-attempts"></a>Integrointiyritykset

**Integrointiyritykset**-ruudukossa on tieto siitä, miten monta kertaa järjestelmä on yrittänyt integroida tapahtumia. Järjestelmä yrittää integroida tietoja tiettyjen päivien ajan, jos ensimmäiset yritykset eivät onnistu. Tiedät, että tietovaraston osajoukko on palautettava, jos yritysten määrä on 8 tai yli ja jos dimensioyhdistelmiä tai tapahtumatietueita on useita. Tässä tapauksessa tietoja ei raportoida.

##### <a name="data-status"></a>Tietojen tila

**Tietojen tila** -ruudukossa on tietovaraston osajoukon tapahtumien, valuuttakurssien ja dimensioiden arvojen tilannevedos. Jos käyttämättömiä tietueita on paljon, tietueita on luultavasti päivitetty useita kertoja. Tämän vuoksi raporttien luonti voi hidastua.

##### <a name="misaligned-main-account-categories"></a>Kohdistamattomat päätililuokat

Jos käytössä on Microsoft Dynamics 365 for Finance and Operationsin taloushallinnon raportoinnin versiota 7.2.1 aiempi versio, tietovaraston osajoukko on ehkä palautettava, jos annat tileille uudet nimet ja siirrät tilejä tililuokasta toiseen. Näiden toimintojen vuoksi päätililuokista voi tulla kohdistamattomia. **Kohdistamattomat päätililuokat** -kenttä osoittaa, onko tämä ongelma ajankohtainen.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Finance and Operationsin taloushallinnon raportoinnin version 7.2.6.0 tietovaraston osajoukon palauttaminen

Voit palauttaa tietovaraston osajoukon Finance and Operationsin taloushallinnon raportoinnin versiossa 7.2.6.0 ja aiemmissa versioissa valitsemalla **Palauta tietovaraston osajoukko** -valintaikkunassa **Palauta tietovaraston osajoukko** -valintaruutu ja valitse sitten **OK**. Palauta tietovaraston osajoukko vain ajoitetun käyttökatkon aikana.

[![Palauta tietovaraston osajoukko -valintaruutu](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Tietovaraston osajoukon palauttaminen ja syyn valitseminen Microsoft Dynamics 365 for Finance and Operationsin taloushallinnon raportoinnin versiossa 7.3.0

Jos tietovaraston osajoukon palauttaminen on mielestäsi välttämätöntä, valitse **Palauta tietovaraston osajoukko** -valintaruutu ja valitse sitten **Syy**-kentässä syy. Käytettävissä ovat seuraavat asetukset:

- **Puuttuvat tai virheelliset tiedot** – Tilastotietojen perusteella olet sitä mieltä, että tietoja saattaa puuttua. Ennen kuin jatkat, suosittelemme pääsyyn selvittämistä tuen kanssa.
- **Palauta tietokanta** – Finance and Operations -tietokanta on palautettu, mutta taloushallinnon raportoinnin tietovaraston osajoukkoa ei.
- **Muu** – Olet palauttamassa tietovaraston osajoukkoa jonkin muun syyn vuoksi. Jos epäilet, että jossakin on ongelma, ota yhteys tukeen asian selvittämistä varten.

[![Palauta tietovaraston osajoukko](./media/Integration.png)](./media/Integration.png)

> [!NOTE]
> Vahvista, että kaikki tietovaraston palautustehtävät ovat suorittaneet ensimmäisen kuormituksen ennen palauttamisen aloittamista. Voit vahvistaa sen etsimällä Edellisen suorituksen aika -sarakkeen arvon valitsemalla **Työkalut** &gt; **Integroinnin tila**.

#### <a name="clear-users-and-companies"></a>Poista käyttäjät ja yritykset

Valitse **Poista käyttäjät ja yritykset** -valintaruutu, jos palautit tietokannan ja teit sen jälkeen muutoksia käyttäjien tai yritysten tietoihin. Tämän valintaruudun valinnan tulisi olla ajankohtaista vain harvoin.

Kun palautusprosessi voidaan aloittaa, valitse **OK**. Näyttöön tulee kehote, jossa pyydetään vahvistamaan, että kaikki on valmista prosessin aloittamista varten. Ota huomioon, että taloushallinnon raportointi ei ole käytettävissä palauttamisen ja sen jälkeen tapahtuvan aloitustietojen integroinnin aikana.

Jos haluat tarkistaa integroinnin tilan, valitse **Työkalut** &gt; **Integroinnin tila**. Tämän jälkeen näet integroinnin edellisen suoritusajankohdan ja tilan.

[![Integroinnin tilan tarkasteleminen](./media/New-integration.PNG)](./media/New-integration.PNG)

> [!NOTE]
> Palautus on valmis, kun kaikkien yhdistämismääritysten tila on RanToCompletion ja vasemmassa alakulmassa olevassa integroinnin tilaikkunassa on ilmoitus Integrointi on valmis.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Finance and Operationsin taloushallinnon raportoinnin version 7.0.10000.4 ja uudemman version talousraportoinnin tietovaraston osajoukon palauttaminen

Jos joskus palautat Finance and Operations -tietokannan varmuuskopiosta tai toisen ympäristön tietokannasta, sinun noudatettava tämän osan ohjeita. Tällä tavoin voit varmistaa, että taloushallinnon raportoinnin tietovaraston osajoukko käyttää oikein palautettua Finance and Operations -tietokantaa.

> [!NOTE]
> Tämän prosessin vaiheita tuetaan Microsoft Dynamics AX -sovelluksen versiossa 7.0.1 (toukokuu 2016) (sovelluksen versio 7.0.1265.23014 ja taloushallinnon raportoinnin versio 7.0.10000.4) ja uudemmissa versioissa. Jos käytössä on Finance and Operationsin aiempi versio, ota yhteys tukeen.

### <a name="export-report-definitions"></a>Raporttimääritysten vieminen

Vie ensin raportin rakenteet raportin suunnitteluohjelmasta näiden ohjeiden avulla.

1. Valitse raportin suunnitteluohjelmassa **Yritys** &gt; **Rakenneosaryhmät**.
2. Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**.

    > [!NOTE]
    > Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.

3. Valitse vietävät raporttimääritykset seuraavasti:

    - Jos haluat viedä kaikki raporttimääritykset ja niihin liittyvät rakenneosat, valitse **Valitse kaikki**.
    - Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet. Voit valita välilehdessä useita kohteita pitämällä Ctrl-näppäintä alhaalla. Kun valitset vietävät raportit, niihin liittyvät rivit, sarakkeet, puut ja dimensioyhdistelmät tulevat valituiksi.

4. Valitse **Vie**.
5. Anna tiedostonimi ja valitse turvallinen paikka, jonne viedyt raporttimääritykset tallennetaan.
6. Valitse **Tallenna**.

Voit kopioida tai ladata tiedoston turvalliseen paikkaan. Näin tiedosto voidaan tuoda toiseen ympäristöön myöhemmin. Lisätietoja Microsoft Azure -tallennustilin käyttämisestä on kohdassa [Tietojen siirtäminen AzCopy-komentorivin apuohjelman avulla](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Microsoft ei tarjoa tallennustiliä Finance and Operations -sopimuksen osana. Osta tallennustili tai käytä erillisen Azure-tilauksen tallennustiliä.

> [!WARNING]
> Ota huomioon Azuren virtuaalikoneiden D-aseman toiminta. Älä tallenna vietyjä rakenneosaryhmiä pysyvästi D-asemalle. Lisätietoja väliaikaisista asemista on kohdassa [Tietoja Windows Azuren virtuaalikoneiden väliaikaisesta asemasta](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Palveluiden pysäyttäminen

Seuraavilla Microsoft Windows -palveluilla on avoimet yhteydet Finance and Operations -tietokantaan. Tämän vuoksi kaikkiin ympäristön tietokoneisiin on muodostettava yhteys Microsoftin etätyöpöydän avulla. Palvelut pysäytetään services.msc:n avulla.

- WWW-julkaisupalvelu (kaikissa AOS (Application Object Server -palvelimet) -tietokoneissa)
- Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)
- Management Reporter 2012 Process Service (vain BI (Business intelligence) -tietokoneissa)

### <a name="reset"></a>Palauta

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Uusimman MinorVersionDataUpgrade.zip-paketin lataaminen

Lataa uusin MinorVersionDataUpgrade.zip-paketti. Lisätietoja oikean tietojen päivityspakettiversion etsimisestä ja lataamisesta on kohdassa [Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). 

MinorVersionDataUpgrade.zip-paketin lataaminen ei edellytä päivitystä. Seuraa siis ohjeaiheen Uusimman tietojen päivityksen käyttöönotettavan paketin lataaminen -osan vaiheita. Voit ohittaa ohjeaiheen muut vaiheet.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Komentosarjojen suorittaminen Finance and Operations -tietokannassa

Suorita seuraavat komentosarjat Finance and Operations -tietokannassa (ei taloushallinnon raportointitietokannassa):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Näiden komentosarjojen avulla voidaan varmistaa, että käyttäjien, roolien ja muutosten seurannan asetukset on määritetty oikein.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Tietokannan palauttaminen Windows PowerShell -komennon suorittamisen avulla

Käynnistä Microsoft Windows PowerShell AOS-tietokoneessa järjestelmänvalvojana ja suorita seuraavat komennot, jos haluat palauttaa Finance and Operationsin ja taloushallinnon raportoinnin väliset integrointiasetukset.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Seuraavassa esitellään **Reset-DatamartIntegration** -komennon parametrit:

- **-Reason**-parametrin sallitut arvot ovat **SERVICING**, **BADDATA** ja **OTHER**.
- **-ReasonDetail**-parametri on vapaatekstikenttä.
- Sekä reason että reason detail tallennetaan telemetria-/ympäristövalvonnassa.

> [!NOTE]
> Kun olet suorittanut komennot, sinua pyydetään vahvistamaan tietokannan palauttaminen syöttämällä **Y**.

#### <a name="restart-services"></a>Palveluiden käynnistäminen uudelleen

Käynnistä aiemmin pysäyttämäsi palvelut uudelleen services.msc:n avulla:

- WWW-julkaisupalvelu (kaikissa AOS-tietokoneissa)
- Microsoft Dynamics 365 for Finance and Operationsin erähallintapalvelu (vain muissa kuin yksityisissä AOS-tietokoneissa)
- Management Reporter 2012 Process Service (vain BI-tietokoneissa)

#### <a name="import-report-definitions"></a>Raporttimääritysten tuominen

Tuo raportin rakenteet raportin luontiohjelmasta käyttämällä viennin aikana luodun tiedoston avulla.

1. Valitse raportin suunnitteluohjelmassa **Yritys** &gt; **Rakenneosaryhmät**.
2. Valitse vietävä rakenneosaryhmä ja valitse sitten **Vie**.

    > [!NOTE]
    > Finance and Operations tukee vain yhtä **oletusarvoista** rakenneosaryhmää.

3. Valitse **oletusrakenneosa** ja valitse sitten **Tuo**.
4. Valitse viedyt raporttimääritykset sisältävä tiedosto ja valitse sitten **Avaa**.
5. Valitse **Tuo**-valintaikkunassa tuotavat raporttimääritykset:

    - Jos haluat tuoda kaikki raporttimääritykset ja niihin liittyvät rakenneosat, valitse **Valitse kaikki**.
    - Jos haluat tuoda tietyt raportit, rivit, sarakkeet, puut tai dimensioyhdistelmät, valitse tuotavat raportit, rivit, sarakkeet, puut tai dimensioyhdistelmät.

6. Valitse **Tuo**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Finance and Operationsin (paikallinen) taloushallinnon raportoinnin tietovaraston osajoukon palauttaminen

1. Pyydä kaikkia käyttäjiä poistumaan raportin suunnitteluohjelmasta ja Finance and Operationsin taloushallinnon raportoinnin alueesta.
2. Suorita seuraava komentosarja taloushallinnon raportoinnin tietokannassa (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Katkaise tai poista FINANCIALREPORTS-taulukon kaikki tietueet Finance and Operations -tietokannassa (AXDB).
4. Katkaise tai poista FINANCIALREPORTVERSION-taulukon kaikki tietueet, jos taulukko on Finance and Operations -tietokannassa. Jos Finance and Operations -tietokannassa ei ole tätä taulukkoa, ohita tämä vaihe.
5. Suorita **ResetDatamart.sql**-komentosarja taloushallinnon raportoinnin tietokannassa. Tämä komentosarja poistaa tietovaraston osajoukon integroinnin käytöstä, poistaa kaikki tietovaraston osajoukon tiedot ja ottaa lopuksi tietovaraston osajoukon integroinnin uudelleen käyttöön.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Palauttamisen jälkeen voit tarkistaa tietojen uudelleenlataamisen manuaalisesti, kun suoritat seuraavan kyselyn taloushallinnon raportoinnin tietokannassa.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Varmista, että kaikilla riveillä on **LastRunTime**-arvo ja että **StateType**-kohdan arvoksi on annettu **5**. **StateType**-kohdan arvo **5** osoittaa, että tietojen uudelleenlataaminen onnistui. Arvo **7** osoittaa vikatilan. Joskus organisaatiohierarkian määrityksellä on tämä tila ensimmäisen suorituskerran jälkeen. Virhetilan tulisi ratketa automaattisesti.

