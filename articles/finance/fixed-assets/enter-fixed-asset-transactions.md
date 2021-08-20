---
title: Käyttöomaisuuserien tapahtuma-asetukset
description: Tässä ohjeaiheessa kerrotaan käyttöomaisuustapahtumien luomisessa käytettävät menetelmät.
author: ShylaThompson
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1857d68a0dfaa25386f19344e4cb3ddc9ffd39b8a75860a1642773d6bd59cce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764260"
---
# <a name="fixed-asset-transaction-options"></a>Käyttöomaisuuserien tapahtuma-asetukset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan käyttöomaisuustapahtumien luomisessa käytettävät menetelmät.

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
| Luovutus                            | Käyttöomaisuuserät             | Käyttöomaisuuserät                              |
| ** **                               | Kirjanpito           | Kirjauskansio                           |
| ** **                               | Myyntireskontra      | Vapaatekstilasku                         |

Käyttöomaisuuden poistokausien jäljellä olevaa arvoa ei päivitetä, kun poistotapahtumatyypin kirjauskansion rivi luodaan tai tuodaan manuaalisesti tietoyksikön kautta. Tämä arvo päivitetään, kun kirjauskansion rivi luodaan käyttämällä poistoehdotusprosessia.

Lisätietoja on ohjeaiheessa [Käyttöomaisuuden integrointi](fixed-asset-integration.md).

### <a name="transactions-that-require-different-voucher-numbers"></a>Tapahtumat, joille vaaditaan eri tositenumeroita

Seuraavissa käyttöomaisuustapahtumissa käytetään eri tositenumeroita:

- Käyttöomaisuudelle tehdään lisähankinta ja kertynyt poisto lasketaan.
- Käyttöomaisuus jaetaan.
- Parametri, jota käytetään luovutuksen poistossa, on käytössä. Käyttöomaisuus poistetaan.
- Käyttöomaisuuden käyttöottopäivämäärä on ennen hankintapäivämäärää. Tämän vuoksi kirjataan poisto-oikaisu.

> [!NOTE]
> Varmista tapahtumia syötettäessä, että kaikki tapahtumat kohdistetaan samaan käyttöomaisuuteen. Tositetta ei kirjata, jos siinä enemmän kuin yksi käyttöomaisuus, vaikka **Uusi tosite** -kentän asetuksena on **Vain yksi tositenumero** **Kirjauskansioiden nimet** -sivulla kirjanpidossa. Jos tositteessa on useampi kuin yksi käyttöomaisuus, sanoma "Tositetta kohden voi olla vain yksi käyttöomaisuustapahtuma" avautuu etkä voi kirjata tositetta.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
