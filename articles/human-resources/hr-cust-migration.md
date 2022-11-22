---
title: Dynamics 365 Human Resources -asiakkaiden siirto talous- ja toimintosovellusinfrastruktuuriin
description: Tässä artikkelissa kuvataan Microsoft Dynamics 365 Human Resources -asiakkaiden siirtoa talous- ja toimintosovellusinfrastruktuuriin.
author: twheeloc
ms.date: 10/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4df9a68ea0128378224bf77bd66423fd2e13fa55
ms.sourcegitcommit: e5b290bac7e8f468167caa1a5607aac6eac9aaea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760359"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources -asiakkaiden siirto

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Asiakkaiden siirto on "nosta ja siirrä" -tyyppinen operaatio, jossa asiakastietokanta siirretään talous- ja toimintosovellusinfrastruktuuriin. Siihen käytetään automaattista siirtotyökalua. Tuloksena on uusi talous- ja toimintosovellusympäristö, joka käyttää asiakkaan HR-tietokantaa.

## <a name="prerequisites"></a>Edellytykset

### <a name="user-access-and-permissions"></a>Käyttäjien käyttöoikeudet

- Microsoft Dynamics Lifecycle Services -käyttäjällä tulisi olla **Organisaation järjestelmänvalvoja** -rooli.
- Käyttäjän tulisi pystyä [luomaan Azure DevOps -projekteja](/azure/devops/organizations/projects/create-project) tai käyttämään aiemmin luotua Azure DevOps -projektia.
- Käyttäjällä tulisi olla oikeus [luoda henkilökohtainen Azure DevOps -suojaustunnus](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) tai hänellä tulisi olla käytettävissä oleva tunnus.

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse-ympäristön varmuuskopio (eristysympäristö)

 - Valinnainen, mutta suositeltavaa: Päivitä nykyinen HR-eristysympäristö käyttämällä HR-tuotantoympäristön kopiota.
 - Luo uusi Dataverse-ympäristö käyttämällä Power Platform -hallintakeskusta.
 - Kopioi edellisessä vaiheessa luomaasi ympäristöön nykyinen Dataverse-ympäristö, joka on linkitetty erilliseen Human Resources -sovellukseen.

> [!NOTE]
> Varmista tietokantaa lisätessäsi, että **Ota Dynamics 365 -sovellukset käyttöön** -vaihtoehdoksi on valittu **Kyllä**. Lisätietoja on kohdassa [Power Platform -ympäristön valmisteleminen](hr-cust-migration.md#prepare-a-power-platform-environment)

### <a name="dataverse-capacity"></a>Dataversen kapasiteetti

1. Käytä Power Platform -hallintakeskuksen **Yhteenveto**-sivua vahvistaaksesi, että [Dataverse -tallennustilassa](/power-platform/admin/finance-operations-storage-capacity) on tarpeeksi vapaata kapasiteettia ympäristön kopiolle.
2. Jos käytettävissä oleva kapasiteetti ei riitä, vapauta tilaa käyttämällä [tallennustilan vapauttamista koskevia ohjeita](/power-platform/admin/free-storage-space). Asiakkaat voivat myös [lisätä tallennustilan kapasiteettia](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Asiakkaiden siirtoprosessi

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Lifecycle Services -projektin luominen Human Resources -ympäristön siirtoa varten

Ensimmäinen vaihe on uuden talous- ja toimintosovellusten käyttöönottoprojektin luominen Lifecycle Services -portaalissa. Asiakkaalla tulee olemaan Human Resources Lifecycle Services -projekti. Nykyiset Human Resources -ympäristöt siirretään uuteen talous- ja toimintosovellusten käyttöönottoprojektiin.

Luo uusi projekti noudattamalla seuraavia ohjeita.

1. Kirjaudu Lifecycle Services -portaaliin yleisenä järjestelmänvalvojana tai määritettynä palvelutilin käyttäjänä.
2. Valitse Lifecycle Services -aloitussivulta **Luo/uusi (+)**.
3. Valitse tuotteeksi talous- ja toimintosovellukset.
4. Valitse **Projektin tarkoitus**-kentästä **Toteutus**.
5. Syötä projektin nimi ja kuvaus.
6. Valitse **Projektin mukautettu tyyppi** -kentästä **Microsoft Dynamics 365 Human Resources -siirto**.
7. Hyväksy ehdot ja edellytykset valitsemalla valintaruutu.
8. Valitse **Luo**.

Kun olet luonut uuden Lifecycle Services -projektin, määritä ja konfiguroi se noudattamalla seuraavia ohjeita:

1. Viimeistele projektin perehdytys valitsemalla **Projektin perehdytys**. Lisätietoja on kohdassa [Projektin käyttöönotto](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Valitse nykyisiä ympäristöjäsi vastaava alue. Tämä valinta ei vaikuta siirtoon.
    - Jos käytät vanhempia järjestelmiä, valitse **Muu**.

2. Viimeistele projektin asetukset. Sinun tulisi määrittää SharePoint Online -kirjasto Azure DevOps ja Azure-yhteydet osana tätä vaihetta, jos tarvitset niitä. Lisätietoja on [Lifecycle Services (LCS) -käyttöoppaassa](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Asiakkaat voivat käyttää aiemmin luotua Azure DevOps -projektia ja siihen liitettyä henkilökohtaista suojaustunnusta. Jos käytät aiemmin luotua projektia, projektiin liitetyt kokoonpanot ovat automaattisesti käytettävissä ja ne voidaan tarkistaa sopivuuden varmistamiseksi.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Human Resources -eristysympäristön siirto

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Eristysympäristöön siirtoon valmistautuminen

Kun uusi Lifecycle Services -projekti on luotu ja projektin perehdytysprosessi on suoritettu, olet valmis siirtämään ensimmäisen ympäristösi. Ennen kuin aloitat tämän prosessin, suosittelemme päivittämään tuotantoympäristöstäsi siirrettävän eritysympäristön erillisessä infrastruktuurissa.

#### <a name="prepare-a-power-platform-environment"></a>Power Platform -ympäristön valmisteleminen

> [!NOTE]
> Tämä vaihe koskee vain eristysympäristön siirtoa. Kun siirrät tuotantoympäristön, siihen liitettyä Power Platform -hallintakeskusympäristöä siirretään eteenpäin. Varmista tietokantaa lisätessäsi, että **Ota Dynamics 365 -sovellukset käyttöön** -painikkeen arvoksi on valittu **Kyllä**. 

- Avaa Power Platform -hallintakeskus, [luo ympäristö ja tietokanta](/power-platform/admin/create-environment#create-an-environment-with-a-database), jota haluat käyttää eristysympäristön siirrossa, tai valitse aiemmin luotu ympäristö.
- [Kopioi ympäristö](/power-platform/admin/copy-environment) päivittääksesi yhdistämismäärityksissä käytetyn Power Platform -ympäristön.

#### <a name="migrate-the-sandbox-environment"></a>Eristysympäristön siirto

1. Kirjaudu Lifecycle Services -portaaliin yleisenä järjestelmänvalvojana tai määritettynä palvelutilin käyttäjänä.

    > [!NOTE]
    > Suosittelemme, että käytät nimettyä käyttäjätiliä. Sisäänkirjautuneella käyttäjällä tulisi olla **Projektin omistaja**- tai **Ympäristövastaava**-käyttöoikeusrooli erillisessä henkilöstönhallinnon Lifecycle Services -projektissa.

2. Avaa juuri luotu Human Resources -siirtoprojekti.
3. Tarkista ja suorita siirtomenetelmän ja projektiperehdytyksen asiaankuuluvat vaiheet.
4. Valitse projektin koontinäytön **Oletus: Standard-hyväksyntätestaus** -ruudusta **Siirrä HR**.
5. Valitse **Valitse siirrettävä ympäristö** -ruudusta asiaankuuluva Lifecycle Services -projekti ja Human Resources -lähdeympäristö (erillisestä Human Resources -lähdesovelluksestasi).
6. Ota **Määritä uuteen Power Platform -ympäristöön** -vaihtoehto käyttöön ja valitse asiaankuuluva Power Platform -ympäristö. Valitse sitten **Seuraava**.
7. Suorita ohjattu **Käyttöönottoasetukset (talous- ja toimintosovellukset – eristysympäristö)** -toiminto vahvistaaksesi tiedot ja asiakkaan uloskirjautumisen ja valitse sitten **Ota käyttöön**.

Ympäristön tila näyttää edistymisen. Tila muuttuu ensin **Ladataan**-tilasta **Otetaan käyttöön** -tilaan ja sitten **Otettu käyttöön** -tilaan.

> [!NOTE]
> Tuotantoruutu ei ole käytettävissä ennen kuin projektin julkaisemisen valmiustarkistusluettelo on suoritettu. Lisätietoja on kohdassa [Julkistamisen valmistelu](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Huomautuksia ja oletuksia

Vuokraajassa olevassa Lifecycle Services -projektissa on Human Resources -eristysympäristö, jolla on seuraavat ominaisuudet:

- Human Resources -eristysympäristöä ei ole linkitetty olemassa olevaan yhdistettyyn ympäristöön. Yhdellä Human Resources -ympäristöllä voi olla käynnissä vain yksi siirto kerrallaan.
- Kerralla sallittu eristysympäristöjen määrä perustuu Human Resources -lisensseihin. Jos vuokraajalle on ostettu tarpeeksi lisenssejä, projektin **Ympäristöt**-ruudussa näkyy lisää eristysympäristöjä.
- Siirrot täytyy tehdä samantyyppisiin ympäristöihin. Toisin sanoen siirrot voidaan tehdä vain eristysympäristöstä eristysympäristöön tai tuotantoympäristöstä tuotantoympäristöön.

    > [!NOTE]
    > Tuotanto- tai eristysympäristön tilaa määritettäessä huomioidaan vain Human Resources -ympäristötyypit. Jos ympäristöt on luokiteltu väärin (eli tuotantoympäristö on merkitty eristysympäristöksi tai eristysympäristö on merkitty tuotantoympäristöksi), ota yhteyttä tukeen.

- Jos siirto epäonnistuu, näet virheilmoituksen ja **Poista**-painikkeen. Voit poistaa epäonnistuneen siirron tämän painikkeen avulla. Sen jälkeen voit siirtää ympäristön uudelleen.

#### <a name="validate-the-sandbox-migration"></a>Eristysympäristön siirron vahvistus

Kun eristysympäristön siirtoprosessi on suoritettu onnistuneesti, luo yksityiskohtainen testaussuunnitelma kaikkien liiketoimintaprosessien tarkistamista ja vahvistamista varten.

Tarkista seuraavat tiedot ennen testauksen aloittamista:

- Varmista, että siirrytty ympäristö on käytettävissä luodussa URL-osoitteessa.
- Varmista, että käyttäjät voivat käyttää siirrettyä eristysympäristöä.
- Varmista, että siirrettyyn eristysympäristöön liitetty Dataverse-ympäristö on käytettävissä.
- Tarkista tietojen eri osia varmistaaksesi, että saatavilla olevat tiedot ovat ajan tasalla.
- Suorita kriittiset liiketoimintaprosessit vahvistusta varten.
- Varmista, että tietoturvakäytäntösi ovat yhteensopivia.
- Varmista, että erätyöt käynnistetään odotetulla tavalla.

Sinulla ei ole etätyöpöytäkäytön käyttöoikeutta eristysympäristössä. Voit käyttää itsepalvelutoimintoja ja -työkaluja seuraavien toimenpiteiden suorittamiseen Tason 2 + eristysympäristöillesi:

- Käytä [Azure SQL -tietokantaa](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Käytä [lokitiedostoja](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Käytä [perfmon-työkaluja](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- [Ota ylläpitotila käyttöön / pois käytöstä](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- [Käynnistä palvelut uudelleen](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- Määritä [Regression Suite Automation Tool](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Lisätietoja on kohdassa [Itsepalvelukäyttöönoton usein kysytyt kysymykset](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Human Resources -tuotantoympäristön siirto

Kun olet siirtänyt ja vahvistanut eristysympäristön, siirrä tuotantoympäristö noudattamalla näitä ohjeita.

#### <a name="prerequisites"></a>Edellytykset

- Tilauksen arviointityökalu tulisi olla suoritettuna.
- [Julkaisuvalmiuden arviointi](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) tulisi olla suoritettuna.

#### <a name="migrate-the-production-environment"></a>Tuotantoympäristön siirto

1. Kirjaudu Lifecycle Services -portaaliin yleisenä järjestelmänvalvojana tai määritettynä palvelutilin käyttäjänä.

    > [!NOTE]
    > Suosittelemme, että käytät nimettyä käyttäjätiliä. Sisäänkirjautuneella käyttäjällä tulisi olla **Projektin omistaja**- tai **Ympäristövastaava**-käyttöoikeusrooli Lifecycle Services -projektissa.

2. Avaa uusi Human Resources -siirtoprojekti.
3. Tarkista ja suorita siirtomenetelmän ja projektiperehdytyksen asiaankuuluvat vaiheet.
4. Valitse projektin koontinäytön **Tuotanto**-ruudusta **Siirrä HR**.
5. Valitse **Valitse siirrettävä ympäristö** -ruudusta asiaankuuluva Lifecycle Services -projekti ja henkilöstönhallinnan lähdeympäristö (erillisestä henkilöstönhallinnon lähdesovelluksestasi). Valitse sitten **Seuraava**.
6. Suorita ohjattu **Käyttöönottoasetukset (talous- ja toimintosovellukset – eristysympäristö)** -toiminto vahvistaaksesi tiedot ja asiakkaan uloskirjautumisen ja valitse sitten **Ota käyttöön**.

Ympäristön tila näyttää käyttöönoton edistymisen. Tila muuttuu ensin **Ladataan**-tilasta **Otetaan käyttöön** -tilaan ja sitten **Otettu käyttöön** -tilaan.

#### <a name="post-migration-considerations"></a>Siirron jälkeen huomioitavat asiat

- Ota uusimmat [laatupäivitykset](/fin-ops-core/fin-ops/get-started/quality-updates) käyttöön ympäristöillesi.
- Jos käytät [virtuaalitaulukoita](hr-admin-integration-common-data-service-virtual-entities.md), määritä päätepisteet uudelleen.
- Määritä kaksoiskirjoituksen integrointi uudelleen. Arvioi, mitkä entiteetit täytyy ottaa käyttöön.
- Harkitse virtuaalitaulukoiden käyttämistä kaksoiskirjoituksen integroinnin sijaan.

#### <a name="dual-write-integration"></a>Kaksoiskirjoituksen integrointi

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Microsoft Power Platformin kaksoiskirjoituksen integroinnin määrittäminen uudelleen

1. Siirry Power Platform -hallintakeskukseen ja valitse vasemmasta siirtymisruudusta **Ympäristöt** .
2. Valitse aiemmin kopioitu/päivitetty ympäristö ja varmista, että sen tila on **Valmis**.
3. Avaa Lifecycle Services ja vahvista, että siirtoprojektin tila on **Otettu käyttöön**.
4. Valitse siirretyn ympäristön alta **Kaikki tiedot** nähdäksesi lisätietoja ja [määrittääksesi kaksoiskirjoitussovelluksen](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. Valitse **Kaksoiskirjoitussovelluksen määritys** -ruudun valintaruutu hyväksyäksesi yhdistämismääritykset ja synkronoidaksesi tiedot tietokantojen välillä ja valitse sitten **Määritä**.
6. Kun viestiruutu ilmoittaa, että kaksoiskirjoituksen määritys onnistui, valitse **OK**.
7. Voit valvoa määrityksen etenemistä lisätiedoista.
8. Kun määritys on valmis, valitse **Linkitä Power Platform -ympäristöön** synkronoidaksesi käytettävissä olevat tietoentiteetit.
9. Kun tila osoittaa, että ympäristöt on linkitetty onnistuneesti, siirry Power Platform -hallintakeskukseen tarkistaaksesi ja valitaksesi asiaankuuluvat tietoentiteetit.
10. Valitse vasemmanpuoleisesta ruudusta **Dynamics 365 -sovellukset \> Resurssit**.
11. Varmista, että kaksoiskirjoituksen Human Resources -sovelluksen tila **Käytössä**.
12. Valitse kaksoiskirjoituksen henkilöstönhallintasovellus ja valitse sitten **Asenna**.
13. Valitse **Asenna kaksoiskirjoituksen Dynamics 365 Human Resources -sovellus** -ruudusta ympäristö, johon haluat asentaa paketin.
14. Hyväksy palveluehdot valitsemalla valintaruutu ja valitse sitten **Asenna**.
15. Tila on Dynamics 365 -ympäristössä **Asennetaan**, kun asennus on käynnissä. Tilaksi päivitetään **Asennettu**, kun asennus on valmis.

##### <a name="review-and-apply-a-dual-write-solution"></a>Kaksoiskirjoitusratkaisun tarkistaminen ja käyttöönotto

1. Siirry uudessa talous- ja toimintosovellusympäristössä kohtaan **Tietojen hallinta \> Kaksoiskirjoitus**.
2. Valitse **Käytä ratkaisua**.
3. Valitse ruudusta **Asennetut Dynamics-ratkaisut**, **Kaksoiskirjoituksen sovellusytimen entiteettien yhdistämismääritykset** ja **Dynamics 365 Human Resources -kartat**. Valitse sitten **Käytä**. Viesti vahvistaa, että ratkaisua otetaan käyttöön. Kun ratkaisu on otettu onnistuneesti käyttöön, näet kaikki käytettävissä olevat taulukartat.
4. Tarkista käytettävissä olevat taulukartat ja valitse ja suorita integrointi käyttämällä kaksoiskirjoitusta.
5. Kun suoritat kaksoiskirjoituksen integroinnin ensimmäistä kertaa taulukartoille, valitse **Alkusynkronointi**-valintaruutu. Jos sinulla on Human Resources -lähdeympäristöstä peräisin oleva integraatio, sinun ei tarvitse valita **Alkusynkronointi**-valintaruutua, kun suoritat integroinnin taulukartoille.

#### <a name="recommended-practices"></a>Suositellut käytännöt

Tässä osiossa tarjotaan suosituksia siirtymisestä erillisestä infrastruktuurista talous- ja toimintosovellusinfrastruktuuriin.

- Suosittelemme vahvasti, että suoritat Human Resources -ympäristösi siirron Microsoft Dynamics -kumppanisi kanssa.
- Varaa tarpeeksi aikaa käyttäjien hyväksyntätestausta (UAT) varten siirretyssä eristysympäristössä.
- Suunnittele ja dokumentoi yksityiskohtaiset vaiheet siirtääksesi integroinnit siirrettyyn ympäristöön.
- Luo yksityiskohtainen tarkistusluettelo, joka kuvaa siirtosi edistymisen prosessin.
- Varaa tarpeeksi aika yrityksesi palvelukatkokseen, kun suoritat siirron.
- Suosittelemme vahvasti, että FastTrack-asiakkaat pyytävät FastTrack-ratkaisuarkkitehdiltään apua siirtoprosessin valvomiseen.
- Suosittelemme vahvasti, ett päivität eristysympäristösi erillisessä infrastruktuurissa ennen ensimmäisen siirron suorittamista. Tämän päivityksen tulisi sisältää Dataverse-ympäristösi, joka on yhdistetty siirron kohteena toimivaan eristysympäristöön.
- Suosittelemme vahvasti, että käytät Lifecycle Services -projektisi käyttöönottoon, siirtämiseen ja luomiseen palvelutiliä.
- Suunnittele eristysympäristön päivittäminen käyttäjien hyväksyntätestausta varten uusimmassa yleisen saatavuuden (GA) julkaisussa. Lisätietoja on [huomioitavissa asioissa](hr-infrastructure-merge.md#considerations).
