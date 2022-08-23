---
title: Live-synkronoinnin ongelmien vianmääritys
description: Tässä artikkelissa on vianmääritystietoja, joiden avulla voit korjata ongelmia suoralla synkronoinnilla.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b6650c92d22aee5394460e4e32bfd0ad3a7698c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289451"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Live-synkronoinnin ongelmien vianmääritys

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten sekä Microsoft Dataversen välillä. Erityisesti se tarjoaa tietoja, joiden avulla voit korjata ongelmia suoralla synkronoinnilla.

> [!IMPORTANT]
> Jotkin tämän artikkelin osa-alueet saattavat edellyttää joko järjestelmänvalvojan roolia tai Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tiettyjä tunnistetietoja.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Live-synkronointi näyttää virheen, kun rivi luodaan

Näyttöön saattaa tulla seuraava virhesanoma, kun luot rivin talous- ja toimintosovelluksessa:

*\[{\\"virhe\\":{\\"koodi\\":\\"0x80072560\\",\\"viesti\\":\\"Käyttäjä ei ole organisaation jäsen.\\"}}\], Etäpalvelin palautti virheen: (403) Kielletty."}}".*

Voit korjata ongelman noudattamalla [Järjestelmän vaatimukset ja edellytykset](requirements-and-prerequisites.md)-kohdan ohjeita. Näiden vaiheiden suorittaminen Dataversessä edellyttää, että sovelluksessa luoduilla kaksoiskirjoituskäyttäjillä on järjestelmänvalvojan rooli. Omistavan ryhmän oletusryhmällä on oltava myös järjestelmänvalvojan rooli.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Live-synkronointi näyttää virheen, kun taulukkotietoja yritetään tallentaa

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität tallentaa taulukkotietoja talous- ja toimintosovelluksessa:

*Muutoksia ei voi tallentaa tietokantaan. Työyksikkö ei voi sitoutua tapahtumaan. Tietoja ei voi kirjoittaa yksikön mittayksikköön. Kirjoitukset UnitOfMeasureEntity-kohtaan epäonnistuivat ja näkyviin tuli virhesanoma Ei voi synkronoida mittayksikön kanssa.*

Voit korjata ongelman varmistamalla, että sekä talous- ja toimintosovelluksessa että Dataversessä on tarvittavat viitetiedot. Jos esimerkiksi asiakastietue kuuluu tiettyyn asiakasryhmään, varmista, että asiakasryhmätietue on olemassa Dataversessä.

Jos molemmissa sijainnissa on tietoja ja olet vahvistanut, että ongelma ei liity tietoihin, toimi seuraavasti.

1. Avaa **DualWriteProjectConfigurationEntity**-yksikkö käyttämällä Excel-lisäosaa. Apuohjelman käyttöä varten on otettava käyttöön suunnittelutila talous- ja toimintosovellusten Excel-apuohjelmassa ja lisättävä **DualWriteProjectConfigurationEntity** laskentataulukkoon. Lisätietoja on kohdassa [Yksikön tietojen näyttäminen ja päivittäminen Excelissä](../../office-integration/use-excel-add-in.md).
2. Valitse ja poista tietueet, joissa on ongelmia kaksoiskirjoituksen yhdistämismäärityksessä ja projektissa. Jokaista kaksoiskirjoituksen yhdistämismääritystä kohden on kaksi tietuetta.
3. Julkaise muutokset Excel-lisäosan avulla. Tämä vaihe on tärkeä, koska se poistaa tietueet yksiköstä ja sen pohjana olevista taulukoista.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Luku- tai kirjoitusoikeusvirheiden käsitteleminen talous- ja toimintosovelluksen tietojen luonnin yhteydessä

Näyttöön saattaa tulla virheellisestä pyynnöstä ilmoittava virhesanoma, kun luot tietoja talous- ja toimintosovelluksessa.

![Esimerkki virheellisen pyynnön virhesanomasta.](media/error_record_id_source.png)

Ongelman korjaaminen edellyttää puuttuvan oikeuden käyttöön ottamista määrittämällä oikea käyttöoikeusrooli yhdistetyn Dynamics 365 Sales- tai Dynamics 365 Customer Service -liiketoimintayksikköjen ryhmälle.

1. Etsi talous- ja toimintosovelluksessa liiketoimintayksikkö, joka on yhdistetty tietojen integroinnin yhteysjoukkoon.

    ![Organisaation yhdistämismääritys.](media/mapped_business_unit.png)

2. Kirjaudu ympäristöön asiakasvuorovaikutussovelluksessa, siirry kohtaan **Asetus \> Tietoturva** ja etsi yhdistetyn liiketoimintayksikön ryhmä.

    ![Yhdistetyn liiketoimintayksikön ryhmä.](media/setting_security_page.png)

3. Avaa ryhmän sivu muokkaamista varten ja valitse sitten **Hallitse rooleja**.

    ![Roolien hallinta -painike.](media/manage_team_roles.png)

4. Määritä **Hallitse ryhmärooleja** -valintaikkunassa rooli, jolla on luku-/kirjoitusoikeus asianomaisiin taulukkoihin ja valitse sitten **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Synkronointiongelmien korjaaminen äskettäin muuttuneessa Dataverse -ympäristössä

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

Näyttöön saattaa tulla seuraava virhesanoma, kun luot tietoja talous- ja toimintosovelluksessa:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Hyötykuormaa ei voida luoda yksikölle CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Hyötykuorman luonti epäonnistui, väärä URI: URI on tyhjä."}\],"isErrorCountUpdated":true}*

Virhesanoma näyttää tältä asiakasvuorovaikutussovelluksessa:

> Odottamaton virhe ISV-koodista. (ErrorType = ClientError) Odottamaton poikkeus laajennuksesta (Suorita): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: yksikön tilin käsittely epäonnistui - (yhteysyritys epäonnistui, koska yhdistetty osapuoli ei vastannut oikein tietyn ajanjakson jälkeen tai muodostettu yhteys epäonnistui, koska liitetty isäntä ei vastannut.

Tämä virhe ilmenee, jos Dataverse-ympäristö palautetaan virheellisesti, kun yrität luoda tietoja talous- ja toimintosovelluksessa.

> [!IMPORTANT]
> Jos olet linkittänyt ympäristöt uudelleen, sinun on pysäytettävä kaikki yksikköjen yhdistämismääritykset, ennen kuin voit jatkaa korjaustoimia.

Ongelman korjaamiseksi sinun on suoritettava toimenpiteitä sekä Dataversessä että talous- ja toimintosovelluksessa.

1. Toimi talous- ja toimintosovelluksessa seuraavasti:

    1. Avaa **DualWriteProjectConfigurationEntity**-yksikkö käyttämällä Excel-lisäosaa. Apuohjelman käyttöä varten on otettava käyttöön suunnittelutila talous- ja toimintosovellusten Excel-apuohjelmassa ja lisättävä **DualWriteProjectConfigurationEntity** laskentataulukkoon. Lisätietoja on kohdassa [Yksikön tietojen näyttäminen ja päivittäminen Excelissä](../../office-integration/use-excel-add-in.md).
    2. Valitse ja poista tietueet, joissa on ongelmia kaksoiskirjoituksen yhdistämismäärityksessä ja projektissa. Jokaista kaksoiskirjoituksen yhdistämismääritystä kohden on kaksi tietuetta.
    3. Julkaise muutokset Excel-lisäosan avulla. Tämä vaihe on tärkeä, koska se poistaa tietueet yksiköstä ja sen pohjana olevista taulukoista.
    4. Jos haluat estää virheet, kun linkität talous- ja toimintosovellusten tai Dataversen ympäristöjä uudelleen, varmista, että kaksoiskirjoituksen määrityksiä ei ole jäljellä.

2. Noudata Dataversessä näitä ohjeita:

    1. Kirjaudu Dataverse-ympäristöysi (esim. `https://*****.crm.dynamics.com/`).
    2. Siirry kohtaan **Lisäasetukset** \> **Erikoishaku**.
    3. Valitse **DualWriten suorituksenaikainen määritys**.
    4. Valitse tarkasteltava sarake.
    5. Tarkastele määrityksiä valitsemalla **Tulokset**.
    6. Poista kaikki esiintymät.

3. Toimi talous- ja toimintosovelluksessa seuraavasti:

    1. Avaa **DualWriteProjectConfigurationEntity**-yksikkö käyttämällä Excel-lisäosaa. Apuohjelman käyttöä varten on otettava käyttöön suunnittelutila talous- ja toimintosovellusten Excel-apuohjelmassa ja lisättävä **DualWriteProjectConfigurationEntity** laskentataulukkoon. Lisätietoja on kohdassa [Yksikön tietojen näyttäminen ja päivittäminen Excelissä](../../office-integration/use-excel-add-in.md).
    2. Valitse ja poista tietueet, joissa on ongelmia kaksoiskirjoituksen yhdistämismäärityksessä ja projektissa. Jokaista kaksoiskirjoituksen yhdistämismääritystä kohden on kaksi tietuetta.
    3. Julkaise muutokset Excel-lisäosan avulla. Tämä vaihe on tärkeä, koska se poistaa tietueet yksiköstä ja sen pohjana olevista taulukoista.
    4. Jos haluat estää virheet, kun linkität talous- ja toimintosovellusten tai Dataversen ympäristöjä uudelleen, varmista, että kaksoiskirjoituksen määrityksiä ei ole jäljellä.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Live-synkronoinnin virhe, kun koko tietokanta on kopioitu

Näyttöön saattaa tulla seuraava virhesanoma, kun teet koko tietokannasta kopion yhdestä järjestelmästä toiseen ja yrität sitten suorittaa tietokantatoiminnon:

*SecureConfig-organisaatio (???) ei vastaa nykyistä CRM-organisaatiota (???).*

Virhesanoma näytetään kaksoiskirjoituksen suorituspalvelulisäosasta sen varmistamiseksi, että yhdessä järjestelmässä määritettyä kaksoiskirjoitusmääritystä ei voi käyttää toisessa järjestelmässä.

Voit korjata ongelman poistamalla kaikki tietueet **msdyn_dualwriteruntimeconfig**-taulukosta, kun olet palauttanut tietokannan. Lisätietoja: [Kaksoiskirjoitusympäristöjen linkityksen poisto ja uudelleenlinkitys](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Live-synkronoinnin ongelmat, jotka johtuvat virheellisestä kyselysuodattimen syntaksista kaksoiskirjoituksen yhdistämismäärityksissä

Vaikka kaksoiskirjoituksen yhdistämismäärityksen suodattimen kyselylausekkeen syntaksi olisi virheetön, se ei välttämättä toimi odotetulla tavalla. Suodattimen lauseke kohdistuu yksikköön eikä yksittäiseen kyselykohteen tietolähteeseen. Siten luotu SQL-kysely ei palauta odotettuja tuloksia.

Esimerkki:

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Odotuksena voi olla, että projektit, joilla ei ole pääprojektia, suodatetaan pois. Suodatin ei kuitenkaan toimi, koska se on käännetty kyselyksi, joka muistuttaa seuraavaa esimerkkiä.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Todellinen tulos on, että `parentProject`-kentän arvoksi arvioidaan `null`. `null` ei kuitenkaan ole sama asia kuin tyhjä merkkijono. Tämän ristiriidan vuoksi kyselysuodatin ei palauta kelvollisia tuloksia.

Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Lisää laskettu sarake, joka voidaan lisätä laajennusmalliin ja jota tukee arvon `null` tyhjäksi merkkijonoksi muuntava logiikka.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Käytä uuden lasketun sarakkeen suodatinta oletussarakkeen sijaan.

Voit arvioida suodatinta kehitysympäristössä käyttämällä seuraavaa X++-koodia tulosten vahvistamiseksi. Suorita tämä koodi erillisenä ohjelmana. Sen avulla voit arvioida erilaisia suodattimia, joita voi käyttää yksikköön, ennen kuin käytät niitä kaksoiskirjoituksen yhdistämismäärityksiin. Kysely voidaan kohdistaa tietokantaan eroavaisuuksien arvioimista varten.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Talous- ja toimintosovellusten tietoja ei synkronoida Dataversen kanssa

Live-synkronoinnin aikana saattaa ilmetä ongelma, jossa vain osa tiedoista synkronoidaan talous- ja toimintosovelluksista Dataverseen tai tietoja ei synkronoida lainkaan.

> [!NOTE]
> Tämä ongelma on korjattava kehityksen aikana.

Tarkista seuraavat edellytykset ennen ongelman korjaamisen aloittamista:

+ Varmista, että mukautetut muutokset on kirjoitettu yhteen tapahtuma-alueeseen.
+ Liiketoimintatapahtumat ja kaksoiskirjoituskehys eivät käsittele toimintoja `doinsert()`, `doUpdate()` tai `recordset()` eivätkä tietueita, joissa `skipBusinessEvents(true)` on merkittynä. Jos koodi on näiden toimintojen sisällä, kaksoiskirjoitusta ei käynnistetä.
+ Liiketoimintatapahtumat on rekisteröitävä yhdistettyä tietolähdettä varten. Joissakin tietolähteissä käytetään ulkoliitosta, ja ne voivat olla merkittynä vain luettaviksi talous- ja toimintosovelluksissa. Näitä tietolähteitä ei seurata.
+ Muutokset tehdään vain, jos muutokset on tehty yhdistettyihin kenttiin. Muutokset muihin kuin yhdistettyihin kenttiin eivät käynnistä kaksoiskirjoitusta.
+ Varmista, että suodatinarvioinnit tuottavat kelvollisen tuloksen.

### <a name="troubleshooting-steps"></a>Vianmääritysvaiheet

1. Tarkista kenttien yhdistämismääritykset kaksoiskirjoituksen järjestelmänvalvojan sivulta. Jos kenttää ei ole yhdistetty talous- ja toimintosovelluksista Dataverseen, sitä ei seurata. Seuraavassa kuvassa **Kuvaus**-kenttää seurataan Dataversessä, mutta ei talous- ja toimintosovelluksissa. Tähän kenttään talous- ja toimintosovelluksissa tehtäviä muutoksia ei seurata.

    ![Seurattu kenttä.](media/live-sync-troubleshooting-1.png)

2. Määritä, seurataanko tietolähdettä liiketoimintatapahtuman määritelmässä. Seuraavassa kuvassa esimerkiksi mitään **DefaultDimensionDAVs**-taulukon tai sen alitaulukon kenttien muutoksia ei seurata. Tietolähteitä, jotka käyttävät ulkoliitosta ja jotka on merkitty vain luetuksi, ei seurata.

    ![Kenttä, jota ei seurata.](media/live-sync-troubleshooting-2.png)

3. Selvitä, näkyvätkö yhdistetyt taulukkokentät **BUSINESSEVENTSDEFINITION**-taulukossa seuraavassa kuvassa näkyvällä tavalla. Jos et löydä haettavaa kenttää kyselyn tuloksesta, se ei käynnistä kaksoiskirjoitusta.

    ![Jäljitetty kenttä taulukossa.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Esimerkkiskenaario

Talous- ja toimintosovelluksissa on päivitetty yhteyshenkilötietueen osoitetta, mutta muutos ei synkronoidu Dataverseen. Tämä tapahtuu, koska missään **BusinessEventsDefinition**-taulukon tietueessa ei ole kulloisenkin taulukon ja yksikön yhdistelmää. Tarkemmin ottaen **LogisticsPostalAddress**-taulukko ei ole **smmContactpersonCDSV**-yksikön suora tietolähde. **smmContactpersonCDSV2Entity**-yksikön tietolähteenä on **smmContactPersonV2Entity** ja **smmContactPersonV2Entity**-yksiköllä vuorostaan tietolähteenä on **LogisticsPostalAddressBaseEntity**. **LogisticsPostalAddress**-taulukko on **LogisticsPostalAddressBaseEntity**-yksikön tietolähde.

Sama voi toistua erikoistilanteissa, kuten silloin, kun talous- ja toimintosovelluksissa muokattavaa taulukkoa ei ole selkeästi linkitetty yksikköön, joka sisältää sen. Esimerkiksi ensisijaiset osoitetiedot voidaan laskea **smmContactPersonCDSV2Entity**-yksikössä. Kaksoiskirjoituskehys yrittää määrittää, miten alitaulukon muutos yhdistetään takaisin yksikköihin. Yleensä tämä menetelmä riittää. Joissakin tapauksissa linkki on kuitenkin niin monimutkainen, että sen kanssa on oltava tarkka. Sinun on varmistettava, että asiaan liittyvän taulukon **RecId** on saatavilla suoraan yksikössä. Lisää sitten staattinen menetelmä taulukon seuraamiseksi muutosten osalta.

Esimerkkinä tästä on tarkista **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()** -menetelmä. **CustCustomerV3entity** ja **VendVendorV2Entity** on mukautettu tämän tilanteen käsittelemiseksi.

Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Lisää **PrimaryPostalAddressRecId**-kenttä **smmContactPersonV2Entity**-yksikköön. Tee siitä sisäinen.

    ![Kenttä lisätty smmContactPersonV2Entity-yksikköön.](media/Troubleshoot_live_sync_issue_1.png)

2. Lisää sama kenttä **smmContactPersonCDSV2Entity**-yksikköön.

    ![Kenttä lisätty smmContactPersonCDSV2Entity-yksikköön.](media/Troubleshoot_live_sync_issue_2.png)

3. Lisää seuraava menetelmä **smmContactPersonCDSV2Entity**-luokkaan.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Synkronoi tietokanta ja luo sovellus.
5. Keskeytä kaikki kaksoiskirjoituksen yhdistämismääritykset, jotka luodaan **smmContactPersonCDSV2Entity**-yksikköön.
6. Käynnistä yhdistämismääritys. Näkyviin pitäisi tulla uusi taulukko (**LogisticsPostalAddress** tässä esimerkissä), jonka seurannan olet aloittanut käyttämällä **RefTableName**-saraketta riville, jossa **refentityname**-arvo on sama kuin **smmContactPersonCDSV2Entity** **BusinessEventsDefinition**-taulukossa.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Virhe luotaessa tietuetta, jossa useita tietueita lähetetään talous- ja toimintosovelluksesta Dataverseen samassa erässä

Talous- ja toimintosovellus luo tietoerän mitä tahansa tapahtumaa varten ja lähettää sen eränä Dataverseen. Jos kaksi tietuetta luodaan osana samaa tapahtumaa ja ne viittaavat toisiinsa, tuloksena voi olla virhesanoma, joka muistuttaa seuraavaa esimerkkiä talous- ja toimintosovelluksessa:

*Tietoja ei voi kirjoittaa yksikköön aaa_fundingsources. ebecsfs_contracts-yksikköä, jonka arvot ovat {PC00...} ei voi noutaa. aaa_fundingsources-yksikköä, jonka arvot ovat {PC00...} ei voi noutaa. Kirjoittaminen aaa_fundingsources-yksikköön epäonnistui ja virhesanomana on poikkeussanoma: Etäpalvelin palautti virheen: (400) Virheellinen pyyntö.*

Voit korjata ongelman luomalla yksikkösuhteita talous- ja toimintosovelluksessa ilmaisemaan, että kaksi yksikköä liittyvät toisiinsa ja että toisiinsa liittyvät tietueet käsitellään samassa tapahtumassa.

## <a name="enable-verbose-logging-of-error-messages"></a>Virhesanomien sanallisen kirjaamisen käyttöönotto

Talous- ja toimintosovelluksessa saattaa ilmetä virheitä, jotka liittyvät Dataverse-ympäristöön. Virhesanoma ei välttämättä sisällä sanoman koko tekstiä tai kaikkia muita merkityksellisiä tietoja. Lisätietoja saa ottamalla sanallisen kirjaamisen käyttöön määrittämällä **DualWriteProjectConfigurationEntity**-yksikössä kaikissa talous- ja toimintosovellusten projektimäärityksissä olevan **IsDebugMode**-merkinnän.

1. Avaa **DualWriteProjectConfigurationEntity**-yksikkö käyttämällä Excel-lisäosaa. Apuohjelman käyttöä varten on otettava käyttöön suunnittelutila talous- ja toimintosovellusten Excel-apuohjelmassa ja lisättävä **DualWriteProjectConfigurationEntity** laskentataulukkoon. Lisätietoja on kohdassa [Yksikön tietojen näyttäminen ja päivittäminen Excelissä](../../office-integration/use-excel-add-in.md).
2. Määritä **IsDebugMode**-merkinnän arvoksi **Kyllä** projektissa.
3. Suorita skenaario.
4. Sanalliset lokit ovat käytettävissä **DualWriteErrorLog**-taulussa. Voit etsiä tietoja taulukkoselaimella käyttäen seuraavaa URL-osoitetta: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`
5. Jos haluat tallentaa enemmän lokeja virheenkorjaustilassa, asenna päivitys osoitteessa [KB 4595434 (korjaus tyhjien arvojen täyttämiseen kaksoiskirjoituksen live-synkronoinnissa)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Virhe lisättäessä asiakkaan tai yhteyshenkilön osoitetta

Saatat saada seuraavan virhesanoman, kun yrität lisätä asiakkaan tai yhteyshenkilön osoitetta talous- ja toimintosovelluksissa tai Dataversessä:

*Yksikköön msdyn_partypostaladdresses ei voi kirjoittaa tietoja.Kirjoittaminen DirPartyPostalAddressLocationCDSEntity-yksikköön epäonnistui tilakoodilla BadRequest ja CDS-virhekoodi : 0x80040265 vastaussanoma: Lisäosassa tapahtui virhe. Tietue, jolla on määritearvot Sijaintitunnus on jo olemassa. Yksikön sijaintitunnuksen avain vaatii, että tämä määritesarja sisältää yksilöllisiä arvoja. Valitse yksilölliset arvot ja yritä uudelleen.*

Voit korjata tämä ongelman asentamalla kaksoiskirjoituksen orkestrointipaketin version (2.2.2.60), jotta **Osoite**-taulukon avaimet on määritetty seuraavassa taulukossa näkyvällä tavalla.

| Ominaisuus | Arvo |
|---|---|
| Näyttönimi | **Sijaintiavain** |
| Nimi | **msdyn_locationkey** |
| Kentät | **msdyn_locationid**, **parentid** |
| Tila | **Käytössä** |
| Järjestelmätyö | Tyhjä |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Virhe lisättäessä asiakasta Dataversessä

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität lisätä asiakkaan Dataversessä:

*"RecordError0":"Kirjoitus yksikössä Customers V3 epäonnistui tuntemattomalla poikkeuksella – Osapuolitietuetta ei löytynyt osapuolityypille 'Organisaatio'"}.*

Kun asiakas luodaan Dataversessä, uusi osapuolinumero luodaan. Virhesanoma tulee näkyviin, kun asiakastietua synkronoidaan yhdessä osapuolen kanssa talous- ja toimintosovelluksiin, mutta olemassa on jo asiakastietue, jolla on eri osapuolinumero.

Voit korjata ongelman hakemalla asiakkaan osapuolihaulla. Jos asiakasta ei ole olemassa, luo uusi asiakastietue. Jos asiakas on olemassa, käytä olemassa olevaa osapuolta uuden asiakastietueen luomiseen.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Virhe luotaessa uutta asiakasta, toimittajaa tai yhteyshenkilöä Dataversessä

Saatat saada seuraavan virhesanoman, kun yrität luoda uuden asiakkaan, toimittajan tai yhteyshenkilön Dataversessä:

*Osapuolen tyyppiä ei voi päivittää arvosta 'DirOrganization' arvoksi 'DirPerson', sen sijaan olemassa oleva osapuoli on poistettava ja uusi tyyppi on lisättävä.*

Dataversen **msdyn_party**-taulukossa on numerosarja. Kun Dataversessä luodaan tili, luodaan uusi osapuoli (esimerkiksi **Organisaatio**-tyyppiä oleva **Osapuoli-001**). Nämä tiedot lähetetään talous- ja toimintosovellukseen. Jos Dataverse-ympäristö palautetaan tai talous- ja toimintosovellusympäristö linkitetään eri Dataverse-ympäristöön ja uusi yhteyshenkilötietue luodaan Dataversessä, luodaan uusi osapuoliarvo, joka alkaa **Osapuoli-001**. Tällä kertaa luodaan **Henkilö**-tyyppiä oleva **Osapuoli-001**-osapuolitietue. Kun nämä tiedot on synkronoitu, edellinen virhesanoma näkyy talous- ja toimintosovelluksissa, koska tyyppiä **Organisaatio** oleva **Osapuoli-001**-osapuolitietue on jo olemassa.

Voit korjata tämän ongelman muuttamalla Dataversen **msdyn_party**-taulukon **msdyn_partynumber**-kentän automaattisen numerosarjan eri automaattiseksi numerosarjaksi.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Suorituskykyongelma asiakkaiden tai yhteyshenkilöiden yhdistämismäärityksessä

Asiakkaiden ja yhteyshenkilöiden live-synkronointia voi olla mahdollista tehostaa hieman mukauttamalla **getEntityDataSourceToFieldMapping**-menetelmää (**CustCustomerV3Entity**-yksikössä) ja **getEntityDataSourceToFieldMapping**-menetelmää (yksikössä **smmContactPersonCDSV2Entity**). Nämä mukautukset vähentävät **BusinessEventsDefinition**-taulukon tietuemäärää. Tämä tietuemäärän vähennys vuorostaan vähentää ilmenevien tapahtumien määrää.

**getEntityDataSourceToFieldMapping** -menetelmä **CustCustomerV3Entity**-yksikössä varmistaa, että asiakkaan sähköposti- tai postiosoitteen muutos käynnistää liiketoimintatapahtumia, jotta päivitetyt tiedot lähetetään Dataverseen. Jos et käytä kaikkia kenttiä eikä tietoja tarvitse kaksoiskirjoittaa, poista asianomaiset rivit käytöstä menetelmässä. Jokainen tähän menetelmään lisätty seurattu kenttä ja taulukko lisää tietueen **BusinessEventsDefinition**-taulukkoa varten seuratun taulukon ja seuratun yksikön yhdistämistä varten.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Samalla tavalla **getEntityDataSourceToFieldMapping** -menetelmä **smmContactPersonCDSV2Entity**-yksikössä varmistaa, että yhteyshenkilön sähköposti- tai postiosoitteen muutos käynnistää liiketoimintatapahtumia, jotta päivitetyt tiedot lähetetään Dataverseen. Menetelmässä voit poistaa käytöstä niiden kenttien rivit, joita et käytä.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Kun olet päivittänyt menetelmät, noudata seuraavia ohjeita.

1. Synkronoi tietokanta ja luo sovellus.
2. Keskeytä kaikki kaksoiskirjoituksen yhdistämismääritykset, jotka yksikköihin **smmContactPersonCDSV2Entity** ja **CustCustomerV3Entity**.
3. Käynnistä yhdistämismääritys. Nyt yksiköissä **smmContactPersonCDSV2Entity** ja **CustCustomerV3Entity** sekä taulukossa **BusinessEventsDefinition** pitäisi olla vähemmän tietueita ja suorituskyky saattaa parantua hieman.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

