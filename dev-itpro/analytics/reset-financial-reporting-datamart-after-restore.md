---
title: "Palauta tiedot taloudellisen raportoinnin mart jälkeen tietokannan palauttaminen"
description: "Tässä aiheessa kuvataan, miten Microsoft Dynamics-365 toimintoja tietokannan palautuksen jälkeen Palauta taloudellisen raportoinnin tietojen mart."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Palauta tiedot taloudellisen raportoinnin mart jälkeen tietokannan palauttaminen

Tässä aiheessa kuvataan, miten Microsoft Dynamics-365 toimintoja tietokannan palautuksen jälkeen Palauta taloudellisen raportoinnin tietojen mart. 

On useita skenaarioita, joissa kannattaa käyttää Dynamics 365 toimintoja tietokannan palauttaminen varmuuskopiosta tai kopioida tietokannasta toiseen ympäristöön. Kun tämä tapahtuu, sinun on myös tarpeelliset toimenpiteet sen varmistamiseksi, taloudellisen raportoinnin tietojen mart oikein käyttää palautettua Dynamics 365 tietokannan toiminnot toimi. Jos sinulla on kysyttävää palauttaminen taloudellisen raportoinnin tietojen mart syystä ulkopuolella Dynamics-365 toimintoja tietokannan palauttaminen, katso [palauttaminen Management Reporter tietojen mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) lisätietoja. Huomaa, että tämän prosessin vaiheissa tuetaan toiminnolle Dynamics 365 päivänä 2016 release (App build 7.0.1265.23014 ja taloudellisen raportoinnin build 7.0.10000.4) ja uudempia versioita. Jos työvaiheiden 365 Dynamics aiemman version, ota yhteyttä tukiryhmäämme.

## <a name="export-report-definitions"></a>Viedä raporttimääritykset
Vie ensin raportti malleja sijaitsee raportin rakennenäkymässä seuraavasti:

1.  Siirry raportin, Suunnittelija **yrityksen**&gt;**rakenneosan ryhmiä**.
2.  Rakenneosan viedä, ja valitse ryhmä **Vie**. **Huomautus:** Dynamics 365 operaatioille, tuetaan vain yksi rakenneosa ryhmä, **oletus**.
3.  Valitse raporttimääritykset vieminen:
    -   Voit viedä kaikki raporttien määritykset ja liittyvät rakenneosat valitsemalla **Valitse kaikki**.
    -   Voit viedä tiettyjä raportti-, rivi-, sarake-, puu- ja dimensioyhdistelmiä valitsemalla kyseisen välilehden ja valitsemalla sitten vietävät kohteet. Voit valita useita välilehden kohteita pitämällä Ctrl-näppäintä alhaalla. Raporttien vieminen valittaessa valitaan liittyvät rivit, sarakkeet, puut ja Dimensioyhdistelmät.

4.  Valitse **Vie**.
5.  Kirjoita tiedostonimi ja valitse turvalliseen paikkaan, johon haluat tallentaa viedyn raporttimäärityksiä.
6.  Click **Save**.

Tiedoston voi kopioida tai ladata turvalliseen paikkaan, jolloin tuodaan myöhemmin eri ympäristössä. Tietoja Microsoftin Azure-tallennustilan tiliin löytyvät [siirtää tietoja AzCopy Command-Line-apuohjelman kanssa](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Huomautus:** Microsoft ei tarjoa varastointi tili Dynamics-365 osana toimintojen sopimuksen. Osta tallennustilaa tiliä tai käyttää erillistä Azure tilauksesta varastointi. **Tärkeää:** olla tietoinen D-aseman Azure virtuaalisten laitteiden toimintaa. Älä säilytä viety rakenneosan ryhmiä tähän pysyvästi. Saat lisätietoja väliaikainen asemien [väliaikainen asema-Windows Azure virtuaalikoneet ymmärtäminen](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Pysäytä palvelut
Etätyöpöydän avulla voit yhdistää kaikki ympäristön tietokoneet ja lopettaa avulla services.msc seuraavat Windows-palvelut:

-   World wide web-julkaisupalvelu (kaikissa tietokoneissa AOS)
-   Toimintojen erän hallinta-palvelun (ja yksityisen AOS-tietokoneiden vain) Microsoft Dynamics-365
-   Reporter 2012 prosessi hallintapalvelu (tietokoneissa BI vain)

Nämä palvelut on avoimia yhteyksiä tietokannan toimintoja Dynamics-365.

## <a name="reset"></a>Palauta
#### <a name="locate-the-latest-dataupgradezip-package"></a>Etsi uusimmat DataUpgrade.zip-paketti

Etsi ajo-ohjeet löytyvät käyttäen uusimman DataUpgrade.zip paketti [lataa komentosarjan DataUpgrade.zip](..\migration-upgrade\upgrade-data-to-latest-update.md). Ohjeita kerrotaan, kuinka Etsi tiedot päivitetty paketti ympäristön oikea versio.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Suorittaa toimintoja tietokannan komentosarjoja vastaan Dynamics 365

Suorita seuraavat komentosarjat Dynamics-365 (ei vastaan taloudellisia raportointitietokannan) tietokannan toimintoja vastaan.

-   DataUpgrade.zip\\AosService\\komentosarjojen\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\komentosarjojen\\GrantAzViewChangeTracking.sql

Nämä komentosarjat että käyttäjiä, rooleja ja muutosten jäljityksen asetukset ovat oikeat.

#### <a name="execute-powershell-command-to-reset-database"></a>Suorita PowerShell-komennolla tietokannan palauttaminen

Suorita seuraava komento suoraan tietokoneen AOS-Dynamics 365 operaatioille ja talousraportointi integroinnin palauttaminen:

1.  Avaa Windows PowerShell järjestelmänvalvojana.
2.  Suoritus: F:
3.  Suoritus: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Suoritus: Import-Module. \\Server\\MRDeploy\\MRDeploy.psd1
5.  Suoritus: Palauta-DatamartIntegration-muu syy - ReasonDetail "&lt;omiin nollaaminen syy&gt;"
    -   Sinua pyydetään vahvistamaan "Y" kirjoittamaan.

Parametrien selitys:

-   Kelvolliset arvot - syy ovat: ylläpito, BADDATA, muut.
-   -ReasonDetail parametri on vapaamuotoinen.
-   Syy ja reasonDetail tallennetaan kaukomittaus/ympäristön seurannassa.

## <a name="start-services"></a>Käynnistä palvelut
Käytä services.msc uudelleen palvelut, jotka aiemmin keskeytetty:

-   World wide web-julkaisupalvelu (kaikissa tietokoneissa AOS)
-   Toimintojen erän hallinta-palvelun (ja yksityisen AOS-tietokoneiden vain) Microsoft Dynamics-365
-   Reporter 2012 prosessi hallintapalvelu (tietokoneissa BI vain)

## <a name="import-report-definitions"></a>Tuo raporttimääritykset
Raportti-mallien tuominen Report Designer, että viennin aikana luodun tiedoston käyttäminen:

1.  Siirry raportin, Suunnittelija **yrityksen**&gt;**rakenneosan ryhmiä**.
2.  Rakenneosan viedä, ja valitse ryhmä **Vie**. **Huomautus:** Dynamics 365 operaatioille, tuetaan vain yksi rakenneosa ryhmä, **oletus**.
3.  Valitse **oletus** lohko ja valitse **tuo**.
4.  Viety raporttimääritykset sisältävä tiedosto ja valitse **auki**.
5.  Valitse Tuo-valintaikkunassa tuotavat raporttien määritykset.
    -   Voit tuoda kaikki raporttien määritykset ja niitä tukevat rakenneosat valitsemalla **Valitse kaikki**.
    -   Voit tuoda tiettyjä raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmiä valitsemalla tuotavat raportti-, rivi-, sarake-, puu- tai dimensioyhdistelmät.

6.  Click **Import**.



