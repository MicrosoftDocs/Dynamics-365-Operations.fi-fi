---
title: Kyselylomakkeen tulosten analysointi
description: Kyselylomakkeen tilastotietoja voidaan käyttää keskiarvojen, kokonaissummien ja prosenttiosuuksien laskemiseen demografiatietojoukon perusteella.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b8e4fd5d9fabd35de067ab61c1e64156ce4f0ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418396"
---
# <a name="analyzing-questionnaire-results"></a>Kyselylomakkeen tulosten analysointi



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

