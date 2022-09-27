---
title: Käyttäjän määrittämät vähittäismyymälöiden varmenneprofiilit
description: Tämä artikkeli on yleiskatsaus varmenneprofiileista, jotka ovat käytettävissä Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558434"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Käyttäjän määrittämät vähittäismyymälöiden varmenneprofiilit

[!include [banner](../includes/banner.md)]

Tämä artikkeli on yleiskatsaus varmenneprofiileista, jotka ovat käytettävissä Microsoft Dynamics 365 Commercessa. Tämä toimintaa laajentaa [Vähittäismyyntikanavien salaisuuksien hallinta](../dev-itpro/manage-secrets.md) -ominaisuutta lisäämällä paikallisten varmenteiden tuen.

Jos myyntipistettä käytetään offline-tilassa, se voi käyttää Microsoft Azure Key Vaultiin tallennettuja varmenteita. Silloin onkin käytettävä paikallista varmennetta. Tuetut ominaisuudet:

- Paikallisten varmenteiden käyttö Key Vaultin varmistusskenaarioissa
- Paikallisten varmenteiden käyttö ilman Key Vaultia (esimerkiksi paikallisessa asennuksessa)
- Varmenteiden vähittäinen päivitys, jolloin joissakin myymälöissä ja päätteissä on käytössä varmenteen uusi versio mutta joissakin myymälöissä ja päätteissä jatketaan edellisen version käyttöä

Varmenneprofiilitoiminnolla voi määrittää oletusvarmenteen ja määrittää, missä järjestyksessä varmenteita haetaan samassa varmenneprofiilissa. Toiminto mahdollistaa myös samankaltaisen paikallisten varmenteiden ja Key Vault -varmenteiden määrittämisen. Voit lisätä varmenteille yrityskohtaiset asetukset, mutta Commerce-kanavissa voidaan käyttää kunkin varmenteen osalta yksilöivää yritystenvälistä tunnusta.

### <a name="scenarios"></a>Skenaariot

Varmenneprofiilitoiminto tukee seuraavia skenaarioita Commerce-kanavissa:

- Paikallisen varmenteen käyttö Key Vaultin varmistusskenaarioissa. Esimerkkejä varmistusskenaarioista:

    - Avainsäilötallennusta ei voi käyttää.
    - Varmennetta ei löydy avainsäilötallennuksesta.
    - Myyntipistettä käytetään offline-tilassa.

- Paikallisten varmenteiden käyttö tallentamatta niitä Key Vaultiin (esimerkiksi paikallisessa asennuksessa).
- Varmenteiden vähittäinen päivitys, jolloin varmenteen uutta versiota käytetään vain niissä myymälöissä tai terminaaleissa, jos uusi versio on jo saatavana.
- Samaa varmennetta käytetään useissa yrityksissä.

## <a name="set-up-certificate-profiles"></a>Varmenneprofiilien määrittäminen

Seuraavissa ohjeissa käsitellään varmenneprofiilien määrittämistä.

### <a name="set-up-key-vault"></a>Key Vaultin määrittäminen

Seuraavat vaiheet on suoritettava, ennen kuin voit käyttää Key Vaultiin tallennettua digitaalista varmennetta.

1. Luo Key Vault-tallennustili. On suositeltavaa käyttöönottaa tallennustili samalla maantieteellisellä alueella kuin Commerce Scale Unit.
1. Lataa digitaalinen varmenne Key Vault -tallennustiliin.
1. Anna Application Object Server (AOS) -sovelluksella valtuudet lukea salaisia koodeja Key Vault -tallennustilasta.

Lisätietoja Key Vaultin käyttämisestä: [Azure Key Vaultin käytön aloittaminen](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Määritä järjestelmän parametrit

Ennen kuin voit määrittää varmenteen profiilit Commerce-kanavissa, ota käyttöön Commerce sekä Key Vaultiin että varmenteen profiileihin tallennetuissa varmenteissa.

Voit määrittää järjestelmän parametrit Commerce headquartersissa alla olevien vaiheiden mukaisesti.

1. Määritä **Järjestelmäparametrit**-sivulla **Käytä edistyksellistä varmennesäilöä** -vaihtoehdon arvoksi **Kyllä**.
1. Ota **Käyttäjän määrittämät vähittäismyymälöiden varmenneprofiilit** -ominaisuus käyttöön **Ominaisuuksien hallinta** -työtilassa.

### <a name="set-up-key-vault-parameters"></a>Key Vault -parametrien määrittäminen

Määritä **Key Vault -parametrit** -sivulla seuraavat parametrit Key Vault -tallennustilan käyttämistä varten:

- **Nimi** ja **Kuvaus** – Key Vault -tallennustilin nimi ja kuvaus.
- **Key Vault URL** – Key Vault -tallennustilin URL-osoite.
- **Key Vault -asiakasohjelma** - Key Vault -tallennustiliin liittyvän Azure Active Directory (Azure AD) -sovelluksen vuorovaikutteinen asiakastunnus todennusta varten. Asiakasohjelman tulisi pysytä lukea salaisia koodeja tallennustililtä.
- **Key Vaultin salainen avain** – Azure AD -sovellukseen liittyvä salainen avain, jota käytetään Key Vault -tallennustilin todennusta varten.
- **Nimi**, **Kuvaus** ja **Salainen viite** – Sertifikaatin nimi, kuvaus ja salainen viittaus.

Lisätietoja: [Azure Key Vault -asiakasohjelman määrittäminen](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Varmenneprofiilin määrittäminen

Voit määrittää varmenneprofiilin Commerce headquarters -sovelluksessa alla olevien vaiheiden avulla.

1. Valitse **Järjestelmän hallinta \> Asetukset \> Varmenneprofiilit**.
1. Luo tietue valitsemalla toimintoruudussa **Uusi**.
1. Anna arvot **Varmenneprofiili**-, **Nimi**- ja **Kuvaus**-kenttiin.

    > [!NOTE]
    > Varmenneprofiili on varmenteen yksilöivä tunnus kaikissa yrityksissä ja Commerce-komponenteissa.

1. Lisää rivi valitsemalla **Yritykset**-pikavälilehdessä **Lisää**.
1. Valitse **Yritys**-kohdassa yritys, jossa nykyistä varmenneprofiilia on käytettävä.

    Jos varmenneprofiilia käytetään useissa yrityksissä, lisää rivi kullekin yritykselle toistamalla tämä vaiheet 4 ja 5.

1. Valitsemalla **Asetukset** voit avata **Varmenneprofiilin asetukset** -sivun, jossa voit antaa varmenneprofiilin yrityskohtaiset asetukset. Määritä, mitä varmenteita käytetään, kun nykyistä varmenneprofiilia kutsutaan Commerce-kanavissa. Lisää haluamasi määrä varmenteita ja määritä niiden prioriteetit. Jos korkean tason varmenne ei ole käytettävissä, käytetään seuraavaa varmennetta prioriteetin perusteella. Lisätietoja on [Työnkulku: varmenteiden hakeminen Commerce Runtime -palvelussa](#workflow-searching-certificates-in-the-commerce-runtime) -osassa.

    > [!NOTE]
    > **Prioriteetti**-kenttä määritetään automaattisesti. Arvo **1** ilmaisee korkeimman prioriteetin. Kun uusi rivi lisätään **Varmenneprofiilin asetukset** -sivulla, sen prioriteetiksi luku, joka on yhden suurempi kuin edellisen rivin prioriteetti. Voit muuttaa tietyn rivin prioriteettia valitsemalla ensin riviin ja sitten joko **Siirrä ylös**, joka nostaa prioriteettia, tai **Siirrä alas**, joka laskee prioriteettia.

1. Voit määrittää seuraavat kentät, kun lisäät uuden rivin **Varmenneprofiilin asetukset** -sivulla:

    - **Sijainnin tyyppi** – Valitse varmenteen tallennussijainti. Kentällä on kaksi arvoa: **paikallinen varmenne** ja **Key Vault**.
    - **Key Vault -varmenne** – Tämä kenttä on pakollinen, jos **Sijainnin tyyppi** -kentän arvo on **Key Vault**. Sen avulla määritetään Key Vault -varmenteen salainen koodi.
    - **Myymälän nimi** – Tämä kenttä on valinnainen ja käytettävissä vain, jos **Sijainnin tyyppi** -kentän arvo on **Paikallinen varmenne**. Määritä sen avulla oletusmyymälän nimi, jolla haetaan paikallisia varmenteita.
    - **Myymälän sijainti** – Tämä kenttä on valinnainen ja käytettävissä vain, jos **Sijainnin tyyppi** -kentän arvo on **Paikallinen varmenne**. Määritä sen avulla oletusmyymälän sijainti, jolla haetaan paikallisia varmenteita.

        > [!NOTE]
        > Oletusmyymälän nimi ja sijainti lisätään yksinkertaistamaan paikallisten varmenteiden hakuprosessia Commerce Runtime -palvelussa. X509StoreProvider sisältää kansioluettelon, johon varmenteen tallennetaan. Jos oletusmyymälän nimeä ja sijaintia ei ole määritetty, X509StoreProvider yrittää löytää varmenteen luettelon muista kansioista. Lisätietoja myymälän nimen ja sijainnin käytettävissä olevista arvoista on kohdissa [StoreName-luettelointi](/dotnet/api/system.security.cryptography.x509certificates.storename) ja [StoreLocation-luettelointi](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Allekirjoitus** – Tämä kenttä on pakollinen ja käytettävissä vain, jos **Sijainnin tyyppi** -kentän arvo on **Paikallinen varmenne**. Käytetään määrittämään varmenteen allekirjoitus.

        > [!IMPORTANT]
        > Varmista, että sovellusta käyttävällä käyttäjällä, jolla on oltava paikallinen varmenne (esimerkiksi Modern POS offline-tilassa), on vähintään vain luku -oikeus varmenteen yksityiseen avaimeen.

    - **Kommentit** – käyttäjät voivat lisätä muistiinpanoja tähän valinnaiseen kenttään.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Työnkulku: varmenteiden hakeminen Commerce Runtime -palvelussa

Seuraavalla perustyönkululla haetaan varmennetta, kun varmenneprofiili kutsutaan Commerce Runtime -palvelussa.

1. Järjestelmä määrittää, onko varmenneprofiilissa nykyisen yrityksen yrityskohtaisia asetuksia.
1. Järjestelmä yrittää etsiä varmennetta käyttämällä **Varmenneprofiilin asetukset** -arvoja rivillä, jonka **Prioriteetti**-kentän asetus **1**.

    - Jos **Sijainnin tyyppi** -kentän asetuksena on **Key Vault**, **Key Vault -varmenteen salainen koodi** -kentän arvoa käytetään hakemaan varmenne **Avainsäilön parametrit** -sivulla. Varmennetta haetaan sitten avainsäilötallennuksesta.
    - Jos **Sijainnin tyyppi** -kentän asetuksena on **Paikallinen varmenne**, X509StoreProvider hakee varmennetta ensin käyttämällä oletusmyymälän nimeä ja sijaintia, jos nämä parametrit on määritetty. Se tekee sen jälkeen hakuja kaikissa muissa kansioluettelon kansioissa.

1. Jos varmennetta ei löydy, prosessi toistetaan rivillä, jonka **Prioriteetti**-kentän asetuksena on **2**, ja niin edelleen.

> [!NOTE]
> Jos varmenneprofiililla ei ole asetuksia nykyisessä yrityksessä tai jos varmennehaku epäonnistuu kaikilla **Varmenneprofiilin asetukset** -sivun riveillä, varmennetta ei löytynyt.

### <a name="caching-the-results-of-certificate-searches"></a>Varmennehakujen tulosten tallentaminen välimuistiin

Varmennehakujen tulokset tallennetaan välimuistiin. Välimuisti vanhenee oletusarvoisesti tunnissa. Tätä aikaa voi kuitenkin mukauttaa, ja enimmäisarvo on 24 tuntia.

## <a name="gradual-update"></a>Asteittainen päivitys

Jos varmenteen uusi versio on otettu käyttöön, mutta sitä ei voi päivittää kaikissa myymälöissä samanaikaisesti, varmenneprofiilitoiminnot mahdollistavat varmenteen asteittaisen päivityksen.

1. Etsi päivitettävä varmenneprofiili ja rivi ja valitse sitten **Asetukset**.
1. Lisää rivi ja määritä varmenteen uusimpaan versioon liittyvät asetukset.
1. Suurenna uuden rivin **Prioriteetti**-arvoa. Siirrä riviä ylöspäin **Siirrä ylös** -painikkeella siten, että se on saman varmenteen edellisen version rivin yläpuolella.
> [!NOTE]
> Varmenteen uusi versio kutsutaan Commerce Runtimessa ensimmäisenä. Jos varmennetta ei ole vielä päivitetty jossain myymälässä tai päätteessä, edellinen versio kutsutaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
