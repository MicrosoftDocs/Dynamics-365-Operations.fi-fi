---
title: Tuotannon käyttöliittymän suunnitteleminen
description: Tässä aiheessa käsitellään kunkin määrityksen käyttöliittymän sisällön suunnittelua.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ee206ced76dbdd356c77d34a4b8f197879e9a3f0
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384769"
---
# <a name="design-the-production-floor-execution-interface"></a>Tuotannon käyttöliittymän suunnitteleminen

[!include [banner](../includes/banner.md)]

Kunkin tuotannon käyttöliittymän käyttämän määrityksen käyttöliittymän sisältö voidaan suunnitella. Esimerkiksi tietyn työsolun työntekijöiden on ehkä voitava avata työohjeet tuotannossa, kun toisessa työsolussa näitä ohjeita ei tarvita. Siinä tapauksessa on luotava kaksi määritystä, joista toisessa on painike asiakirjaliitteiden avaamiseen ja toisessa kyseistä painiketta ei ole.

## <a name="design-a-tab"></a>Välilehden suunnitteleminen

**Määritä tuotantoliittymä** -sivulla voi luoda ja määrittää välilehtiä valitsemalla toimintoruudussa **Suunnittele välilehtiä**.

Kukin välilehti on jaettu neljään osaan, kuten seuraavassa kuvassa.

![Välilehden asettelu.](media/pfe-tab-layout.png "Välilehden asettelu")

Kuvassa näkyy seuraavat elementit:

1. Ensisijainen työkalurivi
1. Toissijainen työkalurivi
1. Päänäkymä
1. Tarkka näkymä

Uusi välilehti luodaan ja määritetään seuraavasti:

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Määritä tuotantoliittymä**.

1. Avaa **Suunnittele välilehtiä** -sivu valitsemalla toimintoruudussa **Suunnittele välilehtiä**.

    ![Suunnittele välilehtiä -sivu.](media/pfe-design-tabs.png "Suunnittele välilehtiä -sivu")

1. Valitse toimintoruudussa **Uusi**.

1. Määritä seuraavat asetukset sivun otsikossa:

    - **Välilehden nimi** – määritä välilehden nimi.
    - **Päänäkymä** – valitse jokin esimääritetyistä työluetteloista (*Aktiiviset työt*, *Kaikki työt*, *Omat työt* tai *Oma kone*).
    - **Tietonäkymä** – Valitse joko tyhjä arvo tai **Työn tiedot**. Jos valitset tyhjän arvon, välilehdessä ei ole tietonäkymää. Jos valitse **Työn tiedot**, tietonäkymässä on tarkka kuvaus päänäkymän työluettelossa valitusta työstä.

1. Valitse **Ensisijainen työkalurivi** -osassa ensisijaisessa työkalurivissä käytettävissä olevat painikkeet. **Käytettävissä olevat toiminnot** -sarakkeessa on luettelo lisättävistä painikkeista. **Valitut toiminnot** -sarakkeessa on luettelo kaikista painikkeista, jotka sisältyvät nykyiseen määritykseen. Siirrä nimikkeitä tarvittaessa sarakkeesta toiseen sarakkeiden välissä olevilla painikkeilla. Määritä järjestys, jossa painikkeet näytetään käyttöliittymässä, **Valitut toiminnot** -sarakkeen vieressä olevilla ylä- ja alanuolipainikkeilla.

1. Valitse **Toissijainen työkalurivi** -osassa toissijaisessa työkalurivissä käytettävissä olevat painikkeet. **Käytettävissä olevat toiminnot** -sarakkeessa on luettelo lisättävistä painikkeista. **Valitut toiminnot** -sarakkeessa on luettelo kaikista painikkeista, jotka sisältyvät nykyiseen määritykseen. Siirrä nimikkeitä tarvittaessa sarakkeesta toiseen sarakkeiden välissä olevilla painikkeilla. Määritä järjestys, jossa painikkeet näytetään käyttöliittymässä, **Valitut toiminnot** -sarakkeen vieressä olevilla ylä- ja alanuolipainikkeilla.

## <a name="associate-a-tab-with-a-configuration"></a>Välilehden liittäminen määritykseen

Kun kaikki tarvittavat välilehdet on suunniteltu, voit liittää ne määritykseen.

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Määritä tuotantoliittymä**.

    ![Määritä tuotannon suoritus.](media/pfe-config-prod-floor-execution.png "Määritä tuotannon suoritus")

1. Valitse **Välilehtivalinta**-pikavälilehdessä **Lisää**.

1. Uusi rivi lisätään ruudukkoon. Valitse uudelle riville määritykseen lisättävän välilehden nimi.

1. Jatka lisäämällä välilehtiä tarpeen mukaan.

1. Järjestele välilehtiä tarpeen mukaan työkalurivin **Siirrä ylös**- ja **Siirrä alas** -painikkeilla. Välilehdet näytetään vasemmalta oikealle edellä olevassa näyttökuvassa olevassa järjestyksessä (ylhäällä oleva välilehti näytetään vasemmalla).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
