---
title: Vapauta varastoon
description: Tämä artikkeli sisältää tietoja varastoon vapauttamisen prosessista. Siinä kuvataan yksiköt, jotka luodaan, kun vapautat tilauksen varastoon sekä valinnat, joita voi käyttää prosessin käynnistämiseen.
author: Mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: caa38c4ed1c7fb8cf1ead3ba6534f8405a5ff57f
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428033"
---
# <a name="release-to-warehouse"></a>Vapauta varastoon

[!include [banner](../../includes/banner.md)]

Tämä artikkeli sisältää tietoja varastoon vapauttamisen prosessista. Siinä kuvataan yksiköt, jotka luodaan, kun vapautat tilauksen varastoon sekä valinnat, joita voi käyttää prosessin käynnistämiseen.

## <a name="release-to-warehouse-overview"></a>Varastoon vapauttamisen yhteenveto

Varastoon vapauttaminen on prosessi, jossa varastotuotteet valmistellaan lähetyskäsittelyä varten. Kun vapautat tilauksen varastoon, järjestelmä luo kuormarivit ja lähetykset. Jos automaattinen aallonkäsittely on määritetty, myös kuormat ja vaadittu työ luodaan. Asiaan liittyvien yksikköjen määritys riippuu järjestelmän asetuksista. Tässä artikkelin osassa käsitellään varastoon vapauttamisen aikana luotuja yksikköjä sekä ne määrittäviä järjestelmän asetuksia.

*Lähetys* on myynti- tai siirtotilausrivien ryhmä samalle asiakkaalle tai samalle toimitusosoitteelle.

*Kuorma* on ryhmä myynti- tai siirtotilausrivejä, jotka on ryhmitelty yhteen ja jotka yleensä kuljetetaan yksittäisellä kuorma-autolla, junavaunulla tai muulla kuljetustavalla. Kuorma voi koostua yhdestä tai useammasta lähetyksestä. Voit luoda kuorman manuaalisesti lisäämällä tilausrivejä uuteen kuormaan. Tällöin tilausrivit osoitetaan kuormalle ennen varastoon vapauttamisen prosessin aloittamista, ja ne voi vapauttaa vain **Kuormasuunnittelun työtila** -sivulla.

Varaston *työ* on mikä tahansa varastotoimenpide, jonka suorittaa varastotyöntekijä. Yleensä varastotyötoiminnot koostuvat vähintään kahdesta peräkkäisestä toiminnosta: varaston työntekijä keräilee käsillä olevan varaston yhdessä sijainnissa ja asettaa sen sitten toiseen paikkaan.

Kun tilauksia vapautetaan varastoon, järjestelmä luo *kuormarivejä* ja ryhmittelee ne lähetyksiksi. Lähetyksen konsolidointiprosessi mahdollistaa lähetyksen automaattisen konsolidoinnin varastoon vapauttamisen prosessin aikana. Lisätietoja: [Lähetyksen konsolidointikäytäntöjen yleiskatsaus](about-shipment-consolidation-policies.md).

Järjestelmä käyttää poimintatöiden ja lähetyskuormien luonnissa *aaltoja*. Luotavalle aaltotyypille ja tilausrivin varastolle on oltava käytettävissä *aaltomalli*. *Lähetys*-tyypin aaltomalleja käytetään myynti- ja siirtotilausten nimikkeiden lähettämiseen.

Jokainen aaltomalli sisältää *aaltomenetelmiä*. Aaltomenetelmät suorittavat toimintoja. Ne luovat esimerkiksi töitä aallolle tai kuormia. Esimerkiksi lähetysaaltojen aaltomalli voi sisältää menetelmiä kuormien luontiin, rivien liittämiseksi aaltoihin, täydentämiseen ja keräilytyön luomiseksi aallolle. Aaltomalli määrittää monia asetuksia sille, miten aallot luodaan ja käsitellään, mitä vaiheita on tehtävä manuaalisesti ja mitkä tehdään automaattisesti. Lisätietoja on kohdassa [Aaltomallit](wave-templates.md). Siksi riippuen aaltomallin määrityksestä joko luodaan, käsitellään ja vapautetaan aalto, kun vapautat tilauksen varastoon, tai osa tai kaikki nämä toiminnot suoritetaan manuaalisesti sen jälkeen, kun varastoon vapautus on tehty.

Kun aaltoa käsitellään, järjestelmä luo poimintatyötä soveltuvan *työmallin* ja *sijaintidirektiivin* perusteella ja asettaa tämän työn saataville mobiililaitteisiin. Työmalli määrittää, miten työt suoritetaan kunkin varastoprosessin osalta ja sijaintidirektiivi määrittää varastonsiirron poiminta- ja hyllytyspaikat. Lisätietoja on kohdassa [Varastotyön valvonta työmallien ja sijaintidirektiivien avulla](control-warehouse-location-directives.md).

> [!NOTE]
> Oletusarvoisesti aallot käsitellään erämuodossa.

Aallon käsittelyn aikana järjestelmä yleensä luo uuden kuorman kaikille lähetyksille, joihin ei vielä ole liitetty kuormaa. Jos haluat, että järjestelmä kohdistaa kohdistamattomia lähetyksiä sen sijaan olemassa oleviin kuormiin, voit käyttää edistynyttä aaltokuorman luontitoimintoa. Lisätietoja: [Edistynyt kuormanluonti aallon aikana](advanced-load-building-during-wave.md).

Sivuilla **Myyntitilaukset** ja **Siirtotilaukset** voit tarkastella yksikköjä, jotka on luotu tilausrivejä varten varastoon vapauttamisen prosessin aikana.

- **Myyntitilaukset**-sivu:

    - Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto** ja valitse sitten valikosta **Lähetystiedot** avataksesi asiaan liittyviä lähetyksiä, **Kuormatiedot** avataksesi asiaan liittyviä kuormia tai **Työtiedot** avataksesi asiaan liittyviä työtieoja.
    - Valitse **Rivitiedot**-pikavälilehdessä **Kuorma**-välilehti tarkastellaksesi asiaan liittyviä kuormia.

- **Siirtotilaukset**-sivu:

    - Avaa asiaan liittyvät lähetykset valitsemalla toimintoruudun **Lähetä**-välilehdessä **Lähetystiedot** tai asiaan liittyvät kuormat valitsemalla **Kuormatiedot**.
    - Avaa asiaan liittyvät työtiedot valitsemalla **Siirtotilausrivit**-pikavälilehdestä **Työtiedot**.

Kun tilaus lopulta vapautetaan varastoon, pisimmälle automatisoitu työnkulku toimii seuraavasti:

1. Järjestelmä luo lähetyksen tilaukselle ja aallolle.
1. Aalto käsitellään.
1. Järjestelmä luo kuorman ja työtunnuksen.

Aaltomalleista, työmalleista ja sijaintidirektiiviasetuksista riippuen jotkut tämän työnkulun vaiheet voivat olla manuaalisia. Kokonaistyönkulku pysyy kuitenkin samana.

Voit vapauttaa tilauksen varastoon usealla eri tavoilla. Voit suorittaa työvaiheen manuaalisesti tai voit määrittää erätyön. Tämän artikkelin jäljellä olevissa osissa tarkastellaan yksityiskohtaisesti eri tapoja, joilla varastoon vapauttaminen voidaan suorittaa.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Manuaalinen varastoon vapauttaminen Myyntitilaukset- ja Siirtotilaukset-sivuilta

Voit vapauttaa tilauksen varastoon suoraan **Myyntitilaukset**-sivulta tai **Siirtotilaukset**-sivulta valitsemalla **Vapauta varastoon**.

- **Myyntitilaukset**-sivulla painike on toimintoruudun **Varasto**-välilehdessä.
- **Siirtotilaukset**-sivulla painike on toimintoruudun **Lähetä**-välilehdessä.

**Myyntitilaukset**-sivulla voit vapauttaa useita myyntitilauksia samanaikaisesti.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Manuaalinen varastoon vapautus Vapauta varastoon -sivuilta

Järjestelmässä on tällä hetkellä kolme sivua, joilla voit tarkastella useiden tilausten rivejä ja vapauttaa niitä varastoon:

- **Vapauta varastoon** (**Varastonhallinta \> Vapauta varastoon \> Vapauta varastoon**) – tällä sivulla voit käsitellä sekä myynti- että siirtotilauksia. Se toimii kuitenkin hitaammin kuin kaksi muuta sivua. Tämä sivu poistetaan pian käytöstä.
- **Vapauta myyntitilauksia varastoon** (**Varastonhallinta \> Vapauta varastoon \> Vapauta myyntitilauksia varastoon**) – tällä sivulla voit käsitellä vain myyntitilauksia. Sen suorituskyky on kuitenkin parempi kuin **Vapauta varastoon** -sivun.
- **Vapauta siirtotilauksia varastoon** (**Varastonhallinta \> Vapauta varastoon \> Vapauta siirtotilauksia varastoon**) – tällä sivulla voit käsitellä vain siirtotilauksia. Sen suorituskyky on kuitenkin parempi kuin **Vapauta varastoon** -sivun.

Kaikilla kolmella sivulla on samat toiminnot, kuten tässä osassa kuvaillaan jäljempänä. Kaikkien niiden avulla voit valita tilausrivejä tai kokonaisia tilauksia ja vapauttaa ne varastoon.

Kukin sivu koostuu yläosasta, jossa voit valita tilausrivejä, sekä alaosasta, jossa voit aloittaa varastoon vapauttamisen prosessin. Yläosassa voit käyttää suodattimia hakeaksesi vapautettavia myyntitilauksia. **Vapauta varastoon**-sivulla on erillinen välilehti myyntitilauksia ja siirtotilauksia varten yläosassa, kun taas kahdella muulla sivulla näkyy vain yhdenlaisia tilauksia.

Yläosan työkalurivi sisältää seuraavat painikkeet, joita voi käyttää varastoon vapautettavien tilausrivien valitsemiseen:

- **Lisää** – Valitse vähintään yksi tilausrivi yläosasta ja siirrä valitut tilausrivit alaosaan tällä painikkeella.
- **Lisää kaikki** – Lisää kaikki rivit yläosasta alaosaan.
- **Lisää tilaus** – Valitse tilaus ja valitse sitten tämä painike, jotta kaikki kulloisenkin tilauksen rivit lisätään alaosaan.

Kun olet lisännyt haluamasi rivit alaosaan, merkitse kaikki vapautettavat rivit. Vapauta nämä rivit sitten varastoon valitsemalla työkalupakista **Vapauta varastoon**.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Manuaalinen varastoon vapautus Kuormansuunnittelu-työtilasivulta

Voit vapauttaa tilauksia varastoon manuaalisesti myös käyttäen **Kuormansuunnittelu**-sivua. Tällä sivulla voit järjestää tilausrivit kuormiksi ja vapauttaa nämä kuormat sitten varastoon.

Avaa **Kuormansuunnittelun työtila** -sivu siirtymällä kohtaan **Varastonhallinta \> Kuormat**. Voit myös avata sen **Myyntitilaukset**- ja **Siirtotilaukset**-sivuilta. Sivun yläosassa voit valita myyntitilausrivejä **Myyntirivit**-välilehdestä ja siirtotilausrivejä **Siirtorivit**-välilehdestä ja lisätä nämä rivit sitten uuteen tai aiemmin luotuun kuormaan.

Toimintoruudun **Tarjonta ja kysyntä** -välilehti sisältää seuraavat painikkeet, joita voit käyttää lisätessäsi yläosan tilausrivejä kuormaan:

- **Uuteen kuormaan** – Valitse tilausrivejä yläosasta ja luo tällä painikkeella uusi kuorma, johon valitut rivit lisätään.
- **Aiemmin luotuun kuormaan** – Valitse tilausrivejä yläosasta ja lisää valitut rivit aiemmin luotuun kuormaan tällä painikkeella.
- **Koko tilaus uuteen kuormaan** – Valitse tilauksia ja luo sitten tällä painikkeella uusi kuorma, johon kaikki näiden tilausten rivit lisätään.
- **Koko tilaus aiemmin luotuun kuormaan** – Valitse tilaus ja lisää sitten kyseisen tilauksen kaikki rivit aiemmin luotuun kuormaan tällä painikkeella.

Alaosassa voit tarkastella luotuja kuormia. Vapauta kuormia varastoon valitsemalla ne ja valitsemalla sitten työkalupalkissa **Vapauta \> Vapauta varastoon**. Jos käytät automaattista aaltojen käsittelyä, koska tilausriveille on jo määritetty kuormia, järjestelmä luo lähetyksiä ja työtunnuksia, kun varastoon vapauttamisen toiminto suoritetaan.

## <a name="automatic-release-to-the-warehouse"></a>Automaattinen varastoon vapauttaminen

Voit vapauttaa tilauksia varastoon automaattisesti käyttämällä tehtäviä **Myyntitilausten automaattinen vapautus** ja **Siirtotilausten automaattinen vapautus**.

Myyntitilauksia vapauttava erätyö määritetään seuraavalla tavalla.

1. Valitse **Varastonhallinta \> Vapauta varastoon \> Myyntitilausten automaattinen vapautus**.
1. Määritä **Myyntitilausten automaattinen vapautus** -valintaikkunan **Parametrit**-pikavälilehdessä seuraavat kentät:

    - **Vapautettava määrä** – Valitse, vapautetaanko varastoon koko määrä vai vain fyysisesti varattu määrä.
    - **Salli osittain vapautettujen tilausten vapautus** – Määritä, vapautetaanko osittain vapautettujen tilausten jäljellä olevat määrät varastoon.
    - **Säilytä varaukset, jos vapautus epäonnistuu** – Määritä, pysyvätkö myyntitilaukselle automaattisesti varatut määrät varattuna, jos varastoon vapauttamisen prosessi epäonnistuu.
    - **Ryhmittele julkaisut asiakkaan mukaan** – Määritä, käsitteleekö järjestelmä vapautus varastoon -toimintoja erikseen kullekin asiakkaalle vai vapautetaanko kaikki myyntitilaukset samanaikaisesti. Kun tämä vaihtoehto on arvossa *Kyllä*, järjestelmä kerää valitun asiakkaan kaikki myyntitilausrivit, vapauttaa kyseiset tilaukset varastoon ja käsittelee sitten seuraavan asiakkaan. Kun tämän vaihtoehdon arvo on *Ei*, järjestelmä vapauttaa kaikki käytettävissä olevat myyntitilausrivit yhtenä vapautuksena varastotoimintoihin. Tämän vaihtoehdon ottaminen käyttöön voi parantaa varastoonvapautusprosessin suorituskykyä ja vikasietoisuutta. Tätä vaihtoehtoa on käytettävä kuitenkin varoen yhdessä Käsittele aalto, kun se vapautetaan varastoon -tyyppisten aaltomallien kanssa, koska yhdistelmä voi luoda useita yhden asiakkaan aaltoja, joista kukin sisältää vain tälle asiakkaalle luodun työn. Jos haluat luoda työt, joissa eri asiakkaiden lähetykset yhdistetään, poista *Ryhmittele vapautukset asiakkaan mukaan* -vaihtoehto käytöstä tai määritä aaltomallit käyttämään lykättyä käsittelyä.
    - **Lukittu tilausten käsittely** – Valitse, miten järjestelmä käsittelee myyntitilaukset, jotka ovat lukittuna, koska muu käyttäjä tai prosessi muokkaa niitä:

        - *Odota tilausten avaamista* – Järjestelmän on odotettava tilausten avautumista, ennen kuin se vapauttaa ne varastoon. Tällöin varastoon vapauttamisen prosessi saattaa kestää kauemmin.
        - *Ohita lukitut tilaukset* – Järjestelmä ohittaa lukitut tilaukset.

    - **Kelvolliset tilaustyypit** – Valitse erään sisällytettävien myyntitilausten tyyppi.
    - **Luottorajatyyppi** – Valitse, tehdäänkö luottorajatarkastukset varastoon vapauttamisen prosessin aikana ja, jos tarkastukset tehdään, tarkastusten kohteena olevat tiedot.

1. Voit määrittää, mitkä tilaukset käsitellään, valitsemalla **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**. Näyttöön tulee vakiokyselyvalintaikkuna, jossa voit määrittää valintaehtoja, lajitteluehtoja ja liitoksia. Kentät toimivat samalla tavalla kuin muissakin kyselyissä Microsoft Dynamics 365 Supply Chain Managementissa.
1. **Suorita taustalla** -pikavälilehdessä valitse, suoritetaanko työ erätilassa, ja/tai määritä toistuva aikataulu. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.
1. Ota asetuksesi käyttöön ja aloita varastoon vapauttamisen prosessi valitsemalla **OK**.

Siirtotilauksia vapauttava erätyö määritetään seuraavalla tavalla.

1. Valitse **Varastonhallinta \> Vapauta varastoon \> Siirtotilausten automaattinen vapautus**.
1. Määritä **Siirtotilausten automaattinen vapautus** -valintaikkunan **Parametrit**-pikavälilehdessä seuraavat kentät:

    - **Vapautettava määrä** – Valitse, vapautetaanko varastoon koko määrä vai vain fyysisesti varattu määrä.
    - **Salli osittain vapautettujen tilausten vapautus** – Määritä, vapautetaanko osittain vapautettujen tilausten jäljellä olevat määrät varastoon.
    - **Ryhmittele tiedot kohdevaraston mukaan** – Määritä, vapauttaako järjestelmä kaikki siirtotilaukset samanaikaisesti vai ryhmitelläänkö siirtotilausrivit kohdevaraston mukaan ja vapautetaan sitten kukin ryhmä varastoon erikseen.

1. Voit määrittää, mitkä tilaukset käsitellään, valitsemalla **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**. Näyttöön tulee vakiokyselyvalintaikkuna, jossa voit määrittää valintaehtoja, lajitteluehtoja ja liitoksia. Kentät toimivat samalla tavalla kuin muissakin kyselyissä Supply Chain Managementissa.
1. **Suorita taustalla** -pikavälilehdessä valitse, suoritetaanko työ erätilassa, ja/tai määritä toistuva aikataulu. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.
1. Ota asetuksesi käyttöön ja aloita varastoon vapauttamisen prosessi valitsemalla **OK**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
