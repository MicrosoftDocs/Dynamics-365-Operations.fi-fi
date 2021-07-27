---
title: Mobiililaitteen valikkovaihtoehdon määrittäminen tuottamaan keräilyrivin yhteenvedon
description: Tässä ohjeaiheessa selitetään, miten voit määrittää, milloin kaikkien työrivien luettelo näytetään varastotyöntekijöille, jotka käsittelevät varastotyötä mobiililaitteilla. Tämä ominaisuus voi olla hyödyllinen varastotyöntekijöille, jotka tarvitsevat usein yhteenvedon työtilauksen keräilyriveistä, jotta he voivat optimoida keräilyjärjestyksen.
author: MarkusFogelberg
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e6459620e0353e47d53445e54bddf08a2b7071af
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339966"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Mobiililaitteen valikkovaihtoehdon määrittäminen tuottamaan keräilyrivin yhteenvedon

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa selitetään, miten määritetään keräilyrivien mobiililaitteille tarkoitettuun yhteenvetoon liittyvät valikkovaihtoehdot, joita käytetään keräilytyön käsittelyssä. Keräilyrivin yhteenvedon avulla varastotyöntekijät pystyvät tarkastelemaan ja valitsemaan töitä luettelosta, joka sisältää kaikki heidän kulloiseenkin tehtäväänsä liittyvät työrivit. Tämä ominaisuus voi auttaa työntekijöitä optimoimaan keräilyjärjestyksensä. Toiminto sisältää vaihtoehtoja vakiomuotoisen **Ohitus**-painikkeen korvaamiseksi. Tällä painikkeella työntekijät voivat käydä rivit läpi yksi kerrallaan kiinteässä järjestyksessä. (Painikkeen käyttäminen on kuitenkin edelleen mahdollista.)

Järjestelmänvalvojat voivat määrittää kunkin valikkovaihtoehdon erikseen ja hallita miten, milloin ja missä varastonhallinnan mobiilisovellus esittää keräilyrivin yhteenvedon.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>Työn keräilyriviyhteenveto-toiminnon käyttöönotto

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** _Varastonhallinta_
- **Toiminnon nimi:** _Työn keräilyrivin yhteenveto_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Valikkovaihtoehtojen määrittäminen näyttämään luettelon kaikista työriveistä

Määritä mobiililaitteen valikkovaihtoehto tuottamaan keräilyrivin yhteenveto seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse tai luo keräilytyöhön liittyvä valikkovaihtoehto ja määritä seuraavat arvot:

    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Kyllä*
    - **Ohjaaja:** *Käyttäjän ohjaama* tai *Järjestelmän ohjaama*

    Lisätietoja valikkovaihtoehtojen luomisesta ja **Mobiililaitteen valikkovaihtoehdot** -sivulla käytettävissä olevien eri asetusten käyttämisestä: [Mobiililaitteiden määrittäminen varastotyötä varten](configure-mobile-devices-warehouse.md).

1. Määritä toiminto **Yleiset**-pikavalikossa määrittämällä **Näytä työriviluettelo** -kentän arvoksi jokin seuraavista:

    - **Näytä vain pyydettäessä** – Työntekijät voivat avata keräilyriviluettelon valitsemalla **Siirry kohteeseen** -painikkeen varastonhallinnan mobiilisovelluksessa.
    - **Näytä jokaisen keräilyn alussa** – Työntekijät näkevät luettelon aina, kun he aloittavat keräilyrivin tai saavat sen valmiiksi. He voivat myös tarkastella luetteloa uudelleen valitsemalla **Siirry kohteeseen** -painikkeen varastonhallinnan mobiilisovelluksessa.
    - **Näytä vain ensimmäisen keräilyn alussa** – Työtekijät näkevät luettelon aina, kun he aloittavat uuden keräystyön, mutta eivät jokaisen rivin jälkeen. He voivat myös tarkastella luetteloa uudelleen valitsemalla **Siirry kohteeseen** -painikkeen varastonhallinnan mobiilisovelluksessa.
    - **Älä näytä koskaan** – Vakiomuotoinen **Ohita**-painike näkyy varastonhallinnan mobiilisovelluksessa ja työriviluettelon näyttö on kytketty pois. **Ohita**-painikkeen avulla työntekijät käyvät rivit läpi yksi kerrallaan kiinteässä järjestyksessä. He voivat myös selata luetteloa niin monta kertaa kuin on tarpeen, kunnes kaikki rivit on käsitelty.

1. Valitse toimintoruudussa **Tallenna**.

    Jos määrität **Näytä työriviluettelo**-kentän arvoksi minkä tahansa muun kuin *Älä näytä koskaan*, toimintoruudun **Kenttäluettelo**-painike muuttuu käytettäväksi.

1. Valitse toimintoruudussa **Kenttäluettelo**.
1. Määritä **Kenttäluettelo**-sivulla tiedot, jotka varastonhallinnan mobiilisovellus näyttää kunkin luettelon rivin osalta.

    - **Ensisijainen ohjausobjekti** -kentän arvona on aina *LineNum*. Siksi jokainen luettelon rivi alkaa rivinumerolla.
    - Käytä jäljellä olevia **Näyttökenttä**-kenttiä lisätäksesi jopa seitsemän lisänäyttökenttää tarpeen mukaan. Valitse jokaisessa **Näyttökenttä**-kentässä työrivikentän nimi. Kukin rivi näyttä tällöin arvon kyseiselle kentälle. Arvot näytetään tässä valitussa järjestyksessä. Voit jättää osan **Näyttökenttä**-kentistä tyhjiksi, jos et tarvitse kaikkia seitsemää arvoa.

1. Valitse toimintoruudussa **Tallenna** ja sulje sitten **Kenttäluettelo**-sivu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]