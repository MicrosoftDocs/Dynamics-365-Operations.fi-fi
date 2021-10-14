---
title: Vaihda työpoolia työssä
description: Tässä ohjeaiheessa käsitellään aiemmin luodun työn työpoolin vaihtaminen käyttämällä työnimikkeiden Vaihda työpoolia -painikkeella.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 066655b58d4676bafb6e8ed8d80a95636c047444
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566020"
---
# <a name="change-work-pool-on-work"></a>Vaihda työpoolia työssä

[!include [banner](../includes/banner.md)]

Voit järjestää työn ryhmiin työpoolien avulla. Voit esimerkiksi luoda työpoolin luokitellaksesi työn, joka tapahtuu tietyssä varastosijainnissa.

*Vaihda työpoolia työssä* -toiminto lisää **Vaihda työpoolia** painikkeen työnimikkeiden toimintoruutuun. Varastopäälliköiden onkin helppo vaihtaa aiemmin luodun työn työpoolia. Päälliköt voivat reagoida nopeasti tällä toiminnolla varaston tuotannossa tapahtuviin muutoksiin. Se myös parantaa heidän mahdollisuuksia sopeutua muuttuviin tilanteisiin ja tarpeeseen siirtää työ toiseen työpooliin.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Vaihda työpoolia työssä -toiminnon ottaminen käyttöön

Varmista ennen toiminnon määrittämistä tai käyttämistä, että se on saatavana järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Vaihda työpoolia työssä*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>Vaihda työpoolia työssä -toiminnon määrittäminen

Toiminnon käyttö edellyttää, että muutamia työpooleja on määritetty. Myös työmallit voidaan määrittää siten, että ne määrittävät poolin automaattisesti. Jos haluat kokeilla tässä aiheessa myöhemmin esiteltävää esimerkkitilannetta, määritä järjestelmäsi tämän osion ohjeiden mukaan.

### <a name="set-up-work-pools"></a>Työpoolien määrittäminen

Työnimikkeet voidaan järjestää tyypin mukaan työpoolien avulla. *Vaihda työpoolia työssä* -toiminnon käyttöä varten käytettävissä on oltava vähintään kaksi työpoolia. Työpooleja voi tarkastella ja lisätä seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Työ \> Työpoolit**.
1. Jos käytät **USMF**-yrityksen esittelytietoja ja tässä aiheessa jäljempänä olevaa esimerkkiskenaariota, lisää kaksi työpoolia, joissa on seuraavat asetukset:

    - Työpooli 1:

        - **Työpoolin tunnus:** *WebShop*
        - **Kuvaus:** *Verkkokauppa*

    - Työpooli 2:

        - **Työpoolin tunnus:** *CallCenter*
        - **Kuvaus:** *Puhelinkeskus*

1. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-work-templates"></a>Määritä työmallit

Kullekin työmallille voi määrittää tarpeen mukaan oletustyöpoolin. Kussakin soveltuvassa mallissa työpooli määritetään **Työpoolin tunnus** -sarakkeessa. Tässä tapauksessa kaikki työnimikkeet luodaan siten, että annettu malli perii automaattisesti määritetyn työpoolin. Jos käytät **USMF**-yrityksen esittelytietoja ja tässä aiheessa jäljempänä olevaa esimerkkiskenaariota, toimi seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Siirrä sivu muokkaustilaan valitsemalla toimintoruudussa **Muokkaa**.
1. Muokkaa mallia määrittämällä seuraavat arvot:

    - **Työmalli:** *62 Kerää pakettiin*
    - **Työpoolin tunnus:** *WebShop*

1. Valitse **Tallenna**.

## <a name="example-scenario"></a>Esimerkkiskenaario

Tämä skenaario näyttää, miten aiemmin luodun työnimikkeen käsittelyvirtaa muutetaan muuttamalla sen työpoolia. Se käyttää **USMF**-yrityksen esittelytietoja ja aiemmin tässä ohjeaiheessa suositeltuja asetuksia.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Myyntitilauksen luominen ja sen vapauttaminen varastoon

1. Vahvista, että nimikkeitä *A0001* ja *A0002* käytettävissä oleva varasto on riittävä varastossa *62*. Valitse **Varastonhallinta \> Kyselyt ja raportit \> Varastoluettelo** ja muokkaa suodattimet seuraavasti.

    - **Varasto**-arvon alussa on *62*.
    - **Nimiketunnus** on joko *A001* tai *A002*.

    Esimerkkitiedoissa kummankin määrän on oltava 10.

    Seuraavaksi on luotava myyntitilaus.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-007*
    - **Varasto**: *62*

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilaus avataan. **Myyntitilausrivit**-pikavälilehden ruudukossa pitäisi olla uusi tyhjä rivi. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *2*

1. Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.
1. Varaa varasto **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.
1. Sulje sivu.
1. Lisää toinen rivi myyntitilaukseen valitsemalla **Myyntitilausrivit**-pikavälilehdessä **Lisää rivi**. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *A0002*
    - **Määrä** *2*

1. Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.
1. Varaa varasto **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.
1. Sulje sivu.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.
1. Näyttöön tulee tiedotteita, joissa kerrotaan, että vapautuksesta luotiin aallon tunnus ja lähetystunnus. Kirjoita aallon tunnus muistiin.

### <a name="review-the-outbound-wave"></a>Lähtevän aallon tarkistaminen

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Hae ruudukossa myyntitilauksen vapautuksesta luotu aallon tunnus.
1. Voit tarkastella tietoja valitsemalla aallon tunnuksen.
1. Varmista **Aallon rivit** -pikavälilehdessä, että myyntitilauksen lähetystunnus on näkyvissä.

    > [!TIP]
    > Jos **Käsittele aalto, kun se vapautetaan varastoon** -asetuksena on *Ei* lähetyksen aaltomallin asetuksissa, aalto on käsiteltävä manuaalisesti valitsemalla **Käsittely** toimintoruudun **Aalto**-välilehdessä ja luomalla työ.

1. Varmista, että aalto on käsitelty. Tämä käsittely luo vaaditun työn.

### <a name="view-work-details-and-change-the-work-pool"></a>Työn tietojen tarkasteleminen ja työpoolin vaihtaminen

Voit tarkastella **Työn tiedot** -sivulla luotua työtä ja hallita työpoolia.

1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. Valitse juuri luodun työn rivi. Myyntitilauksen numero näkyy **Tilausnumero**-sarakkeessa.

    **Työpoolin tunnus** -kenttään määritetään työpoolin tunnus, joka määritettiin työmallissa.

    > [!TIP]
    > Jos **Työpoolin tunnus** -kenttä ei ole näkyvissä, lisää sarake ruudukkoon ja päivitä sivu.

1. Voit vaihtaa työtunnukseen liitetyn työpoolin valitsemalla toimintoruudun **Työ**-välilehdessä **Vaihda työpoolin tunnus**.
1. Valitsee **Vaihda työpoolia** -valintaikkunan **Parametrit**-pikavälilehden **Työpoolin tunnus** -kentässä *CallCenter*.
1. Ota muutos käyttöön valitsemalla **OK**.
1. Huomaa, että **Työpoolin tunnus** -kentän arvo on nyt *CallCenter*.

> [!IMPORTANT]
> Kun **Vaihda työpooli** -valintaikkuna avautuu, **Työpoolin tunnus** -kenttä voi olla oletusarvoisesti tyhjä. Jos kenttä on tyhjä, kun ota muutokset käyttöön valitsemalla **OK**, työpooli poistetaan kokonaan työstä.
>
> Työpoolien vaihtamisen lisäksi työpooli voidaan lisätä tällä menettelyllä mihin tahansa työnimikkeeseen, jossa sitä ei ole, tai poistaa työpoolin mistä tahansa työnimikkeestä, jossa sellainen on.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]