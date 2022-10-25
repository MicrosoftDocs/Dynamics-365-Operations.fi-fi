---
title: Suunnittelun optimoinnin julkaisuprosessi ja julkaisuhistoria
description: Tässä artikkelissa on tietoja suunnittelun optimoinnin julkaisuprosessista ja julkaisuhistoriasta.
author: t-benebo
ms.date: 10/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: e2437214b4a2a850f121bb86272bf7dc3d313507
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682557"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Suunnittelun optimoinnin julkaisuprosessi ja julkaisuhistoria

[!include [banner](../../includes/banner.md)]

Microsoft päivittää suunnittelun optimointia kuukausittain. Liiketoimintavaatimusten perusteella ajoitettujen julkaisujen välillä voidaan kuitenkin tehdä lisäpäivityksiä.

Kukin versio julkaistaan yksittäisillä alueilla, joilla suunnittelun optimointi on käytettävissä. Prosessi kestää yleensä kolme päivää.

Suunnittelun optimointia päivitetään, mutta pääsuunnittelu saattaa olla hitaampi kuin tavallisesti.

Ympäristöt, joissa suunnittelu optimointia käytetään, saavat automaattisesti viimeisimmän version. Käyttäjän toimenpiteitä ei tarvita: palvelu päivitetään automaattisesti. Yhtään katkeamistoimintoa ei kuitenkaan aina automaattisesti työnnetä ympäristöihin. Oletusarvon mukaan kaikki katkeamisena pidettävät muutokset on poistettu käytöstä, ja ne on nimenomaisesti otettava käyttöön käyttämällä [ominaisuuksien hallintaa](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Muutokset eivät tule näkyviin ympäristöissä, ennen kuin otat muutokset käyttöön.

Koska ilmoitukset eivät näy, kun suunnittelun optimointi päivitetään ympäristössäsi, voit tarkistaa julkaisutiedot seuraavassa taulukossa ja selvittää, milloin muutokset on julkaistu ja mitä toimintoja on otettu käyttöön. Tässä taulukossa näkyvät suunnittelun optimointiin vapautetut muutokset sekä tiedot siitä, liittyvätkö muutokset ominaisuuden hallintaan, ja päivämäärän, jolloin muutokset on tehty.

| Muutokset | Ominaisuuksien hallinnan tiedot | Vapautuspäivät |
|---|---|---|
| <p>[Erän käsittelykoodit](../../inventory/batch-disposition-codes.md)</p><p>Käytettävissä olevan varaston ja varastotapahtumien parametrien sisällyttäminen pääsuunnitelmiin</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset</p> | Ominaisuuksien hallintaa ei tarvita | 10.–14. lokakuuta 2022 |
| <p>[Resurssien ajoitus rajallisen kapasiteetin avulla](finite-capacity.md)</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset</p> | Ominaisuuksien hallintaa ei tarvita | 19.–23. syyskuuta 2022 |
| Yleiset suorituskyvyn, laadun ja vakauden parannukset | Ominaisuuksien hallintaa ei tarvita | 29.8.–3.9.2022 |
| <p>[Keskitetty kalenterin ylläpito](../supply-chain-calendars-master-planning.md)</p><p>[Ehdotuksia aiemmin luodun tarjonnan optimointia varten](../action-messages.md)</p><p>[Alihankinnan tuki](../../production-control/manage-subcontract-work-production.md)</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset</p> | Ominaisuuksien hallintaa ei tarvita | 7.–11. maaliskuuta 2022 |
| Tuotantotilausten suunnittelun prioriteetin tuki | Saatavana versiossa 10.0.25 osana toimintoa nimeltä *Suunnittelun optimointiin perustuva prioriteetin MRP-tuki*. | 12.-18.11.2021 |
| Yleiset suorituskyvyn, laadun ja vakauden parannukset | Ominaisuuksien hallintaa ei tarvita | 12.-18.11.2021 |
| <p>Käsittelyajan laskentakaavojen, päällekkäisen tuotantoreitin ja tuotannon työvaihenumeron toimintojen tuki tarvetapahtumissa</p><p>Parannettiin tuotannon aikataulutuksen virhesanomia, jotka liittyvät aikakatkaisuun, kapasiteettiin, jota ei löytynyt, ja sykliseen reittiin</p><p>Parannettiin yhdenmukaisuutta laskettaessa vastaanotto- ja varasto-ottopäivämääriä sekä suunnitelluissa että vahvistetuissa tilauksissa</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset</p> | Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus* | 22.–27. lokakuuta 2021 |
| <p>Hävikkiprosentin huomioonottamisen tuki aikalaskentaa käsiteltäessä</p><p>Työvaihenumeron ja materiaalin käytön aikataulutuksen aikainen tuki</p> | Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus* | 5.–7. lokakuuta 2021 |
| <p>Tuotantoreittien työtyyppien tuki: **Jonon ennen**, **Jono jälkeen** ja **Kuljetusaika**</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset</p> | Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus* | 25.–30. syyskuuta 2021 |
| <p>Pääsuunnitelmien tuki asettamalla **Ajoitusmenetelmä** arvoon *Työvaiheiden ajoitus*</p><p>Säilytä **Reititysryhmät** -sivulla **Aktivointi**-, **Työaika**- ja **Kapasiteetti**-valintaruutujen asetukset riveillä, joissa **Työreitin/työn laji** on *Asennus* tai *Prosessi* </p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset</p> | <p>Työvaiheiden ajoitus on käytettävissä ominaisuuksien hallinnassa versiosta 10.0.20</p><p>Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus*</p> | 9.–17. syyskuuta 2021 |
| Yleiset suorituskyvyn, laadun ja vakauden parannukset | Ominaisuuksien hallintaa ei tarvita | 25.–30. elokuuta 2021 |
| <p>Lisättiin **Läpimenoaika**-kenttä suunniteltuihin tilauksiin.</p><p>Yleiset suorituskyvyn, laadun ja vakauden parannukset.</p> | Ominaisuuksien hallintaa ei tarvita | 12.–17. elokuuta 2021 |
| <p>Lisättiin rajattoman kapasiteetin ajoituksen resurssityypin vaatimukset</p><p>Parannettiin rajattoman kapasiteetin ajoituksen resurssin tehokkuutta ja kalenterin tehokkuutta</p><p>Lisätietoja on kohdassa [Ajoittaminen rajattoman kapasiteetin avulla](infinite-capacity-planning.md)</p> | <p>Käytettävissä ominaisuuksien hallinnassa versiosta 10.0.20</p><p>Ominaisuuden nimi: *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus*</p> | 6.–12. heinäkuuta 2021 |
| Yleiset laadun parannukset | Ominaisuuksien hallintaa ei tarvita | 6.–12. heinäkuuta 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
