---
title: Keräilyrivin ryhmittely
description: Tässä ohjeaiheessa on keräilyrivin yhteenveto.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906265"
---
# <a name="pick-line-grouping"></a>Keräilyrivin ryhmittely

[!include [banner](../includes/banner.md)]

Keräilyrivin ryhmittelyssä useita työrivejä, joilla on sama nimike ja sijainti voidaan yhdistää yhdeksi keräilyksi, joka esitetään käyttäjälle mobiililaitteessa. Tämän vuoksi varastotyöntekijät voivat saada mahdollisimman tehokkaat ohjeet, mutta myös vaadittavien työlinjojen erottaminen järjestelmässä säilyy (esimerkiksi eri kontteihin ja tilauksiin).

## <a name="set-up-pick-line-grouping"></a>Määritä keräilyrivin ryhmittely

### <a name="create-a-mobile-device-menu-item"></a>Luo mobiililaitteen valikkovaihtoehto

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot** ja luo uusi valikkokohde, jonka nimi on **Myyntiryhmän keräily – käyttäjän ohjaama**.
2. Määritä seuraavat arvot **Mobiililaitteen valikkovaihtoehdot** -valinnan alla:

    - Valitse **Valikkovaihtoehdon nimi** -kenttä ja syötä **Myynnin poiminta - ryhmän rivi**.
    - Valitse **Otsikko** -kenttä ja syötä **Myynnin keräily - ryhmän rivi**.
    - Valitse **Tila**-kentässä **Työ**.
    - Valitse **Käytä nykyistä työtä** -asetukseksi **Kyllä**.

3. **Yleiset**-pikavälilehdessä voit määrittää seuraavat arvot:

    - Valitse **Ohjaaja**-kentässä **Järjestelmäohjattu**.
    - Määritä **Luo rekisterikilpi** -valinnan asetukseksi **Kyllä**.
    - Määritä **Ryhmäkeräily** -asetukseksi **Kyllä**.

4. Määritä **Työluokat**-pikavälilehdessä mobiililaitteen valikkokohteelle kelvolliset työluokat noudattamalla näitä vaiheita:

    1. Valitse **Uusi**.
    2. Valitse **Työluokan tunnus** -kentässä**Myynti** tai **Tilauksen keräily** sen mukaan, mitä varastoa käytät.
    3. Valitse **Työtilaustyyppi**-kentässä **Myyntitilaukset**.

### <a name="set-up-a-mobile-device-menu"></a>Määritä varaston mobiililaitteen valikko

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**. 
1. Lisää juuri luomasi valikkokohde haluamaasi valikkoon.

### <a name="set-up-a-work-template"></a>Määritä työmalli

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Etsi työmalli, jota käytetään tämän funktion kanssa. Tässä esimerkissä valitaan **Standard 51-poiminta** vaiheeseen Contoso-työmalli.
1. Valitse valikosta **Muokkaa kyselyä**.
1. Valitse **Lajittelu**-välilehdestä **Lisää** ja määritä sitten seuraavat arvot:

    - Valitse **Taulu**-kentästä **Väliaikaiset työtapahtumat**.
    - Valitse **Johdettu taulu**-kentästä **Väliaikaiset työtapahtumat**.
    - Valitse **Kenttä** -kentässä **Nimikkeen numero**.
    - Valitse **Hakusuunta**-kentässä **Laskeva**.

> [!NOTE]
> Jotta poimintarivin ryhmittelytoiminto toimisi, työrivit on lajiteltava nimiketunnuksen mukaan. Jos rivejä, joilla on samat nimikkeet, ei ole järjestetty yksitellen, niitä ei ryhmitellä.

## <a name="example"></a>Esimerkki

### <a name="create-picking-work"></a>Luo keräystyö

Ennen kuin voit määrittää keräilyrivin ryhmittelyn, sinun on luotava joitakin tukikelpoisia lähteviä töitä.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
2. Luo uusi myyntitilaus valitsemalla **Uusi**. 
3. Valitse **Asiakastili**-kentässä mikä tahansa asiakas. 
4. Valitse **Yleinen**-pikavälilehden **Varasto**-kentässä **51**. Valitse sitten **OK**.
5. Lisää seuraavat kuusi riviä **myyntitilausriveille**:

    - Valitse **Rivi 1:** **Nimikkeen numero** -kentässä **M9200**. Kirjoita **Määrä**-kenttään **3**.
    - Valitse **Rivi 2:** **Nimikkeen numero** -kentässä **M9201**. Kirjoita **Määrä**-kenttään **3**. 
    - Valitse **Rivi 3:** **Nimikkeen numero** -kentässä **M9202**. Kirjoita **Määrä**-kenttään **2**. 
    - Valitse **Rivi 4:** **Nimikkeen numero** -kentässä **M9200**. Kirjoita **Määrä**-kenttään **1**. 
    - Valitse **Rivi 5:** **Nimikkeen numero** -kentässä **M9200**. Kirjoita **Määrä**-kenttään **3**.
    - Valitse **Rivi 6:** **Nimikkeen numero** -kentässä **M9202**. Kirjoita **Määrä**-kenttään **7**. 

    Tässä on yhteenveto kunkin nimikkeen kokonaismääristä:

    - **Nimike M9200:** 7 kukin
    - **Nimike M9201:** 3 kukin
    - **Nimike M9202:** 9 kukin

6. Ennen kuin vapautat tilaukset varastoon, varmista, että poiminnan sijainneissa on tarpeeksi varastoa kaikkien tilausten kaikille nimikkeille. Tarkista **Toimipaikkadirektiivin** asetus ja määritä, mitä keräilysijainteja myyntitilausten keräilyyn käytetään.
7. Varaa varasto ja vapauta se varastoon. Työtunnus, jossa on kuusi riviä on luotu. Rivit lajitellaan nimiketunnuksen mukaan.

### <a name="run-the-mobile-device-flow"></a>Suorita mobiililaitteen virtaus

1. Valitse mobiililaitteessa valikko, joka sisältää uuden mobiililaitteen valikkovaihtoehdon.
1. Valitse **Myynnin poiminta – ryhmärivi** -valikkonimike ja aloita poiminta.

    Kun olet valinnut valikon ja kirjoitat työn tunnuksen, näet poimintavaiheen, jossa kaikki nimikkeen M9200 poimintarivit ryhmitellään. Saat ohjeen, jossa voit valita 7 kutakin nimikettä M9200.

1. Vahvista ensimmäinen vaihe. 
1. Siirry keskeneräisen työn asiakasnäyttöön ja huomaa, että kohteen M9200 kaikki kolme poimintariviä suljettiin samanaikaisesti.

    Työlinja 4 on esitetty.

1. Vahvista ensimmäinen vaihe.

    Matkaviestimen viimeinen poimintavaihe kokoaa yhteen kaksi viimeistä poimintariviä työtilauksesta.

1. Täytä poiminnan vaihe 9 jokaiselle nimikkeelle M9202.
1. Vahvista laittovaihe ja mahdolliset muut poiminta-/laittovaiheet töiden suorittamiseen.

> [!NOTE]
> - Työrivit voidaan ryhmitellä vain, jos ne ovat järjestyksessä.
> - Seuraavaa toimintoa ei tueta:
>
>    - Todellisen painon nimikkeet. Jos työssä on mitään todellisen painon nimikkeitä, näyttöön tulee virhesanoma, ennen kuin aloitat poiminnan.
>    - Kappaleen keräily.
>    - Työrivit, joilla on keskeneräinen täydennystyö.
>    - Ylikeräily.
