---
title: Työtilauksien luonti
description: Tässä artikkelissa selitetään, miten työtilaukset luodaan käyttöomaisuuden hallinnassa.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ba01a90f805300a27e4550e1371fb55d5e3a7536
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335042"
---
# <a name="creating-work-orders"></a>Työtilauksien luonti

[!include [banner](../../includes/banner.md)]

Kun ennaltaehkäisevät ylläpitotyöt on aikataulutettu, seuraava vaihe on niiden työtilausten luominen. Tämä vaihe voidaan suorittaa käyttämällä jotakin ylläpitoaikataulua. Ylläpitoaikataulun aikataulutettujen töiden viitetyypit voivat olla erilaiset, ja niitä käsitellään seuraavassa taulukossa.

| Viitetyyppi | kuvaus |
|---|---|
| Ylläpitosuunnitelmat | *Aika*- tai *Laskuri*-ylläpitosuunnitelmatyyppiin perustuvat ennaltaehkäisevät ylläpitotyöt. |
| Ylläpitokierrokset | Useita saman tyyppistä ylläpitoa edellyttäviä resursseja sisältävät ennaltaehkäisevät ylläpitotyöt. |
| Ylläpitopyyntö | Resurssin manuaalisesti luotu ylläpito- tai korjauspyyntö. Tämä pyyntö voidaan muuntaa työtilaukseksi. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Työtilausten luominen ylläpitoaikataulun perusteella

Ylläpitoaikatauluun perustuvia työtilauksia luodaan seuraavasti:

1. Avaa jokin seuraavista sivuista sen mukaan, miten työtilausten aikataulutusnimikkeet valitaan:

    - Kaikki ylläpitoaikataulut (**Resurssien hallinta \> Hallinta-aikataulu \>Kaikki ylläpitoaikataulut**)
    - Avoimet ylläpitoaikataulurivit (**Resurssien hallinta \> Hallinta-aikataulu \> Avoimet ylläpitoaikataulurivit**)
    - Avoimet ylläpitoaikataulupoolit (**Resurssien hallinta \> Hallinta-aikataulu \> Avoimet ylläpitoaikataulupoolit**)

1. Valitse ruudukossa niiden aikataulutettujen ylläpitotöiden valintaruutu, joille haluat luoda työtilauksen. Valitse sitten toimintoruudussa **Työtilaus**.

    **Luo työtilaukset** -valintaikkuna avautuu. Valittujen rivien ennustetuntien kokonaismäärä näkyy **Ylläpitoennusteen tunnit** -kentässä.

    ![Luo työtilaukset -valintaikkuna.](media/18-preventive-maintenance.png)

1. Määritä **Parametrit**-osassa luotavien työtilausten määrä. Valitse jompikumpi seuraavista vaihtoehdoista:

    - **Yksi rivikohtainen työtilaus** – yksi työtilaus luodaan kullekin ylläpitoaikatauluriville.
    - **Yksi työtilaus perustuu** – Luotavat työtilaukset ryhmitellään muiden asetusten vaihtoehtojen mukaan. Nämä vaihtoehdot ovat käytettävissä, kun tämä vaihtoehto valitaan.

1. Valitse **Työtilaustyyppi**-kentässä työtilaustyyppi, jotka käytetään kaikissa luotavissa työtilauksissa.
1. Luo asetusten mukaisia työtilauksia valitsemalla **OK**.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Ylläpitosuunnitelman suorittamisen aikana automaattisesti luotavien työtilausrivien ryhmitteleminen

Tällä toiminnolla voidaan määrittää ylläpitosuunnitelman perusteella säännöt, joilla työtilausrivit ryhmitellään yhteen työtilaukseen, kun järjestelmä on määritetty luomaan työtilauksia automaattisesti. Aiemmin automaattisesti luoduissa työtilauksissa saattoi olla vain yksi rivi. Työtilaukset voidaan kuitenkin nyt ryhmitellä esimerkiksi resurssin, resurssin tyypin tai toiminnallisen sijainnin perusteella. (Tällainen ryhmittely oli jo mahdollisesti manuaalisesti luoduissa työtilauksissa tämän artikkelin edellisessä osassa kuvatulla tavalla.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Automaattisesti luotujen työtilausten ryhmittelyn ottaminen käyttöön

Ennen kuin voit käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Resurssien hallinta*
- **Toiminnon nimi:** *Työtilausten ryhmittelysääntöjen käyttäminen ylläpitosuunnitelmaa suoritettaessa*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Automaattisesti luotujen työtilausten ryhmittelyn määrittäminen

Automaattisesti luotujen työtilausten ryhmittely määritetään seuraavasti:

1. Valitse **Resurssien hallinta \> Asetukset \> Ennalta ehkäisevä ylläpito \>Ylläpitosuunnitelmat**.
1. Toimi seuraavasti jokaisessa suunnitelmassa, jossa halutaan luoda ryhmiteltyjä työtilauksia:

    1. Valitse suunnitelma luetteloruudussa.
    1. Varmista **Rivit**-pikavälilehdessä, että jokaisen rivin **Luo automaattisesti** -valintaruutu on valittu.

1. Valitse **Resurssien hallinta \> Kausittainen \> Ennalta ehkäisevä ylläpito \> Aikatauluta ylläpitosuunnitelmat**.
1. Määritä **Aikatauluta ylläpitosuunnitelmat** -valintaikkunan **Kausi**-osassa suunnitelman aikajakso (kuinka pitkältä tulevaisuudesta etsitään aikataulutettuja ylläpitotöitä, joille työ luodaan).
1. Määritä **Luo työtilaus automaattisesti aikataulusta** -asetukseksi *Kyllä*.
1. Valitse **Työtilaus**-osasta jokin seuraavista vaihtoehdoista:

    - **Yksi rivikohtainen työtilaus** – yksi työtilaus luodaan kullekin ylläpitoaikatauluriville. (Tämä vaihtoehto sisältää saman toiminnon, joka oli käytettävissä, kun *Työtilausten ryhmittelysääntöjen käyttäminen ylläpitosuunnitelmaa suoritettaessa* -toiminto oli poistettu käytöstä.)
    - **Yksi työtilaus perustuu** – Luotavat työtilaukset ryhmitellään muiden asetusten vaihtoehtojen mukaan. Nämä vaihtoehdot ovat käytettävissä, kun tämä vaihtoehto valitaan.

1. Jos vaihtoehtoja halutaan käyttää, kun vain osa ylläpitosuunnitelmista suoritetaan, lisää **Sisällytettävät tietueet** -pikavälilehdessä sopivat suodattimet aivan kuten muissakin Microsoft Dynamics 365 Supply Chain Managementin erätöissä.
1. Määritä **Suorita taustalla** -pikavälilehdessä tarvittavat erä- ja aikataulutusvaihtoehdot aivan kuten muissakin Supply Chain Managementin erätöissä.
1. Suorita ja/tai aikatauluta valitut ylläpitosuunnitelmat valitsemalla **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]