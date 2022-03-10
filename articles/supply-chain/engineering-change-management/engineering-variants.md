---
title: Muuttujan muodostaminen suunnittelutuotteita varten
description: Tässä aiheessa kuvataan, miten muuttuja luodaan suunnittelutuotteita varten
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e24bceac9457212ecaafda876d19ba62df049371
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/27/2021
ms.locfileid: "7471833"
---
# <a name="generate-variants-for-engineering-products"></a>Muuttujan muodostaminen suunnittelutuotteita varten

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten muuttuja luodaan suunnittelutuotteita varten.

## <a name="turn-on-variant-generation-for-engineering-products"></a>Ota suunnittelutuotteiden muuttujien muodostaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Suunnittelun muutostenhallinta*
- **Ominaisuuden nimi:** *Suunnittelutuotteiden muuttujien muodostus*

> [!IMPORTANT]
> *Suunnittelutuotteiden muuttujien muodostus* -ominaisuus tulee näkyviin järjestelmässä vasta, kun *Suunnittelun muutostenhallinta* -määritysavain on otettu käyttöön. Ohjeet: [Suunnittelun muutostenhallinnan yleiskatsaus](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Suunnittelutuotteen yhden tai useamman uuden muuttujan muodostaminen

Voit luoda tuotteelle yhden tai useita uusia muuttujia kopioimatta tietoja olemassa olevasta tuotteesta. Tästä on hyötyä, kun samanaikaisesti on luotava useita tuotemuuttujia.

Seuraavassa on esimerkki siitä, miten voit luoda useita eri versioita, jotka sisältävät väridimension.

1. Avaa **Vapautetut tuotteet** -sivu (siirry esimerkiksi **Suunnittelumuutosten hallinta \> Yhteiset \> Vapautetut tuotteet** -sivulle).
1. Avaa toimintoruudun **Tuote**-välilehti ja valitse **Uusi**-ryhmässä **Suunnittelutuote**.
1. Näyttöön tulee **Uusi tuote** -valintaikkuna. Valitse asianmukainen **Suunnitteluluokka**.
1. Jos valittuun suunnitteluluokkaan sisältyy muuttujadimensioita, voit määrittää niille arvot nyt. Jos tässä esimerkissä on **väri**-dimensio, voit määrittää sen arvoksi *Sininen*.
1. Tee tarvittavat muut asetukset. Valitse **OK**, kun haluat luoda tuotteen.
1. Tuote ja sininen V-1 on luotu, ja uusi tuote avautuu.
1. Lisää muuttujaan tuoterakenne ja reititys tarpeen mukaan.
1. Avaa sitten toimintoruudun **Tuote**-välilehti ja valitse **Päätuote**-ryhmästä **Tuotedimensiot**.
1. **Tuotedimensiot** -sivu avautuu. Sivulla on välilehti jokaista käytettävissä olevaa dimensiota kohti. Lisää kuhunkin välilehteen rivi jokaista arvoa varten, joka tukee kutakin asiaankuuluvaa dimensiota. (Tässä esimerkissä voit lisätä **Väri**-välilehdelle rivit *Valkoinen*, *Keltainen* ja *Vihreä*).
1. Sulje sivu ja valitse sitten **Vapautetut tuotemuuttujat**. Ota huomioon, että näkyviin tulee ensimmäinen luotu muuttuja (sininen V-1).
1. Valitse toimintoruudun **Tuotevariantti**-välilehdessä **Varianttiehdotukset**.
1. Noudata **Varianttiehdotukset**-valintaikkunassa yhtä seuraavista ohjeista:

    - Valintaikkunan yläreunassa on osio kullekin käytettävissä olevalle dimensiolle. Valitse kullekin dimensiolle valintaruutu jokaiselle arvolle, jolle haluat luoda varianttiehdotuksen ja valitse sitten työkalupalkista **Ehdota**. Asiaankuuluvat ehdotukset lisätään **Ehdotetut variantit** -osioon.
    - Valitse työkaluriviltä **Ehdota kaikkia**, kun haluat luoda varianttiehdotuksia kaikille käytettävissä oleville dimensioarvojen yhdistelmille. Ehdotukset lisätään **Ehdotetut variantit** -osioon.

1. Valitse **Ehdotetut variantit** -osassa kunkin luotavan variantin valintaruutu. Muodosta ja vapauta valitut variantit suunnitteluyritykselle valitsemalla **Luo**. Seuraavat ehdot pätevät:

    - Millään luoduilla muuttujavaihtoehdoilla ei ole tuoterakennetta tai reititystä.
    - Näiden muuttujien määritteet ovat oletusarvona suunnitteluluokasta, eikä niitä kopioida edellisestä versiosta.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Muuttujan muodostaminen toisen tuotemuuttujan kopiona

Voit luoda tuotteen muuttujan toisen tuotemuuttujan perusteella. Ohjelma kopioi tuoterakenteen ja reitityksen lähdetuotemuuttujasta uuteen muuttujaan. Tämä voi olla hyödyllistä, jos käytössä on erillisiä valmistustuotteita, kun tuoterakenteen luominen voi perustua aloitustuoterakenteeseen ja seurata edellisen muuttujan muutoksia. Ylläpitoa varten järjestelmä tallentaa, mitä muuttujaa on kopioitu luotaessa uusi kopio.

Seuraavassa on esimerkki siitä, miten voit luoda uuden muuttujan, joka sisältää väridimension, luomalla kopion aiemmin luodusta muuttujasta.

1. Avaa **Vapautetut tuotteet** -sivu (siirry esimerkiksi **Suunnittelumuutosten hallinta \> Yhteiset \> Vapautetut tuotteet** -sivulle).
1. Avaa toimintoruudun **Tuote**-välilehti ja valitse **Uusi**-ryhmässä **Suunnittelutuote**.
1. Näyttöön tulee **Uusi tuote** -valintaikkuna. Valitse asianmukainen **Suunnitteluluokka**.
1. Jos valittuun suunnitteluluokkaan sisältyy muuttujadimensioita, voit määrittää niille arvot nyt. Jos tässä esimerkissä on **väri**-dimensio, voit määrittää sen arvoksi *Sininen*.)
1. Tee tarvittavat muut asetukset. Valitse **OK**, kun haluat luoda tuotteen.
1. Tuote ja sininen V-1 on luotu, ja uusi tuote avautuu.
1. Lisää muuttujaan tuoterakenne ja reititys tarpeen mukaan.
1. Lisää muuttujat tuotevarianttiin tarpeen mukaan.
1. Lisää V-1-tuotemuuttuja suunnittelumuutostilaukseen.
1. Määritä **vaikutus** *uuteen muuttujaan*.
1. Valitse uusi väriarvo (esimerkiksi *Valkoinen*). Huomaa, että seuraavat ehdot täyttyvät: 
    - Uudella muuttujalla on tuoterakenne ja reititys, jotka on kopioitu edellisestä muuttujasta.
    - Uudessa muuttujassa määritteet on kopioitu edellisestä muuttujasta.
1. Hyväksy muutostilaus.
1. Käsittele muutostilaus. Kun tilaus on käsitelty, uusi V-1-versio luodaan ja vapautetaan suunnitteluyhtiölle.