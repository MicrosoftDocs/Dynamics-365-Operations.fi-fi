---
title: Suunnittelun optimoinnin julkaisuprosessi ja julkaisuhistoria
description: Tässä artikkelissa on tietoja suunnittelun optimoinnin julkaisuprosessista ja julkaisuhistoriasta.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: da97490cb065365a0502aa82c63205d5c34da9eb
ms.sourcegitcommit: 15b331f39d6e3ef811b9c2bf055a4f5b4572bae2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/26/2022
ms.locfileid: "9591874"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Suunnittelun optimoinnin julkaisuprosessi ja julkaisuhistoria

[!include [banner](../../includes/banner.md)]

Microsoft päivittää suunnittelun optimointia kuukausittain. Liiketoimintavaatimusten perusteella ajoitettujen julkaisujen välillä voidaan kuitenkin tehdä lisäpäivityksiä.

Kukin versio julkaistaan yksittäisillä alueilla, joilla suunnittelun optimointi on käytettävissä. Prosessi kestää yleensä kolme päivää.

Suunnittelun optimointia päivitetään, mutta pääsuunnittelu saattaa olla hitaampi kuin tavallisesti.

Ympäristöt, joissa suunnittelu optimointia käytetään, saavat automaattisesti viimeisimmän version. Käyttäjän toimenpiteitä ei tarvita: palvelu päivitetään automaattisesti. Yhtään katkeamistoimintoa ei kuitenkaan aina automaattisesti työnnetä ympäristöihin. Oletusarvon mukaan kaikki katkeamisena pidettävät muutokset on poistettu käytöstä, ja ne on nimenomaisesti otettava käyttöön käyttämällä [ominaisuuksien hallintaa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Muutokset eivät tule näkyviin ympäristöissä, ennen kuin otat muutokset käyttöön.

Koska ilmoitukset eivät näy, kun suunnittelun optimointi päivitetään ympäristössäsi, voit tarkistaa julkaisutiedot seuraavassa taulukossa ja selvittää, milloin muutokset on julkaistu ja mitä toimintoja on otettu käyttöön. Tässä taulukossa näkyvät suunnittelun optimointiin vapautetut muutokset sekä tiedot siitä, liittyvätkö muutokset ominaisuuden hallintaan, ja päivämäärän, jolloin muutokset on tehty.

<!-- KFM: Add this? [Use batch disposition codes to mark batches as available or unavailable](../../inventory/batch-disposition-codes.md) --> 

| Muutokset | Ominaisuuksien hallinnan tiedot | Vapautuspäivät |
|---|---|---|
| <p> Resurssin ajoituksen tuki rajallisen kapasiteetin kanssa. <p>Yleiset suorituskyvyn, laadun ja vakauden parannukset. | Ominaisuuksien hallintaa ei tarvita. | 19.–23. syyskuuta 2022 |
| <p>Yleiset suorituskyvyn, laadun ja vakauden parannukset. | Ominaisuuksien hallintaa ei tarvita. | 29.8.–3.9.2022 |
| <p>Yleiset suorituskyvyn, laadun ja vakauden parannukset.<p>[Suunnittelun optimointi - keskitetty kalenterin ylläpito](../supply-chain-calendars-master-planning.md)<p>[Optimointiehdotusten suunnittelu aiemmin luodun toimituksen optimointia varten](../action-messages.md)<p>[Alihankinnan tuki suunnittelun optimoinnissa](../../production-control/manage-subcontract-work-production.md) | Ominaisuuksien hallintaa ei tarvita. | 7.–11. maaliskuuta 2022 |
| <p>Tuotantotilausten suunnittelun prioriteetin tuki lisätty. | Saatavana versiossa 10.0.25 osana toimintoa nimeltä *Suunnittelun optimointiin perustuva prioriteetin MRP-tuki*. | 12.-18.11.2021 |
| <p>Yleiset suorituskyvyn, laadun ja vakauden parannukset. | Ominaisuuksien hallintaa ei tarvita. | 12.-18.11.2021 |
| <p>Lisättiin käsittelyajan laskentakaavojen, päällekkäisen tuotantoreitin ja tuotannon työvaihenumeron toimintojen tuki tarvetapahtumissa.</p><p>Parannettiin tuotannon aikataulutuksen virhesanomia, jotka liittyvät aikakatkaisuun, kapasiteettiin, jota ei löytynyt, ja sykliseen reittiin.</p><p>Parannettiin yhdenmukaisuutta laskettaessa vastaanotto- ja varasto-ottopäivämääriä sekä suunnitelluissa että vahvistetuissa tilauksissa.</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset. | Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus* | 22.–27. lokakuuta 2021 |
| <p>Lisättiin hävikkiprosentin huomioonottamisen tuki aikalaskentaa käsiteltäessä.</p><p>Lisättiin työvaihenumeron ja materiaalin käytön aikataulutuksen aikainen tuki. | Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus* | 5.–7. lokakuuta 2021 |
| <p>Lisättiin tuotantoreittien työtyyppien tuki: **Jonon ennen**, **Jono jälkeen** ja **Kuljetusaika**.</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset. | Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus* | 25.–30. syyskuuta 2021 |
| <p>Lisätty pääsuunnitelmien tuki asettamalla **Ajoitusmenetelmä** arvoon *Työvaiheiden ajoitus*.</p><p>Pidä **Reititysryhmät** -sivulla **Aktivointi**-, **Työaika**- ja **Kapasiteetti**-valintaruutujen asetukset riveillä, joissa **Työreitin/työn laji** on *Asennus* tai *Prosessi*. </p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset. | <p>Työvaiheiden ajoitus on käytettävissä ominaisuuksien hallinnassa versiosta 10.0.20.</p><p>Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus*</p>  | 9.–17. syyskuuta 2021 |
| Yleiset suorituskyvyn, laadun ja vakauden parannukset. | Ominaisuuksien hallintaa ei tarvita. | 25.–30. elokuuta 2021 |
| <p>Lisättiin **Läpimenoaika**-kenttä suunniteltuihin tilauksiin.</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset.</p> | Ominaisuuksien hallintaa ei tarvita. | 12.–17. elokuuta 2021 |
| <p>Lisättiin rajattoman kapasiteetin ajoituksen resurssityypin vaatimukset.</p><p>Parannettiin rajattoman kapasiteetin ajoituksen resurssin tehokkuutta ja kalenterin tehokkuutta.</p><p>Lisätietoja on kohdassa [Ajoittaminen rajattoman kapasiteetin avulla](infinite-capacity-planning.md). | <p>Käytettävissä ominaisuuksien hallinnassa versiosta 10.0.20.</p><p>Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus*</p> | 6.–12. heinäkuuta 2021 |
| Yleiset laadun parannukset. | Ominaisuuksien hallintaa ei tarvita. | 6.–12. heinäkuuta 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
