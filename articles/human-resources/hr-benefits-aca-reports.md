---
title: Affordable Care -lain (ACA) mukaisten raporttien luominen
description: Affordable Care Act (ACA) -raportointi luo lomakkeita 1095-B ja 1095-C, mikä tukee Affordable Care Act (ACA) -lain **Työnantajan valtakirja** -osaa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 055de1f0ff3f8fd4fadba0a685fd703b9d19d918
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805991"
---
# <a name="generate-aca-reports"></a>ACA-raporttien luominen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Affordable Care Act (ACA) -raportointi luo lomakkeita 1095-B ja 1095-C, mikä tukee Affordable Care Act (ACA) -lain **Työnantajan valtakirja** -osaa.

> [!NOTE]
> ACA-raportointi on käytössä vain yrityksissä Yhdysvalloissa.

## <a name="getting-started"></a>Aloittaminen

Voit seurata 1095-B- ja 1095-C-lomakkeiden tietoja luomalla ensin yhden tai useita Affordable Care -kattavuusryhmiä. Affordable Care -kattavuusryhmät ilmaisevat:

- Työntekijän kattavuustarjous
- Työntekijän osuus pienimmän kustannuksen kuukausittaisen lisän kustannuksista, jos kustannukset ovat liittovaltion köyhyysrajan yläpuolella
- Työnantajan käyttämä Safe Harbor (jos sovellettavissa)

Affordable Care Act -kattavuusryhmien avulla voit hallita näitä kenttiä koskevia tietoja ilman jokaisen työtekijätietueen muuttamista silloin, kun ehdot ovat samat. Affordable Care -kattavuusryhmät voi helposti määrittää helposti yhdelle tai usealle työntekijälle sivun **Joukkomääritys**-toiminnolla.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Kattavuusryhmän useiden versioiden ylläpitäminen

Voit ylläpitää useita versioita mistä tahansa kattavuusryhmästä. Tämän toiminnon avulla voit tehdä muutoksia ilman, että sinun tarvitse luoda uutta ryhmää ja määrittää siihen työntekijöitä uudelleen. 

Kun olet luonut ACA-kattavuusryhmät, voit määrittää ryhmät joukkotoimintona työntekijöille **Joukkomääritys**-vaihtoehdon avulla. Voit myös määrittää erikseen, seurataanko ja raportoitaanko ACA-tietoja, ja määrittää työntekijän Affordable Care -kattavuusryhmään.

Joitakin ACA-kattavuustietoja, kuten osa-aikatyöntekijöitä, ei tarvitse seurata. Määritä tällöin **Raportin kattavuus** -kentän arvoksi **Ei**. Vaikka jokaiselle työntekijälle on määritettävä jäljitettävät ACA-tiedot Affordable Care -kattavuusryhmään, voit silti muuttaa seuraavia asetuksia kuukausille, joissa on eri arvoja:

- **Kattavuustarjous**
- **Työntekijän osa kustannuksista**
- **Safe Harbor**

Voit määrittää Affordable Care -kattavuusryhmän arvoille poikkeuksille napsauttamalla **Työntekijän tiedot** -sivulla **Affordable Care -kattavuus** -linkkiä. Tämä linkki sijaitsee **Työsuhde**-välilehden **Lisätiedot**-osassa.

## <a name="reporting-health-care-coverage"></a>Terveydenhuollon kattavuuden raportointi

Sen lisäksi että seurataan minkä laajuinen terveydenhuolto kokopäiväisille työntekijöille on mahdollisesti tarjottu, lisätietoja on raportoiva 1095-C-lomakkeella, jos työntekijä tarjoaa työnantajan sponsoroimaa omakustanteista terveydenhuoltoa, johon työntekijä on rekisteröity (riippumatta siitä, onko kyse koko- vai osa-aikaisesta työntekijästä). Jokainen työntekijä (ja heidän huollettavansa), jonka työnantajan sponsoroimat etusuunnitelmat kattavat, on sisällytettävä raporttiin niiden kuukausien ajalta, joita kattavuus koskee. 

Voit ilmaista, onko kukin etusuunnitelma raportoiva, valitsemalla **ACA-raportoitavien** valintaruudun.

Jos työtekijät ovat lisäksi valinneet, että etu kattaa myös jonkin heidän huollettavansa, voit ilmaista **etujen ylläpitosivulla** kunkin työntekijän kohdalla päivämäärät, jolloin he olivat katettuna.. Voit ilmaista, että etu kattaa huollettavat, valitsemalla **Huollettavat**-pikavälilehden toimintoruudussa **Muokkaa**-painikkeen.

Voit ilmoittaa **Huollettavaa koskevien kattavuuspäivämäärien hallinta** -sivulla päivämäärät, jolloin etu kattoi huollettavan. Kun tällä sivulla annetaan päivämääriä, **Katettu**-valintaruutu valitaan automaattisesti **Etujen ylläpito** -sivulla.

## <a name="generate-1095-b-and-1095-c-forms"></a>Luo 1095-B- ja 1095-C-lomakkeita

Voit luoda 1095-B- ja 1095-C-lomakkeita myös tuotteesta ja jakaa ne työntekijöille. Järjestelmä voi myös luoda sähköisesti 1095-C-lomakkeita ja 1094-C IRS -siirtotiedostoja.  

Anna 1095-C-lomaketta luotaessa oikea verovuosi ja ilmaise, onko sosiaaliturvatunnukset peitettävä. Jos tulostat 1095-C-lomakkeet yli 500 työntekijälle, PDF-tiedostoja on useita. Lisäksi suositellaan, että **Tiedoston enimmäiskoko** -asetukseksi määritetään **Tiedostonhallintaparametrit**-ikkunassa 150 Mt.

## <a name="viewing-information"></a>Tietojen tarkastelu

Voit tarkistaa **Työntekijän Affordable Care -kattavuus** -sivulla kuhunkin kattavuusryhmään määritetyt työntekijät, työntekijät, joita ei tarvitse sisällyttää raporttiin, ja määrittämättömät työntekijät.

Jos jokin Affordable Care -kattavuusryhmän oletusarvoista on korvattu, muutetun arvon vieressä näkyy tähtimerkki. Jos jokaisen 12 kuukauden arvo on sama eikä sitä ole korvattu, arvo tulostuu **Kaikki 12 kuukautta** -sarakkeessa.

Kyselyikkunan avulla voit myös ymmärtää, mitkä työntekijät on merkitty siten ettei niitä ilmoiteta ACA:n mukaan. Sinun ei tarvitse seurata, onko kattavuus tarjottu heille, eikä heille tarvitse antaa 1095-C-lomaketta vuoden lopussa. Jos valitset **Suodatus**-kentästä **Ei ACA-raporttia**, näyttöön tulee luettelo kaikista työntekijöistä, jotka eivät saa 1095-C-lomaketta.

Sen lisäksi voit tarkastella määrittämättömiä työntekijöitä (**ACA-raportoinnin kattavuuden** kenttä on tyhjä) tai työntekijöitä, jotka on määritetty **Vuosi**-kentässä valittuna vuonna vanhentuneeseen Affordable Care -kattavuusryhmään.

Voit viedä erilaisilla suodatusvalinnoilla luodun työntekijäluettelon Exceliin.

Jos sinun on raportoitava kattavuuteen kuuluvat henkilöt itsevakuutettujen kattavuuden vuoksi, voit tarkastella kaikkia huollettavia, jotka on katettu **ACA-raportoitaviksi** merkityissä etusuunnitelmissa. Valitse toimintoruudussa **Näytä huollettavien kattavuus**.

> [!NOTE]
> Vain **ACA-raportoitavat** etusuunnitelmat näkyvät kyselyikkunassa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]