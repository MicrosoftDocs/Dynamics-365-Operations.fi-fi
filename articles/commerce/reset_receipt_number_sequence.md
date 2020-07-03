---
title: Vastaanottonumeroiden palauttaminen
description: Tässä ohjeaiheessa kuvataan, miten voit nollata eri toimenpiteille käytettävät vastaanottonumerot haluamanasi päivämääränä (esimerkiksi tilivuosi tai kalenterivuosi).
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.openlocfilehash: e3243a69b98aae25ad8514890fb984c8a0d9f694
ms.sourcegitcommit: 218e22014a964b8b52fc0152e355b07b0b84ae2c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456570"
---
# <a name="reset-receipt-numbers"></a>Kuittinumeroiden nollaaminen 

[!include [banner](includes/banner.md)]

> [!NOTE]
> Toimintoprofiiliin kaikissa vastaanottotyypeissä on valittava **Itsenäinen sarja** -ominaisuus ennen tämän toiminnon käyttöä. Lisäksi sen laitteen järjestelmän aikavyöhykkeen, jossa myyntipistettä käytetään, on vastattava myymälän vastaavaa aikavyöhykettä. Nämä rajoitukset on tarkoitus poistaa tulevassa versiossa. Ota yhteys Microsoft-tukee ennen toiminnon käyttöä tuoteympäristössä.

Vähittäiskauppiaat luovat vastaanottonumeroita myymälän eri toimenpiteille, kuten käteis- ja siirtotapahtumille, palautustapahtumille, asiakastilauksille, tarjouksille ja maksuille. Vaikka vähittäiskauppiaat määrittävät omat kuittimuotonsa, joillakin mailla tai alueilla on asetuksia, jotka asettavat rajoituksia näille kuittimuodoille. Nämä asetukset voivat esimerkiksi rajoittaa kuitin merkkien määrää, vaatia peräkkäisiä vastaanottonumeroita, rajoittaa tiettyjä erikoismerkkejä tai vaatia vastaanottonumeroiden palauttamista vuoden alussa. Microsoft Dynamics 365 Commerce tekee vastaanottonumeroiden hallinnasta erittäin joustavia, jotta jälleenmyyjät voivat täyttää lakisääteiset vaatimukset. Tässä ohjeaiheessa kerrotaan, kuinka vastaanottonumeroiden nollaamiseen käytetään toimintoa.

Commercessa kuitin muodot voivat olla aakkosnumeerisia. Voit sijoittaa niihin sekä staattista että dynaamista sisältöä. Staattinen sisältö sisältää aakkosmerkin, numeroita ja erikoismerkkejä. Dynaaminen sisältö sisältää yhden tai useita merkkejä, jotka edustavat tietoja, kuten myymälän numeroa, päätteen numeroa, päivämäärää, kuukautta, vuotta ja numerosarjoja, joita kasvatetaan automaattisesti. Muodot määritetään toimintoprofiilin **Kuittien numerointi** -osassa. Seuraavassa taulukossa kuvataan dynaamista sisältöä edustavat merkit.

| Merkit | Kuvaus |
|------------|-------------|
| L          | Myymälän numerossa käytetään merkkiä **S**. Jos myymälän numero on esimerkiksi numeroitu HOUSTON1, **SSS**-muoto näkyy kuitissa ON1-muotona. Muodossa **SSSSS** näkyy kuitissa muodossa STON1. |
| T          | Päätteen numerossa käytetään merkkiä **T**. Jos päätteen numero on esimerkiksi numeroitu 0001, **TTTT**-muoto näkyy kuitissa 0001-muotona. |
| K          | Henkilökunnan numerossa käytetään merkkiä **C**. Jos esimerkiksi henkilökunnan jäsenellä on 000160 tunnus, **CCCC** -muoto näkyy kuitissa muodossa 0160. |
| ppp        | **Ppp**-merkit vastaavat vuoden päivää, 1 – 366. Esimerkiksi 15. tammikuuta **ppp**-muodossa näyttää kuitissa tekstin 015. |
| MM         | Merkkejä **KK** käytetään kaksinumeroisessa kuukaudessa. Esimerkiksi tammikuussa **KK**-muoto näyttää kuitissa tekstin 01. |
| PP         | Merkkejä **PP** käytetään kaksinumeroisessa kuukauden päivässä. Esimerkiksi 15. tammikuuta **PP**-muodossa näyttää kuitissa tekstin 15. |
| VV         | Merkkejä **VV** käytetään kaksinumeroisessa vuodessa. Esimerkiksi missä tahansa kuussa vuoden aikana 2020, muoto **VV** näyttää "20" kuitissa. |
| \#         | Numeromerkkiä (**\#**) käytetään peräkkäisessä numeroinnissa. Esimerkiksi muoto **####** näkyy kuitissa muodossa 0001, 0002, 0003, jne. |

Voit nollata vastaanoton peräkkäiset numerot tiettynä päivänä. Tämän jälkeen järjestelmä palauttaa ensimmäisen tapahtuman, joka tapahtuu, kun valittu nollauspäivämäärä on 12:00 AM, ja nollaa kuitin numerosarjan arvoksi 1. Voit myös määrittää, tapahtuuko palauttaminen vain kerran vai toistuuko se joka vuosi. Jos vuosittainen toistuminen määritetään, palautus tapahtuu automaattisesti joka vuosi, kunnes jälleenmyyjä päättää lopettaa sen. 

Nollaus otetaan käyttöön seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**.
1. Valitse **Kuitin numerointi** -pikavälilehdessä **Nollaa numeron nollauspäivämäärä**.
1. Valitse avattavasta valintaikkunasta **Nollaa päivämäärä** -kentästä tuleva päivämäärä, jolloin nollaus tapahtuu.
1. Valitse **Nollaa vastaanottotyyppi** -kentässä **Vain kerran** tai **Vuosittain**.
1. Valitse **OK**.

![Vastaanoton palautuspäivämäärän valitseminen](media/Enable_receipt_reset.png "Vastaanoton palautuspäivämäärän valitseminen")

Kun olet valinnut päivän, se näkyy **Seuraava kuitin numeron nollauspäivämäärä** -sarakkeessa. Palautuspäivämäärää voi soveltaa kaikkiin vastaanottotapahtumatyyppeihin. Tämän vuoksi vastaanoton numerosarja palautetaan kaikille kuittityypeille.

Kun nollauspäivämäärä saapuu, kunkin tyypin ensimmäisen tapahtuman vastaanottonumero palautetaan. Lisäksi toimintoprofiilissa palautetaan palautuspäivämäärä **Seuraava vastaanottonumeron nollauspäivämäärä** -sarakkeesta **Nykyisen vastaanottonumeron nollauspäivämäärä** -sarakkeeseen. Tämä muutos ilmaisee, että jos rekisteriä ei käytetä nollauspäivänä, vastaanottonumero palautetaan, kun rekisteriä seuraavan kerran *käytetään*. Esimerkiksi 3. joulukuuta 2019 -kohdassa valitaan palautuspäiväksi **1. tammikuuta 2020**. 1. tammikuuta, kun rekisterit tekevät ensimmäisen tapahtuman, vastaanottonumero nollataan. Yhtä rekisteriä ei kuitenkaan käytetä lainkaan joulukuun ja tammikuun aikana, mutta sen jälkeen sitä aletaan käyttää helmikuussa. Tässä tapauksessa, koska palautustoimenpide on määritetty, kyseisen rekisterin vastaanottonumero nollataan, kun rekisteri tekee ensimmäisen tapahtuman helmikuussa.

**Tyhjennä palautuspäivämäärä** -toiminnon avulla voit tyhjentää tulevat palautuspäivämäärät. Jos nollauspäivämäärä on kuitenkin tapahtunut menneisyydessä, sitä ei voi kumota. Näin ollen palautus tapahtuu edelleen kaikissa sellaisissa rekistereissä, joissa nollausta ei ole vielä tapahtunut.

> [!NOTE]
> Valitun palautuspäivämäärän ja kuitin muodon mukaan voi olla päällekkäisiä vastaanottonumeroita. Vaikka myyntipisteen (POS) järjestelmä voi käsitellä näitä tilanteita, se kasvattaa palautusten käsittelyyn tarvittavaa aikaa, koska myyntiedustajan on valittava kuittien kaksoiskappaleet. Muita tietojen tyhjennykseen liittyviä komplikaatioita voi ilmetä, jos päällekkäiset kuitit eivät ole suunniteltu seuraus. Tämän vuoksi on suositeltavaa käyttää dynaamisia päivämäärämerkkejä (esimerkiksi **ppp**, **KK**, **PP** ja **VV**), jotta voit estää kaksoisarvojen vastaanoton numeroiden nollautumisen jälkeen.
