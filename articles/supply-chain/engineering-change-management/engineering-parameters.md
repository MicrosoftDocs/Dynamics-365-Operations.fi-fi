---
title: Suunnittelun muutosten hallinnan parametrit
description: Tässä aiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementn suunnittelun muutostenhallintatoimintojen määrittämistä.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: dbe51e9e44cbdbf71d02e84c3a8634750f45ffa13b213fc1306a1047fb9e0b63
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725743"
---
# <a name="engineering-change-management-parameters"></a>Suunnittelun muutosten hallinnan parametrit

[!include [banner](../includes/banner.md)]

**Suunnittelun muutostenhallinnan parametrit** -sivulla on määritysparametreja, jotka muuttavat tuoterakenteen vapauttamis- ja suunnittelun muutostenhallintaprosesseihin liittyvää oletustoimintaa.

## <a name="open-the-engineering-change-management-parameters-page"></a>Suunnittelun muutostenhallinnan parametrit -sivun avaaminen

Avaa **Suunnittelun muutostenhallinnan parametrit** -sivu valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnittelun muutostenhallinnan parametrit**. Kentät voidaan sitten määrittää jäljempänä tässä aiheessa kuvatussa tavalla.

## <a name="release-control-tab"></a>Vapauta hallinta -välilehti

Seuraavassa taulukossa käsitellään kenttiä, jotka ovat käytettävissä **Suunnittelun muutostenhallinnan parametrit** -sivun **Vapauta hallinta** -välilehdessä. Nämä kentät vaikuttavat tuoterakenteen vapautusprosessiin.

| Kenttä | kuvaus |
|---|---|
| Nimikenumeron sääntö | Valitse, miten nimiketunnus määritetään, kun tuote vapautetaan yritykseen. Valitse *Suunnittelun tuotenumero*, jos vastaanottavan yrityksen tuotenumeron on vastattava suunnitteluyrityksen tuotenumeroa. Valitse *Paikallinen nimiketunnusjärjestys*, jos tuotteessa on käytettävä seuraavaa numeroa vastaanottavan yrityksen tuotenumeroiden numerojärjestyksessä. |
| Tuoterakenteen nimisääntö | Valitse, miten tuoterakenteen nimi määritetään, kun tuote vastaanotetaan (vapautetaan) yrityksessä. Valitse joko *Suunnittelunimi* tai *Vastaanoton nimiketunnus*. |
| Reitin nimisääntö | Valitse, miten reitin nimi määritetään, kun tuotteen reitti vastaanotetaan (vapautetaan) yrityksessä. Valitse joko *Suunnittelunimi* tai *Vastaanoton nimiketunnus*. |
| Suorita tuoterakennetarkistus | Valitse, suoritetaanko tuoterakennetarkistus, kun tuote vastaanotetaan (vapautetaan) yrityksessä. |
| Passiivisen tuoterakenteen julkaisukäyttäytyminen | Valitse, vapautetaanko tuote, jos siinä on passiivinen tuoterakenne. Valitse *Hyväksy*, *Vain varoitus* tai *Ei sallittu*. |
| Passiivisen reitin julkaisukäyttäytyminen | Valitse, vapautetaanko tuote, jos siinä on passiivinen reitti. Valitse *Hyväksy*, *Vain varoitus* tai *Ei sallittu*.|
| Tuotteen hyväksyntä | Valitse, tarvitaanko ylimääräinen hyväksyntävaihe ennen tuotteen vapauttamista yritykseen. Lisää hyväksyntävaihe valitsemalla *Manuaalinen*. Siinä tapauksessa tuotteet näkyvät **Avoimet tuotevapautukset** -sivulla. Valitse *Automaattinen*, jolloin tuotteet näytetään suoraan kohdeyritykset **Vapautetut tuotteet** -sivulla heti, kun tuote on vapautettu yhdessä vapautetun tuoterakenteen kanssa. |

## <a name="engineering-change-management-tab"></a>Suunnittelun muutostenhallinta -välilehti

Seuraavassa taulukossa käsitellään kenttiä, jotka ovat käytettävissä **Suunnittelun muutostenhallinnan parametrit** -sivun **Suunnittelun muutostenhallinta** -välilehdessä. Nämä asetukset vaikuttavat suunnittelun muutosten hallintaprosessiin.

| Kenttä | kuvaus |
|---|---|
| Luokka | Oletusluokka, jota käytetään, kun suunnittelun muutospyyntö luodaan. |
| Prioriteetti | Oletusprioriteetti, jota käytetään, kun suunnittelun muutospyyntö luodaan. |
| Vakavuussääntö | Valitse, miten suunnittelun muutostilauksen vakavuusaste luodaan. Valitse *Manuaalinen*, jos käyttäjän odotetaan antavan arvon **Vakavuusaste**-kenttään. Valitse *Laske*, jos järjestelmä laskee **Vakavuusaste**-kentän arvon, kun suunnittelun muutostilauksen toimintoruudussa valitaan **Laske vakavuusaste**. Siinä tapauksessa järjestelmä käyttää **Vakavuussääntöjoukko**-sivulla määritettyjä vakavuussääntöjä. Valitse *Laske automaattisesti*, jos **Vakavuusaste**-kentän arvo lasketaan ja täytetään automaattisesti vakavuussääntöjoukkojen mukaisesti. |
| Julkaise uudelleen tuotteet, joihin vaikutus kohdistuu | Tätä kenttää käytetään, kun tuotteita vapautetaan uudelleen suunnittelun muutostilausta käyttämällä. Voit valita, ehdotetaanko **Vapautukset**-valintaikkunassa kaikkia tuotteita vai vain tuotteita, joihin vaikutus kohdistuu. |
| Julkaistavat tuoterakennetasot | Vapautettavan tuoterakennetason syvyys. Jos tuoterakenteessa on enemmän tasoja (eli jos se on syvempi) kuin tässä määritetty arvo, tasot vapautetaan vain määritettyyn arvoon saakka. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]