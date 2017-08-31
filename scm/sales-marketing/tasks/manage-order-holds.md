--- 
title: Tilausten pidon hallinta
description: "Tämä menettely näyttää, miten asiakkaan myyntitilaukset asetetaan pitoon, miten tilauksen pitojen uloskuittausten kanssa toimitaan ja miten tilauksen pito poistetaan."
author: omulvad
manager: AnnBe
ms.date: 01/09/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 6a9487567620b7b7d6d15015f7f0b7675e227c8a
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="manage-order-holds"></a>Tilausten pidon hallinta

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tämä menettely näyttää, miten asiakkaan myyntitilaukset asetetaan pitoon, miten tilauksen pitojen uloskuittausten kanssa toimitaan ja miten tilauksen pito poistetaan. Tilaus on saatettu asettaa pitoon monesta eri syystä. Voit esimerkiksi pitää tilausta, kunnes asiakkaan osoite tai maksutapa voidaan varmistaa tai kunnes johtaja voi tarkistaa asiakkaan luottorajan. Varasto ei voi käsitellä pidossa olevaa tilausta toimitusta varten. 

Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="set-up-order-holds"></a>Tilauksen pitojen määrittäminen
1. Valitse Myynti ja markkinointi > Asetukset > Myyntitilaukset > Tilauksen pitokoodit.
2. Valitse Uusi.
3. Kirjoita arvo Pitokoodi-kenttään.
    * Kirjoita esimerkiksi Uusintapuhelu.  
4. Kirjoita arvo Kuvaus-kenttään.
    * Esimerkki: Tilaus odottaa asiakkaan uusintapuhelua.  
    * Voit halutessasi poistaa fyysiset varaukset tilauksesta valitsemalla Poistetut varaukset -valintaruudun, kun tämä pitokoodi lisätään.  
5. Valitse Tallenna.

## <a name="place-order-on-hold"></a>Tilauksen asettaminen pitoon
1. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Syötä tai valitse arvo Asiakastili-kentässä.
4. Valitse OK.
5. Syötä tai valitse arvo Nimiketunnus-kentässä.
6. Kirjoita numero Määrä-kenttään.
7. Valitse toimintoruudussa Myyntitilaus.
8. Valitse Tilausten pidot.
9. Valitse Uusi.
10. Valitse Pitokoodi-kentässä edellisessä alitehtävässä luotu koodi.
11. Valitse Tallenna.
12. Sulje sivu.
13. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
14. Merkitse valittu rivi luettelossa.
    * Tällä hetkellä pidossa olevien tilausten Älä käsittele- ja Pito-kentät on merkitty.    
15. Valitse toimintoruudussa Kerää ja pakkaa.

## <a name="manage-order-holds"></a>Tilausten pidon hallinta
1. Valitse Myynti ja markkinointi > Myyntitilaukset > Avoimet tilaukset > Tilausten pidot.
    * Tilausten pidot -sivu on kuin eräänlainen työtila, jossa on yhteenveto kaikista nykyisistä ja käsitellyistä pidoista ja jossa voit käsitellä niitä ja liitettyjä myyntitilauksia.      
2. Merkitse valittu rivi luettelossa.
3. Valitse toimintoruudussa Pidä uloskuittaus.
4. Valitse Kuittaa ulos.
5. Poista valitun rivin merkintä luettelossa.
    * Käyttäjätunnuksesi näkyy nyt uloskuittauksen kentässä.   
6. Valitse Poista uloskuittaus.
7. Valitse toimintoruudussa Vapauta pito.
    * Kun olet valmis poistamaan pidon ja sallimaan tilauksen käsittelyn tilauksen täyttämisen seuraavaan vaiheeseen, pito on vapautettava. Voit tilausta ei tarvitse muuttaa, voi suorittaa Vapauta pidot -toiminnon. Käytä kuitenkin Vapauta ja muokkaa -toimintoa, jos tilaus on päivitettävä vapautuksen yhteydessä.      
    * Vapauta ja lähetä -toiminto on käytettävissä vain, kun käytät Puhelinkeskus-toimintoa.  
8. Valitse Vapauta pidot.
    * Tilauksen pito on nyt vapautettu ja se on poistettu aktiivisten pitojen luettelosta. Jos haluat nähdä kaikki pidot tai niiden alijoukot tietyn tilaan mukaan, muuta Näytä-kentän arvoa.     


