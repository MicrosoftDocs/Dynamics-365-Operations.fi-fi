--- 
title: "Määritä jälkeen päin päivitetyt sekit"
description: "Tässä ohjeaiheessa kuvataan, kuinka voit määrittää, kirjataanko kirjauskansiomerkinnät jälkikirjatuille sekeille ja mitä kirjauskansioita käytetään merkintöjen ja toimittajamaksujen selvittämiseen."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: be0bf9e091b198f054745b29fa24318cee0b69ab
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-postdated-checks"></a>Määritä jälkeen päin päivitetyt sekit

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka voit määrittää, kirjataanko kirjauskansiomerkinnät jälkikirjatuille sekeille ja mitä kirjauskansioita käytetään merkintöjen ja toimittajamaksujen selvittämiseen. Voit myös määrittää selvitystilit lähetetyille ja vastaanotetuille sekeille sekä ennakonpidätykselle. Myöhemmäksi päivätyt sekit ovat sekkejä, jotka on asetettu tulevan päivämäärän omaavien maksujen vastaanottamista varten. Voit määrittää, onko sekin näyttävä kirjanpidossa ennen sen erääntymispäivämäärää.



Tämä menettelyn rooli on Rahastonhoitaja. Näissä toimintaohjeissa käytetään esittely-yritystä USMF.


## <a name="set-up-postdated-checks"></a>Määritä jälkeen päin päivitetyt sekit
1. Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.
2. Valitse Myöhemmäksi päivätyt sekit -välilehti.
3. Valitse Ota käyttöön myöhemmäksi päivätyt sekit -valintaruutu tai poista sen valinta.
4. Valitse Myöhemmäksi päivättyjen sekkien kirjauskansiokirjaukset -valintaruutu tai poista sen valinta.
5. Määritä Asetettujen sekkien siirtotili -kentän arvot.
6. Määritä Vastaanotettujen sekkien siirtotili -kentän arvot.
7. Kirjoita Siirtokirjausten kirjauskansio -kenttään arvo.
8. Kirjota Siirrä myöhemmäksi päivättyjä sekkejä tämän toimittajan maksukirjauskansioon -kenttään arvo.
9. Määritä Ennakonpidätyksen selvitystili -kentän arvot.
10. Valitse Tallenna.
11. Sulje sivu.
12. Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksutavat.
13. Valitse Uusi.
14. Syötä arvo Maksutapa-kenttään.
15. Myöhemmäksi päivättyjen sekkien siirtokirjaus -vaihtoehdon valinta osoittaa, , että sekin summa kirjataan selvitystilille.
16. Valitse Tilityyppi-kentässä Pankki.
    * Maksutavan vastatili on pankki.  
17. Määritä Maksutili-kentän arvot.
    * Valitse laskun summan vähennyksessä käytettävä pankkitili.  
18. Sulje sivu.
19. Valitse Myyntireskontra > Maksun asetukset > Maksutavat.
20. Valitse Uusi.
21. Syötä arvo Maksutapa-kenttään.
22. Myöhemmäksi päivättyjen sekkien siirtokirjaus -vaihtoehdon valinta osoittaa, , että sekin summa kirjataan selvitystilille.
23. Valitse Tilityyppi-kentässä Pankki.
    * Maksutavan vastatili on pankki.  
24. Määritä Maksutili-kentän arvot.
    * Valitse laskun summan vähennyksessä käytettävä pankkitili.  
25. Sulje sivu.


