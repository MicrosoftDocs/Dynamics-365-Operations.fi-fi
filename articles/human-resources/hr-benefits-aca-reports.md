---
title: Affordable Care Act (ACA) -raporttien luominen
description: Toiminnon tarkoituksena on auttaa niitä työnantajia, joiden on seurattava lomakkeissa 1095-B- ja 1095-C-ilmoitettavia tietoja. Näitä lomakkeita käytetään Affordable Care Act -lain työnantajan valtakirjaosassa. Huomaa, että toiminto on käytössä vain yhdysvaltalaisissa yrityksissä.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 3555be3067db459625df9f9b0ac6b78fc2715289
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418333"
---
# <a name="generate-affordable-care-act-aca-reports"></a>Affordable Care Act (ACA) -raporttien luominen

Toiminnon tarkoituksena on auttaa niitä työnantajia, joiden on seurattava lomakkeissa 1095-B- ja 1095-C-ilmoitettavia tietoja. Näitä lomakkeita käytetään Affordable Care Act -lain **työnantajan valtakirjaosassa**. Huomaa, että toiminto on käytössä vain yhdysvaltalaisissa yrityksissä.

## <a name="getting-started"></a>Aloittaminen
Kun 1095-B- ja 1095-C-lomakkeilla raportoitavien tietojen seuranta aloitetaan, aivan ensimmäiseksi on luotava vähintään yksi Affordable Care -kattavuusryhmä. Näillä Affordable Care -kattavuusryhmillä ilmaistaan työntekijälle tarjottava kattavuus, työntekijän osuus edullisimmasta kuukausimaksusta (jos kustannus ylittää liittovaltion köyhyysrajan) ja työnantajan mahdollisesti käyttämä Safe Harbor -ohjelma. Affordable Care Act -ryhmien käytön avulla voit hallita näitä kenttiä koskevia tietoja ilman jokaisen työtekijätietueen käsittelyä silloin, kun ehdot ovat samat. Lisäksi Affordable Care -kattavuusryhmät voi määrittää helposti yhdelle tai usealle työntekijälle sivun joukkomääritystoiminnolla.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Kattavuusryhmän useiden versioiden ylläpitäminen
Voit ylläpitää useita kattavuusryhmän versioita, joten voit ryhmän tiedot pysyvät ajan tasalla tekemällä muutoksia sen sijaan, että työntekijät määritettäisiin luotuun uuteen ryhmään aina, kun organisaatiossa ja tarjotuissa eduissa tapahtuu muutoksia. 

Kun olet luonut tarvittavat Affordable Care -kattavuusryhmät, voit määrittää työntekijät kerralla ryhmiin valitsemalla sivulla **Joukkomääritys**-toiminnon. Vaihtoehtoisesti voit siirtyä kunkin työntekijän sivulla ja ilmoittaa, onko ACA-tietoja seurattava ja onko ne raportoiva samalla kun määrität työntekijän Affordable Care -kattavuusryhmään.

Jos työntekijän Affordable Care -kattavuustietoja ei tarvitse seurata eikä raportoida esimerkiksi siksi, että kyseessä on osa-aikainen työntekijä, **Raportoi kattavuus** -kentässä voi valita Ei. Vaikka jokainen työntekijä, jonka ACA-tietoja on seurattava, on määritettävä Affordable Care -kattavuusryhmään, voit silti muuttaa minkä tahansa kuukauden tai kuukausien **Kattavuustarjous**-, **Työntekijän osa kustannuksista**- ja **Safe Harbor** -asetuksia, jos niissä on käytettävä jotain muuta kuin Affordable Care -kattavuusryhmälle annettua arvoa.

Voit määrittää Affordable Care -kattavuusryhmän arvoille poikkeuksille napsauttamalla Työntekijän tiedot -sivulla Affordable Care -kattavuuslinkkiä. Tämä linkki sijaitsee Työsuhde-välilehden Lisätiedot-osassa.

## <a name="reporting-health-care-coverage"></a>Terveydenhuollon kattavuuden raportointi
Sen lisäksi että seurataan minkä laajuinen terveydenhuolto kokopäiväisille työntekijöille on mahdollisesti tarjottu, lisätietoja on raportoiva 1095-C-lomakkeella, jos työntekijä tarjoaa työnantajan sponsoroimaa omakustanteista terveydenhuoltoa, johon työntekijä on rekisteröity (riippumatta siitä, onko kyse koko- vai osa-aikaisesta työntekijästä). Jokainen työntekijä (ja heidän huollettavansa), jonka työnantajan sponsoroimat etusuunnitelmat kattavat, on sisällytettävä raporttiin niiden kuukausien ajalta, joita kattavuus koskee. 

Voit ilmaista, onko kukin etusuunnitelma raportoiva, valitsemalla **ACA-raportoitavien** valintaruudun.

Jos työtekijät ovat lisäksi valinneet, että etu kattaa myös jonkin heidän huollettavansa, voit ilmaista etujen ylläpitosivulla kunkin työntekijän kohdalla päivämäärät, jolloin he olivat katettuna.. Voit ilmaista, että etu kattaa huollettavat, valitsemalla Huollettavat-pikavälilehden toimintoruudussa muokkauspainikkeen.

Voit ilmoittaa **Huollettavaa koskevien kattavuuspäivämäärien hallinta** -sivulla päivämäärät, jolloin etu kattoi huollettavan. Kun tällä sivulla annetaan päivämääriä, **Katettu**-valintaruutu valitaan automaattisesti **Etujen ylläpito** -sivulla.

## <a name="generate-1095b-and-1095c-forms"></a>1095B- ja 1095C-lomakkeiden luominen
Voit luoda 1095-B- ja 1095-C-lomakkeita myös tuotteesta ja jakaa ne työntekijöille. Järjestelmässä voidaan luoda myös sähköinen 1095-C- ja vastaava 1094-C-tiedosto, jotka voidaan lähettää IRS-virastoon.  

Anna 1095-C-lomaketta luotaessa oikea verovuosi ja ilmaise, onko sosiaaliturvatunnukset peitettävä. Jos tulostat 1095-C-lomakkeet yli 500 työntekijälle, PDF-tiedostoja on useita. Lisäksi suositellaan, että **Tiedoston enimmäiskoko** -asetukseksi määritetään **Tiedostonhallintaparametrit**-ikkunassa 150 Mt.

## <a name="viewing-information"></a>Tietojen tarkastelu
Voit tarkistaa **Työntekijän Affordable Care -kattavuus** -sivulla kuhunkin kattavuusryhmään määritetyt työntekijät, työntekijät, joita ei tarvitse sisällyttää raporttiin, ja määrittämättömät työntekijät.

Jos jokin Affordable Care -kattavuusryhmän oletusarvoista on korvattu, muutetun arvon vieressä näkyy tähtimerkki. Jos jokaisen 12 kuukauden arvo on sama eikä sitä ole korvattu, arvo tulostuu **Kaikki 12 kuukautta** -sarakkeessa.

Voit myös selvittää kyselyikkunan avulla työntekijät, joita ei tule ilmoittaa ACA:lle ja jotka on merkitty siten. Toisin sanojen heidän kohdallaan ei tarvitse selvittää, koskiko kattavuus heitä eikä heille tarvitse luoda 1095-C-lomaketta vuoden lopussa. Kun valitset **Suodatusperuste**-kentässä **Ei tule ilmoittaa ACA:lle**, voit luoda luettelon kaikista työntekijöistä, joilla on merkitä siitä, etteivät he saa 1095-C-lomaketta.

Sen lisäksi että käytössä luettelo työntekijöistä, joita ei ilmoiteta ACA:lle, voit tarkastella myös määrittämättömiä työntekijöitä (**ACA-raportoinnin kattavuuden** kenttä on tyhjä) tai työntekijöitä, jotka on määritetty **Vuosi**-kentässä valittuna vuonna vanhentuneeseen Affordable Care -kattavuusryhmään.

Voit viedä erilaisilla suodatusvalinnoilla luodun työntekijäluettelon Exceliin.

Jos katetut henkilöt on raportoitava, koska tarjoat työnantajana omakustanteisen vakuutuksen, voit tarkastella myös niiden etusuunnitelmien kattamia huollettavia, joissa on merkintä **ACA:lle ilmoitettavuudesta**, valitsemalla toimintoruuturivissä Näytä huollettavien kattaminen -toiminnon.

**Huomautus:** kyselyikkunassa näkyvät vain ne suunnitelmat, joissa on merkintä **ACA:lle raportoitavuudesta**.
