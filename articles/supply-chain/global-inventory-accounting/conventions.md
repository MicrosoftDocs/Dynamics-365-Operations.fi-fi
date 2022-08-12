---
title: Käytännöt
description: Tässä artikkelissa kuvataan, miten määritetään yleisessä varastokirjanpidossa käytännöt kustannusten huomioon ottamiseksi.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f148d4c6ece543c8a11eee3e6dcdff47b3767936
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135497"
---
# <a name="conventions"></a>Käytännöt

[!include [banner](../includes/banner.md)]

Käytännöt ovat joukko käytäntöjä, jotka vaikuttavat järjestelmän toimintaan. Liiketoimintavaatimusten mukaan on määritettävä käytännöt käyttämällä niiden eri käytäntöjen yhdistelmiä, jotka määrittävät, miten kustannukset otetaan huomioon yleisessä varastokirjanpidossa. Kukin käytäntö voidaan liittää yhteen tai useaan kirjanpitoon, jotta kirjanpidossa käytettävät kirjanpitokäytännöt ovat yhdenmukaisia keskenään.

Voit määrittää käytännöt kohdassa **Yleinen varastokirjanpito \> Asetukset \> Käytännöt**. Määritä kullekin käytännölle seuraavat kentät:

- **Nimi** – Anna käytännön nimi.
- **Kuvaus** – anna käytännön kuvaus.
- **Kustannuskohdekäytäntö** – Valitse kustannuskohteen käytäntö. Nämä käytännöt määrittävät rakeisuustason, jota järjestelmä käyttää varastoarvon laskennassa ja ylläpitämisessä. Käytettävissä ovat seuraavat esimääritetyt asetukset:

    - Tuote
    - Tuote – toimipaikka
    - Tuote – toimipaikka – varasto

    Jos esimerkiksi valitset *tuote - toimipaikka*, jokaista varaston siirtotapahtumaa (sisään- tai uloskulkua) varten järjestelmä laskee ja ylläpitää kunkin tuotteen varastokustannuksia toimipaikkatasolla. Näin ollen alemman tason varastosiirrot, kuten fyysisen varaston taso, eivät vaikuta varastoarvoon. (Esimerkki fyysisen varaston tason siirrosta on nimikesiirto kahden fyysisen varaston välillä yhdessä toimipaikassa.) Samoin varastokustannuksia ei voi tarkastella alemmalla tasolla, esimerkiksi fyysisen varaston tasolla.

- **Syötemittausperusteen käytäntö** – Valitse syötemittausperusteen käytäntö. Nämä käytännöt määrittävät varastotiliin virtaavat kustannukset ja veloitettavat kustannukset. Kauppayrityksiä koskevat seuraavat vaihtoehdot:

    - **Normaali historia** – Kaikki kustannuskomponentit virtaavat varastotilille.
    - **Vakio** – Vakiokustannukset virtaavat varastotileille ja sovellettujen kustannusten ja toteutuneiden kustannusten erotus veloitetaan varianssitileille. Jos haluat luoda *Vakio*-syötemittausperusteen käytännön, sinun on ensin luotava hinnasto, josta käytäntö voi etsiä nimikkeen standardikustannuksia.
    - **Hinnastot** – Yleinen varastokirjanpito tukee nimikehintojen hakemista useista eri yrityksistä. Voit määrittää hinnaston, jota syötemittausperusteen käytäntö käyttää. Näin järjestelmä tietää, mistä nimikkeen hinta on haettava. Voit määrittää hinnastot noudattamalla seuraavia ohjeita:

        1. Anna nimi **Nimi**-kenttään.
        1. Syötä **Kuvaus**-kenttään kuvaus.
        1. Valitse **Kustannuslaskentatyyppi**-kentästä kustannuslaskentatyyppi (*Vakiokustannus* tai *Suunniteltu kustannus*).
        1. Valitse **Hintatyyppi**-kentässä hintatyyppi (*Kustannus*, *Osto* tai *Myyntihinta*).
        1. Lisää kustannuslaskentaversio.
        1. Vahvista hinnaston nimikehinnat valitsemalla toimintoruudussa **Hinta**.

- **Kustannusvirran oletuskäytäntö** – Valitse kustannusvirran oletuskäytäntö. Nämä käytännöt määrittävät, miten kustannukset poistetaan varastosta ja raportoidaan myytyjen tuotteiden kustannuksina. Käytettävissä ovat seuraavat esimääritetyt asetukset:

    - Keskimääräinen
    - Tietty – Erä

    > [!NOTE]
    > Yleinen varastokirjanpito on jatkuva varastojärjestelmä. Siksi järjestelmä seuraa varastoarvoa tapahtumakohtaisesti.

- **Kustannuselementin käytäntö** – Voit määrittää kustannuselementtien käytäntöjä ja linkittää ne tähän kenttään. *Kustannuselementti* on tapahtuman kuluttaman resurssin kustannus. Kustannuselementtien avulla voit seurata ja luokitella kustannuksia. Voit luoda kustannuselementtien käytäntöjä kirjoittamalla tiedot seuraaviin paikkoihin:

    - **Nimi**-kenttä
    - **Kuvaus**-kenttä
    - **Kustannuselementti**-luettelo
    - **Sääntö**-ruudukko

    Jos et halua enää jakaa varastoarvoa pidemmälle, sinun on silti luotava kustannuselementtiluettelo, jossa on yksi kustannuselementti. Sen jälkeen on luotava kustannuselementtien käytäntö, jonka mukaan kaikki asianmukaiset mittaustyypit (kustannuskomponentit) voidaan yhdistää tähän kustannuselementtiin.
