---
title: Varaston määrittäminen varaston konfigurointimallin avulla
description: Tässä artikkelissa käsitellään varaston määrittämistä varaston konfigurointimallin avulla.
author: yufeihuang
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: dafd51a46b19f3709963ffc12b3c8c77b6c809ac
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070436"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Varaston määrittäminen varaston konfigurointimallin avulla

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään varaston määrittämistä varaston konfigurointimallin avulla. Käytössäsi on useita valmiiksi määritettyjä konfigurointimalleja. Lisätietoja näiden mallien käyttämistä on kohdassa [Konfigurointitietomallit](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Skenaariot, joissa konfigurointimallit voivat olla hyödyllisiä

Konfigurointimallit voivat olla hyödyllisiä monissa skenaarioissa: Seuraavassa on muutamia esimerkkejä:

- Sinulla on valmis konfigurointiasetus, jota olet testannut testiympäristössä, ja haluat nyt kopioida asetuksen tuotantoympäristöön.
- Haluat siirtää varastoasetuksen useisiin yrityksiin tai luoda uuden varaston samaan yritykseen.
- Haluat luoda nopeasti varastotoiminnon esittelyn.
- Haluat, että nykyiset nimikkeet ja varastot käyttävät varastonhallinnan eikä varastoinninhallinnan toimintoa.

Tässä artikkelissa käsitellään ensimmäistä näistä skenaarioista. Se näyttää, miten konfigurointiasetuksen voi kopioida testiympäristöstä tuotantoympäristöön konfigurointimallin avulla.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Konfigurointiasetuksen kopioiminen testiympäristöstä tuotantoympäristöön

Tässä skenaariossa testiympäristössä on jo varaston konfigurointiasetus ja joitakin tapahtumaprosesseja. Haluat nyt kopioida varaston konfigurointiasetuksen testiympäristöstä tuotantoympäristöön.

> [!NOTE]
> Konfigurointiasetusta kopioitaessa on tärkeää, että mukana on myös muut liittyvät asetustiedot. Esimerkki: Haluat määrittää tuotteet kopioimalla asetuksen testiympäristöstä. Et voi kuitenkaan määrittää tuotteelle kiinteää keräilysijaintia, ennen kuin tuote on luotu. Vaikka yksittäiset konfigurointimallit eivät tue tämän tyyppistä riippuvuutta, tietyt oletustietomallit tukevat sitä. Nämä oletustietomallit on helppo sisällyttää konfigurointiprosessiin.

### <a name="export-a-default-warehouse-template"></a>Oletus varastomallin vienti 

1. Avaa **Tietojen hallinta** -työtila.

    > [!NOTE]
    > Jos käytät työtilaa ensimmäistä kertaa, sinun on ladattava kaikki tietoyksiköt, ennen kuin voit jatkaa.

2. Lataa oletusmallit valitsemalla ensin **Mallit**-ruudun ja sitten **Lataa oletusmallit**.

    > [!NOTE]
    > **Lataa oletusmallit** on käytettävissä vain **parannetussa** näkymässä. Valitse ensin **Kehikkoparametrit** ja sitten **Näytä oletusarvot** -kentässä **Parannettu näkymä**.

3. Kun kaikki oletusmallit on ladattu, voit muokata niitä vastaamaan liiketoimintasi tarpeita.

    > [!NOTE]
    > Oletusmallien lataaminen ja mallien tuominen edellyttää järjestelmänvalvojan oikeuksia. Tämä edellytys auttaa varmistamaan, että kaikki yksiköt ladataan oikein malliin.

4. Varmista, että olet siinä yrityksessä, josta haluat viedä yrityskohtaisia tietoja.
5. Valitse työtilassa **Vie**.
6. Luo uusi vientiprojekti.
7. Valitse **+ Lisää malli** ja etsi **400 - Varastonhallintajärjestelmä** -oletusvarastomalli. Tämä malli lisää varastokonfiguroinnin tietoyksiköt.

    > [!NOTE]
    > Jos vietävät tiedot on suodatettava, jokainen tietoyksikkö on arvioitava ja suodatus lisätään kyselyn avulla. (Voit esimerkiksi haluta viedä vain tiedot, jotka liittyvät tiettyyn varastoon.) Vaihtoehtoisesti voit viedä kaikki tiedot ja poistaa sitten tietueet, joita ei tarvita kohdetiedostoissa.

8. Valitse **Vie**. Kaikkiin projektin tietoyksiköihin liittyvät tiedot viedään.

Voit ladata tietopaketin zip-tiedoston. Tämä tiedosto sisältää kaikki tiedot valitussa muodossa (esimerkiksi Excel-muodossa). Kun aiemmin mainittiin, jotkin tietopakettitiedostojen tiedot on ehkä päivitettävä, ennen kuin ne voidaan tuoda tuotantoympäristöön. Jos päivität tietueen, et saa vaihtaa tiedoston nimeä.

### <a name="import-a-warehouse-configuration-setup"></a>Varaston konfigurointiasetuksen tuonti

1. Varmista kohdeympäristössä, että olet yrityksessä, johon haluat tuoda varastotiedot.

    > [!NOTE]
    > Etsi tietojen mahdolliset riippuvuudet ennen tuontia. Esimerkiksi **Varastonhallinta**-mallissa on **Varaston käsittelykoodit** -niminen tietoyksikkö. Tässä yksikössä on tietoja, jotka liittyvät **Käsittelykoodit**-asetussivulle (**Varastonhallinta** > **Asetukset** > **Mobiililaite** > **Käsittelykoodit**). Jos jo aiemmin määritetty asetus jo käsittelee myyntitilausten palautusprosessin, **Palauta käsittelykoodi** -kentässä on arvo. Tämän kentän käsittelykoodi liittyy **Käsittelykoodi**-tietoyksikköön, joka on osa **Myynti ja markkinointi** -mallia. Jos **Käsittelykoodi**-tietoyksikön tietoja ei tuoda ennen **Varaston käsittelykoodit** -kentän tietoja, tuonti epäonnistuu.

2. Valitse **Tietojen hallinta** -työtilassa **Tuo**.
3. Luo uusi tuontiprojekti.
4. Valitse **+ Lisää tiedosto** ja lataa tietopaketin zip-tiedosto.
5. Valitse **Tuo**. Voit käyttää **parannetussa** näkymässä **Suodata**-asetusta, jolla saat nopeasti yleiskuvan tuonnin aikana mahdollisesti esiintyvistä ongelmista.

**Näytä suoritusloki** sisältää tarkkoja tietoja jokaisesta tuotavasta tietoyksiköstä. Pääset nopeasti kohdetietoihin väliaikaisen tallennuksen tiedoista. Näet tällä tavoin, miltä tuodut tiedot näyttävät sovelluksen sivuilla. Oletustietomalleja käytettäessä kunkin tietoyksikön tuontijakso toimii ennalta määritetyllä tavalla. Tämä auttaa varmistamaan, että kaikki riippuvat tiedot tuodaan ensimmäiseksi. Jos projektissa on mukautettuja tietoyksiköitä, varmista, että oikea järjestys on määritetty. Lisätietoja on kohdassa [Konfigurointitietomallit](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

Jos haluat lisätietoja tavasta, jolla varastomääritys voidaan kopioida varastomallin avulla yrityksen varastosta uuteen yritykseen samassa esiintymässä, katso tämä 3 minuuttia kestävä YouTube-video, joka käsittelee [talous- ja toimintosovellusten määritysten kopiointia varastomallin avulla](https://www.youtube.com/watch?v=K2WIfFlqJYs).

## <a name="related-article"></a>Liittyvä artikkeli

[Konfigurointitietomallit](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
