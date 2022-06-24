---
title: Asiakasnoudon ajankohtien luominen ja päivittäminen
description: Tässä artikkelissa kuvataan, miten asiakasnoudon aikavälit luodaan, määritetään ja päivitetään Commerce Headquarters -sovelluksessa.
author: anupamar-ms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: a135f592225e4b388b5c9fdaa5fe23e60baf0185
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882230"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Asiakasnoudon ajankohtien luominen ja päivittäminen

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, miten asiakasnoudon aikavälit luodaan, määritetään ja päivitetään Commerce Headquarters -sovelluksessa.

Aikaväliominaisuuden avulla jälleenmyyjät voivat määrittää aikavälin nimikkeille, joille asiakasnouto-toimitustapa on otettu käyttöön. Aikavälien avulla jälleenmyyjät voivat määrittää päivät ja ajat, jolloin tilaukset voidaan noutaa myymälästä. Vähittäiskauppiaat voivat myös määrittää tilausten määrän, joka voidaan noutaa tietyn jakson aikana. Näin vähittäiskauppiaat voivat rajoittaa tiettynä päivänä ja tiettynä ajankohtana kerättävissä olevien tilausten määrää. Tuloksena on laadukkaampi kokemus asiakkaille.

> [!NOTE]
> Aikaväli-ominaisuus on käytettävissä Microsoft Dynamics 365 Commerce -versiossa 10.0.15 ja uudemmissa versioissa.

Seuraavassa kuvassa näkyy esimerkki aikavälin valinnasta sähköisen kaupankäynnin kassalla.

![Esimerkki aikavälin valinnasta sähköisen kaupankäynnin kassalla.](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Aikavälin ominaisuudet

Aikaväli on tietty aikaväli, jolloin asiakas voi halutessaan noutaa tilauksen tietystä myymälästä tai sijainnista. Aikavälin hallintatoiminto on käytettävissä vain, kun asiakkaan noutotoimitustila on määritetty Dynamics 365 Commercessa.

Aikaväli määritetään seuraavien ominaisuuksien avulla:

- **Toimitustapa** – Määritä noutotapa, jota aikaväli koskee.
- **Minimipäivät** ja **Maksimipäivät** – Määritä ensimmäiset ja viimeiset päivämäärät, jotka voidaan valita noutoa varten suhteessa tilauksen päivämäärään. 

    **Minimipäivät**-ominaisuus varmistaa, että on riittävästi aikaa, jotta jälleenmyyjä voi käsitellä tilauksen, ennen kuin se on valmis noudettavaksi. **Maksimipäivät**-ominaisuus varmistaa, että käyttäjä ei voi valita päivä määrää, joka on liian kaukana tulevaisuudessa. Jos esimerkiksi vähimmäisarvoksi on määritetty **1** ja tilaus tehdään syyskuun 20. päivänä, tilaus on noudettavissa seuraavasta päivämäärästä (21. syyskuuta) eteenpäin. Samalla tavalla määrittämällä maksimiarvon voit määrittää päivien maksimimäärän, joiden aikana tilauksen voi noutaa. Kun vähimmäis- ja enimmäisarvot on määritetty, sivuston käyttäjät voivat tarkastella ja valita vain tietyn päivien aikavälin kassakokemuksensa aikana.

    Voit määrittää vähimmäisarvoksi desimaaliarvon, joka on pienempi kuin 1. Jos esimerkiksi nouto on käytettävissä neljä tuntia tilauksen jälkeen, määritä vähimmäisarvoksi **0,17** (= 4 ÷ 24, pyöristettynä kahden desimaalin tarkkuudella). Jos kuitenkin määrität vähimmäisarvoksi desimaaliarvon, joka on suurempi kuin 1, se pyöristetään aina lähimpään kokonaislukuun. Esimerkiksi arvo **1,2** pyöristetään ylöspäin lukuun **2**. Samoin, jos määrität enimmäisarvoksi desimaaliarvon, se pyöristetään aina lähimpään kokonaislukuun. 

- **Alkamispäivä**- ja **Päättymispäivä** – Määritä aikavälin alkamis- ja päättymispäivämäärät. Jokaisella aikavälillä on alkamis- ja päättymispäivämäärä. Siksi sinulla on joustavuutta lisätä eri aikavälejä ympäri vuoden (esimerkiksi noudot loma-aikoina). Jos aikavälin alkamis- ja päättymispäiviä muutetaan tilauksen jälkeen, muutokset eivät koske tätä tilausta. Kun määrität alkamis- ja päättymispäivät, sinun on otettava huomioon myymälän sulkemispäivämäärät (esimerkiksi joulupäivä) ja varmistettava, että aikavälejä ei ole määritetty näille päiville.
- **Aktiiviset noutoajat** – Määritä ajanjakso, jolloin nouto on sallittu. Esimerkiksi noutoajat voivat olla päivittäin klo 14.00-17.00. Tämän ominaisuuden avulla noutoajat voivat olla myymälän aukioloajoista riippumattomia. Näin ollen vähittäiskauppias voi määrittää erityiset liiketoimintavaatimuksensa täyttävät noutoajat. Kun määrität aktiiviset noutotunnit, sinun on otettava huomioon myymälän aukiolo ja varmistettava, etteivät noutoajat ole määritettynä ajankohtiin, jolloin myymälä on suljettu.

    > [!NOTE]
    > Myymälän noutotunnit on määritettävä asianmukaisen myymälän aikavyöhykkeellä.

- **Aikavälin kesto** – Määritä kesto, joka voidaan määrittää kullekin aikavälille. Esimerkiksi kunkin aikavälin kesto voi olla 15 minuuttia, 30 minuuttia tai yksi tunti. Jos ajanjakson arvo on 0, ajanjakso on käytettävissä koko keston ajan alkamis- ja päättymisajan välillä.
- **Tilauksia aikaväliä kohden** – Määritä niiden asiakkaiden tai tilausten määrä, jotka voidaan palvella noudettavaksi kunkin aikavälin aikana. Kirjoita esimerkiksi **1**, **2**, **3** tai jokin muu kokonaisluku.
- **Aktiiviset päivät** – Määritä viikonpäivät, jolloin noutoaikavälit ovat aktiivisia. Tämän ominaisuuden avulla vähittäiskauppias voi määrittää päivät, jolloin se haluaa tukea noutotilauksia.
- **Vähittäismyyntikanavat** – Määritä vähittäismyyntikanavat. Jokainen aikaväli voidaan liittää yhteen tai useampaan vähittäiskauppaan. Kunkin myymälän aukioloaikojen mukaan voidaan luoda yksi tai useita aikavälimerkintöjä, jotka liittyvät kanavaan. 

<!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Kanavaa kohden voidaan määrittää vain yksi aikavälimalli. Näitä kanavia ovat esimerkiksi kivijalkamyymälät, puhelineskukset, mobiililaitteet ja verkkokauppapaikat.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Aikaväliominaisuuden määrittäminen Commerce Headquarters -sovelluksessa

Aikavälit on määritettävä kunkin noutotavan mukaan Commerce Headquarters -sovelluksessa, jolloin myyntipiste- ja verkkokauppakanavat voivat viitata niihin.

- Kuhunkin myymälään tai kanavaan voidaan liittää vain yksi aikavälimalli.
- Jokaisen luotavan aikavälin tulee olla yksilöllinen kullekin toimitustavalle kussakin mallissa.
- Kun aikavälitoiminto on määritetty, aikavälikalenteri on käytettävissä valituissa myymälöissä tai myymäläryhmissä. Se näkyy myös myyntipisteessä viitteenä.

Voit määrittää aikaväliominaisuuden Commerce Headquarters -sovelluksessa seuraavasti.

1. Siirry kohtaan **Commerce** \> **Kanavan määritys** \> **Myymälän noutoaikaväli**.
1. Luo uusi aikavälimalli valitsemalla **Uusi**. Jos haluat käyttää aiemmin luotua mallia, valitse malli vasemmanpuoleisesta ruudusta.
1. Kirjoita arvot **Aikavälin tunnus**- ja **Kuvaus**-kenttiin.
1. Valitse **Tilauksen nouto – aika-asetukset** -pikavälilehdessä **Lisää**.
1. Määritä **Tilauksen nouto – aika-asetukset** -valintaikkunassa päivämääräväli, toimitustapa, aktiiviset toimitusajat, aktiiviset päivät, aikavälin kesto, tilaukset aikaväliä kohti sekä muut asetukset.

    Jos aikavälit ovat lähitulevaisuudessa pysyviä, määritä **Päättymispäivä**-kentän arvoksi **Ei koskaan**.

    > [!NOTE]
    > Voit luoda useita malleja, mutta vain yksi malli voidaan liittää yksittäiseen kanavaan tai myymälään.

    ![Tilauksen nouto – aika-asetukset -valintaikkuna.](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Kun olet valmis, valitse **OK**.
1. Jos päivän aikavälit vaihtelevat, varmista, että päivämäärät ja ajat eivät mene päällekkäin, luomalla lisä merkintöjä **Tilauksen nouto – aika-asetukset** -pikavälilehdessä.
1. Valitse **Vähittäismyyntikanavat**-pikavälilehdessä **Lisää**, jos haluat liittää aikavälimallin myymälöihin tai kanaviin, joissa sitä käytetään.
1. Valitse **Valitse organisaatiosolmut** -valintaikkunassa nuolinäppäimillä valiten (tai tyhjentämällä valinnan) ne myymälät, alueet ja organisaatiot, joihin malli liitetään.

    <!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Kun olet valmis, valitse **OK**.
1. Synkronoi tiedot kanaviin suorittamalla **Jakeluaikataulu** -sivulla **1070**- ja **1135**-työt.

## <a name="time-slot-selection-for-pos-orders"></a>Aikavälin valinta myyntipistetilauksissa

Kun myyntipisteessä on noutoa varten määritetty tilaus tai tilausrivi, kassanhoitaja voi valita noutomyymälän tai -sijainnin sekä päivämäärän ja aikavälin. Jos asiakkaalla on eri myymälään noutotilaus, kassanhoitaja voi valita päivämäärät, jolloin nouto on käytettävissä kyseisessä myymälässä. Myymälähaku sisältää viittauksen päivämääriin ja aukioloaikoihin.

Seuraavassa kuvassa näkyy esimerkki aikavälin valinnasta myyntipistetilauksessa.

![Esimerkki myyntipistetilauksen aikavälin valinnasta.](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Aikavälin valinta sähköisen kaupankäynnin tilauksissa

Lisätietoja siitä, miten aikavälin valinta on käytettävissä sähköisen kaupankäynnin tilauksille, on kohdassa [Noutotietomoduuli](../pickup-info-module.md).

> [!NOTE]
> Käyttäjät voivat tarkastella tai muokata noutoaikavälejä paikkoja Commerce-sivuston kassasivulla vain, jos noutotietomoduuli on lisätty kyseiselle sivulle. Jos kassasivu ei sisällä noutotietomoduulia, tilakset tehdään antamatta käyttäjien määrittää tai tarkastella aikavälin tietoja.

Seuraavassa kuvassa on esimerkki sähköisen kaupankäynnin tilauksesta, jossa noutoaikaväli on valittu.

![Esimerkki sähköisen kaupankäynnin tilauksesta, jossa noutoaikaväli on valittu.](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Aikavälin valinta puhelinkeskuksen tilauksissa

Soittokeskuksen asiakaspalvelijat voivat valita soittokeskussovelluksessa noutomyymälän tai -sijainnin sekä päivämäärän ja ajanjakson, kuten seuraavassa kuvassa on korostettu.

![Esimerkki puhelinkeskuksen tilauksesta, jossa noutoaikaväli on valittu.](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Lisäresurssit

[Noudon tiedot -moduuli](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]