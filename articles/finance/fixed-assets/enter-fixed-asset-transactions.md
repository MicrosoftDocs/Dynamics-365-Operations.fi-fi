---
title: Käyttöomaisuuserien tapahtuma-asetukset
description: Tässä artikkelissa kerrotaan käyttöomaisuustapahtumien luomisessa käytettävät menetelmät.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: kfend
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 402679b6f1003f14f7e277a326784edaaea719d5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883355"
---
# <a name="fixed-asset-transaction-options"></a>Käyttöomaisuuserien tapahtuma-asetukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan käyttöomaisuustapahtumien luomisessa käytettävät menetelmät.

Voit määrittää käyttöomaisuuden integrointiin ostoreskontran, myyntireskontran, hankinnan ja kirjanpidon kanssa. Varastossa olevia nimikkeitä voi myös siirtää käyttöomaisuuteen sisäistä käyttöä varten.

## <a name="accounts-payable"></a>Ostoreskontra
Voit määrittää käyttöomaisuustapahtumia Kirjaustosite-sivulla. Tämä sivu voidaan avata Laskukirjauskansio-sivulta. Voit avata Kirjaustosite-sivun myös Hyväksyttyjen laskujen kirjauskansio -sivulta. Valitse Vastatilityyppi-kentässä Käyttöomaisuudet. Valitse sitten Vastatili-kentässä käyttöomaisuuserän numero. Anna Käyttöomaisuudet-välilehteen Tapahtumatyyppi- ja Kirja-kenttien arvot.

## <a name="accounts-receivable"></a>Myyntireskontra
Voit määrittää käyttöomaisuustapahtumia Vapaatekstilasku-sivulla.  Valitse rivinimike Vapaatekstilasku-sivun Laskurivit-ruudukossa. Valitse Rivin erittely -pikavälilehti. Kirjoita poistotapahtuman käyttöomaisuuserän numero ja kirja. Vapaatekstilaskujen käyttöomaisuustapahtumatyyppi on aina Poistomyynti.

## <a name="procurement-and-sourcing"></a>Hankinta
Voit määrittää käyttöomaisuustapahtumia Ostotilaus-sivulla. Luo ostotilaus antamalla vaaditut tiedot ja valitse sitten OK. Valitse Ostotilaus-sivulla Rivin erittely -pikavälilehti. Anna sitten Käyttöomaisuudet-välilehdessä käyttöomaisuuden tiedot. 

Kirjaa hankintatapahtuma olemassa olevalle käyttöomaisuuserälle määrittämällä kirja numero, kirja ja tapahtumatyyppi. Käyttöomaisuutta ei voi kirjata, jos jokin näistä tiedoista puuttuu. Kirjaa hankintatapahtuma uudelle käyttöomaisuuserälle valitsemalla Uusi käyttöomaisuus? -asetus ja valitsemalla sitten käyttöomaisuuserä, johon uusi omaisuuserä liitetään. Käyttöomaisuuskentät eivät ole käytettävissä, jos nimike kuuluu varastomalliryhmään, joka käyttää muuta vakiovarastomallia. Käyttöomaisuuden parametrit -sivulla määritetyt asetukset määrittävät lisäksi, voitko kirjata hankintatapahtumia ostomoduuleista. 

Jos käyttöomaisuuserien hankinnoissa käytetään ostotilauskirjauskansiota tai Siirto varastosta käyttöomaisuuteen -kirjauskansiota, sillä on vaikutusta varastoarvoon.

## <a name="general-ledger"></a>Kirjanpito
Käyttöomaisuustapahtumatyyppejä voi kirjata Kirjauskansio-sivulla. Voit käyttää myös käyttöomaisuuden kirjauskansioita kirjaamaan käyttöomaisuustapahtumat.

### <a name="options-for-entering-fixed-asset-transaction-types"></a>Käyttöomaisuustapahtumatyyppien kirjausvaihtoehtotyypit


| Tapahtumatyyppi                    | Moduuli                   | Optiot                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Hankinta, hankintaoikaisu | Käyttöomaisuudet             | Käyttöomaisuudet, Siirto varastosta käyttöomaisuuteen   |
|                                     | Kirjanpito           | Kirjauskansio                           |
|                                     | Ostoreskontra         | Laskukirjauskansio, hyväksyttyjen laskujen kirjauskansio |
|                                     | Hankinta | Ostotilaus                            |
| Poisto                        | Käyttöomaisuudet             | Käyttöomaisuudet                              |
|                                     | Kirjanpito           | Kirjauskansio                           |
| Luovutus                            | Käyttöomaisuus             | Käyttöomaisuus                              |
|                                     | Kirjanpito           | Kirjauskansio                           |
|                                     | Myyntireskontra      | Vapaatekstilasku                         |

Käyttöomaisuuden poistokausien jäljellä olevaa arvoa ei päivitetä, kun poistotapahtumatyypin kirjauskansion rivi luodaan tai tuodaan manuaalisesti tietoyksikön kautta. Jäljellä oleva arvo päivitetään, kun kirjauskansion rivi luodaan käyttämällä poistoehdotusprosessia.

Lisätietoja on ohjeaiheessa [Käyttöomaisuuden integrointi](fixed-asset-integration.md).

Järjestelmä estää poiston kirjauksen kahdesti samalla kaudella. Jos esimerkiksi kaksi käyttäjää luo poistoehdotukset erikseen tammikuulle, ensimmäisen käyttäjän poisto kirjataan ensimmäisessä kirjauskansiossa. Kun toinen käyttäjä kirjaa poiston toisessa kirjauskansiossa, järjestelmä tarkistaa päivämäärän, jolloin poisto suoritettiin viimeksi eikä kirjaa saman kauden poistoa toista kertaa.

### <a name="transactions-that-require-a-different-voucher-number"></a>Tapahtumat, joissa tarvitaan eri tositenumero

Seuraavissa käyttöomaisuustapahtumissa käytetään eri tositenumeroita:

- Käyttöomaisuudelle tehdään lisähankinta ja kertynyt poisto lasketaan.
- Käyttöomaisuus jaetaan.
- Parametri, jota käytetään luovutuksen poistossa, on käytössä. Käyttöomaisuus poistetaan.
- Käyttöomaisuuden käyttöottopäivämäärä on ennen hankintapäivämäärää. Tämän vuoksi kirjataan poisto-oikaisu.

> [!NOTE]
> Varmista tapahtumia syötettäessä, että kaikki tapahtumat kohdistetaan samaan käyttöomaisuuteen. Tositetta ei kirjata, jos siinä enemmän kuin yksi käyttöomaisuus, vaikka **Uusi tosite** -kentän asetuksena on **Vain yksi tositenumero** **Kirjauskansioiden nimet** -sivulla kirjanpidossa. Jos tositteessa on useampi kuin yksi käyttöomaisuus, sanoma "Tositetta kohden voi olla vain yksi käyttöomaisuustapahtuma" avautuu etkä voi kirjata tositetta.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
