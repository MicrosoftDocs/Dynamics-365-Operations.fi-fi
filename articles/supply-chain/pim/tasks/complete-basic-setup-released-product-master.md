---
title: Julkaistun päätuotteen perusmääritysten päättäminen
description: Tässä aiheessa selvitetään, mitkä asetukset on ainakin määritettävä, ennen kuin päätuotetta voi käyttää tuoterakenneversioissa.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c6de9fa9dd49cc32f87a6041a3639198db9f182
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218606"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Julkaistun päätuotteen perusmääritysten päättäminen

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]