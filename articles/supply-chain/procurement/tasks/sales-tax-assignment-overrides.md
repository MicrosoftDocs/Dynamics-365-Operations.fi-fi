---
title: Arvonlisäveron määrittäminen ja ohitukset
description: Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään vähittäismyynnin kanaville.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbaa467c22656aa8d1e39d26a8233250e2bb66f8
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026598"
---
# <a name="sales-tax-assignment-and-overrides"></a>Arvonlisäveron määrittäminen ja ohitukset

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään vähittäismyynnin kanaville. Siinä käydään läpi myös uusien arvonlisävero-ohitusten luontiprosessi sekä niiden määrittäminen olemassa oleviin arvonlisäveron ohitusryhmiin. Menettely käyttää esittelytietojen USRT-yritystä.

1. Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.
2. Napsauta luettelossa Houstonin vähittäismyyntikanavan linkkiä.
3. Valitse Muokkaa.
    * Arvonlisäveroryhmä-kenttä sisältää nykyisen yrityksen arvonlisäveroryhmien luettelon. Tällä hetkellä määritetty ryhmä on yleinen "Teksas"-arvonlisäveroryhmä. Myös seuraavat arvonlisäveroryhmät ovat järjestelmässä: Washington ja Washington, King County. Arvonlisäveroryhmät voivat sisältää useita kuntia koskevia veroja.  
    * "Arvonlisäveron ohitus" -kentässä määritetään kanavan arvonlisäveron ohitusryhmät. Arvonlisäveron ohitusryhmiä voi käyttää useiden arvonlisäveropoikkeuksien ryhmittämiseen, jotka toimivat useille myymälöille. Sen sijaan, että arvonlisäveron ohitukset määritettäisiin yksitellen, voit säästää aikaa luomalla ryhmän ja määrittää sen suoraan kanaviin.  
4. Valitse Tallenna.
5. Sulje sivu.
6. Valitse Vähittäismyynti ja kauppa > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitukset.
7. Valitse Uusi.
8. Anna Arvonlisäveron ohitus -kentässä uudelle ohitukselle nimi.
9. Anna ohituksen kuvaus Kuvaus-kenttään.
10. Ota tilaksi "Käytössä".
11. Laajenna tai tiivistä Ohitus-osa.
12. Valitse vaihtoehto Tyyppi-kentässä.
    * Nimikkeen arvonlisäveroryhmiä voi käyttää verojen ohittamiseen tietyille nimikkeille, jotka kuuluvat ryhmään. Esimerkiksi ruokanimikkeiden verotus on yleensä eri tasolla kuin fyysisillä tuotteilla, ja niillä on yleensä oma arvonlisäveroryhmänsä.     Arvonlisäveroryhmät ovat tietyn kanavan käytettävissä olevia veroryhmiä. Jos esimerkiksi kanava myy sekä vähittäiskauppana sekä yrityksille, nimikkeille voi käyttää eri arvonlisäveroryhmiä. Kaikki sovellettavat verot liitetään arvonlisäveroryhmään.  
    * Nyt voit valita Lähde- ja Kohde-verot tai "Veroryhmästä" ja "Veroryhmään" luodaksesi arvonlisäveron ohituksen.    Lähde-kenttä ilmaisee ohitettavan veron tai veroryhmän. Nimikkeen arvonlisäveroryhmän ohittamisella on eri vaihtoehdot kuin arvonlisäveroryhmän perusteella ohittamisella.    Arvonlisäveron ohitukset voi määrittää ohittamaan verot kokonaisilla tapahtumilla tai vain tietyillä tapahtuman riveillä.  
13. Valitse Tallenna.
14. Sulje sivu.
15. Valitse Vähittäismyynti ja kauppa > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitusryhmät.
    * Tässä vaiheessa määritetään uusi ohitus arvonlisäveron ohitusryhmään, joka on liitetty Houstonin kanavaan.  
16. Valitse Muokkaa.
17. Laajenna tai tiivistä Asetukset-osa.
18. ValitseLisää.
19. Avaa haku valitsemalla Arvonlisäveron ohitusryhmä -kentässä avattavan valikon painike.
20. Valitse luettelosta aiemmin luotu arvonlisäveron ohitus.
21. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
22. Valitse Tallenna.

