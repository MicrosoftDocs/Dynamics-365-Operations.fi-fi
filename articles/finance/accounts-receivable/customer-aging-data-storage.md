---
title: Asiakkaan ikääntymistietojen tallennustila
description: Tässä aiheessa kuvataan asiakkaan erääntymistietojen ulkoisen tallennuksen käyttöprosessia. Suorita asiakkaan erääntymistietojen tallennusprosessi, jotta tiedot voidaan viedä ulkoiseen järjestelmään.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecd4f5359019e3c4778e21cc4946b9998cd519f
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817423"
---
# <a name="customer-aging-data-storage"></a>Asiakkaan ikääntymistietojen tallennustila

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä aiheessa kuvataan asiakkaan erääntymistietojen ulkoisen tallennuksen käyttöprosessia. Microsoft Dynamics 365 Financessa voit suorittaa asiakkaan erääntymistietojen tallennusprosessin, jotta tiedot voidaan viedä ulkoiseen järjestelmään. Kun suoritat prosessin, samat erääntymisraporttivaihtoehdot, jotka ovat käytettävissä järjestelmässä, ovat ulkoisten järjestelmien käytettävissä. Tiedot sisällytetään aina vietyihin tietoihin.

Asiakkaan erääntymistiedot voidaan määrittää ulkoisen järjestelmän käyttöön tallennusta varten, jos tuotoksessa on useita asiakkaita ja/tai useita tapahtumia. Jos **asiakkaan erääntymisraportti** aikakatkaistaan, koska tulostettavana on liian paljon tietoja, tämä ominaisuus tarjoaa vaihtoehtoisen tavan käyttää samoja tietoja.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Asiakkaan erääntymistietojen tallennustoiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sinun on otettava se käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää toimintojen hallinnan asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** Luotonvalvonta
- **Ominaisuuden nimi:** Asiakkaan erääntymistietojen tallennus

## <a name="run-the-customer-aging-data-storage-process"></a>Suorita asiakkaan erääntymistietojen tallennusprosessi

1. Valitse **Luotonvalvonta \> Kyselyt ja raportit \> Asiakas \> Asiakkaan erääntymistietojen tallennus**.
2. Valitse **Uusi**.
3. Kirjoita **Nimi**-kenttään prosessin nimi.
4. Määritä muut parametrit tarpeen mukaan.

    > [!NOTE]
    > Tapahtumatiedot sisällytetään aina, ja käsittely tapahtuu aina erätyönä.

5. Valitse **OK**.
6. Päivitä **Asiakkaan erääntymistietojen tallennus** -sivu, jos haluat nähdä **erän nimen** ja **erän suoritusajan** arvot, jotka näkyvät yhdessä **Käsittelyn tila** -arvon kanssa. Kun erätyö on valmis, **Käsittelytila**-kentän arvoksi tulee **Päättynyt** ja **Erääntymisrivien määrä** -kenttä määritetään. Jos erätyö toistuu, **Käsittelytila**-kentän arvoksi tulee **Odottaa**.
7. Tarkista erätyölle lisätyt suodattimet valitsemalla **Erääntymisrivien määrä** -kentän viereinen **Suodatus**-painike.

**Asiakkaan erääntymistietojen tallennus** -sivu ei sisällä tuloksia. **Asiakkaan erääntymistietojen tallennus** -tietoyksikkö voi kuitenkin viedä tulosteet mihin tahansa tietojenhallinnan tukemaan muotoon.

> [!NOTE]
> Lisää ennen vientiä suodatin, joka rajaa viedyt tulokset viimeisimmän erääntymisen rajoiksi. Voit esimerkiksi palauttaa uusimman eräsuorituksen lisäämällä seuraavat ehdot:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchName())
>
> Vaihtoehtoisesti voit palauttaa nykyisen käyttäjän uusimman eräsuorituksen lisäämällä seuraavat ehdot:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchNameForCurrentUser())
