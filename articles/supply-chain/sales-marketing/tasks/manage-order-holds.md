---
title: Tilausten pidon hallinta
description: Tämä menettely näyttää, miten asiakkaan myyntitilaukset asetetaan pitoon, miten tilauksen pitojen uloskuittausten kanssa toimitaan ja miten tilauksen pito poistetaan.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9caf6651813f0111b873db1769140d973f1a2e3b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981966"
---
# <a name="manage-order-holds"></a>Tilausten pidon hallinta

[!include [banner](../../includes/banner.md)]

Tämä menettely näyttää, miten asiakkaan myyntitilaukset asetetaan pitoon, miten tilauksen pitojen uloskuittausten kanssa toimitaan ja miten tilauksen pito poistetaan. Tilaus on saatettu asettaa pitoon monesta eri syystä. Voit esimerkiksi pitää tilausta, kunnes asiakkaan osoite tai maksutapa voidaan varmistaa tai kunnes johtaja voi tarkistaa asiakkaan luottorajan. Varasto ei voi käsitellä pidossa olevaa tilausta toimitusta varten. 

Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="set-up-order-holds"></a>Tilauksen pitojen määrittäminen
1. Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Asetukset > Myyntitilaukset > Tilauksen pitokoodit**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Pitokoodi**-kenttään. Kirjoita esimerkiksi Uusintapuhelu.  
4. Kirjoita **Kuvaus**-kenttään arvo.
    - Esimerkki: Tilaus odottaa asiakkaan uusintapuhelua.  
    - Voit halutessasi poistaa fyysiset varaukset tilauksesta valitsemalla **Poista varaukset** -valintaruudun, kun tämä pitokoodi lisätään.  
5. Valitse **Tallenna**.

## <a name="place-order-on-hold"></a>Tilauksen asettaminen pitoon
1. Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Syötä tai valitse arvo **Asiakastili**-kentässä.
4. Valitse **OK**.
5. Syötä tai valitse arvo **Nimiketunnus**-kentässä.
6. Anna **Määrä**-kentässä numero.
7. Valitse **toimintoruudussa** **Myyntitilaus**.
8. Valitse **Tilausten pidot**.
9. Valitse **Uusi**.
10. Valitse **Pitokoodi**-kentässä edellisessä alitehtävässä luotu koodi.
11. Valitse **Tallenna**.
12. Sulje sivu.
13. Siirry kohtaan **Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.
14. Merkitse valittu rivi luettelossa. Tällä hetkellä pidossa olevien tilausten Älä käsittele- ja Pito-kentät on merkitty.
15. Valitse toimintoruudussa **Kerää ja pakkaa**.

## <a name="manage-order-holds"></a>Tilausten pidon hallinta
1. Valitse **Myynti ja markkinointi > Myyntitilaukset > Avoimet tilaukset > Tilausten pidot**. **Tilausten pidot** -sivu on kuin eräänlainen työtila, jossa on yhteenveto kaikista nykyisistä ja käsitellyistä pidoista ja jossa voit käsitellä niitä ja liitettyjä myyntitilauksia.     
2. Merkitse valittu rivi luettelossa.
3. Valitse **toimintoruudussa** **Pidä uloskuittaus**.
4. Valitse **Kuittaa ulos**.
5. Poista valitun rivin merkintä luettelossa. Käyttäjätunnuksesi näkyy nyt **Uloskuittaus**-kentässä.   
6. Valitse **Poista uloskuittaus**.
7. Valitse **toimintoruudussa** **Vapauta pito**.
    - Kun olet valmis poistamaan pidon ja sallimaan tilauksen käsittelyn tilauksen täyttämisen seuraavaan vaiheeseen, pito on vapautettava. Voit tilausta ei tarvitse muuttaa, voi suorittaa Vapauta pidot -toiminnon. Käytä kuitenkin Vapauta ja muokkaa -toimintoa, jos tilaus on päivitettävä vapautuksen yhteydessä.      
    - **Vapauta ja lähetä** -toiminto on käytettävissä vain, kun käytät Puhelinkeskus-toimintoa.  
8. Valitse **Vapauta pidot**. Tilauksen pito on nyt vapautettu ja se on poistettu aktiivisten pitojen luettelosta. Jos haluat nähdä kaikki pidot tai niiden alijoukot tietyn tilaan mukaan, muuta Näytä-kentän arvoa.     

