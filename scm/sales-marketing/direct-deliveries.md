---
title: Suoratoimitukset
description: "Tässä artikkelissa on tietoja suoratoimituksista. Suoratoimituksissa nimikkeet lähetetään suoraan toimittajalta asiakkaallesi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c59f82103371ca1a8d43a7dba22213cdd8b13c3c
ms.lasthandoff: 03/31/2017


---

# <a name="direct-deliveries"></a>Suoratoimitukset

Tässä artikkelissa on tietoja suoratoimituksista. Suoratoimituksissa nimikkeet lähetetään suoraan toimittajalta asiakkaallesi.

Suoratoimitukset säästävät aikaa ja vähentävät varaston omistuskustannuksia, koska sinun ei tarvitse säilyttää tuotteita varastossa ennen asiakkaalle toimittamista.  

Voit luoda suoratoimituksia **Myyntitilaus**-sivulla. Luo ensin myyntitilaus ja tilausrivit. Valitse sitten toimintoruudun **Myyntitilaus**-välilehdessä **Suoratoimitus**. Määritä lopuksi rivit, jotka tulee käsitellä suoratoimituksena. Suoratoimituksen myyntitilausrivien ja vastaavien ostotilausrivien välille on nyt luotu linkki.  

**Huomautus:** Jos osa tilatusta määrästä on jo toimitettu, sinun on jaettava jäljellä oleva määrä. Luo uusi rivi määrällä, joka on toimitettava suoraan ja vähennä tämä määrä alkuperäisen rivin määrästä. Jos esimerkiksi alkuperäinen määrä oli 15 ja viisi on toimitettu, sinun on luotava uusi rivi jäljellä olevalle määrälle 10 ja vähennettävä sitten alkuperäistä määrää tällä määrällä.  

Kun olet luonut suoratoimituslinkin myyntitilausrivien ja ostotilausrivien välille, voit päivittää myyntitilauksen käyttämällä pakkausluetteloa. Suorita joko pakkausluettelon tai laskupäivityksen päivitys ostotilauksesta. Myyntitilaus on laskupäivitettävä **Myyntitilaus**-sivulla. Laskun päivityksen jälkeen myyntitilauksen määrä ei saa olla suurempi kuin vastaanotetuksi rekisteröity määrä. Myyntitilausrivillä on 10 kappaletta, mutta vain viisi kappaletta myyntitilausriviltä on päivitetty pakkausluetteloa käyttämällä. Jos valitset **Määrä**-luettelossa **Kaikki** laskupäivitettäessä myyntitilausta, vain ne nimikkeet, jotka on vastaanotettu tai päivitetty käyttämällä pakkausluetteloa, laskupäivitetään. Koko myyntitilausriviä ei päivitetä.

## <a name="delivery-date"></a>Toimituspäivämäärä
Kun päivität myyntitilausrivin **Pyydetty vastaanottopäivämäärä** -kentän, myös vastaavan ostotilausrivin **Toimituspäivämäärä**-kenttä päivitetään. Vastaavasti, kun päivität ostotilausrivin **Vahvistettu**-kentän, myös vastaavan myyntitilausrivin **Vahvistettu vastaanottopäivä**- ja **Vahvistettu lähetyspäivämäärä** -kenttä päivitetään.

## <a name="delivery-address"></a>Toimitusosoite
Ostotilauksen toimitusosoite on yleensä yrityksen osoite. Jos kuitenkin luot suoratoimituksen, asiakkaan osoite syötetään toimitusosoitteeksi. Jos muutat sellaisen ostotilausrivin toimitusosoitteen, jonka toimitustyyppi on **Suoratoimitus**, vastaavan myyntitilausrivin toimitusosoite päivitetään myös. Vastaavasti, jos muutat myyntitilausrivin toimitusosoitteen, myös ostotilausrivin toimitusosoite päivitetään.

## <a name="deleting-order-lines"></a>Tilausrivien poistaminen
Jos yrität poistaa myyntitilausrivin, jonka toimitustyyppi on **Suoratoimitus**, sanomaruutuun tulee viesti, jossa ilmoitetaan, että riviin on liitetty ostotilausrivejä. Jos myyntitilausrivi on toimitettu osittain, et voi poistaa myyntitilausriviä etkä siihen liitettyjä ostotilausrivejä.

## <a name="warehouse"></a>Varasto
Kun luot suoratoimituksen, myymäsi nimikkeet eivät koskaan saavu varastoosi fyysisesti. On kuitenkin määritettävä varasto myyntitilauksen riville. Vastaavasti keräilyvaatimukset voidaan määrittää nimikkeen nimikemalliryhmässä. Koska nimikkeet eivät koskaan saavu fyysisesti varastoosi, nämä vaatimukset jätetään huomioimatta, kun tilaus on suora toimitus.


