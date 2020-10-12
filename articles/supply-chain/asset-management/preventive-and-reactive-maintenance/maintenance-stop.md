---
title: Ylläpidon käyttökatkon tehtävät
description: Tässä aiheessa on tietoja ylläpidon käyttökatkon käyttämisestä kapasiteetin yleiskuvan saamiseksi. Se tarvitaan tietyjen käyttöomaisuuksien kunnossapitotöiden suorittamiseen tiettynä ajanjaksona.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 617fca55226e216197c385c88a9d7a8e3de03b03
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889982"
---
# <a name="maintenance-downtime-activities"></a>Ylläpidon käyttökatkon tehtävät

[!include [banner](../../includes/banner.md)]

Huoltoseisokkien avulla saadaan yleiskuva kapasiteetista, joka tarvitaan tietyjen käyttöomaisuuksien kunnossapitotöiden suorittamiseen tiettynä ajanjaksona. Voit esimerkiksi luoda tuotantolinjalla 10 huoltoseisokkimerkinnän tuotantohallissa nro 29-A (tuotantotoimipaikka 02). Huoltoseisokkien rekisteröinnillä on alkamis- ja päättymisaika, joka ilmaisee ajanjakson, jolloin kunnossapitoon liittyvä käyttöomaisuuserä ei ole käytettävissä tuotannossa.

**Ylläpidon käyttökatkojen toiminnot** on liittyvien resurssien kunnossapitoaikataulurivien ja työtilausten yllläpitotöiden yleiskatsaus tiettynä ajanjaksona. Kaikilla työtilausten kunnossapitotöihin liittyvillä riveillä on odotettu alkamispäivämäärä ylläpidon lopetuskauden aikana. Voit poimia hyödyllisiä tietoja ja tehdä muutoksia suunniteltuihin ylläpitotöihin:

- Hanki yleiskatsaus vaadituista tuotantolaitteiden (käyttöomaisuuden) käyttökatkokausista.  
- Saat yleiskuvan suunnitellun ylläpidon kapasiteetin kuormistuksesta (tunnit), jotka on ryhmitelty osaamisalueiden (vastuullisten huoltotyöntekijäryhmien tai kunnossapitotyöntekijöiden) mukaan, esimerkiksi sähköasentajat, hitsaajat tai muut huoltotyöntekijäryhmät, joita tarvitaan suunniteltujen huoltotöiden tekemiseen.  
- Tee muutoksia kunnossapitoaikatauluriveihin tai työtilausten ylläpitotöihin, jotka liittyvät käyttöomaisuuteen. Voit esimerkiksi muuttaa rivin odotettuja alkamis- ja loppuaikoja, tai valita muita kunnossapitotyöntekijöitä, joiden avulla työntekijöiden ja työntekijärymien työnkulku voidaan optimoida.

Kun kunnossapitoseisokkirekisteröinnissä on valittu käyttöomaisuudet, kaikki aktiiviseen työtilaukseen liittyvät avoimet ylläpitoaikataulurivit ja työtilausten kunnossapitotyöt sisältyvät huoltoseisokkien rekisteröimiseen.

## <a name="maintenance-downtime-activities"></a>Ylläpidon käyttökatkon tehtävät

Voit avata luettelon kaikista huoltoseisokkitehtävistä ja tarkastella joitakin toimintoihin liittyviä tietoja valitsemalla **Resurssien hallinta** > **Yhteiset** > **Ylläpidon käyttökatkojen toiminnot** > **Kaikki ylläpidon käyttökatkojen toiminnot**. Avaa tietonäkymä napsauttamalla **Ylläpidon käyttökatkojen toiminnot** -sarakkeen linkkiä. Alla olevassa kuvassa on esimerkki **Ylläpidon käyttökatkon tehtävät** -luettelosta.

![Kuva 1](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Kunnossapitoseisokkien toiminnon luominen

1. Valitse **Resurssien hallinta** > **Yhteiset** > **Ylläpidon käyttökatkojen toiminnot** > **Kaikki ylläpidon käyttökatkojen toiminnot** tai **Aktiiviset ylläpidon käyttökatkojen toiminnot**.

2. Valitse **Uusi**.

3. Lisää tunnus **Ylläpidon käyttökatkojen toiminnot**-kenttään ja laskurin nimi **Nimi**-kenttään.

4. Lisää huoltopysähdyksen kausi **Alkamispäivä/aika**- ja **päättymispäivä/aika** -kenttiin.

5. Valitse **Ylläpidon käyttökatkojen toimintojen resurssit** -pikavälilehdessä > **Lisää rivi**, jos haluat lisätä käyttöomaisuudet yksi kerrallaan huoltoseisokkitoimintoon.

6. Valitse **Tallenna**, kun kaikki käyttöomaisuudet on lisätty. Alla olevassa kuvassa on esimerkki huoltoseisokkien toiminnoista ja niihin liittyvistä käyttöomaisuuksista ja kunnossapitotöistä.

7. Valittuihin käyttö kohteisiin liittyvät työtilauksen ylläpitotyöt ja avointen kunnossapitoaikataulujen rivit näkyvät **Tuloksena olevat työtilauksen ylläpitotyöt**- ja **Ylläpitoaikataulun rivit** -pikavälilehdissä. **Yleiset**-pikavälilehden > **Työtilaukset**-ryhmän > **Ylläpitoennusteen tunnit** -kentässsä ja **Yleiset**-pikavälilehden > **Ylläpitoaikataulu** -ryhmän > **Ylläpitoennusteen tunnit** -kentässä näkyy työtilausten ylläpitotöiden ja ylläpitoaikataulurivien ennustettujen tuntien kokonaismäärän.

Alla olevassa kuvassa on esimerkki **Ylläpidon käyttökatkon tehtävät** -tietonäkymästä.

![Kuva 2](media/20-preventive-maintenance.png)

>[!NOTE]
>Valittuihin käyttökohteisiin liittyvät työtilauksen ylläpitotyöt ja ylläpitoaikataulurivit päivitetään automaattisesti, jos uusia työtilauksia tai ylläpitoaikataulurivejä luodaan huoltoseisokkien luomisen jälkeen. Jos esimerkiksi ajoitat ylläpitosuunnitelmia tai kunnossapitokierroksia liittyville käyttöomaisuuksille kaksi päivää huoltoseisokkien toiminnon luomisen jälkeen, kunnossapitoseisokkitoimintoon lisätään automaattisesti uudet ylläpitoaikataulurivit.

8. Valitse kohdassa **Kaikki ylläpidon käyttökatkojen toiminnot** > **Ylläpidon käyttökatkojen toiminnot** ylläpidon käyttökatkon toiminto luettelossa ja valitse **Kapasiteetin kuormitus** avataksesi **Laske kapasiteetin kuormitus** -valintaikkunan. Tämän valintaikkunan avulla saat yleiskuvan kapasiteetin kuormituksesta, esimerkiksi päivämääristä, omaisuuseristä, käyttöomaisuuslajeista ja kunnossapitotyötyypeistä. Huomaa, että valintaikkunassa näkyvät päivämäärät ovat **Ylläpidon käyttökatkojen toiminnot** -kohdassa valittuja alkamis- ja päättymispäiviä. Tämä laskenta sisältää huoltoseisokkitoimintoon liittyvät käyttöomaisuudet.

9. **Laske kapasiteetin kuormitus** -valintaikkunassa muokkaa aloitus- ja loppuaikoja tarvittaessa ja valitse, haluatko sisällyttää työtilaukset ja ylläpitosuunnitelmat laskentaan. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisen kapasiteetin kuormituksen laskennasta haluat liittyen toiminnallisiin sijainteihin. Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin resurssit, jotka on valittu huoltoseisokkitoiminnossa, näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kapasiteetin kuormituksen rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

10. Aloita laskenta valitsemalla **OK**. Tuntien kokonaismäärä näkyy **Kapasiteetin kuormitus** -yhteenvedossa. Valitse **Kapasiteetin kuormitus** -välilehden **Ryhmittely...**-toimintoruuturyhmissä painikkeet, joilla saadaan tarkka yleiskatsaus ennustettujen tuntien kohdistuksesta. Alla oleva kuva näyttää **Kapasiteetin kuormitus** -laskennan tulokset.

![Kuva 3](media/21-preventive-maintenance.png)

11. Kun olet saanut yleiskuvan kapasiteetin kuormituksesta ja haluat tehdä muutoksia työtilausten ylläpitotöihin tai ylläpitoaikatauluriveihin, palaa **Ylläpidon käyttökatkojen toiminnot** -tietonäkymään ja valitse oikaistavat rivit **Tuloksena olevat työtilauksen ylläpitotyöt**- ja **Ylläpitoaikataulun rivit** -pikavälilehdissä.

12. Napsauta **Oikaise**-painiketta ja päivitä valittujen työtilausten ylläpitotöiden tai ylläpitoaikataulurivien odotetut alkamis- ja päättymispäivämäärät, palvelutaso tai vastuulliset ylläpitotyöntekijät.

13. Valitse **OK**, kun olet tehnyt tarvittavat oikaisut. 

>[!NOTE]
>Työtilauksen ylläpitotyöt ja ylläpitoaikataulurivit, jotka eivät sisälly kunnossapitoseisokkikauteen sen jälkeen, kun olet tehnyt oikaisut, poistetaan automaattisesti kohdasta **Ylläpidon käyttökatkojen toiminnot**.

14. Valitse kohdassa **Kaikki ylläpidon käyttökatkojen toiminnot** > **Ylläpidon käyttökatkojen toiminnot** ylläpidon käyttökatkon toiminto luettelossa ja valitse **Nimike-ennuste** avataksesi **Laske nimikkeen ennuste** -valintaikkunan. Tämän valintaikkunan avulla voit laskea nimikkeiden (varaosien ja muiden tarvittavien nimikkeiden) ennusteita ja ryhmitellä ne niin, että ne saat yleiskuvan, esimerkiksi päiväyksen, käyttöomaisuuden, käyttöomaisuustyypin ja ylläpitotyön tyypin mukaan. Huomaa, että valintaikkunassa näkyvät päivämäärät ovat **Ylläpidon käyttökatkojen toiminnot** -kohdassa valittuja alkamis- ja päättymispäiviä. Tämä laskenta sisältää varaosia ja nimikkeitä, jotka liittyvät kunnossapitoseisokin toiminnoissa valittuihin käyttökohteisiin.

15. **Laske nimikkeen ennuste** -valintaikkunassa muokkaa aloitus- ja loppuaikoja tarvittaessa ja valitse, haluatko sisällyttää työtilaukset ja ylläpitosuunnitelmat laskentaan. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisen kapasiteetin kuormituksen laskennasta haluat liittyen toiminnallisiin sijainteihin. Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin resurssit, jotka on valittu huoltoseisokkitoiminnossa, näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kapasiteetin kuormituksen rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

16. Aloita laskenta valitsemalla **OK**. Nimike-ennusteiden kokonaismäärä näkyy **Nimike-ennuste** -yhteenvedossa. Valitse **Nimike-ennuste** -välilehden **Ryhmittely...**-toimintoruuturyhmissä painikkeita, joilla saadaan yleiskatsaus ennustettujen nimikkeiden kohdistuksesta. Alla olevassa kuvassa on **Nimike-ennuste**-laskennan tuloksia.

![Kuva 4](media/22-preventive-maintenance.png)

- Voit kopioida käyttökohteita yhdestä huoltoseisokkitehtävästä toiseen. Valitse**Kaikki ylläpidon käyttökatkojen toiminnot** -kohdassa **Kopioi ylläpidon käyttökatkojen toiminnot** -painike ja tee valinnat **Ylläpidon käyttökatkojen toiminnoista**- ja **Ylläpidon käyttökatkojen toimintoihin** -kentissä ja valitse **OK**.
- Napsauta **Kaikki ylläpidon käyttökatkojen toiminnot** -kohdassa **Ylläpitoaikataulun rivit**- tai **Aktiiviset työtilaukset**-painike ja avaa liittyvät luettelot ja tarkastele valittuun kunnossapitoseisokin toimintoon liittyviä rivejä.

