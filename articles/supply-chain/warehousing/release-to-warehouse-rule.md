---
title: Vapauta varastoon -sääntö
description: Tässä ohjeaiheessa on tietoja vapauta varastoon -sääntöominaisuudesta, joka mahdollistaa joustavuuden varastoon vapauttaessa. Se lisää konfigurointivaihtoehdon, joka määrittää, salliko järjestelmä osittaisten varattujen tilausrivien vapauttamisen.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5fef1d942f2e9d3467fb8a00c6d89cc5c018a5aa
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674614"
---
# <a name="release-to-warehouse-rule"></a>Vapauta varastoon -sääntö

[!include [banner](../includes/banner.md)]

*Vapauta varastoon -sääntö* -toiminto antaa joustavuutta varastoon vapauttaessa. Se lisää kullekin varastolle konfigurointivaihtoehdon. Tämän vaihtoehdon avulla voit määrittää, voidaanko kyseiselle varastolle vapauttaa osittain varattuja tilausrivejä. Ominaisuus toimii yhdessä kehittyneiden cross-docking-toimintojen kanssa tilanteissa, joissa osa tilausrivin määrästä on merkitty toimituslähteeseen, mutta jäljelle jäävä osa voidaan käsitellä varastossa. Tämän vuoksi rivi voidaan vapauttaa niin, että käytettävissä olevan varastomäärän varastokäsittely voi jatkua.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Vapautuksen ottaminen käyttöön ja alustaminen varastosääntötoimintoon

### <a name="turn-on-the-feature"></a>Toiminnon ottaminen käyttöön

Ennen kuin voit käyttää *Vapauta varastoon -sääntö* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Ominaisuuden nimi:** *Vapauta varastoon -sääntö*

### <a name="initialize-the-feature"></a>Toiminnon alustaminen

Kun toiminto on otettu käyttöön järjestelmässä, se on alustettava siten, että sääntö on kaikkien varastojen oikea alkutila.

- Jos varastot eivät ole käytössä varastonhallinnassa, säännön arvoksi määritetään aluksi **Ei sovellettavissa**.
- Jos varastot ovat käytössä varastonhallinnassa, säännön arvoksi määritetään aluksi **Salli osittainen varaus**

Jos haluat alustaa toiminnon ja määrittää kaikkien varastojen vapauta varastoon -säännön, toimi seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. **Valitse varastonhallinnan parametrit** -sivun **Yleiset**-välilehden **Yrityksen tiedot** -osassa **Valmistele vapauta varastoon** -säännön linkki. (Jos tätä linkkiä ei näy, joko toiminto ei ole käytössä tai se on jo alustettu.)
1. Kun järjestelmä pyytää vahvistamaan toiminnon, alusta toiminto valitsemalla **Kyllä**.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Määritä kukin varaston vapauta varastoon -sääntö

Kun ominaisuus on otettu käyttöön ja alustettu, kaikilla varastollasi on alkuasetus, kuten edellisessä osassa on kuvattu. Voit muuttaa tätä asetusta yksittäisille varastoille noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Varastot**.
1. Valitse määritettävä varasto.
1. Valitse **Muokkaa**, jotta saat sivun muokkaustilaan.
1. **Varaston varausvaatimus** -kenttä määrittää, onko tilauksen osittainen vapauttaminen sallittu **Varasto**-pikavälilehden **Varaukset**-osassa. Valitse jokin seuraavista:

    - **Ei käytettävissä** – Kun ominaisuus otetaan ensimmäisen kerran käyttöön ja alustetaan, tämä arvo määritetään automaattisesti kaikille varastoille, jotka eivät ole käytössä varastonhallinnassa. Arvoa ei voi muuttaa. Tämä arvo ei ole käytettävissä varastoissa, jotka on otettu käyttöön varastonhallinnassa.
    - **Salli osittainen varaus** – Tilaukset voidaan vapauttaa, kun määrä varataan. Järjestelmä arvioi, onko varauksettoman määrän oltava merkitty pitkälle cross-dockingia varten, ja merkitsee määrän tarpeen mukaan. Jos merkintää ei ole, järjestelmä luo työn vain varattua määrää varten. Kun ominaisuus otetaan ensimmäisen kerran käyttöön ja alustetaan, tämä arvo määritetään automaattisesti kaikille varastoille, jotka ovat käytössä varastonhallinnassa. Tämä arvo ei ole käytettävissä varastoissa, joita ei ole otettu käyttöön varastonhallinnassa.
    - **Vaadi täysi varaus** – Tilaukset voidaan vapauttaa vain, jos koko määrä on varattu. Niitä ei voi vapauttaa, jos kokonaismäärä ei ole fyysisesti varattu tai suunniteltu cross-dockingia varten. Tämä arvo ei ole käytettävissä varastoissa, joita ei ole otettu käyttöön varastonhallinnassa.

1. Valitse **Tallenna**.

## <a name="scenarios"></a>Skenaariot

Tässä osassa on kaksi skenaariota, joiden avulla voit selvittää, mitä toiminto tekee ja miten sitä käytetään.

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

Näiden skenaarioiden käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

Voit hyödyntää näitä skenaarioita ominaisuuden ohjeena, kun työskentelet tuotantojärjestelmän parissa. Tässä tapauksessa sinun on kuitenkin korvattava omat arvosi, ja sinulta saattaa puuttua joitakin pakollisia tietoja, joita vakiodemotiedot sisältävät.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>Skenaario 1: Vaadi täysi julkaisu (ei suunniteltua cross-dockingia)

Tämä skenaario näyttää, miten toiminto toimii sellaisissa varastoissa, joiden arvoksi on määritetty **Vaadi täysi varaus**.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Varastot**.
1. Jos kyseessä on varasto _62_, määritä **varaston varaustarve** -kentän arvoksi **edellyttää täyttä varausta**, joka on kuvattu aiemmin tässä ohjeaiheessa olevan [Määritä vapautus fyysiseen varastoon](#set-option-warehouse) -säännön mukaisesti.
1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo uusi myyntitilaus valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi _US-004_.
    - Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi _62_.

1. Valitse **OK** luodaksesi uuden ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilauksesi avataan. **Myyntitilausrivit**-osan ruudukko sisältää tyhjän rivin. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *2*

1. Lisää uusin rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:

    - **Nimiketunnus:** *A0002*
    - **Määrä** *2*

1. Valitse ensimmäinen tilausrivi ja valitse sitten ruudukon yläpuolella olevasta **Varasto**-valikosta **Varaus**.
1. Valitse **Varaus**-sivulla **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Älä varaa toista tilausriviä.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.
1. Huomaa, että näyttöön tulee seuraava virhesanoma: Koko määrän on oltava fyysisesti varattu. Siksi järjestelmä ei luo tilaukselle mitään työtä, toimitusta tai kuormitusta.

    > [!NOTE]
    > Näyttöön tulee sama virhesanoma, jos varaat toisen rivin osittain.

### <a name="scenario-2-allow-partial-release"></a>Skenaario 2: osittaisen vapautuksen salliminen

Tämä skenaario näyttää, miten toiminto toimii sellaisissa varastoissa, joiden arvoksi on määritetty **Salli osittainen vapautus**.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Varastot**.
1. Jos kyseessä on varasto _62_, määritä **varaston varaustarve** -kentän arvoksi **Salli osittainen varaus**, joka on kuvattu aiemmin tässä ohjeaiheessa olevan [Määritä vapautus fyysiseen varastoon](#set-option-warehouse) -säännön mukaisesti.
1. Kuten teit [edellisessä skenaariossa](#scenario1), siirry kohtaan **Myynti- ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset** ja luo myyntitilaus asiakastilille _US-004_ varastosta _62_. Lisää seuraavat kaksi tilausriviä:

    - **Rivi 1:** Aseta **Nimiketunnus**-kentän arvoksi _A0001_, **Määrä**-kentän arvoksi _2_ ja **Yksikkö**-kentän arvoksi _kpl_.
    - **Rivi 2:** Aseta **Nimiketunnus**-kentän arvoksi _A0002_, **Määrä**-kentän arvoksi _2_ ja **Yksikkö**-kentän arvoksi _kpl_.

1. Kuten teit [edellisessä skenaariossa](#scenario1), varaa rivin 1 koko tilausmäärä, mutta älä varaa tilausriviä 2.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.
1. Huomaa, että et saa virhesanomaa tällä kertaa. Sen sijaan järjestelmä luo työt, lähetykset ja kuormat tarpeen mukaan ja näyttää tulokset.
1. Voit tarkastella lähetyksen, kuormituksen ja työmäärän tietoja käyttämällä ruudukon yläpuolella olevia **Varastointi**-valikon vaihtoehtoja:

    - **Rivi 1:** Käytettävissä on kolme vaihtoehtoa: **Lähetyksen tiedot**, **Kuormitustiedot** ja **Työtiedot**. Valitse kukin vaihtoehto, jos haluat nähdä tiedot lähetyksestä, kuormituksesta ja työstä, jotka luotiin, kun tilaus vapautettiin varastoon.
    - **Rivi 2:** Vain **Työtiedot**-vaihtoehto on käytettävissä. Valitse se ja huomaa, että työtä ei ole luotu, koska varastoa ei ole varattu. Tällöin ei myöskään luotu siirtoa tai kuormitusta.

> [!NOTE]
> Sama tulos on odotettavissa, kun toinen rivi on varattu osittain. Tässä tapauksessa työ luodaan varatun rivin määrälle, mutta ei varauksettoman määrän osalta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]