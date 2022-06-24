---
title: Manuaalisen varastosiirron lykätty käsittely
description: Tässä artikkelissa kuvataan, miten manuaalisen varastosiirron lykättyä käsittelyä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5e5d0a93a4c628d4867161d082b0f0e177ddb95c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863734"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Manuaalisen varastosiirron lykätty käsittely

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten manuaalisen varastosiirron lykättyä käsittelyä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

Lykätyn käsittelyn avulla varastotyöntekijät jatkavat työskentelyä, kun hyllytystoimintoa käsitellään taustalla. Lykätty käsittely on hyödyllinen silloin, kun palvelimella voi olla satunnaisia tai suunnittelemattomia lisäyksiä käsittelyaikaan, ja lisääntynyt käsittelyaika saattaa vaikuttaa työntekijän tuottavuuteen. *Varastosiirto*-työtyyppi on nyt lisätty tämän toiminnon tukemiin työlajeihin.

Taustakäsittely saadaan aikaan käyttämällä [Käsittele varastosovelluksen tapahtumia -ominaisuutta](warehouse-app-events.md).

## <a name="turn-on-this-feature-for-your-system"></a>Tämän ominaisuuden ottaminen käyttöön järjestelmällesi

Jos haluat käyttää tätä toimintoa, ota seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Ne on otettava käyttöön tässä järjestyksessä:

1. *Organisaation laajuinen työn esto*<br>(Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on pakollinen, joten se on oletusarvoisesti otettu käyttöön eikä sitä poistaa uudelleen käytöstä.)
1. *Käsittele varastosovelluksen tapahtumat*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä.)
1. *Lykätyt hyllytystoiminnot*
1. *Manuaalisen varastosiirtotoiminnon lykätty käsittely*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen, joten se on oletusarvoisesti otettu käyttöön eikä sitä poistaa uudelleen käytöstä.)

## <a name="configure-the-work-processing-policies"></a>Työn käsittelykäytäntöjen konfiguroiminen

Jos haluat käyttää lykättyä käsittelyä, sinun on määritettävä ja käytettävä työn käsittelykäytäntöä. Lykätyssä hyllykäsittelyssä [Varastotyön lykätty käsittely -ominaisuus](deferred-put.md) tukee seuraavia työtyyppejä: *Myyntitilaus*, *Siirtotilauksen varasto-otto* ja *Täydennys*. *Manuaalisen varastosiirron lykätty käsittely -toiminto* lisää uuden työtyypin: *Varastosiirto*.

Työn käsittelykäytäntö määritetään seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työn käsittelykäytännöt**.
1. Valitse aiemmin luotu käytäntö luettelosta tai luo uusi käytäntö valitsemalla toimintoruudussa **Uusi**. Jokaisen käytännön otsikossa on seuraavat kentät:

    - **Työn käsittelykäytännön nimi** – Työn käsittelykäytännön nimi.
    - **Kuvaus** – Työn käsittelykäytännön kuvaus.

1. Määritä **Käsittelysäännöt**-pikavälilehdessä sääntökokoelma, jota käytäntö koskee. Lisää ja poista sääntöjä tarpeen mukaan työkalurivin painikkeilla. Määritä kullekin säännölle seuraavat kentät:

    - **Työtilaustyyppi** – Valitse työtyyppi, jota käytäntö koskee.
    - **Toiminto** – Valitse toiminto, jota käsitellään käytännöllä. Jos olet valinnut *Varastosiirto* **Työtilaustyyppi**-kentästä, tätä kenttää ei tarvitse määrittää, koska sekä keräily- että poispanotoiminnot käsitellään yhtenä tapahtumana.
    - **Työn käsittelymenetelmä** – Valitse menetelmä, jota käytetään työrivin käsittelyssä. Jos valitset *Välitön*, käyttäytyminen muistuttaa toimintaa, jolloin rivin käsittelyyn ei käytetä työn käsittelykäytäntöjä. Jos valitset *Lykätty*, järjestelmä käyttää eräkehystä käyttävää lykättyä käsittelyä.
    - **Lykätty käsittelykynnys** – Jos määrität tämän kentän arvoksi *0* (nolla), rajaa ei ole. Tässä tapauksessa käytetään *lykättyä* käsittelymenetelmää, jos mahdollista. Jos tietyn raja-arvon laskenta on kynnysarvon alapuolella, käytetään *Välitön*-menetelmää. Muussa tapauksessa käytetään *Lykätty*-menetelmää, jos mahdollista. Myyntiin ja siirtoon liittyvän työn osalta kynnys lasketaan työhön liittyvien lähdekuormitusrivien määrän mukaan. Täydennystyötä varten raja-arvo lasketaan työrivien määräksi, joita työ täydentää. Jos määrität raja-arvoksi esimerkiksi *5* myynnille, varmistat, että pienemmät työt, joissa on vähemmän kuin viisi alkuperäistä lähdekuormitusriviä, eivät käytä lykättyä käsittelyä, mutta suuremmissa töissä sitä käytetään. Kynnys vaikuttaa vain, jos **Työn käsittelymenetelmä** on *Lykätty*.
    - **Lykätty käsittelyn eräryhmä** – Määritä eräryhmä, jota käytetään käsittelyyn. Jos olet valinnut *Varastosiirto* **Työtilaustyyppi**-kentässä, tätä kenttää ei tarvitse määrittää, koska eräryhmä on valittu **Käsittele varastosovelluksen tapahtumat** -valintaikkunassa.

## <a name="assign-the-work-creation-policy"></a>Työn luontikäytännön määrittäminen

Lisätietoja työn luontikäytännön määrittämisestä on kohdassa [Varastotyön lykätty käsittely](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Erätyön määrittäminen käsittelemään varastosovelluksen tapahtumia

Jos haluat käyttää *Manuaalisen varastosiirron lykätty käsittely -toiminnon* prosessia, määritä ajoitettu erätyö.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Käsittele varastosovelluksen tapahtumat**.
1. Määritä **Käsittele varastosovelluksen tapahtumat** -valintaruudussa **Suorita taustalla** -pikavälilehdessä **Eräkäsittely**-asetuksen arvoksi *Kyllä*.
1. Valitse **Toistuminen** ja määritä ajoaikataulu, joka vastaa yrityksesi vaatimuksia.
1. Valitse jokaisessa valintaikkunassa **OK**.

## <a name="inquire-about-the-warehouse-app-events"></a>Varastosovellustapahtumien kysely

Voit näyttää varastosovelluksen luoman tapahtumajonon ja tapahtumasanomat valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Mobiililaitteen lokit \> Varastosovelluksen tapahtumat**.

*Varastosiirto*-tapahtuman sanomien tilaksi tulee *Jonossa*, kun ne luodaan. Tämä tila ilmaisee, että **Käsittele varastosovelluksen tapahtumat** -erätyö poimii tapahtumasanomat ja käsittelee ne. Kun tilaksi päivitetään *Valmis*, kaikki liittyvät tapahtumat poistetaan jonosta.

Kaikki *Varastosiirto*-tapahtumat kertyvät yhteen kokoelmaan tapahtumatyyppiä ja varastoa kohden.

Erätyö käsittelee varastosovelluksen tapahtumat **Käsittele varastosovelluksen tapahtumat** -valintaikkunassa määritetyn toistumisen mukaan. Siksi kunnes sanoma on käsitelty, varastotunnus löytyy **Tunniste**-kentästä.

Sanoman tiedot sisältävät siirtoa koskevat tiedot (esimerkiksi kohteesta- ja kohteeseen-sijainnit).

Lisätietoja on kohdassa [Varastosovellustapahtuman käsittely](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Mobiililaitteen valikon määrittäminen ohittamaan lykätty käsittelykäytäntö

Lisätietoja siitä, miten mobiililaitteen valikon voi konfiguroida niin, että se ohittaa lykätyn käsittelykäytännön, on kohdassa [Varastotyön lykätty käsittely](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Vaikutus suljettuihin työpäiviin

Lisätietoja vaikutuksesta suljettuihin työpäiviin on kohdassa [Varastotyön lykätty käsittely](deferred-put.md).

## <a name="additional-resources"></a>Lisäresurssit

- [Varastotyön lykätty käsittely](deferred-put.md)
- [Varastosovelluksen tapahtumakäsittely](warehouse-app-events.md)
- [Varastotyön mobiililaitteiden määrittäminen](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
