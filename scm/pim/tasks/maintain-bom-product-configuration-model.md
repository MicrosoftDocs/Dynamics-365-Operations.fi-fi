--- 
title: "Ylläpidä tuotemääritysmallin tuoterakennetta"
description: "Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 645d748235935ae67867295a87a84a6539710ab0
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Ylläpidä tuotemääritysmallin tuoterakennetta

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin. Tämä menettely luodaan käyttämällä USMF-demoyrityksen Korkealaatuinen kaiutin -mallia.


## <a name="add-a-bom-line"></a>Lisää tuoterakennerivi
1. Valitse Tuotevarianttimallin määritys.
2. Valitse Tuotekonfiguraation mallit.
3. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tähän menettelyyn korkealaatuinen kaiutin.  
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Laajenna Tuoterakennerivi-osa.
6. ValitseLisää.
7. Kirjoita arvo Nimi-kenttään.
8. Kirjoita arvo Kuvaus-kenttään.
9. Valitse Tallenna.

## <a name="add-bom-line-details"></a>Lisää tuoterakennerivin tiedot
1. Valitse Tuoterakennerivin tiedot.
2. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Valitse esimerkiksi nimike M0055.  
    * Voit valita kunkin tuoterakennerivin ominaisuuden kohdalla, annetaanko sille kiinteä arvo vai yhdistetäänkö se määritteeseen.  
3. Valitse Määritä-valintaruutu.
4. Valitse Laskenta-kentässä Kyllä.
    * Laskelma-ominaisuuden määrittäminen arvoksi Kyllä varmistaa, että tuoterakennerivi sisältyy kustannuslaskentaan.  
5. Valitse Asetukset-välilehti.
6. Valitse Määritä-valintaruutu.
7. Kirjoita numero Määrä-kenttään.
    * Määräkenttä määrittää, miten suuri osa nimikkeestä sisällytetään tuoterakenteeseen. Tämä voisi olla hyvä ehdokas määritteen yhdistämiselle.  
8. Valitse Dimensio-välilehti.
    * Tarkista, onko yksikään tuotedimensio aktiviinen ja onko sillä siksi oltava arvo tai määrite määritettynä.  
9. Valitse OK.


