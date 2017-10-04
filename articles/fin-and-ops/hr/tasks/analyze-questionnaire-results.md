--- 
title: Analysoi kyselylomakkeen tulokset
description: "Kyselylomakkeen tilastotietoja voidaan käyttää keskiarvojen, kokonaissummien ja prosenttiosuuksien laskemiseen demografiatietojoukon perusteella."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 353faa30ba37c077479afd985b8808fcdbdcaae6
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="analyze-questionnaire-results"></a>Analysoi kyselylomakkeen tulokset

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kyselylomakkeen tilastotietoja voidaan käyttää keskiarvojen, kokonaissummien ja prosenttiosuuksien laskemiseen demografiatietojoukon perusteella. Aloita tämä menettely siirtymällä kohtaan Kyselylomake > Näytä ja analysoi tulokset > Kyselylomakkeen tilastotiedot. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-questionnaire-statistics-record"></a>Kyselylomakkeen tilastotietotietueen luominen
1. Siirry Kyselylomakkeen tilastotiedot -kohtaan.
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Syötä arvo Tilastotiedot-kenttään.
5. Kirjoita Kuvaus-kenttään arvo.
6. Avaa haku valitsemalla Kyselylomake-kentässä avattavan valikon painike.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Valitse Yleiset-välilehti.
    * Määritä, haluatko ottaa mukaan nimettömät tulokset vai työntekijöiden, yhteyshenkilöiden ja hakijoiden tulokset.  
9. Valitse Työntekijä-valintaruutu tai poista valintaruudun valinta.
    * Jos tarkastelet tuloksia virkaiän tai iän perusteella, määritä tulosten ryhmittelyssä käytettävät välit.  
    * Kun ikäväliksi syötetään 5, tulokset ryhmitellään viiden vuoden ikävälien perusteella.  
10. Syötä numero Ikä-kenttään.
    * Määritä, haluatko suorittaa laskelman koko kyselylomakkeelle, jokaiselle tulosryhmälle, jokaiselle kysymykselle tai jokaiselle kysymysriville.  
    * Määritä, miten haluat ryhmitellä tulokset.  
    * Jos esimerkiksi lasket saatujen pisteiden keskiarvon kysymystä kohti, kysymykset on hyvä nähdä tulosryhmän mukaan ryhmiteltyinä.  
    * Valitse tiedot, joihin laskelma perustuu.  
    * Ajatellaan, että haluat tietää kyselylomakkeen työntekijöiltä saadun keskimääräisen prosentin verrattuna työntekijöiden saamiin keskimääräisiin pisteisiin.  
11. Valitse Alue-välilehti.
    * Alueiden avulla voit rajata tulosjoukon sisältämään vain alueen ehtoja vastaavat kohteet.  
12. Valitse Ryhmittely-välilehti.
    * Ryhmittelyiden avulla voit määrittää, miten tulokset näytetään.  
    * Voit ryhmitellä tulokset esimerkiksi ensin sukupuolen ja sitten iän perusteella.  
13. Etsi haluamasi tietue luettelosta ja valitse se.
    * Siirrä ryhmittelyt Valittu puoli -kohtaan ja aseta ne haluttuun järjestykseen.  

## <a name="execute-the-statistics-calculation"></a>Tilastotietojen laskelman suorittaminen
1. Valitse Suorita.
    * Määritä, mitä laskentatoimintoa tulosten käsittelyssä käytetään.  
    * Voit laskea esimerkiksi valittujen ryhmien kyselylomakkeen keskimääräiset prosenttiosuudet tai tulosryhmien pisteiden kokonaistuloksen.  
2. Valitse Poista edelliset haut -valintaruutu tai poista sen valinta.
3. Valitse OK.

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Tarkastele kyselylomakkeen tilastotietojen saatuja tuloksia.
1. Valitse Tulos.
2. Valitse Tulos.
3. Sulje sivu.

