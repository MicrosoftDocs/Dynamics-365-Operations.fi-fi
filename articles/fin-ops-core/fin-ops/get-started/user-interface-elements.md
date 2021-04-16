---
title: Käyttöliittymäelementit
description: Tässä ohjeaiheessa kuvataan sovelluksen käyttöliittymäelementit.
author: tlefor
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: ''
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: feb6d5751bc22c05dbd2f01f47d5a0f99fca07a0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754725"
---
# <a name="user-interface-elements"></a>Käyttöliittymäelementit

Tässä ohjeaiheessa kuvataan sovelluksessa käytetyt käyttöliittymäelementit. Ennen kuin käyttäjät voivat navigoida käyttöliittymässä, on tärkeää tietää niiden elementtien nimet ja toiminnot, jotka muodostavat käyttöliittymän.

## <a name="overview"></a>Yleiskuvaus

- **Toimintoruutu** – siirtymispalkin alla oleva palkki. Tässä voit valita välilehtiä, jos haluat muuttaa sivulla näkyviä tietueita. Voit muokata ja tallentaa tietoja tässä.  
- **Tietoruutu** – voit tarkastella tietoja ja seurata tämän ruudun tiettyjen tietueiden aktiviteetteja.  
- **Tietoruutu** – Tässä voit vierittää tietueen eri puolia tietoruudussa tarkasteltavaksi.  
- **Suodatinruutu** – Joillakin sivuilla voit avata tämän ruudun valitsemalla **Näytä suodattimet**. Sen avulla voit rajata sivulla näkyviä tuloksia.  
- **Siirtymispalkki** – käyttöliittymän yläosassa oleva palkki. Siinä on **Dynamics 365 -portaali**, **Haku**, **yrityksen valitsin**, **toimintokeskus**, **Asetukset**, **Ohje ja tuki** sekä käyttäjäprofiili.  
- **Siirtymisluettelo** – Joillakin sivuilla voit etsiä tietyn tietueen vierittämällä tätä ruutua. Kun tämä on valittuna, tietueen tiedot tulevat näkyviin sivulle.  
- **Siirtymisruutu** – vasemmanpuoleisin ruutu. Tästä voit löytää minkä tahansa sivun tuotteesta.  
- **Sivu** – Käyttöliittymän keskeisin näkymä. Muissa käyttöliittymäkomponenteissa tehdyt valinnat vaikuttavat siihen, mitä tietoja tässä näytetään.  
- **Ruutu** – oikeanpuoleisin ruutu. Tämä avautuu joissakin tapauksissa, kun tietueen tietoja on muutettava ja tallennettava.  
- **Välilehti** – Kun toimintoruutuun viitataan, se on vaihtoehtojen valikko, joka tulee näkyviin, kun toimintoruudusta valitaan tietty vaihtoehto.  

![Seuraavassa kuvassa näkyy näiden elementtien sijoittelu käyttöliittymässä.](media/user-interface-01.png)

## <a name="tabs-fields-and-sections"></a>Välilehdet, kentät ja osat

*Välilehti* on sivulla tehty valinta, joka avaa tietueen eri osan samalla sivulla. Usein sen avulla voit muuttaa tiettyjä *kenttiä* tai käyttöliittymän elementtejä, jotka sallivat kirjoitetun syötteen. 

*Pikavälilehti* on välilehti, jonka lisäetuna on, että useat välilehdet näkyvät yhtä aikaa. Voit laajentaa pikavälilehden valitsemalla alaspäin osoittavan nuolen sen oikeasta reunasta.

![Seuraavassa kuvassa näkyy esimerkki välilehdistä ja pikavälilehdistä.](media/user-interface-02.png)

*Osa* on samantyyppinen kuin välilehti. Sanaa "osa" käytetään usein kuvaamaan mitä tahansa sivun aluetta, joka järjestää tietyn tietoluokan. Seuraavassa kuvassa Yhteenveto, Tilaukset ja Suosikit sekä Linkit ovat esimerkkejä osista.

![Seuraavassa kuvassa näkyy esimerkki välilehdistä ja osista.](media/user-interface-03.png)

## <a name="dialog-boxes-and-drop-down-menus"></a>Valintaikkunat ja avattavat valikot

*Valintaikkuna* on ruutu, joka avautuu, kun haluat muuttaa tietuetta tai luoda tietueen tiettyjä valintoja käyttäen. Valintaikkunoissa on kenttiä, joiden avulla voit syöttää kirjoitettua tekstiä. Joskus tietyn kentän avulla voidaan valita alaspäin osoittava nuoli, joka avaa luettelon valittavissa olevista vaihtoehdoista. Tätä kutsutaan *avattavaksi valikoksi*. Seuraavassa kuvassa **Tyyppi**- ja **Asiakasryhmä** -kentät sisältävät avattavan valikon.

![Seuraavassa kuvassa näkyy esimerkki valintaikkunasta.](media/user-interface-04.png)

Joissakin tapauksissa valintaikkuna avautuu tietyn painikkeen lähelle, kun valitset sen. Tätä kutsutaan *avattavaksi valintaikkunaksi*. Seuraavassa kuvassa on valittu **Alkupäivämäärä** -painike, joka avasi avattavan valintaikkunan.

![Seuraavassa kuvassa näkyy esimerkki avattavasta valintaikkunasta.](media/user-interface-05.png)

## <a name="notifications"></a>Ilmoitukset

Jotkin valvomiesi objektien muutokset näkyvät *ilmoituksina*. Ilmoitukset voivat ilmoittaa, kun tietyn asiakkaan tietoja on muutettu, tai se voi hälyttää, kun järjestelmä ei voi hyväksyä tiettyihin kenttiin lisäämiäsi syötteitä. Tietoja saamiesi ilmoitusten mukauttamisesta on [hälytysten yleiskatsauksessa](../get-started/alerts-overview.md).

Ilmoitukset näkyvät useilla eri tavoilla.
- **Kuvatekstitoiminto** – Tämä näkyy kentän, välilehden tai muun painikkeen vieressä, ja se antaa selityksen siihen, mihin ominaisuutta käytetään. 
- **Toimintokeskus** – ilmoituksen sisältävä ruutu näkyy siirtymispalkin Toimintokeskus-painikkeen vieressä. Voit tarkastella ilmoituksen tietoja valitsemalla **Toimintokeskus.**  
- **Sanomapalkki** – tämä näkyy toimintoruudun alla.  

Seuraavassa kuvassa esitetään esimerkkejä tällaisista ilmoituksista.

![Seuraavassa kuvassa esitetään esimerkkejä ilmoituksista.](media/user-interface-06.png)

- **Sanomaruutu** – tämä näkyy käyttöliittymän päällä, ja siihen on reagoitava, ennen kuin voit jatkaa tuotteen käyttöä.  

![Seuraavassa kuvassa näkyy esimerkki sanomaruudusta.](media/user-interface-07.png)

## <a name="toolbars-grids-and-lists"></a>Työkalurivit, ruudukot ja luettelot

*Työkalurivi* sisältää työkaluja, kuten mahdollisuuden lisätä kenttiä tai poistaa tietueita. Joskus-työkalu rivi näkyy sivulla *ruudukon* yläpuolella. Tämä alue, ruudukko, on nimi, joka annetaan riveille, joilla on useita tietosarakkeita. Kaikissa ruudukoissa ei ole työkalurivejä niiden yläpuolella.

*Luettelo* on nimi, joka annetaan sellaisen tietueen kokoelmalle, jota voi vierittää. Voit tuoda nämä tiedot sivulle valitsemalla ne. Usein tämä avaa ruudukon.

![Seuraavassa kuvassa näkyy esimerkkejä työkaluriveistä, ruudukoista ja luetteloista.](media/user-interface-08.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]