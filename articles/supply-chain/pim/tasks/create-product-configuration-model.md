--- 
title: "Luo tuotemääritysmalli"
description: "Tässä menettelyssä käsitellään tuotemallien luomista sekä perustietojen, kuten määritteiden ja alikomponenttien antamista."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 866a4f29723e10eb0a1e1be86d6d4f6da8a69b1c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-product-configuration-model"></a>Luo tuotemääritysmalli

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään tuotemallien luomista sekä perustietojen, kuten määritteiden ja alikomponenttien antamista. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-product-model"></a>Tuotemallin luominen
1. Valitse Tuotevarianttimallin määritys.
2. Valitse Tuotekonfiguraation mallit.
3. Valitse Uusi.
4. Kirjoita arvo Nimi-kenttään.
5. Kirjoita arvo Kuvaus-kenttään.
6. Valitse Solver-strategia-kentässä vaihtoehto.
    * Selvitysstrategia määrittää, miten poissulkevan tuotekonfiguraation mallin rajoitukset käsitellään. Tämä valinta voi vaikuttaa tuotekonfiguraatiomallin suorituskykyyn.  
7. Kirjoita arvo Nimi-kenttään.
    * Juurikomponentti vastaa tuotekonfiguraatiomallia, mutta sitä voi käyttää myös muissa tuotemalleissa.  
8. Valitse OK.
9. Valitse vaihtoehto Käytä konfigurointeja -kentässä.
    * Jos konfiguraation parametrin uudellenkäyttöasetukseksi on valittu Kyllä, järjestelmä etsii identtisiä konfiguraatioita jokaisen konfigurointi-istunnon jälkeen ja käyttää niitä uudelleen, jos tarkka vastine löytyy.  

## <a name="add-attributes"></a>Lisää määritteet
1. Laajenna Määritteet-osa.
2. ValitseLisää.
3. Merkitse valittu rivi luettelossa.
4. Kirjoita arvo Nimi-kenttään.
5. Kirjoita arvo Selvityksen nimi -kenttään.
    * Tuotekonfiguroinnin rajoiteselvitys käyttää selvitysnimeä. Siinä ei saa olla välilyöntejä tai erikoismerkkejä. Alaviivaa (_) saa kuitenkin käyttää.  
6. Kirjoita arvo Kuvaus-kenttään.
    * Konfiguraation käyttäjä näkee kuvaustekstin, joten se auttaa valitsemaan oikean määritteen arvon.  
7. Anna tai valitse arvo Määritteen tyyppi -kentässä.
    * Määritteen tyyppi määrittää, mitä arvoja määritteessä voi käyttää.  
8. Valitse Sisällytä uudelleenkäyttöön -valintaruutu.
    * Tämä vaihtoehto on käytettävissä vain, kun Käytä konfigurointeja -asetus on valittu. Sisällytetyn määritteen uudelleenkäytön valintaruutu tarkoittaa, että määritettä harkitaan, kun järjestelmää etsii tarkkaa vastinetta.  

## <a name="add-subcomponents"></a>Lisää alikomponentit
1. Laajenna Alikomponentit-osa.
2. ValitseLisää.
3. Merkitse valittu rivi luettelossa.
4. Kirjoita arvo Nimi-kenttään.
5. Kirjoita arvo Selvityksen nimi -kenttään.
6. Kirjoita arvo Kuvaus-kenttään.
7. Anna tai valitse arvo Komponentti-kentässä.
    * JokaisenKunkin alikomponentin on viitattava komponentin määritykseen. Tämä rakenne tukee komponenttien uudelleenkäyttöä ja varmistaa, että määritettyä komponenttia voidaan käyttää useissa tuotemalleissa.  
8. Valitse Tallenna.
9. Valitse Tuoterakennerivin tiedot.
    * Tuoterakennerivin tiedot -lomakkeen avulla käyttäjä voi valita alikomponentin pakolliset osat. Jokaiselle komponentille annetaan kiinteä arvo tai se yhdistetään määritteeseen. Yhdistettäessä määritteeseen tuoterakennerivin ominaisuus saa eri arvon valitun konfiguraation mukaan.  
10. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Jokain alikomponentin vastaa määritettävää päätuotetta, jossa on poissulkevan konfiguraation tekniikkaa. Viittaus tehdään nimiketunnuksen avulla.  
11. Valitse Määritä-valintaruutu.
12. Valitse Laskenta-kentässä Kyllä.
    * Laskenta-asetuksen määrittäminen varmistaa, että tuote sisällytetään tuotteen kustannuslaskentaan.  
13. Valitse Asetukset-välilehti.
14. Valitse Määritä-valintaruutu.
15. Kirjoita numero Määrä-kenttään.
    * Määräkentän määrittää, kuinka paljon tätä tuotetta kulutetaan määritetyssä tuotteessa.  
16. Valitse Määritä-valintaruutu.
17. Lisää Per sarja -kenttään numero.
18. Valitse OK.


