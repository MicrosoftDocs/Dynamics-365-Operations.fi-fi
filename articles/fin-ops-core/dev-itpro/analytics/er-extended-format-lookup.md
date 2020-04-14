---
title: Sähköisen raportoinnin (ER) laajennettu muodon haku
description: Tässä ohjeaiheessa esitellään, miten ER-muotoviite voidaan määrittää ER-muodon haussa, kun tarvittava muoto on tallennettu yleiseen tietovarastoon.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 28bdd02c25db27536a489f9e8ab2a91a5ca0f09c
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138857"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Salli käyttäjien määrittää ER-muotoviittaus, jolla kysytään muotoa yleisestä tietovarastosta

[!include [banner](../includes/banner.md)]

Voit käyttää [Sähköisen raportoinnin](general-electronic-reporting.md) (ER) kehystä määrittääksesi [muotoja](general-electronic-reporting.md#FormatComponentOutbound) lähteville asiakirjoille eri maiden ja alueiden lakisääteisten vaatimusten mukaan. Voit käyttää ER-kehystä myös [muotojen](general-electronic-reporting.md#FormatComponentInbound) määrittämiseen saapuvien asiakirjojen jäsentämistä ja kyseisten asiakirjojen tietojen sovellustietoihin liittämistä tai sovellustietojen päivittämistä varten. Kaikkia näitä muotoja voi käyttää Dynamics 365 Finance -esiintymässä saapuvien tai lähtevien liiketoiminta-asiakirjojen käsittelyyn osana tiettyjä liiketoimintaprosesseja. 

Tavallisesti sinun on määritettävä, mitä ER-muotoa on käytettävä tietyssä liiketoimintaprosessissa. Valitse tätä varten yksittäinen ER-muoto hakukentässä, joka on määritetty osana liiketoimintaprosessikohtaisia parametreja. Näitä hakukenttiä käytetään useimmiten asianmukaisen ER-kehyksen ohjelmointirajapinnan avulla. Lisätietoja on kohdassa [ER-kehyksen ohjelmointirajapinta – koodi muodon yhdistämismäärityksen haun näyttämistä varten](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Kun esimerkiksi määrität [ulkomaankaupan parametreja](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters), sinun on määritettävä viitteet yksittäisiin ER-muotoihin, joita käytetään Intrastat-ilmoituksen sekä Intrastat-ilmoituksen valvontaraportin luomiseen. Alla olevissa näyttökuvissa näkyy, miltä ER-muotojen hakukentät näyttävät **Ulkomaankaupan parametrit** -sivulla.

Jos kulloinenkin Finance-esiintymä ei sisällä Intrastat-liiketoimintaprosessiin liittyviä ER-muotoja, tämä hakukenttä on tyhjä.

[![Ulkomaankaupan parametrisivu](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Jos kulloinenkin Finance-esiintymä sisältää Intrastat-liiketoimintaprosessiin liittyviä ER-muotoja, tämä hakukenttä tarjoaa ER-muodot.

[![Ulkomaankaupan parametrisivu](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Tämä haku tarjoaa vain ne ER-muodot, jotka on jo tuotu kulloiseenkin Finance-esiintymään. [Tuodaksesi](./tasks/er-import-configuration-lifecycle-services.md) ER-ratkaisuja kulloiseenkin Finance-esiintymään sinulla on oltava käyttöoikeudet suorittaa asianmukainen ER-kehyksen toiminto, joka tukee ER-muotoja sisältävien ER-ratkaisujen [elinkaarta](general-electronic-reporting-manage-configuration-lifecycle.md).

Alkaen Financen versiosta 10.0.9 (huhtikuun 2020 julkaisu) ER-muodon haun käyttöliittymää, jota käytetään ER-kehyksen ohjelmointirajapinnan avulla, on laajennettu. Voit edelleen valita olemassa olevia ER-muotoja, jotka löydät **Valitse muotomääritys** -pikavälilehdestä. Tämän lisäksi laajennettu haku tarjoaa uuden mahdollisuuden etsi tiettyjä ER-muotoja yleisestä tietovarastosta. Kaikki yleisen tietovaraston ER-muodot esitetään **tuo yleisestä tietovarastosta** -pikavalikossa.

[![Ulkomaankaupan parametrisivu](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Samankaltaisesti kuin**Valitse muodon määritys** -pikavälilehti myös **Tuo yleisestä tietovarastosta**-pikavälilehdessä näkyvät vain sille liiketoimintaprosessille sopivat ER-muodot, jolle on valittu ER-muoto tässä hakukentässä. Tässä esimerkissä luodaan Intrastat-ilmoitus. ER-muoto on sovellettavissa sille yritykselle, johon käyttäjä on tällä hetkellä kirjautunut yrityksen maakontekstista riippuen.

Kun valitset **Tuo yleisestä tietovarastosta** -pikavälilehdestä ER-muodon, valitun ER-muodon [määritys](general-electronic-reporting.md#Configuration) tuodaan yleisestä tietovarastosta kulloiseenkin Finance-esiintymään.

[![Ulkomaankaupan parametrisivu](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Jos tuonti sitten saadaan suoritettua loppuun onnistuneesti, viite tuotuun ER-muotoon tallennettaan tähän hakukenttään. Huomaa, että kun käytät yleistä tietovarastoa ensimmäisen kerran, sinun on seurattava annettua linkkiä ja rekisteröidyttävä [Regulatory Configuration Serviceen](https://aka.ms/rcs) (RCS), jota käytetään yleisen tietovaraston käyttöoikeuksien hallintaan.

[![Ulkomaankaupan parametrisivu](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Oletusarvoisesti **Tuo yleisesti** -pikavälilehdessä näkyy yleisen tietovaraston sisällön perusteella suorituskykyparannuksia varten automaattisesti luotavan väliaikaisen tallennustilan ER-muotojen luettelo. Tämä tapahtuu, kun **Tuo yleisestä tietovarastosta** -pikavälilehti avataan ensimmäistä kertaa, mikä saattaa kestää useita sekunteja.

Jos et näe tarvittavaa ER-muotoa **Tuo yleisestä tietovarastosta** -pikavälilehdessä, mutta olet varma, että kyseinen ER-muoto on tallennettu yleiseen tietovarastoon, valitse vaihtoehto **Synkronoi**. Tämä päivittää väliaikaisen tallennustilan ja synkronoi yleisen tietovaraston kulloisenkin sisällön kanssa.

## <a name="feature-activation"></a>Ominaisuuden aktivointi

Tämän toiminnon käytettävyyttä ohjaa toiminto **ER:n muotomääritysten laajennettu haku, joka sallii kyselyt yleiseen tietovarastoon** kohdassa **Ominaisuuksien hallinta**. Tämä ominaisuus on oletusarvoisesti käytössä.

[![Toimintojen hallintasivu](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Tietojen suojaamisesta

**Ylläpidä määritystietovarastoja** (**ERMaintainSolutionRepositories**) -oikeus hallitsee yleisen tietovaraston käyttöoikeuksia sellaisten käyttäjien osalta, jotka avaavat ER-muotohaun käyttöön otetulla **Tuo yleisestä tietovarastosta** -pikavälilehdellä. Jotta käyttäjät voivat käyttää yleisen tietovaraston sisältöä ER-muotohauissa, sinun on muutettava käyttöoikeusasetuksia myöntämällä **ERMaintainSolutionRepositories**-oikeus käyttäjille joko suoraan tai käyttämällä jo osoitettuja rooleja ja velvollisuuksia.

Seuraavassa näyttökuvassa näkyy, miten tämä oikeus voidaan myöntää käyttäjille, joilla on **Kirjanpitäjä**-rooli. Tämän roolin avulla käyttäjät voivat määrittää ulkomaankaupan parametreja ja määrittää viitteitä ER-muotoihin kentissä **Tiedostomuodon yhdistämismääritys** ja **Raporttimuodon yhdistämismääritys** sivulla **Ulkomaankaupan parametrit**.

[![Suojauskonfiguraatiosivu](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Rajoitukset

Yleisen tietovaraston käyttöä ER-muotohaussa tuetaan tällä hetkellä vain sellaisten ER-muotojen valinnassa, joita käytetään lähtevien asiakirjojen luomiseen.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Miksi en voi käyttää yleistä tietovarastoa ER-muotohausta?

Jos olet ottanut **ER:n muotomääritysten laajennettu haku, joka sallii kyselyt yleiseen tietovarastoon** -ominaisuuden käyttöön **Ominaisuuksien hallinta** -sivulla, mutta käyttäjät eivät näe ER-muotoja **Tuo yleisestä tietovarastosta** -pikavälilehdessä ja **Synkronoi**-valinta näkyy muttei ole käytössä, varmista, että käyttäjälle on myönnetty **Ylläpidä määritystietovarastoja** **ERMaintainSolutionRepositories** -oikeus. Pyydä tätä oikeutta järjestelmänvalvojalta.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin (ER) kehysohjelmointirajapinta](er-apis-app73.md)
- [Sähköisen raportoinnin (ER) määritysten elinkaaren hallinta](general-electronic-reporting-manage-configuration-lifecycle.md)
