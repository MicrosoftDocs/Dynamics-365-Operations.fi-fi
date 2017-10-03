---
title: "Käyttöomaisuuserien tapahtuma-asetukset"
description: "Tässä artikkelissa kerrotaan käyttöomaisuustapahtumien luomisessa käytettävät menetelmät."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 40ab6f8d7e7b7a04ec1533acf2919dea345b0804
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-asset-transaction-options"></a>Käyttöomaisuuserien tapahtuma-asetukset

[!include[banner](../includes/banner.md)]


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

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Käyttöomaisuustapahtumatyyppien kirjausvaihtoehtotyypit


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



Lisätietoja on ohjeaiheessa [Käyttöomaisuuden integrointi](fixed-asset-integration.md).




