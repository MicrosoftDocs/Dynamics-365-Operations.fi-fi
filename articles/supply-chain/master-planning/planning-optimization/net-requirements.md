---
title: Nettotarpeet ja tarvekohdistustiedot
description: Tässä artikkelissa on tietoja lasketuista nettotarpeista ja tarvekohdistustiedoista.
author: t-benebo
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a31ff5490b08d92f0d966388b65de02bca25b050
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748435"
---
# <a name="net-requirements-and-pegging-information"></a>Nettotarpeet ja tarvekohdistustiedot

[!include [banner](../../includes/banner.md)]

Pääsuunnittelun ajon yhteydessä on tärkeää ymmärtää sen tuotos, kuinka nykyinen toimitus kattaa kysynnän ja miksi tietty toimitus on luotu. **Nettovaatimukset** -sivulla voit paremmin ymmärtää pääsuunnittelun tuottamat lasketut tarpeet.

**Nettotarpeet**-sivulla näkyvät nettotarpeet, jotka pääsuunnittelu on laskenut tuotteelle. Se näyttää myös pääsuunnittelun ajon aikana käyttöönottamisen kattavuusasetukset, erittelyn vaatimuksesta kokonaissummat tapahtumatyypeittain ja tarvekohdistustiedot.

## <a name="open-the-net-requirements-page"></a>Nettotarpeet-sivun avaaminen

Voit avata **Nettovaatimukset**-sivun seuraavilla tavoilla:

- Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**. Valitse tai avaa tuote. Valitse sitten toimintoruudun **Suunnittelu**-välilehden **Vaatimukset**-ryhmässä **Nettovaatimukset**.
- Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**. Avaa myyntitilaus. Valitse sitten **Myyntitilausrivit**-pikavälilehden työkaluriviltä **Tuotteet ja toimitus \> Nettotarpeet**.
- Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suunnitellut tilaukset**. Valitse tai avaa suunniteltu tilaus. Valitse sitten toimintoruudun **Näkymä**-välilehden **Vaatimukset**-ryhmässä **Vaatimusprofiili**.

## <a name="use-the-net-requirements-page"></a>Käytä Nettotarpeet-sivua

**Nettotarpeet**-sivu koostuu ylä- ja alaosasta. Tämän sivun toimintoruudussa on **Päivitys**-painike. Kun tämä painike on valittuna, näyttöön tulee komentovalikko.

### <a name="select-a-master-plan-to-view"></a>Valitse pääsuunnitelma, jota haluat tarkastella

Ennen kuin tarkistat tuotteen nettotarpeet, valitse asiaankuuluva pääsuunnitelma sivun yläosan **Suunnitelma**-kentästä.

### <a name="upper-section"></a>Yläosa

Sivun yläosassa on seuraavat välilehdet:

- **Yhteenveto** – Tarkastele tuotedimensioiden nimikevaatimuksia.
- **Nimikkeen kattavuus** – Tarkastele kattavuusasetuksia, joita käytettiin tarpeita laskettaessa.
- **Yhteenveto** – Tarkastele tarpeita koskevien loppusummien erittelyä tapahtumatyypin mukaan.
- **Kausi** – Tarkastele vastaanottoja, varasto-ottoja ja arvioitua käytettävissä olevia varastoja kullakin kausimalliin määritetyllä kaudella. Voit myös tarkastella oletetun varastosaatavuuden graafista näkymää.

### <a name="lower-section"></a>Alaosa

Sivun alaosassa on seuraavat välilehdet:

- **Yhteenveto** – Tarkastele pääsuunnittelun suorittamisen aikana laskettujen tuotevaatimusten luetteloa sekä tarpeita vastaavat varasto-otto- ja vastaanottotapahtumat. Oletusarvon mukaan luettelo lajitellaan tarvepäivän mukaan. Kun valitset tarpeen, alaosan **Tarvekohdistus**-pikavälilehti näyttää tarpeen lähteen tai tarpeen täyttävät tapahtumat.
- **Yleinen** – Näytä valitun vaatimuksen yksityiskohtaiset tiedot.
- **Toimenpide** – Tarkastele vaatimusten toimenpidesanomia.

### <a name="the-action-pane"></a>Toimintoruutu

Toimintoruudussa ovat käytettävissä seuraavat käskyt:

- **Päivitä \> Pääsuunnittelu** - Suorita pääsuunnittelu suoraan **Nettovaatimukset**-sivulta.
- **Päivitä \> Ennustesuunnittelu** - Suorita ennustesuunnittelu suoraan **Nettovaatimukset**-sivulta. Suunnittelun optimointi ei tue tätä toimintoa.
- **Päivitä \> Jatkuvuuden ajoitus** – Suorita jatkuvuuden ajoitus suoraan **Nettovaatimukset**-sivulta. Suunnittelun optimointi ei tue tätä toimintoa.

## <a name="example-scenario"></a>Esimerkkiskenaario

Tässä esimerkissä kerrotaan, miten tarvekohdistuksen tiedot näytetään **Nettovaatimukset**-sivulla.

### <a name="prerequisites"></a>Edellytykset

Valmistele seuraavat edellytykset ennen skenaarion käsittelyä:

1. Työskentele järjestelmässä, jossa vakio-otantatiedot ovat käytettävissä, ja määritä yrityksen arvoksi *USFM*.
2. Tässä esimerkissä käytetään tuotetta *1000*, joka on osa USMF-näytetietoja. Varmista, että tämä tuote on käytettävissä ja että se on määritetty seuraavasti:

    - **Oletustilaustyyppi:** *Ostotilaus*
    - **Käytettävissä oleva varasto** *10,00*

3. Luo myyntitilaus, jonka määrä on *25,00* ja tuote *1000*. Käytä varastodimensioita, joissa käytettävissä oleva varasto sijaitsee.
4. Suorita *DynPlan*-pääsuunnitelman pääsuunnittelu.

### <a name="review-the-calculated-requirements"></a>Tarkista lasketut vaatimukset

Seuraavaksi avaat tuotteen *1000* **nettovaatimuksia** tarkastelemalla, miten lasketut tarpeet vastaavat toisiaan.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse tuote, jonka **nimiketunnuksen** arvo on *1000*.
1. Valitse toimintoruudun **Suunnittelu**-välilehden **Vaatimukset**-ryhmässä **Nettovaatimukset**.
1. Määritä **Nettovaatimus**-sivulla **Suunnitelma**-kentän arvoksi *DynPlan*.
1. Varmista sivun alaosan **Yhteenveto**-välilehdessä, että seuraavat vaatimukset on lueteltu ruudukon riveinä.

    | Viite | Tarpeen määrä | Kumulatiivinen |
    |---|---|---|
    | Käytettävissä oleva | 10.00 | 10.00 |
    | Suunnitellut ostotilaukset | 15.00 | 25.00 |
    | Myyntitilaus | -25,00 | (Tyhjä) |

    > [!NOTE]
    > **Tarvemäärä**-kentässä näkyy kokonaismäärä, joka vaatimuksessa joko vaaditaan (jos arvo on negatiivinen) tai toimitus (jos arvo on positiivinen). **Kumulatiivinen**-kenttä edustaa vastaanottojen ja varasto-ottojen kokonaismäärää, joka kertyy valitulla kaudella.

1. Valitse *Käytettävissä oleva varasto* -tarverivi ja tarkista sitten **Tarvekohdistus**-pikavälilehdessä tarpeet, jotka tämä toimitus kattaa. Seuraava rivi tulee näkyviin.

    | Viite | Tarpeen määrä | Katettu määrä |
    |---|---|---|
    | Myyntitilaus | -25,00 | -10,00 |

    Käytettävissä oleva varasto kattaa osittain myyntitilauksesta peräisin olevan kysynnän.

    ![Käytettävissä olevan varaston tarvekohdistaminen](media/pegging-on-hand.png "Käytettävissä olevan varaston tarvekohdistaminen")

1. Valitse *Suunnitellut ostotilaukset* -tarverivi ja tarkista sitten **Tarvekohdistus**-pikavälilehdessä tarpeet, jotka tämä toimitus kattaa. Seuraava rivi tulee näkyviin.

    | Viite | Tarpeen määrä | Katettu määrä |
    |---|---|---|
    | Myyntitilaus | -25,00 | -15,00 |

    Koska myyntitilaus on jo osittain katettu, järjestelmä luo suunnitellun ostotilauksen jäljellä olevalle peruuttamattomalle määrälle.

    ![Suunnitellun ostotilauksen tarvekohdistaminen](media/pegging-planned-purchase-order.png "Suunnitellun ostotilauksen tarvekohdistaminen")

1. Valitse *Myyntitilaus*-tarverivi ja tarkista sitten **Tarvekohdistus**-pikavälilehdessä tarpeet, jotka tämä tarve kattaa. Seuraavat rivit tulevat näkyviin.

    | Viite | Tarpeen määrä | Katettu määrä |
    |---|---|---|
    | Käytettävissä oleva | 10.00 | 10.00 |
    | Suunnitellut ostotilaukset | 15.00 | 15.00 |

    ![Myyntitilauksen tarvekohdistaminen](media/pegging-planned-purchase-order.png "Myyntitilauksen tarvekohdistaminen")

> [!NOTE]
> *Varmuusvarasto*-vaatimustyyppi ei sisälly **Nettotarpeet**-sivuun.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
