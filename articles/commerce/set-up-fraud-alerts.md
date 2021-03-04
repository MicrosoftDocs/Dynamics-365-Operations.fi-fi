---
title: Puhelinkeskuksen petosilmoitusten määrittäminen ja niiden käyttäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää säännöt, jotka hälyttävät asiakaspalvelun edustajalle, kun tilausten käsittelyn aikana havaitaan mahdollisia vilpillisiä tietoja. Voit määrittää tietyt koodit, joilla epäilyttävät tilaukset asetetaan automaattisesti tai manuaalisesti pitoon.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
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
ms.openlocfilehash: 38649e40021d1caaf70f217b3ebae0d488806180
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412050"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Puhelinkeskuksen petosilmoitusten määrittäminen ja niiden käyttäminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten ehdot ja säännöt määritetään siten, että mahdolliset vilpilliset myyntitilaukset voidaan asettaa niiden avulla pitoon myöhempää tarkistusta varten. Petostarkistusominaisuudella voidaan tarkistaa myyntitilauksen tietojen oikeellisuus. Jos myyntitilauksen tiedot näyttävät kyseenalaisilta organisaation petosehtojen ja -sääntöjen perusteella, tilaus voidaan asettaa pitoon myöhempää tarkistusta varten. Siinä tapauksessa tilausta ei vapauteta varastoon lisäkäsittelyä varten, ennen kuin se on poistettu pidosta.

> [!NOTE]
> Tätä toimintoa käytetään vain Commerce-puhelinkeskuskanavan myyntitilausten käsittelyssä.

## <a name="turning-on-the-fraud-check-feature"></a>Petostarkistustoiminnon ottaminen käyttöön

Petostarkistustoimintoa varten kanavan **Ota käyttöön tilausten viimeistely** -asetukseksi on valittava **Kyllä**, kun puhelinkeskuskanava on [määritetty](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options). Kun tilausten viimeistely on otettu käyttöön, puhelinkeskuksen käyttäjien valittava **Viimeistele** kaikkien luotujen myyntitilausten myyntitilaussivulla. Viimeistele-toiminto avaa **Myyntitilauksen yhteenveto** -sivun. Kun käyttäjät ovat antaneet pakolliset maksutiedot **Myyntitilauksen yhteenveto** -sivulla, he viimeistelevät tilauksen valitsemalla **Lähetä**. Tilauksen lähettäminen käynnistää petostarkistustoiminnon ja järjestelmässä mahdollisesti aktiivisina olevien sääntöjen mukaiset oikeellisuustarkistukset tehdään.

Valitsemalla **Lähetä** puhelinkeskuksen käyttäjät voivat asettaa myyntitilaukset pitoon petostarkistusta varten myös manuaalisesti. Myyntitilaus asetetaan manuaalisesti pitoon valitsemalla **Myyntitilauksen yhteenveto** -sivulla **Pito** \> **Manuaalinen petospito**. Sinua pyydetään sitten lisäämään kommentti, joka selittää, miksi tilaus asetettiin pitoon. Kommentti näkyy [tilausten pidon](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) työtilassa. Se selventää pidossa olevia tilauksia arvioivalle käyttäjälle, miksi pito asetettiin ja voidaanko tilaus vapauttaa.

Kanavan **Ota käyttöön tilausten viimeistely** -asetuksen määrityksen lisäksi petostarkistustoiminto on määritettävä myös puhelinkeskuksen parametreissa. Valitse **Retail ja Commerce** \> **Kanavan asetukset** \> **Puhelinkeskuksen asetukset** \> **Puhelinkeskuksen parametrit**. Valitse **Puhelinkeskuksen parametrit** -sivun **Pidot**-välilehdessä **Petostarkistus**-asetukseksi **Kyllä**.

Määritä **Pidot**-välilehdessä myös [pitokoodit](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), joita käyttämällä tilaus voidaan asettaa manuaalisesti tai automaattisesti pitoon petostarkistusta varten. Määritä pitokoodit **Manuaalinen petospitokoodi**- ja **Petospitokoodi**-kentissä. Voi olla kätevää luoda kaksi yksilöivää pitokoodia, jotta pidon työtilassa työskentelevät käyttäjät voivat helposti suodattaa ja erottaa automaattisesti pidot manuaalisista pidoista.

Jotta petostarkistustoiminto toimisi tehokkaasti, myös **Vähimmäispisteytys**-kenttä on määritettävä. Jokaisella järjestelmässä määritetyllä ehdolla ja säännöllä on pistemäärä. Kun myyntitilauksesta tarkistetaan petosvastaavuuksia ja mahdollisia vastaavuuksia löytyy, pistemäärät lasketaan yhteen. Tällä tavoin saadaan tilauksen petoksen kokonaispistemäärän. Jos tilauksen petoksen kokonaispistemäärä on suurempi kuin **Vähimmäispisteytys**-kentän arvo, tilaus asetetaan automaattisesti pitoon. Voit halutessasi käyttää muita **Pidot**-välilehden pisteytykseen liittyviä kenttiä ja määrittää niiden avulla sähköpostin, postinumeron ja laajennetun postinumeron pisteytyksen. Jos et määritä minkään tällaisen staattisen petosehdon pisteytystä, kun määrität niitä **Staattiset petostiedot** -sivulla, järjestelmä pisteyttää ne käyttämällä **Puhelinkeskuksen parametrit** -sivun **Pidot**-välilehdellä määritettyjä oletuspistemääriä.

Lopuksi **Petoksen kommenttityyppi** -kenttään määritetään asiakirjatyyppi, jota käytetään, kun käyttäjät lisäävät kommentteja petostarkistusta varten manuaalisesti pitoon asetettuihin tilauksiin. Yleensä tämän kentän arvo on **Huomautus**.

## <a name="defining-fraud-criteria-and-rules"></a>Petosehtojen ja -sääntöjen määrittäminen

Järjestelmä käyttää kahta petosehtotyyppiä määrittämään, on tilaus asetettava pitoon petostarkistusta varten.

- **Staattiset petostiedot** käyttää tiettyä arvoa, kuten estettyjen puhelinnumeroiden luetteloon lisättyä puhelinnumeroa tai sähköpostiosoitetta, joka on merkitty, koska kyseistä osoitetta on tiedetty käytetyn aiemmissa vilpillisissä tapahtumissa. Voit määrittää staattiset petostiedot valitsemalla **Retail ja Commerce** \> **Kanavan asetukset** \> **Puhelinkeskuksen asetukset** \> **Petos** \> **Staattiset petostiedot**. Voit lisätä petosehdot **Staattiset petostiedot** -sivulla manuaalisesti tai tuomalla ne. Pistemäärät liitetään vilpillisiin tietoihin. Jos petostarkistustoiminto on otettu käyttöön, jokaista kirjattua myyntitilausta verrataan staattisiin tietoihin. Jos tietoja löydetään asiakkaan tilauksen otsikkoon liitetystä laskutus- tai toimitusosoitteesta tai jos tietoja löytyy johonkin myyntitilauksen riviin liitetystä toimitusosoitteesta, yksilöivien vastaavuuksien pistemäärät lasketaan yhteen ja tätä yhteenlaskettua määrää **Vähimmäispisteytys**-arvoon vertaamalla määritetään, asetetaanko tilaus pitoon.

- **Petossäännöt** koostuvat käyttäjän määrittämistä muuttujista ja kyseissä muuttujissa määritetyistä ehdoista. Voit luoda sääntöjä valitsemalla **Retail ja Commerce** \> **Kananvan asetukset** \> **Puhelinkeskuksen asetukset** \> **Petos** \> **Säännöt**. Petossääntöjen avulla yritys voi määrittää useiden ehtojen arviointia varten monimutkaisen sääntöjoukon. Tämä on sääntöjoukko on monimutkaisempi kuin mitä saadaan aikaan **JA**- tai **TAI**-lausekkeita käyttämällä. Esimerkki: Käyttäjä haluaa, että petostarkistusta varten kaikki sellaisten asiakkaiden tilaukset asetetaan pitoon, jotka kuuluvat tiettyyn asiakasryhmään tai jotka tilaavat tietyn tuotteen. Tässä tapauksessa asiakkaan ja tuotteet tarkistavat ehdot määritetään **Säännöt**-sivulla JA-ehtoa käyttämällä. Tilaus asetetaan sitten pitoon vain, jos kumpikin ehto on tosi ja jos kyseiselle säännölle määritetty pisteytysarvo ja tilauksen muiden mahdollisten sääntöjen pisteytysarvo aiheuttavat sen, että tilauksen petoksen kokonaispistemäärä ylittää **Puhelinkeskuksen parametrit** -sivulla määritetyn **Vähimmäispisteytys**-arvon.

> [!NOTE]
> Useiden sääntöjen tai liian monimutkaisten sääntöjen käyttäminen heikentää järjestelmän toimintaa, kun myyntitilauksia lähetetään. Petostarkistustoimintoa ei ole optimoitu käsittelemään staattisten petostietojen tapahtumien suurta määrää eikä useita aktiivisia sääntöjä. Muista, että jokainen sääntö arvioidaan, kun puhelinkeskuksen käyttäjä valitsee **Lähetä** myyntitilausten käsittelyn aikana. Sääntöjä käytetään myyntitilauksen otsikon ja kaikkien tilausrivien arvioinnissa. Mitä enemmän sääntöjä on paljon ja mitä monimutkaisempia ne ovat, sitä enemmän aikaa niiden käsittelyyn tarvitaan. Jos tilauksessa on paljon rivinimikkeitä ja jos aktiivisia sääntöjä ja staattisten tietojen kirjauksia on paljon, kaikkien tietojen automaattinen tarkistus- ja vahvistuskäsittely sekä petospisteiden laskeminen voi vaikuttaa suorituskykyyn huomattavasti. Tätä toimintoa käyttävien organisaatioiden kannattaa aina testata tilausten lähetysten käsittelyyn kuluva aika ja vahvistaa, että tämä aika voidaan hyväksyä, ennen kuin sääntöjen tai staattisten petosehtojen muutokset otetaan käyttöön tuotantoympäristössä.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Petosten tarkistusta varten pitoon asetettujen tilausten tunnistaminen

Kun puhelinkeskuksen käyttäjät lähettävät myyntitilauksen ja kun tilaukselle löytyy vastaavuus petosehdoista tai -säännöistä ja kun pistemäärä ylittää vähimmäistason, käyttäjät saavat varoitusanoman, joka ilmoittaa, että tilaus on asetettu pitoon. Käyttäjät voivat sulkea tämän sanoman, koska se on tarkoitettu vain tiedoksi. Käyttäjillä on myös mahdollisuus ilmoittaa asiasta asiakkaalle. Yrityksen on määritettävä protokolla, jonka mukaan käyttäjät toimivat tässä tilanteessa.

Tilaus on tallennettu, mutta siihen on määritetty **Älä käsittele** -merkintä. Tämä merkintä auttaa varmistamaan, että tilausta ei vapauteta varastoon. Käyttäjät voivat koska tahansa tarkastella kaikkien **Tilan tiedot** -sivulla olevien myyntitilausten **Älä käsitele** -merkinnän asetuksia. Tämä sivu voidaan avata **Kaikki myyntitilaukset**- ja **Asiakaspalvelu**-sivuilta. Järjestelmä päivittää myös tilauksen **Tilan tiedot** -kentän arvoksi **Petospito**.

Voit tarkastella ja hallinta petostarkistusta varten pitoon asetettuja tilauksia valitsemalla **Retail ja Commerce** \> **Asiakkaat** \> **Tilausten pidot**. Valitse **Tilausten pidot** -sivulla luettelosta merkintä ja valitse sitten **Tilaus pidossa**. Näet nyt lisätietoja, kuten tietoja pidon syystä. **Petoksen tiedot** -pikavälilehdessä on tietoja järjestelmän petosehdoista, joille tilauksesta löytyi vastine, ja käytetty pisteytys. Jos tilaus on asetettu manuaaliseen pitoon, voit tarkastella tilauksen pitoon asettaneen käyttäjän antamia tietoja. Nämä tiedot ovat **Huomautukset**-pikavälilehden **Petoksen huomautukset** -osassa.

Lisätietoja tilauksen pitojen käyttämisestä on kohdassa [Tilauksen pidot](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).


[!INCLUDE[footer-include](../includes/footer-banner.md)]