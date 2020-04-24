---
title: Lähetyksen automaattiset päivitykset
description: Tässä ohjeaiheessa on yleiskuvaus lähetysten automaattisesta päivitystoiminnosta.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6215bc21bd3ee377274556f09ba29231118e5002
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201361"
---
# <a name="shipment-auto-updates"></a>Lähetyksen automaattiset päivitykset

[!include [banner](../includes/banner.md)]

Lähetyksen automaattinen päivitystoiminto päivittää automaattisesti lähetykseen liitetyt kuormarivin määrät (sekä lisäykset että vähennykset) sen jälkeen, kun kuorma on vapautettu varastoon. Toiminto on käytössä siihen asti, että lähetyksen tai kuorman kuormarivi on käsitelty aallossa. Kun toimintoa käytetään, tilauspäivitykset voivat siirtyä varastoon ilman manuaalisia toimia varastotyön luontiin saakka.

Jos lähetyksen automaattista päivitystoimintoa ei käytetä, vain määrän vähennykset siirtyvät automaattisesti varastotyön luontiin saakka. Käyttäjien on päivitettävä tai poistettava rivit manuaalisesti, minkä jälkeen rivit on vapautettava manuaalisesti uudelleen, jos määrät kasvavat tai uusia tilausrivejä lisätään. Lähetyksen automaattisen päivitystoiminnon avulla yritykset voivat tehdä varastopäivitykset sujuvasti ilman, että oltava huolissaan siitä, miten liittyvät lähetykset ja kuormat vaikuttavat tilausrivipäivityksiin.

Lähetyksen automaattista päivitystoimintoa käytetään sekä myyntitilaus- että siirtotilausriveillä ja se otetaan käyttöön tietyssä varastossa. Niinpä yritykset voivat tarvittaessa käyttää erilaisia lähetyksen automaattisia päivityskäytäntöjä eri varastoissa. Määrän vähennystä koskevaa lähetyksen automaattista päivityskäytäntöä käytetään oletusarvoisesti kaikissa varastonhallintaprosesseja käyttävissä varastoissa. Jos oletuskäytäntöasetus on käytössä, vain määrän vähennykset siirtyvät automaattisesti lähetykseen ja kuormaan varastotyön luontiin saakka. Tämä toiminta tapa muistuttaa toimintaa, jota käytettiin ennen lähetyksen automaattisen päivitystoiminnon käyttöönottoa.

## <a name="main-elements-of-the-functionality"></a>Toiminnon pääelementit

Lähetyksen automaattinen päivitystoiminto määrittää pääasiassa lähetyksen tilan perusteella, onko kuormarivin määrää muutettava, kun myyntitilaus- tai siirtotilausriviä muutetaan. Se määrittää lähinnä lähetyksen tilan perusteella myös, lisätäänkö uusi kuormarivi automaattisesti aiemmin luotuun kuormaan. Jos lähetyksen tila on vähintään **Aalto**, automaattista päivitystä ei tehdä,

Myös aallon tila otetaan huomioon automaattisissa päivityksissä. Jos kuormariviin liittyvän aallon tila on **Pidetty**, **Suoritetaan**, **Vapautettu**, **Keräilty** tai **Lähetetty** ja jos käyttäjä yrittää vähentää kuormarivin määrää (vähentämällä myyntitilaus- tai siirtotilausrivin määrää), seuraava virhesanoma avautuu: Varauksia ei voi poistaa, koska luotuna on niistä riippuvaisia töitä. Jos aallon tila on lisäksi jokin edellä mainituista ja jos käyttäjä yrittää lisätä kuormarivin määrää epäsuorasti vähentämällä myyntitilaus- tai siirtotilausrivin määrää, kuormarivin määrä ei suurene automaattisesti. Siinä tapauksessa kuormarivi on päivitettävä manuaalisesti.

## <a name="scenarios"></a>Skenaariot

Lähetyksen automaattinen päivitystoiminto tukee neljää skenaariota: uuden tilausrivin lisääminen, tilausrivin määrän suurentaminen, tilausrivin määrän pienentäminen ja tilausrivin poistaminen.

- **Lisää uusi tilausrivi** – Jos **Varastot**-sivun **Varasto**-pikavälilehden **Lähetyksen automaattinen päivitys** -kentän (**Varastonhallinta \> Asetukset \> Varasto \> Varastot**) määrityksenä on **Aina**, jos tilaukselle on aiemmin luotu lähetys ja jos myynti- tai siirtotilaukseen lisätään uusi tilausrivi sen jälkeen, kun kuorma on jo luotu myyntitilaukselle, aiemmin luotua kuormaa ei päivitetä. Uusi kuormarivi, jossa ei ole viittausta aiemmin luotuun kuormaan, luodaan ja liitetään aiemmin luotuun lähetykseen. Uusi rivi lisätään kuormaan ja vapautetaan.
- **Suurenna määrää tilausrivillä** – Jos **Lähetyksen automaattinen päivitys** -kentän määrityksenä on **Aina**, jos tilaukselle on jo luotu lähetys ja jos aiemmin luodun myyntitilaus- tai siirtotilausrivin määrää suurennetaan sen jälkeen, kun myyntitilaukselle on jo luotu kuorma, kuormarivin määrää suurennetaan samalla määrällä kuin tilausriviä. Jos kuorma vapautettiin mutta työtä ei luotu, kuormarivin määrää suurennetaan samalla määrällä kuin tilausriviä.
- **Pienennä määrää tilausrivillä** – Jos **Lähetyksen automaattinen päivitys** -kentän määrityksenä on **Aina** tai **Määrää vähennettäessä**, jos tilaukselle on luotu lähetys aiemmin ja jos aiemmin luodun myyntitilaus- tai siirtotilausrivin määrää vähennetään sen jälkeen, kun myyntitilaukselle on jo luotu kuorma, liitetyn kuormarivin määrä päivitetään vastaavasti ellei kyseisen kuormarivin määrä ole jo yhtä suuri tai pienempi kuin tilausrivin uusi määrä. Siinä tapauksessa kuormarivi ei muutu. Jos kuorma vapautettiin mutta työtä ei luotu, liitetyn kuormarivin määrä päivitetään vastaavaksi ellei kuormarivin määrä ole jo yhtä suuri tai pienempi kuin tilausrivin uusi määrä. Siinä tapauksessa kuormarivi muuttuu.
- **Poista tilausrivi** – Jos **Lähetyksen automaattinen päivitys** -kentän määrityksenä **Aina** tai **Määrää vähennettäessä** ja käyttäjä yrittää poistaa tilausrivin, jolle kuormarivi on luotu, virhesanoma avautuu.

## <a name="example-scenario"></a>Esimerkkiskenaario

Demotietojen on oltava asennettuja tässä skenaariossa, ja sinun on käytettävä **USMF**-demotietoyritystä.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Lähetyksen automaattisen päivitystoiminnon ottaminen käyttöön

Ota lähetyksen automaattisen päivitystoiminto käyttöön seuraavien ohjeiden mukaisesti.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Varastot**.
2. Valitse varasto **24**.
3. Muuta **Varasto**-pikavälilehden **Lähetyksen automaattinen päivitys** -kentän arvo **Määrää vähennettäessä** arvoksi **Aina**.

Sen jälkeen kun arvoksi on muutettu **Aina**, myyntitilaus- ja siirtotilausrivien määrän suurentaminen tai pienentäminen ja uusien rivien lisäykset näkyvät valitun varaston lähetyksissä ja kuormissa. Edellä mainitut päivityksen rajoitukset on kuitenkin otettava huomioon.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Aaltomallin muuttaminen siten, että kuormarivejä ei käsitellä automaattisesti

Määritä aaltomalli seuraavien ohjeiden mukaisesti siten, että se ei käsittele kuormarivejä automaattisesti.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
2. Valitse aaltomalli **24 Lähetyksen oletus**.
3. Valitse **Muokkaa**.
4. Valitse **Yleiset**-pikavälilehden **Automatisoi aallon luonti** -asetukseksi **Kyllä** ja varmista, että kaikkien muiden vaihtoehtojen asetuksena on **Ei**.

On tärkeää, että mitään työtä ei luoda ja vapauteta automaattisesti aallon luontiprosessin osana. Kun myyntitilaukselle luotu kuormariviin liittyvä työ on luotu, kuormariviä ei enää päivitetä automaattisesti, jos myyntitilausrivin määrää muutetaan.

### <a name="create-a-sales-order"></a>Luo myyntitilaus

Luo myyntitilaus seuraavien ohjeiden mukaisesti.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
2. Valitse asiakas **US-003**.
3. Luo rivi nimiketunnukselle **A0001**.
4. Anna määräksi **10**. (Varmista, että käytössä on varasto **24**.)
5. Valitse **Tallenna**.
6. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**. Lähetys ja aalto luodaan.

Koska aaltomallia muutettiin edellisessä menettelyssä, kuormaa tai työtä ei luoda. Lähetyksen tila on **Avoin** ja aallon tila **Luotu**.

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Myyntitilausrivin määrän vähentäminen

Voit vähentää myyntitilausrivillä olevaa määrää seuraavien ohjeiden mukaisesti.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
2. Valitse juuri varastoon vapautettu myyntitilaus.
3. Valitse myyntitilausrivi. Muuta **Määrä**-kentän arvo**10** arvoksi **8**.
4. Valitse myyntitilausrivillä **Varasto \> Lähetyksen tiedot**. **Lähetyksen tiedot** -sivun **Kuormitusrivit**-pikavälilehdessä oleva määrä vastaa myyntitilausriville tehtyä muutosta.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Myyntitilausrivin määrän suurentaminen

Voit suurentaa myyntitilausrivillä olevaa määrää seuraavien ohjeiden mukaisesti.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
2. Valitse aiemmin varastoon vapautettu myyntitilaus.
3. Muuta rivillä olevan määrän arvo **8** arvoksi **12**.
4. Valitse **Tallenna**.
5. Palaa **Kaikki myyntitilaukset** -sivulle ja valitse myyntitilaus uudelleen.
5. Valitse toimintoruudun **Varasto**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Lähetyksen tiedot**. **Lähetyksen tiedot** -sivun **Kuormitusrivit**-pikavälilehdessä oleva määrä vastaa myyntitilausriville tehtyä muutosta.

Vaikka kuormarivillä oleva määrä on suurentunut (ennen 8, nyt 12), vain kahdeksan nimikettä jää varatuksi ellei automaattista varausta ole otettu käyttöön. Koska aiemmin luotuun varaukseen lisättyä määrää ei ole varattu, työ luodaan vain jo varatulle määrälle, jos aalto käsitellään tässä vaiheessa ilman varausta.

> [!NOTE]
> Jos tilausrivillä olevaa määrää vähennetään, kuormarivin määrä ei muutu, jos se on jo yhtä suuri tai pienempi kuin tilausrivin uusi määrä. Jos tilausrivillä olevaa määrää suurennetaan, kuormarivillä olevaa määrää suurennetaan samalla määrällä kuin tilausrivin määrää. Jos tilausrivin määrä ei ole sama kuin kuormarivin määrä, ero säilyy.

### <a name="add-a-sales-order-line"></a>Myyntitilausrivin lisääminen

Voit lisätä myyntitilausrivin seuraavien ohjeiden mukaisesti.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
2. Valitse aiemmin varastoon vapautettu myyntitilaus.
3. Luo rivi nimiketunnukselle **A0002**.
4. Kirjoita **Määrä**-kenttään **10**. (Varmista, että käytössä on varasto **24**.) Uusi rivi lisätään automaattisesti aiemmin luotuun lähetykseen.
5. Valitse **Tallenna**.
6. Palaa **Kaikki myyntitilaukset** -sivulle ja valitse myyntitilaus uudelleen.
7. Valitse toimintoruudun **Varasto**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Lähetyksen tiedot**. Huomaa **Lähetyksen tiedot** -sivun **Kuormitusrivin**-pikavälilehdessä oleva toinen kuormarivi.

Koska aiemmin luotuun lähetykseen juuri lisättyä myyntitilausriviä ei ole varattu, työ luodaan vain ensimmäisellä myyntitilausrivillä ja ensimmäisellä kuormarivillä olevalle määrälle, jos aalto käsitellään tässä vaiheessa.

### <a name="process-a-wave"></a>Aallon käsitteleminen

Käsittele aalto seuraavien ohjeiden mukaisesti.

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
2. Valitse aiemmin luomasi aalto.
3. Valitse toimintoruudun **Aalto**-välilehden **Aalto**-ryhmässä **Käsittele**.

Aalto käsitellään ja kuormariveillä varatuille määrille luodaan työ. Lähetyksen tila **Avoin** päivitetään tilaksi **Aalto**. Kun lähetyksen tilaksi on päivitetty **Aalto**, tapahtuvat muutokset, kuten rivimäärien vähennykset tai lisäykset tai uusien rivien lisääminen myyntitilaukseen, eivät vaikuta aaltolähetykseen liitettyihin aiemmin luotuihin kuormariveihin.

Jos lähetyksen tila on vähintään **Aalto**, myyntirivillä olevien määrien päivitykset eivät vaikuta lähetykseen liitettyyn kuormariviin eikä niitä tarkisteta tämän kuormarivin perusteella. Kuormarivillä olevaa määrää koskevat muutokset on tehtävä suoraan kuormarivillä.

Tarkistus tehdään sitten, kun kuormariville on luotu työ ja varaus on tehty. Myyntitilausrivillä olevan määrän vähennyt tarkistetaan sitten työrivin varauksen perusteella.
