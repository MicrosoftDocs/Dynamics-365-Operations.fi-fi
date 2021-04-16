---
title: Eri dimensioiden määrittäminen pakkausta ja varastointia varten
description: Tässä aiheessa käsitellään, miten määritetään, missä prosessissa (pakkaus, varastointi ja sisäkkäinen pakkaus) kutakin määritettyä dimensiota käytetään.
author: mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e997f8bccde7856303d8b3c6407143598ccc6030
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818917"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Eri dimensioiden määrittäminen pakkausta ja varastointia varten

[!include [banner](../../includes/banner.md)]

Jotkin nimikkeet pakataan tai tallennetaan siten, että fyysisiä dimensioita on ehkä seurattava eri tavalla kussakin prosessissa. *Pakkauksen tuotedimensiot* -toiminnolla voi määrittää kullekin tuotteelle vähintään yhden dimensiotyypin. Kussakin dimensiotyypissä on fyysisten mittojen joukko (paino, leveys, syvyys ja korkeus), ja se muodostaa prosessin, jossa kyseisiä fyysisiä mitta-arvoja käytetään. Kun tämä toiminto on otettu käyttöön, järjestelmä tukee seuraavia dimensiotyyppejä:

- *Varasto* – varastodimensioita käytetään sijainnin tilavuustietojen ohella määrittämään, kuinka monta kappaletta nimikettä voidaan varastoida eri varastosijainteihin.
- *Pakkaus* – pakkausdimensioita käytetään konttiinpakkaamisen ja manuaalisen pakkausprosessin aikana määrittämään, kuinka monta kappaletta nimikettä sopii erilaisiin konttityyppeihin.
- *Sisäkkäinen pakkaus* – sisäkkäisiä pakkausdimensioita käytetään, kun pakkausprosessi sisältää useita tasoja.

*Varastodimensioita* tuetaan myös silloin, kun *Pakkauksen tuotedimensiot* -toimintoa ei ole otettu käyttöön. Ne määritetään **Fyysiset dimensiot** -sivulla Supply Chain Managementissa. Kaikki prosessit, joissa pakkauksen ja sisäkkäisen pakkauksen dimensioita ei ole määritetty, käyttävät näitä dimensioita.

*Pakkauksen* ja *sisäkkäisen pakkauksen* dimensiot määritetään **Fyysiset tuotedimensiot** -sivulla, joka lisätään, kun *Pakkauksen tuotedimensiot* -toiminto otetaan käyttöön.
Tässä aiheessa on skenaario, joka näyttää, miten tätä toimintoa käytetään.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Pakkauksen tuotedimensiot -toiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Pakkauksen tuotedimensiot*

## <a name="example-scenario"></a>Esimerkkiskenaario

### <a name="set-up-the-scenario"></a>Määritä skenaario

Ennen esimerkkiskenaarion suorittamista järjestelmä on valmisteltava tässä osassa kuvatulla tavalla.

#### <a name="enable-demo-data"></a>Esittelytietojen ottaminen käyttöön

Tämän skenaarion käyttäminen tässä määritettyjen esittelytietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakiomuotoiset [esittelytiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava *USMF*-yritys ennen kuin aloitat.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Uuden fyysisen dimension lisääminen tuotteeseen

Tuotteeseen lisätään uusi fyysinen dimensio seuraavasti:

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse tuote, jonka **nimiketunnus** on *A0001*.
1. Valitse toimintoruudun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **Fyysiset tuotedimensiot**.
1. **Fyysiset tuotedimensiot** -sivu avautuu. Lisää uusi dimensio ja seuraavat asetukset ruudukkoon valitsemalla toimintoruudussa **Uusi**:
    - **Fyysisen dimension tyyppi** - *Pakkaus*
    - **Fyysinen yksikkö** - *kpl*
    - **Paino** - *4*
    - **Painon yksikkö** - *kg*
    - **Syvyys** - *3*
    - **Korkeus** - *4*
    - **Leveys** - *3*
    - **Pituus** - *cm*
    - **Tilavuuden yksikkö** - *cm3*

**Tilavuus**-kenttä lasketaan automaattisesti **Syvyys**-, **Korkeus**- ja **Leveys**-asetusten perusteella.

#### <a name="create-a-new-container-type"></a>Uuden konttityypin luominen

Valitse **Varastonhallinta \> Asetukset \> Kontit \> Konttityypit** ja luo uusi tietue, jossa on seuraavat asetukset:

- **Kontin tyyppikoodi** - *Pieni laatikko*
- **Kuvaus** - *Lyhyt laatikko*
- **Enimmäisnettopaino** - *50*
- **Tilavuus** - *144*
- **Pituus** - *6*
- **Leveys** - *6*
- **Korkeus** - *4*

#### <a name="create-a-container-group"></a>Konttiryhmän luominen

Valitse **Varastonhallinta \> Asetukset \> Kontit \> Konttiryhmät** ja luo uusi tietue, jossa on seuraavat asetukset:

- **Konttiryhmän tunnus** - *Lyhyt laatikko*
- **Kuvaus** - *Lyhyt laatikko*

Valitse uusi rivi **Tiedot**-osaan. Määritä **konttityypiksi** *Lyhyt laatikko*.

#### <a name="set-up-a-container-build-template"></a>Aseta kontin muodostusmalli

Valitse **Varastonhallinta \> Asetukset \> Kontit \> Kontin rakennusmallit** ja valitse sitten **Laatikot**. Muuta **konttiryhmän tunnukseksi** *Lyhyt laatikko*.

### <a name="run-the-scenario"></a>Skenaarion suorittaminen

Kun järjestelmä on valmisteltu edellisessä osassa kuvatulla tavalla, seuraavassa osassa kuvattu skenaario voidaan suorittaa.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Myyntitilauksen ja lähetyksen luominen

Tässä prosessissa luodaan lähetys nimikkeen *pakkauksen* dimensioiden perusteella, kun korkeus on alle 3.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-001*
    - **Varasto**: *63*

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilaus avataan. **Myyntitilausrivit**-pikavälilehden ruudukossa pitäisi olla uusi tyhjä rivi. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *5*

1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.
1. Varaa varasto **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.
1. Sulje sivu.
1. Luo varaston työ valitsemalla toimintoruudun **Varasto**-välilehdessä **Vapauta varastoon**.
1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Lähetyksen tiedot**.
1. Valitse toimintoruudun **Kuljetus**-välilehdessä **Näytä kontit**. Vahvista, että nimikkeen konttiinpakkauksessa käytettiin kahta *Lyhyt laatikko* -konttia.

#### <a name="place-an-item-into-storage"></a>Nimikkeen sijoittaminen varastoon

1. Avaa mobiililaite, kirjaudu varastoon 63 ja valitse **Varasto \> Oikaisu sisään**.
1. Anna **Sijainti** = *SHORT-01*. Tee uusi rekisterikilpi, jossa **Nimike** = *A0001* ja **Määrä** = *1 kpl*.
1. Valitse **OK**. Näyttöön avautuu virhe sanoma Sijainti SHORT-01 epäonnistui, koska nimike A0001 ei sovi sijainnin määritettyihin dimensioihin. Tämä johtuu siitä, että tuotteen *Varasto*-tyypin dimensiot ovat suuremmat kuin sijaintiprofiilissa määritetyt dimensiot.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]