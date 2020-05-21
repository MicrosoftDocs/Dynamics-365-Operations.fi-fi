---
title: Yleinen vianmääritys
description: Tässä artikkelissa on yleisiä vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 8cc7c11233c745719af72222eba02fb71d7a8944
ms.sourcegitcommit: 4edc658448612afbf1c1663c166d12e08e4c4165
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/06/2020
ms.locfileid: "3340927"
---
# <a name="general-troubleshooting"></a>Yleinen vianmääritys

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on yleisiä vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Kun kaksoiskirjoituspaketti yritetään asentaa paketin käyttöönottajan avulla, käytettävissä olevia ratkaisuja ei näytetä

Jotkin paketin käyttöönottajan työkalun versiot eivät ole yhteensopivia kaksoiskirjoituksen ratkaisupaketin kanssa. Jos haluat asentaa paketin onnistuneesti, varmista, että käytössä on paketin käyttöönottajan työkalun [versio 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) tai uudempi.

Kun olet asentanut paketin käyttöönottajatyökalun, asenna ratkaisupaketti noudattamalla näitä ohjeita.

1. Lataa uusin ratkaisupakettitiedosto kohteesta Yammer.com. Kun paketin zip-tiedosto on ladattu, napsauta sitä hiiren kakkospainikkeella ja valitse **Ominaisuudet**. Valitse **Poista esto** -valintaruutu ja valitse sitten **Käytä**. Jos et näe **Poista esto** -valintaruutua, zip-tiedosto on jo avattu ja voit ohittaa tämän vaiheen.

    ![Ominaisuudet -valintaikkuna](media/unblock_option.png)

2. Pura paketin zip-tiedosto ja kopioi kaikki tiedostot **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** -kansioon.

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438-kansion sisältö](media/extract_package.png)

3. Liitä kaikki kopioidut tiedostot paketin käyttöönottajan **Työkalu**-kansioon. 
4. Valitse Common Data Service -ympäristö ja asenna ratkaisut suorittamalla **PackageDeployer.exe**-asiakirja.

    ![Työkalut-kansion sisältö](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>Ota käyttöön ja tarkastele laajennuksen jäljitysloki, Common Data Servicessä, kun haluat tarkastella virheen tietoja

**Jäljityslokin ottaminen käyttöön ja virheiden tarkasteleminen:** järjestelmän hallintarooli

Jäljitysloki otetaan käyttöön seuraavasti.

1. Kirjaudu mallipohjaiseen sovellukseen Dynamics 365:ssa, avaa **Asetukset**-sivu ja valitse sitten **Järjestelmä**-kohdasta **Hallinta**.
2. Valitse **Hallinta**-sivulla **Järjestelmäasetukset**.
3. Ota laajennuksen jäljitysloki käyttöön valitsemalla **Mukauttaminen**-välilehden **Laajennuksen ja mukautetun työnkulun tehtävän jäljitys**-kentästä **Kaikki**. Jos haluat kirjata jäljityslokit vain, kun poikkeuksia ilmenee, voit valita kohdan **Poikkeus** sen sijaan.


Jäljitysloki näytetään seuraavasti.

1. Kirjaudu mallipohjaiseen sovellukseen Dynamics 365:ssa, avaa **Asetukset**-sivu ja valitse sitten **Mukautus**-kohdasta **Laajennuksen jäljitysloki**.
2. Etsi jäljityslokit, joiden **Tyyppinimi**-kentän arvoksi on määritetty **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Voit tarkastella koko lokia kaksoisnapsauttamalla kohdetta ja tarkistaa sitten **Suoritus**-pikavälilehdessä **Sanomalohko**-tekstin.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Virheenkorjaustilan käyttöönotto Finance and Operations -sovellusten live-synkronointiongelmien vianmäärityksessä

**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvojan kaksoiskirjoitusvirheet, jotka ovat peräisin Common Data Servicestä voivat näkyä Finance and Operations -sovelluksessa. Joissakin tapauksissa virhesanoman koko teksti ei ole käytettävissä, koska sanoma on liian pitkä tai sisältää henkilökohtaisia tunnistetietoja (PII). Noudattamalla seuraavia ohjeita voit ottaa käyttöön sanallisen kirjaamisen.

1. Kaikilla Finance and Operations -sovellusten projektikokoonpanoilla on **IsDebugMode**-ominaisuus **DualWriteProjectConfiguration**-yksikössä. Avaa **DualWriteProjectConfiguration**-yksikkö käyttämällä Excel-lisäosaa.

    > [!TIP]
    > Helppo tapa avata yksikkö on ottaa **Suunnittelu**-tila käyttöön Excel-lisäosalla ja lisätä sitten taulukkoon **DualWriteProjectConfigurationEntity**. Lisätietoja kohdassa [Avaa yksikön tiedot Excelissä ja päivittä ne käyttämällä Excel-lisäosaa](../../office-integration/use-excel-add-in.md).

2. Aseta **sDebugMode**-ominaisuuden arvoksi projektille **Kyllä**.
3. Suorita virheitä tuottava skenaario.
4. Sanalliset lokit ovat käytettävissä DualWriteErrorLog-taulussa. Voit etsiä tietoja taulukkoselaimesta käyttämällä seuraavaa URL-osoitetta (korvaa **XXX** tarvittaessa):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Finance and Operations -sovelluksen virtuaalikoneen synkronointivirheiden tarkistaminen

**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvoja

1. Kirjaudu Microsoft Dynamics Lifecycle Servicesiin (LCS).
2. Avaa LCS-projekti, jonka valitsit kaksoiskirjoitustestauksen suorittamista varten.
3. Valitse **Pilvipalveluympäristöt**-ruutu.
4. Voit kirjautua Finance and Operations -sovelluksen virtuaalikoneeseen (VM) etätyöpöydän avulla. Käytä LCS:ssä näkyvää paikallista tiliä.
5. Avaa tapahtumien katseluohjelma.
6. Valitse **Sovellusten ja palveluiden lokit \> Microsoft \> Dynamics \> AX -DualWriteSync \> Toiminnassa**.
7. Tarkista viimeaikaisten virheiden luettelo.

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>Toisen Common Data Service -ympäristön linkityksen poistaminen Finance and Operations -sovelluksesta

**Ympäristön linkityksen poistamiseen vaadittu rooli:** Joko Finance and Operations -sovelluksen tai Common Data Service -ohjelman järjestelmänvalvoja.

1. Kirjautuminen Finance and Operations -sovellukseen.
2. Siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu.
3. Valitse kaikki käynnissä olevat yhdistämismääritykset ja valitse sitten **Pysäytä**.
4. Valitse **Poista ympäristön linkitys**.
5. Vahvista toiminto valitsemalla **Kyllä**.

Nyt voit linkittää uuden ympäristön.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Myyntitilausrivin tietolomaketta ei voi tarkastella 

Kun luot myyntitilauksen Dynamics 365 Salesissa, **+ Lisää tuotteet** -vaihtoehdon napsauttaminen saattaa ohjata sinut Dynamics 365 Project Operationsin tilausrivilomakkeeseen. Kyseisessä lomakkeessa ei ole mitään tapaa tarkastella myyntitilausrivin **Tieto**-lomaketta. **Tietoja**-vaihtoehto ei näy **Uuden tilausrivin** alla olevassa avattavassa valikossa. Näin tapahtuu, koska Project Operations on asennettu ympäristöösi.

Voit ottaa **Tieto**-lomakevaihtoehdon uudelleen käyttöön seuraavasti:
1. Siirry **Tilausrivi**-yksikköön.
2. Etsi **Tieto**-lomake lomakkeet-solmussa. 
3. Valitse **Tieto**-lomake ja valitse **Ota käyttöön käyttöoikeusroolit**. 
4. Muuta suojausasetukseksi **Näytä kaikille**.
