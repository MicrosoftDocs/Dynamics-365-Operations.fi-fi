---
title: Ylläpidä tuotemääritysmallin tuoterakennetta
description: Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcdf4b735587b76b7f761f59c56da1ca358a2e37
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426931"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Ylläpidä tuotemääritysmallin tuoterakennetta

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]