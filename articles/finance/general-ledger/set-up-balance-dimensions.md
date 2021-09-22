---
title: Miten taloushallinnon dimensioiden tasaus määritetään?
description: Tässä ohjeaiheessa kuvataan Täsmäyttävä taloushallinnon dimensio -ominaisuuden määrityksen ja käytön vaihtoehdot.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: 188c15c4cb0c295a9fcbb08273ddb391fbc29e24
ms.sourcegitcommit: b4c78655f2ab4b0e7ead96dfb9cf087a18014253
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2021
ms.locfileid: "7468937"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Miten taloushallinnon dimensioiden tasaus määritetään?

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan Täsmäyttävä taloushallinnon dimensio -ominaisuuden määrityksen ja käytön vaihtoehdot.

## <a name="symptom"></a>Oire

Täsmäyttäviä taloushallinnon dimensioita voi määrittää kahdella tavalla. Ensimmäinen vaihtoehto on käyttää **Kirjanpito**-määrityssivun (**Kirjanpito \> Kirjanpidon määritys \> Kirjanpito**) **Täsmäyttävä taloushallinnon dimensio** -kenttää. Toinen vaihtoehto on käyttää **Taloushallinnon dimensiot** -sivun (**Kirjanpito > Tilikartta \> Dimensiot \> Taloushallinnon dimensiot**) **Vaadi dimension täsmäytystä** -kenttää. Tässä ohjeaiheessa kerrotaan näiden kahden vaihtoehdon ero.

## <a name="resolution"></a>Ratkaisu

Organisaatiot käyttävät täsmäyttäviä dimensioita yleensä sellaisen taseen luomiseen, joka täsmää taloushallinnon dimensioiden tasolla. Kummankaan ominaisuuden käyttöönotto ei täsmäytä kirjattuja täsmäyttämättömiä dimensioita. Sinun on ensin syötettävä manuaalisesti oikaisumerkintöjä, jotta tase on täsmäytetty, ennen kuin otat käyttöön kummankaan ominaisuuden.

Nämä kaksi vaihtoehtoa sulkevat toisensa pois. Organisaation käyttämän vaihtoehdon pitäisi perustua sen liiketoimintatarpeisiin. Kuulemme usein asiakkaista, jotka määrittävät täsmäyttävän dimension sekä kirjanpidon määrityksessä että taloushallinnon dimension määrityksessä ja suorittavat sitten osan jäljellä olevasta määrityksestä tai suorittavat sen kokonaan. Nämä asiakkaat eivät silti pysty kirjaamaan, koska taloushallinnon dimension tasolla on epätasapaino.

Seuraavissa osissa kuvataan molemmat vaihtoehdot ja selitetään, miten ne määritetään.

### <a name="ledger--balancing-financial-dimension"></a>Kirjanpito – Täsmäyttävä taloushallinnon dimensio

**Kirjanpito**-määrityssivun täsmäyttävää dimensiota käytetään yksiköiden välisen kirjanpidon mahdollistamiseen. Toiminto otetaan käyttöön seuraavalla tavalla.

1. Määritä, mikä taloushallinnon dimensio on täsmäyttävä dimensio.

    - Tämän toiminnon avulla voit valita täsmäyttäväksi dimensioksi vain yhden taloushallinnon dimension.
    - Älä valitse dimensiota **Kirjanpito**-määrityssivulla.
    - Varmista, että valitun taloushallinnon dimension tase on jo täsmäytetty.

2. Päivitä täsmäyttävän taloushallinnon dimension tilirakenne.

    - Täsmäyttävän taloushallinnon dimension on sisällyttävä kaikkiin kirjanpidossa määritettyihin tilirakenteisiin.
    - Taloushallinnon dimensio ei saa sallia tyhjiä kohtia tilirakenteessa. Tällä rajoituksella varmistetaan, että kaikki kirjanpitoon tehdyt kirjaukset sisältävät taloushallinnon dimension arvon. Tyhjä dimensio ei kelpaa, kun käytetään täsmäyttäviä dimensioita.

3. Määritä **Tilit automaattisia tapahtumia varten** -sivulla (**Kirjanpito \> Kirjausten määritys \> Tilit automaattisia tapahtumia varten**) yksiköiden väliset debitin ja kreditin päätilit.
4. Valitse **Kirjanpito**-määrityssivun (**Kirjanpito \> Kirjanpidon määritys \> Kirjanpito**) **Täsmäyttävä taloushallinnon dimensio** -kentässä täsmäytykseen käytettävä taloushallinnon dimensio.

Jos valittua taloushallinnon dimensiota ei ole täsmäytetty, kun tapahtumia merkitään ja kirjataan, järjestelmä lisää automaattisesti debit- tai kredit-merkinnät, jotka tarvitaan kirjanpitomerkinnän täsmäyttämiseen kirjauksen yhteydessä. Yksiköiden välisen tapahtuman debit- ja kredit-kirjanpitotilit näytetään kirjanpidon kirjatussa tositteessa. Niitä ei kuitenkaan näytetä kirjauskansioissa tai lähdeasiakirjoissa, joiden osalta merkinnät on kirjattu.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Taloushallinnon dimensiot – Vaadi dimension täsmäytys

Vaikka **Taloushallinnon dimensiot** -sivun täsmäyttävää dimensiota käyttävät yleensä julkisen sektorin yritykset, toiminto ei ole linkitettynä mihinkään julkisen sektorin määritysavaimeen. Koska järjestelmässä ei ole rajoituksia, voit käyttää tätä toimintoa, vaikka organisaatio ei olisi julkisen sektorin toimija.

Tätä toimintoa käytetään yleensä julkisen sektorin asiakaskannassa, koska se edellyttää, kirjausmäärityksiä käytetään kunkin tapahtuman automaattiseen täsmäytykseen. Siinä ei käytetä yksiköiden välisiä debit- ja kredit-tilejä, jotka on määritetty **Tilit automaattisia tapahtumia varten** -sivulla, kirjanpitomerkintöjen automaattiseen täsmäytykseen. Jos kirjanpitomerkintää ei täsmäytetä dimensiotasolla kirjausmääritysten käytön jälkeen, tapahtumaa ei kirjata, vaikka yksiköiden väliset debit- ja kredit-tilit olisi määritetty.

Kuulemme usein asiakkaista, jotka määrittävät täsmäyttävän dimensioin sekä kirjanpidon määrityksessä että taloushallinnon dimension määrityksessä. Tässä tapauksessa järjestelmä käyttää taloushallinnon dimensioiden toimintoa. Täsmäyttävien dimensioiden taloushallinnon dimensioiden tason määritys on ensisijainen kirjauksia tehtäessä. Kirjaus epäonnistuu, jos kirjausmääritys ei luo täsmäytettyä kirjanpitomerkintää taloushallinnon dimension tasolla.

Seuraavien ohjeiden avulla voit ottaa täsmäyttävän dimension käytön käyttöön taloushallinnon dimension tasolla.

1. Määritä, mitkä taloushallinnon dimensiot ovat täsmäyttäviä dimensioita.

    - Voit määrittää useita taloushallinnon dimensioita täsmäyttäviksi dimensioiksi.
    - Älä vielä määritä taloushallinnon dimensioita, joita vaaditaan tapahtuman täsmäyttämiseen **Taloushallinnon dimensiot** -sivulla.

2. Määritä kunkin organisaation käyttämän kirjauskansion tai lähdeasiakirjan kirjausmääritykset. Kirjausmääritykset käyttävät kirjaamattoman kirjauskansion tai lähdeasiakirjan kirjanpitotilejä "vastaavuusperusteina". Kirjausmääritys palauttaa tämän jälkeen "luodut merkinnät", jotka muodostavat kirjanpitomerkinnän. Jos kirjausmääritys on määritetty oikein, luotu merkintä sisältää vastaavuuskriteerit täyttävät kirjanpitotilit sekä muita tilejä kirjanpitomerkinnän täsmäyttämiseksi dimensiotasolla. Lisätietoja: [Kirjausmääritykset](posting-definitions.md). 
   
   Kaikki tapahtumatyypit eivät tue kirjausmäärityksiä. Kirjausmäärityksiä ei esimeriksi voi määrittää millekään tapahtumille, jotka on kirjattu kirjanpidon tai käyttöomaisuuden kirjauskansion kautta. Jos kirjauskansiolle ei voida määrittää kirjausmääritystä tai lähdeasiakirjaa, tapahtuma on täsmäytettävä manuaalisesti taloushallinnon dimension arvon osalta. Jos esimerkiksi tehdään kirjauskansiovienti ja Osasto-dimensio on täsmäyttävänä dimensiona, sinun on varmistettava, että kukin osastoarvo täsmää.  Jos jokaisen osastoarvon dimensiota ei ole täsmäytetty, tositetta ei kirjata, ennen kuin epätasapaino on korjattu lisäämällä tositteeseen manuaalisesti yksiköiden välinen debit tai kredit. 

    > [!IMPORTANT]
    > Jos liiallinen määrä tapahtumia on täsmäytettävä manuaalisesti, sinun **ei** kannata käyttää **Taloushallinnon dimensiot** -sivun täsmäyttävän dimension toimintoa. Käytä sen sijaan **Kirjanpito**-määrityssivun täsmäyttävän dimension toimintoa.

3. Kun kirjausmääritykset on määritetty, taloushallinnon dimensiot voidaan merkitä vaadittaviksi täsmäytykseen.

Tapahtumia merkittäessä ja kirjattaessa kirjausmääritykset kutsutaan kirjauksen aikana kirjanpitomerkintöjen määrittämistä varten. Jos taloushallinnon dimensiot täsmäävät, vahvistaminen tapahtuu, kun kirjanpitomerkinnät on määritetty. Jos taloushallinnon dimensiot eivät täsmää, tapahtumaa ei kirjata, ja saat sanoman, jonka mukaan tietyn dimension debitit eivät vastaa kreditejä.
