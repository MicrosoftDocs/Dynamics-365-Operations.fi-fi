---
title: Julkaistun päätuotteen perusmääritysten päättäminen
description: Tässä aiheessa selvitetään, mitkä asetukset on ainakin määritettävä, ennen kuin päätuotetta voi käyttää tuoterakenneversioissa.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd7e02c9aea17fbc3312660d0e50cd8bbf39aa3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845014"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Julkaistun päätuotteen perusmääritysten päättäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä aiheessa selvitetään, mitkä asetukset on ainakin määritettävä, ennen kuin päätuotetta voi käyttää tuoterakenneversioissa.

Tämä on kolmas kahdeksasta menettelystä, joissa selitetään, miten dimensioihin perustuvia konfiguraatioyhdistelmiä luodaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.

1. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.
2. Etsi haluamasi tietue luettelosta ja valitse se. Valitse toisessa menettelyssä vapautettu päätuote. Tämä päätuote on luotu dimensioihin perustuvalla konfiguraatiomenetelmällä.  
3. Valitse toimintoruudussa **Tuote**.
4. Avaa valintaikkunalomake valitsemalla **Dimensioryhmät**.
5. Avaa haku valitsemalla **Varastodimensioryhmä**-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se. Varastodimensioryhmä määrittää, mitä varastodimensioita käytetään tuotetapahtumassa. Valitse **Toimipaikka** tässä menettelyssä.  
7. Avaa haku valitsemalla **Seurantadimensioryhmä**-kentässä avattavan valikon painike.
8. Etsi haluamasi tietue luettelosta ja valitse se. Seurantadimensioryhmä määrittää, mitä seurantadimensioita käytetään tuotetapahtumassa. Valitse tässä menettelyssä **Ei mitään**.  
9. Valitse **OK**.
10. Valitse **Muokkaa**.
11. Avaa haku valitsemalla **Nimikemalliryhmä**-kentässä avattavan valikon painike.
12. Etsi haluamasi tietue luettelosta ja valitse se. Nimikemalliryhmien sisältämät asetukset määrittävät, kuinka nimikkeitä hallitaan ja käsitellään nimikkeiden vastaanotoissa ja varasto-otoissa. Ne määrittävät myös, millä tavalla nimikkeiden kulutus lasketaan. Valitse tähän menettelyyn **FIFO**.  
13. Laajenna **Kustannusten hallinta** -osa.
14. Avaa haku valitsemalla **Nimikeryhmä**-kentässä avattavan valikon painike.
15. Etsi haluamasi tietue luettelosta ja valitse se. Nimikeryhmiä käytetään varaston hallintaan jakamalla varastonimikkeet ryhmiin. Valitse **CarAudio** tähän menettelyyn.  
16. Valitse toimintoruudussa **Suunnitelma**.
17. Valitse **Tilauksen oletusasetukset**.
18. Valitse **Oletusarvoinen tilaustyyppi** -kentässä vaihtoehto. Valitsemalla **Tuotanto** voit määrittää, että tämän päätuotteen oletustoimitusvalinta on sen tuottaminen.  
19. Valitse **Tallenna**.
20. Sulje sivu.
21. Sulje **Vapautetun tuotteen tiedot** -lomake.

