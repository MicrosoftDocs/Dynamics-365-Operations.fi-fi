---
title: "Määritä petoshälytyksiä"
description: "Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää säännöt, jotka hälyttävät asiakaspalvelun edustajalle, kun tilausten käsittelyn aikana havaitaan mahdollisia vilpillisiä tietoja. Voit määrittää erityisiä koodeja, joilla automaattisesti tai manuaalisesti asetetaan epäilyttävät tilaukset pitoon."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Petoshälytysten määrittäminen

[!include[banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten ehdot ja säännöt määritetään mahdollisesti virheelliset myyntitilaukset asetetaan pitoon myöhempää tarkistusta varten. Petosten tarkistustoimintoa käytetään myyntitilauksen tietojen oikeellisuuden määrityksessä. Jos myyntitilauksen tiedot näyttävät kyseenalaisilta organisaation petosehtojen ja -sääntöjen perusteella, tilaus voidaan asettaa pitoon järjestelmänvalvojan myöhempää tarkistusta varten.

> [!NOTE]
> Tätä toimintoa käytetään vain Retail-sovelluksen puhelinkeskuskanavan myyntitilausten käsittelyssä. 

Kun puhelinkeskuskanava määritetään, **Ota käyttöön tilausten viimeistely** -kohdan arvoksi on määritettävä **Kyllä**. Kun tilausten viimeistely on käytössä, käyttäjät voivat tarkastella tilauksen kertausta ja viimeistellä tilauksen valitsemalla **Lähetä**. Käyttäjät voivat asettaa myyntitilauksen pitoon petostarkistusta varten myös manuaalisesti. Puhelinkeskuksen käyttäjän näppäilemät myyntitilaukset tarkistetaan petokseen liittyvien tarkistussääntöjen ja -ehtojen avulla lähetysprosessin aikana.

Järjestelmä tarkistaa tilauksen kahden petokseen liittyvän ehdon perusteella ja määrittää, tuleeko tilaus asettaa estoon petokseen liittyvää tarkistusta varten.

-   **Staattiset säännöt** käyttävät tiettyä arvoa, kuten mustalla listalla olevaa puhelinnumeroa tai sähköpostiosoitetta, jota on käytetty aiemmin vilpillisissä tapahtumissa ja joka on merkitty tämän vuoksi. Petostiedot voidaan lisätä manuaalisesti **Staattiset petostiedot** -sivulla tai tietojen tuonnin kautta. Vilpillisiin tietoihin liitetään pisteet. Jos petosten tarkistus on päällä, jokaista järjestelmään syötettyä myyntitilausta verrataan staattisiin tietoihin. Jos tiedot löytyvät joko asiakkaan laskutus- tai toimitusosoitteesta tai myyntirivin toimitusosoitteesta, kaikkien yksilöivien vastaavuuksien pisteet lasketaan yhteen.  
-   **Dynaamiset säännöt** muodostetaan muuttujista ja näille muuttujille määritetyistä ehdoista. Dynaamisten sääntöjen avulla voidaan tarkistaa muut ehdot, joita ei ole määritetty staattisissa säännöissä. Monimutkaisempia AND-/OR-lausekkeita voidaan käyttää useiden ehtojen kanssa, kun määritetään, löytyykö säännön ehdoista ja lähetettävästä myyntitilauksesta positiivinen vastine. Jos käyttäjä haluaa esimerkiksi asettaa kaikkien tiettyyn asiakasryhmän arvoon liittyvien ja tietyn tuotteen tilanneiden asiakkaiden tilaukset pitoon petostarkistusta varten, asiakkaan ja tuotteiden vahvistuksen ehdot määritetään **Säännöt**-sivulla AND-ehdon avulla. Tilaukselle asetetaan pito petoksen vuoksi vain, jos molemmat ehdot ovat tosia ja jos säännölle määritetty pistearvo antaa tilauksen petoksen kokonaispistemääräksi puhelinkeskuksen parametreissa määritettyä vähimmäispistemäärää suuremman pistemäärän.

Puhelinkeskuksen käyttäjä voi asettaa tilauksen petospidon jonoon myös manuaalisesti. Jos tilausta syöttävä käyttäjä epäilee, että tilauksen tehnyt asiakas voi olla epäilyttävä, hän voi pyytää toista käyttäjää tarkistamaan tilauksen oikeellisuuden ennen tilauksen käsittelyä. Tämä tapahtuu niin, että tilausta syöttävä käyttäjä valitsee **Manuaalinen petospito** -asetuksen **Pidot**-valikosta **Myyntitilauksen yhteenveto** -sivulla (tämä tapahtuu sen jälkeen, kun **Valmis**-tilaustoimintoa on kutsuttu). Käyttäjää pyydetään antamaan tiedot, joissa kerrotaan, miksi tilaus tuntuu vilpilliseltä. Näin tarkistaja saa lisätietoja omaa työtään varten.

Kaikki tilaukset, joita käsitellään manuaalisessa petospidossa tai petospisteiden järjestelmällisessä laskennassa, näkyvät **Tilausten pidot**-sivulla. Sivulla tilaus voidaan tarkistaa ja joko peruuttaa tai vapauttaa käsittelyyn.

> [!NOTE]
> Useiden sääntöjen tai liian monimutkaisten sääntöjen käyttäminen aiheuttaa huonon järjestelmän suorituskyvyn myyntitilausten lähettämisen yhteydessä. Petosilmoitustoimintoa ei ole optimoitu käsittelemään staattisten petostietojen tapahtumien suurta määrää ja useita aktiivisia sääntöjä. On tärkeä muistaa, että jokainen sääntö arvioidaan puhelinkeskuksen myyntitilauskirjauksen lähetystoiminnon aikana. Sääntöjä käytetään myyntitilauksen otsikon ja kaikkien tilausrivien arvioinnissa. Jos sääntöjä on paljon ja jos ne ovat monimutkaisia, niiden käsitteleminen kestää kauan. Jos tilauksen rivinimikkeitä, aktiivisia sääntöjä ja staattisten tietojen kirjauksia on paljon, kaikkien tietojen järjestelmällinen tarkistus- ja vahvistuskäsittely sekä petospisteiden laskeminen voi vaikuttaa suorituskykyyn huomattavasti.  Tätä toimintoa käyttävien organisaatioiden kannattaa aina testata tilausten lähetysten käsittelyyn kuluva aika ja vahvistaa, että tämä on hyväksyttävissä rajoissa, ennen kuin sääntöjen tai staattisten petosehtojen muutokset otetaan käyttöön tuotantoympäristössä.

