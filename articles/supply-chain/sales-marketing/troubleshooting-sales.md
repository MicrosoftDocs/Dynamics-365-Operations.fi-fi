---
title: Myyntitilausten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitilausten käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6e51723915892f465ce09d09ee9ed622bab9451e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889454"
---
# <a name="troubleshoot-sales-orders"></a>Myyntitilausten vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitilausten käytössä voi esiintyä.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Verotietoja ei päivitetä, jos myyntitilauksen otsikon sijaintia muutetaan.

### <a name="issue-description"></a>Ongelman kuvaus

Jos toimipaikkaa, varastoa tai toimitusositetta muutetaan joko myyntitilauksen otsikossa tai rivitasolla, tapauksen verotietoja ei päivitetä riveillä automaattisesti.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus. Ongelma ilmenee, koska toimitusosoitetta, toimipaikkaa ja varastoa ei muuteta automaattisesti myöskään rivitasolla. Ne on päivitettävä manuaalisesti.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Jos samalle jaksolle tai päällekkäisille jakosoille on kaksi kauppasopimusta, valitaan aina sama sopimusrivi.

### <a name="issue-description"></a>Ongelman kuvaus

Jos samalle jaksolle tai päällekkäisille jakosoille on määritetty kaksi kauppasopimusta, vaikuttaa siltä, että sama kauppasopimus valitaan aina, kun luot asianomaisia nimikkeitä sisältäviä myyntitilausrivejä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Jos tietylle päivälle on useita kauppasopimuksia, valitaan aina matalimman hinnan kauppasopimus. Lisä tietoja saat lataamalla seuraavan teknisen raportin: [Kauppasopimukset Microsoft Dynamics AX 2012:ssa](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Voinko linkittää ostotilauksen myyntitilaukseen kysynnän täyttämiseksi?

Voit luoda ostotilauksen myyntitilauksesta. Lisätietoja: [Ostotilauksen luominen myyntitilauksesta](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Palautustilausta tai myyntitilausta ei voi peruuttaa eikä poistaa.

Voit peruuttaa vain myynti- ja palautustilauksia, jotka ovat tilassa *Luotu*. Lisätietoja: [Palautustilauksen peruuttaminen](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Kun yritän peruuttaa myyntitilauksen, näyttöön tulee virhe "Varauksia ei voi poistaa, koska on luotu töitä, jotka ovat riippuvaisia niistä".

Jos myyntitilaukseen liittyy työtä, et voi peruuttaa myyntitilausta, ennen kuin työ peruutetaan ja palautetaan. Tämä vaatimus on pätee, vaikka myyntitilaukseen liittyvä työ olisi suljettu.

Korjaa tämä ongelma seuraavien ohjeiden mukaisesti.

1. Peruuta työ ja siirrä varasto takaisin haluttuun sijaintiin. Siirry asianomaiseen myyntitilauksen kuormaan ja valitse joko **Vähennä kerättävää määrää** kuormarivillä tai **Palauta työ** toimintoruudussa.

    Työn tila on nyt *Peruutettu*, ja uusi varastosiirtotyö luodaan ja käsitellään automaattisesti, jotta varastonimikkeet palautetaan sijaintiin, joka kuvattiin palautuksen yhteydessä.

2. Poista kuorma. Myös lähetys poistetaan.
3. Nyt on pitäisi olla mahdollista siirtyä takaisin myyntitilaukseen ja perua se.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>En voi peruuttaa konsernin sisäistä ostotilausta, joka on linkitetty myyntitilaukseen.

### <a name="issue-description"></a>Ongelman kuvaus

Jos yrität peruuttaa myyntitilaukseen linkitetyn konsernin sisäisen ostotilauksen, näyttöön saattaa tulla seuraava virhesanoma: "Määrää ei voi vähentää, koska jäljelle jäävä päivitysmäärä muuttaa allekirjoitusta".

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä ongelma korjattiin Microsoft Dynamics 365 Supply Chain Managementin versiossa 10.0.13. Tässä versiossa ja uudemmissa versioissa voit nyt peruuttaa konsernin sisäisen ostotilauksen, joka on linkitetty myyntitilaukseen.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Voinko palauttaa poistetun laskutetun myyntitilauksen?

### <a name="issue-description"></a>Ongelman kuvaus

Laskutettu myyntitilaus poistettiin vahingossa, ja haluat palauttaa sen tai tarkastella sen tietoja.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Jos poistettu myyntitilaus on jo laskutettu, siirry kohtaan **Asiakastili \> Tapahtumat \> Alkuperäinen asiakirja \> Näytä tiedot**. Etsi haluamasi lasku ja valitse se, jotta voit tarkastella sen tietoja. Näihin tietoihin sisältyvät myyntitilauksen viite. Myös myyntitilauksen tietojen käytön pitäisi olla mahdollista kyseiseltä sivulta.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Myyntitilauksen otsikon määräaikaa ei löydy tietoentiteetistä SalesOrderHeaderV2Entity.

Entiteetissä *SalesOrderHeaderV2Entiy* ei ole määräaikakenttää.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Minun on poistettava orvoksi jääneet myyntitilaustietueet.

Voit tyhjentää orvoksi jääneet myyntitilaustietueet suorittamalla säännöllisen *Myyntitilausten poisto* -tehtävän kummassa tahansa seuraavista paikoista:

- Myynti ja markkinointi \> Säännölliset tehtävät \> Tyhjennä \> Poista myyntitilaukset
- Vähittäismyynti ja kauppa \> Vähittäiskaupan ja kaupan IT \> Tyhjennä \> Poista myyntitilaukset

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Onko olemassa tapa laskea provisiot jo kirjatuista laskuista?

Supply Chain Management ei tällä hetkellä tue kirjattujen laskujen provisioiden laskemista.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Pakettinimikettä ei tueta konsernin sisäisissä prosesseissa.

Pakettinimike ei ole käytettävissä ostotilauksessa, koska jos tarkastelet pakettinimikkeen myyntitilaus rivejä, määrä on *0* (nolla) ja tila on *Peruutettu*. Tämä on suunniteltu ominaisuus. myyntitilauksella ostetaan vain pakettinimikkeen osat. Sillä ei osteta itse pakettinimikettä.

Jos sinun on ostettava paketti, harkitse, pitääkö se merkitä pakettinimikkeeksi, koska tämä toiminto on tosiasiassa suunniteltu tuottokirjausskenaarioita varten. Lisätietoja pakettinimikkeistä: [Paketit](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).
