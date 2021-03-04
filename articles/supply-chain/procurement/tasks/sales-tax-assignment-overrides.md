---
title: Arvonlisäveron määrittäminen ja ohitukset
description: Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään kaupan kanaville.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74a7eed04648c63c0b19d5de26d2bdbef59aec7d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427123"
---
# <a name="sales-tax-assignment-and-overrides"></a>Arvonlisäveron määrittäminen ja ohitukset

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään kaupan kanaville. Siinä käydään läpi myös uusien arvonlisävero-ohitusten luontiprosessi sekä niiden määrittäminen olemassa oleviin arvonlisäveron ohitusryhmiin. Menettely käyttää esittelytietojen USRT-yritystä.

1. Valitse Retail ja Commerce > Kanavat > Myymälät > Kaikki myymälät.
2. Napsauta luettelossa Houstonin kanavan linkkiä.
3. Valitse Muokkaa.
    * Arvonlisäveroryhmä-kenttä sisältää nykyisen yrityksen arvonlisäveroryhmien luettelon. Tällä hetkellä määritetty ryhmä on yleinen "Teksas"-arvonlisäveroryhmä. Myös seuraavat arvonlisäveroryhmät ovat järjestelmässä: Washington ja Washington, King County. Arvonlisäveroryhmät voivat sisältää useita kuntia koskevia veroja.  
    * "Arvonlisäveron ohitus" -kentässä määritetään kanavan arvonlisäveron ohitusryhmät. Arvonlisäveron ohitusryhmiä voi käyttää useiden arvonlisäveropoikkeuksien ryhmittämiseen, jotka toimivat useille myymälöille. Sen sijaan, että arvonlisäveron ohitukset määritettäisiin yksitellen, voit säästää aikaa luomalla ryhmän ja määrittää sen suoraan kanaviin.  
4. Valitse Tallenna.
5. Sulje sivu.
6. Valitse Retail ja Commerce > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitukset.
7. Valitse Uusi.
8. Anna Arvonlisäveron ohitus -kentässä uudelle ohitukselle nimi.
9. Anna ohituksen kuvaus Kuvaus-kenttään.
10. Ota tilaksi "Käytössä".
11. Laajenna tai tiivistä Ohitus-osa.
12. Valitse vaihtoehto Tyyppi-kentässä.
    * Nimikkeen arvonlisäveroryhmiä voi käyttää verojen ohittamiseen tietyille nimikkeille, jotka kuuluvat ryhmään. Esimerkiksi ruokanimikkeiden verotus on yleensä eri tasolla kuin fyysisillä tuotteilla, ja niillä on yleensä oma arvonlisäveroryhmänsä. Arvonlisäveroryhmät ovat tietyn kanavan käytettävissä olevia veroryhmiä. Jos esimerkiksi kanava myy sekä vähittäiskauppana sekä yrityksille, nimikkeille voi käyttää eri arvonlisäveroryhmiä. Kaikki sovellettavat verot liitetään arvonlisäveroryhmään.  
    * Nyt voit valita Lähde- ja Kohde-verot tai "Veroryhmästä" ja "Veroryhmään" luodaksesi arvonlisäveron ohituksen. Lähde-kenttä ilmaisee ohitettavan veron tai veroryhmän. Nimikkeen arvonlisäveroryhmän ohittamisella on eri vaihtoehdot kuin arvonlisäveroryhmän perusteella ohittamisella. Arvonlisäveron ohitukset voi määrittää ohittamaan verot kokonaisilla tapahtumilla tai vain tietyillä tapahtuman riveillä.  
13. Valitse Tallenna.
14. Sulje sivu.
15. Valitse Retail ja Commerce > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitusryhmät.
    * Tässä vaiheessa määritetään uusi ohitus arvonlisäveron ohitusryhmään, joka on liitetty Houstonin kanavaan.  
16. Valitse Muokkaa.
17. Laajenna tai tiivistä Asetukset-osa.
18. ValitseLisää.
19. Avaa haku valitsemalla Arvonlisäveron ohitusryhmä -kentässä avattavan valikon painike.
20. Valitse luettelosta aiemmin luotu arvonlisäveron ohitus.
21. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
22. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]