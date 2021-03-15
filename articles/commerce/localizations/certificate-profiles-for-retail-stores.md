---
title: Käyttäjän määrittämät vähittäismyymälöiden varmenneprofiilit
description: Tässä ohjeaiheessa on yleiskatsaus varmenteiden käytöstä vähittäismyymälöissä.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 81fa3770a137471e3d7f8cab3c7d7f37febe64fa
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018865"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Käyttäjän määrittämät vähittäismyymälöiden varmenneprofiilit

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>Yleiskuvaus

Tämä ohjeaihe on yleiskatsaus varmenneprofiileista, jotka ovat käytettävissä Microsoft Dynamics 365 Commercessa. Tämä toimintaa laajentaa [Vähittäismyyntikanavien salaisuuksien hallinta](../dev-itpro/manage-secrets.md) -ominaisuutta lisäämällä paikallisten varmenteiden tuen.

Jos myyntipistettä käytetään offline-tilassa, se voi käyttää avainsäilöön tallennettuja varmenteita. Silloin onkin käytettävä paikallista varmennetta. Tuetut ominaisuudet:

- Paikallisten varmenteiden käyttö avainsäilön varmistusskenaarioissa
- Paikallisten varmenteiden käyttö ilman avainsäilöä (esimerkiksi paikallisessa asennuksessa)
- Varmenteiden vähittäinen päivitys, jolloin joissakin myymälöissä ja päätteissä on käytössä varmenteen uusi versio mutta joissakin myymälöissä ja päätteissä jatketaan edellisen version käyttöä

Varmenneprofiilitoiminnolla voi määrittää oletusvarmenteen ja määrittää, missä järjestyksessä varmenteita haetaan samassa varmenneprofiilissa. Toiminto mahdollistaa myös samankaltaisen paikallisten varmenteiden ja Key Vault -varmenteiden määrittämisen. Voit lisätä varmenteille yrityskohtaiset asetukset, mutta Commerce-kanavissa voidaan käyttää kunkin varmenteen osalta yksilöivää yritystenvälistä tunnusta.

### <a name="scenarios"></a>Skenaariot

Varmenneprofiilitoiminto tukee seuraavia skenaarioita Commerce-kanavissa:

- Paikallisen varmenteen käyttö avainsäilön varmistusskenaarioissa. Esimerkkejä varmistusskenaarioista:

    - Avainsäilötallennusta ei voi käyttää.
    - Varmennetta ei löydy avainsäilötallennuksesta.
    - Myyntipistettä käytetään offline-tilassa.

- Paikallisten varmenteiden käyttö tallentamatta niitä avainsäilöön (esimerkiksi paikallisessa asennuksessa).
- Varmenteiden vähittäinen päivitys, jolloin varmenteen uutta versiota käytetään vain niissä myymälöissä tai terminaaleissa, jos uusi versio on jo saatavana.
- Samaa varmennetta käytetään useissa yrityksissä.

## <a name="set-up-certificate-profiles"></a>Varmenneprofiilien määrittäminen

Seuraavissa ohjeissa käsitellään varmenneprofiilien määrittämistä. Määritä asetukset seuraavien ohjeiden mukaisesti, ennen kuin käytät varmenneprofiileja Commerce-kanavissa.

1. Ota **Käyttäjän määrittämät vähittäismyymälöiden varmenneprofiilit** -ominaisuus käyttöön **Ominaisuuksien hallinta** -työtilassa.
2. Valitse **Järjestelmän hallinta \> Asetukset \> Varmenneprofiilit**.
3. Luo tietue ja määritä sen **Varmenneprofiili**-, **Nimi**- ja **Kuvaus**-kentät.

    > [!NOTE]
    > Varmenneprofiili on varmenteen yksilöivä tunnus kaikissa yrityksissä ja Commerce-komponenteissa.

3. Lisää **Yritykset**-välilehdessä rivi ja valitse yritys, jossa nykyistä varmenneprofiilia on käytettävä. Jos varmenneprofiilia käytetään useissa yrityksissä, lisää rivi kullekin yritykselle toistamalla tämä vaihe.
4. Valitsemalla **Asetukset** voit avata **Varmenneprofiilin asetukset** -sivun, jossa voit antaa varmenneprofiilin yrityskohtaiset asetukset.

### <a name="certificate-profile-settings"></a>Varmenneprofiilin asetukset

Kun valitset varmenneprofiiliriveille **Asetukset**, **Varmenneprofiilin asetukset**-sivu avautuu. Voit määrittää tällä sivulla, mitä varmenteita käytetään, kun nykyistä varmenneprofiilia kutsutaan Commerce-kanavissa. Voit määrittää myös järjestyksen, jossa varmenteita haetaan.

> [!NOTE]
> **Prioriteetti**-kenttä määritetään automaattisesti. Arvo **1** ilmaisee korkeimman prioriteetin. Kun uusi rivi lisätään **Varmenneprofiilin asetukset** -sivulla, sen prioriteetiksi luku, joka on yhden suurempi kuin edellisen rivin prioriteetti. Voit muuttaa tietyn rivin prioriteettia valitsemalla ensin riviin ja sitten joko **Siirrä ylös**, joka nostaa prioriteettia, tai **Siirrä alas**, joka laskee prioriteettia.

Voit määrittää seuraavat kentät, kun lisäät uuden rivin **Varmenneprofiilin asetukset** -sivulla:

- **Sijainnin tyyppi** – Valitse varmenteen tallennussijainti. Kentällä on kaksi arvoa: **paikallinen varmenne** ja **Key Vault**.
- **Key Vault -varmenne** – Tämä kenttä on pakollinen, jos **Sijainnin tyyppi** -kentän arvo on **Key Vault**. Sen avulla määritetään Key Vault -varmenteen salainen koodi.

    > [!NOTE]
    > Varmista ennen Key Vault -varmenteen käyttöä varmenneprofiileissa, että varmenne on ladattu avainsäilötallennukseen ja nouda ohjeita kohdassa [Azure Key Vault -asiakasohjelman määrittäminen](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).

- **Myymälän nimi** – Tämä kenttä on valinnainen ja käytettävissä vain, jos **Sijainnin tyyppi** -kentän arvo on **Paikallinen varmenne**. Määritä sen avulla oletusmyymälän nimi, jolla haetaan paikallisia varmenteita.
- **Myymälän sijainti** – Tämä kenttä on valinnainen ja käytettävissä vain, jos **Sijainnin tyyppi** -kentän arvo on **Paikallinen varmenne**. Määritä sen avulla oletusmyymälän sijainti, jolla haetaan paikallisia varmenteita.

    > [!NOTE]
    > Oletusmyymälän nimi ja sijainti lisätään yksinkertaistamaan paikallisten varmenteiden hakuprosessia Commerce Runtime -palvelussa. X509StoreProvider sisältää kansioluettelon, johon varmenteen tallennetaan. Jos oletusmyymälän nimeä ja sijaintia ei ole määritetty, X509StoreProvider yrittää löytää varmenteen luettelon muista kansioista.

- **Allekirjoitus** – Tämä kenttä on pakollinen ja käytettävissä vain, jos **Sijainnin tyyppi** -kentän arvo on **Paikallinen varmenne**. Käytetään määrittämään varmenteen allekirjoitus.
- **Kommentit** – käyttäjät voivat lisätä muistiinpanoja tähän valinnaiseen kenttään.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Työnkulku: varmenteiden hakeminen Commerce Runtime -palvelussa

Seuraavalla perustyönkululla haetaan varmennetta, kun varmenneprofiili kutsutaan Commerce Runtime -palvelussa.

1. Järjestelmä määrittää, onko varmenneprofiilissa nykyisen yrityksen yrityskohtaisia asetuksia.
1. Järjestelmä yrittää etsiä varmennetta käyttämällä **Varmenneprofiilin asetukset** -arvoja rivillä, jonka **Prioriteetti**-kentän asetus **1**.

    - Jos **Sijainnin tyyppi** -kentän asetuksena on **Key Vault**, **Key Vault -varmenteen salainen koodi** -kentän arvoa käytetään hakemaan varmenne **Avainsäilön parametrit** -sivulla. Varmennetta haetaan sitten avainsäilötallennuksesta.
    - Jos **Sijainnin tyyppi** -kentän asetuksena on **Paikallinen varmenne**, X509StoreProvider hakee varmennetta ensin käyttämällä oletusmyymälän nimeä ja sijaintia, jos nämä parametrit on määritetty. Se tekee sen jälkeen hakuja kaikissa muissa kansioluettelon kansioissa.

1. Jos varmennetta ei löydy, prosessi toistetaan rivillä, jonka **Prioriteetti**-kentän asetuksena on **2**, ja niin edelleen.

> [!NOTE]
> Jos varmenneprofiililla ei ole asetuksia nykyisessä yrityksessä tai jos varmennehaku epäonnistuu kaikilla **Varmenneprofiilin asetukset** -sivun riveillä, varmennetta ei löytynyt.

#### <a name="caching-the-results-of-certificate-searches"></a>Varmennehakujen tulosten tallentaminen välimuistiin

Varmennehakujen tulokset tallennetaan välimuistiin. Välimuisti vanhenee oletusarvoisesti tunnissa. Tätä aikaa voi kuitenkin mukauttaa, ja enimmäisarvo on 24 tuntia.

### <a name="gradual-update"></a>Asteittainen päivitys

Jos varmenteen uusi versio on otettu käyttöön, mutta sitä ei voi päivittää kaikissa myymälöissä samanaikaisesti, varmenneprofiilitoiminnot mahdollistavat varmenteen asteittaisen päivityksen.

1. Etsi päivitettävä varmenneprofiili ja rivi ja valitse sitten **Asetukset**.
1. Lisää rivi ja määritä varmenteen uusimpaan versioon liittyvät asetukset.
1. Suurenna uuden rivin **Prioriteetti**-arvoa. Siirrä riviä ylöspäin **Siirrä ylös** -painikkeella siten, että se on saman varmenteen edellisen version rivin yläpuolella.

> [!NOTE]
> Varmenteen uusi versio kutsutaan Commerce Runtimessa ensimmäisenä. Jos varmennetta ei ole vielä päivitetty jossain myymälässä tai päätteessä, edellinen versio kutsutaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]