---
title: Tarjouksiin ja tarjouspyyntöihin perustuvat suunnitelmat
description: Tässä artikkelissa kerrotaan, miten pääsuunnittelu määritetään ottamaan huomioon tarjoukset ja tarjouspyynnöt, kun suunniteltuja tilauksia luodaan.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690078"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Tarjouksiin ja tarjouspyyntöihin perustuva suunnitelma

[!include [banner](../../includes/banner.md)]

Tarjoukset ja tarjouspyynnöt edustavat mahdollisia tai todennäköisiä tulevia tilauksia. Tämän vuoksi ne kannattaa ottaa huomioon pääsuunnittelussa, jotta lisätarjonta voidaan suunnitella olemassa olevien tarjouspyyntöjen ja kunkin tarjouksen todelliseksi tilaukseksi muuttumisen todennäköisyyden perusteella. Tässä artikkelissa kerrotaan, miten pääsuunnittelu määritetään ottamaan huomioon tarjoukset ja tarjouspyynnöt, kun suunniteltuja tilauksia luodaan.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Pääsuunnittelun määrittäminen ottamaan huomioon myyntitarjoukset ja/tai tarjouspyynnöt

Alla olevien ohjeiden avulla voit määrittää pääsuunnittelun ottamaan huomioon myyntitarjoukset ja/tai tarjouspyynnöt.

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse luetteloruudussa aiemmin luotu suunnitelma tai luo uusi suunnitelma valitsemalla toimintoruudussa **Uusi**.
1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

    - **Sisällytä myyntitarjoukset** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat ottaa myyntitarjoukset huomioon, kun nykyinen suunnitelma suoritetaan. Määritä arvoksi *Ei*, jos haluat ohittaa ne.
    - **Todennäköisyysprosentti** – Määritä luottamuksen vähimmäistaso, joka vaaditaan, jotta tarjous sisällytetään pääsuunnitteluun. Pääsuunnittelun laskenta sisältää kaikki tarjoukset, jotka on luotu tämän todennäköisyysprosentin tai korkeamman prosentin omaavista mahdollisuuksista. Jos haluat sisällyttää kaikki tarjoukset, myös ne, joille ei ole määritetty todennäköisyyttä tai joihin ei liity mahdollisuutta, määritä tämän kentän arvoksi *0* (nolla). Lisätietoja tarjousten todennäköisyyksistä on seuraavassa osassa.
    - **Sisällytä tarjouspyynnöt** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat ottaa tarjouspyynnöt huomioon, kun nykyinen suunnitelma suoritetaan. Määritä arvoksi *Ei*, jos haluat ohittaa ne. Jos otat tarjouspyynnön huomioon, järjestelmä luo niille suunnitellut ostotilaukset. Toimittajaa ei voi määrittää, ennen kuin tarjouspyyntö on ratkaistu. Tarjouspyynnöille luodut suunnitellut ostotilaukset voivat vaikuttaa muiden suunniteltujen tilausten määriin.

1. Jatka pääsuunnitelman määrittämistä tavalliseen tapaan.

## <a name="assign-and-view-probabilities-for-quotations"></a>Tarjousten todennäköisyyksien määrittäminen ja tarkasteleminen

Kuten edellisessä osassa mainittiin, pääsuunnitelma ottaa huomioon vain tarjoukset, jotka vastaavat suunnitelmalle määritettyä todennäköisyyden raja-arvoa tai ylittävät sen (jos raja-arvo on määritetty). Todennäköisyyttä ei kuitenkaan määritetä suoraan kussakin tarjouksessa. Sen sijaan se periytyy tarjouksen luomisen yhteydessä käytetyltä mahdollisuudelta. Tämän vuoksi suoraan **Kaikki tarjoukset** -sivulla luotavia tarjouksia, joihin ei ole liitetty todennäköisyyttä tai mahdollisuutta, ei oteta milloinkaan huomioon pääsuunnitelmassa (ellei **Todennäköisyysprosentti**-kentän arvoksi ole määritetty *0* \[nolla\]). Tarjous on luotava mahdollisuudesta, jotta sille määritetään todennäköisyys.

### <a name="create-a-quotation-from-an-opportunity"></a>Tarjouksen luominen mahdollisuudesta

Seuraavia ohjeita noudattamalla voit määrittää mahdollisuudelle todennäköisyyden ja luoda sitten tarjouksen mahdollisuudesta.

1. Siirry kohtaan **Myynti ja markkinointi \> Suhteet \> Mahdollisuudet \> Kaikki mahdollisuudet**.
1. Valitse olemassa oleva mahdollisuus tai luo uusi mahdollisuus valitsemalla toimintoruudussa **Uusi**.
1. Täytä mahdollisuussivu määrittääksesi haluamasi mahdollisuuden. Varmista, että määrität **Todennäköisyys**-kenttään soveltuvan arvon. Vain pääsuunnitelmat, jotka on määritetty etsimään tämän arvon tai suuremman arvon todennäköisyyksiä, otetaan huomioon tästä mahdollisuudesta luoduissa tarjouksissa.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Mahdollisuus**-välilehden **Uusi**-ryhmässä **Myyntitarjous** tai **Projektitarjous** luotavan tarjouksen tyypin mukaan.
1. Määritä **Luo tarjous** -valintaikkunassa haluamasi kentät ja valitse sitten **OK**.
1. Uusi tarjous luodaan ja avataan. Käytä **Rivit**-pikavälilehdessä työkaluriviä lisätäksesi myynti- tai projektirivit vaaditulla tavalla tarjouksen sisällön määrittämistä varten.
1. Valitse toimintoruudussa **Tallenna**. Sulje sitten tarjous.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Tarjoukseen liitetyn todennäköisyyden tarkasteleminen

Ainoa tapa tarjoukselle määritetyn todennäköisyyden tarkastelemiseksi on avata mahdollisuus, jota käytettiin kyseisen tarjouksen luomisessa. Tämä toiminto kuvataan alla olevissa ohjeissa.

1. Valitse **Myynti ja markkinointi \> Myyntitarjoukset \> Kaikki tarjoukset**.
1. Jos **Mahdollisuuden tunnus** -sarake ei ole näkyvissä (se on piilotettu oletusasennuksessa), saat sen väliaikaisesti näkyviin alla olevien ohjeiden avulla. (Vaihtoehtoisesti voit säilyttää **Mahdollisuuden tunnus** -sarakkeen luomalla [tallennetun näkymän](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json), joka sisältää sen.)

    1. Valitse se ja pidä valittuna (tai valitse hiiren kakkospainikkeella) ruudukossa ja valitse sitten **Lisää sarakkeita**.
    1. Etsi **Lisää sarakkeita** -valintaikkunassa rivi, jossa **Kenttä**-kentän arvoksi on määritetty *Mahdollisuus*. Valitse kyseisen rivin **Valitse**-valintaruutu.
    1. Valitse **Päivitä**, jos haluat lisätä valitun sarakkeen **Kaikki tarjoukset** -sivulle.

1. Etsi tarjouksen rivi ruudukosta. Valitse sitten rivin arvo **Mahdollisuuden tunnus** -sarakkeesta.

    > [!NOTE]
    > Jos etsit projektitarjousta, sinun on ehkä valittava **Tarjoustyyppi**-sarakkeen otsikko ja tyhjennettävä sen suodatin. Oletusasennuksessa tämä suodatin määritetään siten, että vain myyntitarjoukset näytetään.

1. Liittyvä mahdollisuus avataan. Voit nyt tarkastella ja muokata **todennäköisyyden** arvoa haluamallasi tavalla.
