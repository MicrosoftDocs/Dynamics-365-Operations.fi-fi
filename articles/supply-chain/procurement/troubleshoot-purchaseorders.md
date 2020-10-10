---
title: Ostotilausten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita ostotilausten käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
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
ms.openlocfilehash: e55974f65577170880e60095f1ba74ea7366e592
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834350"
---
# <a name="troubleshoot-purchase-orders"></a>Ostotilausten vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita ostotilausten käytössä voi esiintyä.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>Toimi voidaan suorittaa vasta, kun rivinumero on täysin jaeltu.

Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.

Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Kun ostotilaukset tuodaan tiedonhallinnan kautta, ostotilausten rivi numerot eivät noudata järjestelmän parametreissa määritettyä korotusta.

### <a name="issue-description"></a>Ongelman kuvaus

Oletusarvoisesti automaattisesti luodut *Ostotilausrivit V2* -tietoyksikön kautta tuotujen tilausrivien rivinumerot eivät käytä järjestelmän parametreissa määritettyä rivinumeron korotusta. Jos luot ostotilauksen manuaalisesti ja lisäät rivejä käyttöliittymän kautta, rivinumerot kasvavat oikein. Jos kuitenkin käytät tiedonhallinnan kehystä (DMF), niitä ei koroteta oikein.

Tämä ongelma ilmenee, koska tuotaessa rivejä DMF-kehyksen kautta järjestelmä käyttää DMF:n menetelmää niiden määrittämiseen, jos tuodussa yksikössä ei ole määritetty rivinumeroita valmiiksi. Tässä menetelmässä rivinumeroita kasvatetaan aina yhdellä.

### <a name="issue-workaround"></a>Ongelman kiertotapa

Varmista, että halutut rivinumerot on jo määritetty tietoyksikön numerokentissä, kun tuot ostotilauksen rivit. Tällöin DMF ei korvaa rivinumeroita.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Oletusveroryhmää ja oletuskäteisalennusta ei täytetä laskutustililtä.

Jos käytät laskutustiliä, joka eroaa asiakkaan tilistä, oletusveroryhmää ja oletuskäteisalennusta ei täytetä laskutustililtä, kun ostotilaus luodaan.

Tämä on suunniteltu ominaisuus. Veroryhmän oletusarvot, käteisalennukset ja muut hintatiedot perustuvat asiakastiliin eivätkä laskutustiliin.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Saan "Kohdeviitettä ei määritetty" -virheen ostotilauksen vahvistuksen aikana tai "Kutsun kohde on aiheuttanut poikkeuksen" -poikkeus esiintyy toimittajan laskun julkaisemisen yhteydessä.

Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.

Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Vähintään yksi kirjanpidollinen jako on joko yli- tai alijaettu.

### <a name="issue-description"></a>Ongelman kuvaus

Näyttöön tulee seuraava virhe: "Vähintään yksi kirjanpidollinen jako on joko yli- tai alijaettu."

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.

Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**. Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Voinko näyttää vain itse luomiani ostotilauksia?

Tämä toiminto ei ole tällä hetkellä käytettävissä.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Voinko varata varastoa ja luoda tapahtumia rekisteröidyn varaston perusteella ostotilauksessa?

### <a name="issue-description"></a>Ongelman kuvaus

Vaikka nimikkeitä olisi ostotilauksessa *Rekisteröity*-tilassa, voit kuitenkin varata varastoa. Toisin sanoen voit luoda tapahtumia rekisteröidyn varaston perusteella.

### <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Luo ostotilaus.
2. Ostotilausrivin rekisteröinti.
3. Huomaa, että voit luoda varauksia tai tapahtumia rekisteröidyn varaston perusteella.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus. Oletetaan, että rekisteröidyt nimikkeet ovat fyysisesti saapuneet varastoon ja että ne ovat näin ollen varattavissa.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Ostotilaukset eivät vastaa yrityksen kieliasetuksia.

### <a name="issue-description"></a>Ongelman kuvaus

Osto tilauksen tuotenimi näkyy järjestelmän kielellä sen kielen sijaan, joka on määritetty sille yrityksellä, jossa ostotilaus on luotu.

### <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Määritä järjestelmän kieleksi *EN-US* (Yhdysvaltojen englanti).
1. Varmista, että käytettävissä tuote, jossa kielet *EN-US* ja *DE* (saksa) ovat käytössä tuotenimen käännöksiä varten.
1. Muuta yrityksen kieleksi *DE*.
1. Luo siinä yrityksessä, jossa kieleksi on määritetty *DE*, tuotteen sisältävä ostotilaus.
1. Huomaa, että tuotteen nimi näkyy edelleen kielellä Yhdysvaltojen englanti (järjestelmän kieli).

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus. Ostotilauksissa tuote näkyy aina järjestelmän kielellä. Ostotilauksen kieltä käytetään luotaessa vahvistuskirjauskansiota.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>Tuoteyksikkökohtainen hyväksyttyjen toimittajien luettelo ei salli voimaantulopäivän muuttamista.

### <a name="issue-description"></a>Ongelman kuvaus

Tuotteella on hyväksytty toimittaja, jonka voimaantulopäivä on esimerkiksi 11. tammikuuta 2018 (*01/11/2018*) ja vanhentumispäivä on *Ei koskaan*. Jos yrität muuttaa voimaantulopäivän muotoon 10. tammikuuta 2018 (*01/10/2018*) tai 12. tammikuuta 2018 (*01/12/2018*), näyttöön tulee seuraava virhesanoma:

> Tietuetta ei voi luoda hyväksyttyjen toimittajien luetteloon (PdsApproveVendorList). Vanhentumispäivän arvon on oltava sama tai suurempi kuin voimaantulopäivän arvo.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Voit pidentää vain sitä jaksoa, jolle toimittaja on hyväksytty. Seuraavat säännöt pätevät:

- Jos haluat muuttaa voimaantulopäivää siten, että se nimikkeen toimittajan olemassa olevia tietueita (jaksoja) aiemmin, uuden jakson vanhanemispäivän on oltava ennen kaikkia olemassa olevien tietueiden vanhenemispäivää.
- Jos haluat muuttaa vanhenemispäivää siten, että se on myöhempi kuin jokin olemassa oleva jakso, voimaantulopäivämäärän ei saa olla ennen olemassa olevan tietueen vanhenemispäivää.
- Jos haluat pienentää kokonaisaikaa, jolle toimittaja on hyväksytty, sinun on poistettava tai muokattava olemassa olevia tietueia. Vaihtoehtoisesti voit käyttää **katkaisu**-valitsinta tuonnin aikana. Tämä valitsin poistaa kaikki olemassa olevat tietueet nimikekohteisten hyväksyttyjen toimittajien taulukosta.

Esimerkiksi ongelmankuvauksessa kuvattu skenaario, jossa tietueen voimaantulopäivä on *01/11/2018* ja vanhenemispäivä *Ei koskaan*, y voit tuoda uuden tiedoston, jonka voimaantulopäivänä on *01/10/2018* vanhenemispäivänä *Ei koskaan*. Et kuitenkaan voi lyhentää ajanjaksoa niin, että voimaantulopäiväksi päivittyy tiedonhallinnan kautta *01/12/2018*. Tämä muutos on tehtävä käyttöliittymässä.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a>Kun muutan ostotilauksen otsikon toimitusosoitetta, toimituksen nimeä ei synkronoida.

### <a name="issue-description"></a>Ongelman kuvaus

Ostotilauksen otsikossa oleva osoite päivitetään osoitteeksi, joka ei ole toimitusosoite. Vaikka osoite päivitetään ostotilauksessa, toimituksen nimeä ei päivitetä päivitetyn osoitteen perusteella.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus. Valittu osoite on luokiteltava toimitusosoitteeksi. Muussa tapauksessa toimituksen nimeä ei päivitetä valitun osoitteen perusteella.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Voinko löytää ostotilauksen peruneen käyttäjän?

Näitä tietoja seurataan vain, jos ostotilaus edellyttää muutoksenhallintaa. Jos käytät muutoksenhallintaa, voit nähdä muutoksen (peruutuksen) lähettäjän ja hyväksyjän.
