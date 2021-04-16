---
title: Määritä jälkeen päin päivitetyt sekit
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää, kirjataanko kirjauskansiomerkinnät jälkikirjatuille sekeille ja mitä kirjauskansioita käytetään merkintöjen ja toimittajamaksujen selvittämiseen.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2adb8b969a6e86becaa3c0a3b59d8f8f259e5a64
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834593"
---
# <a name="set-up-postdated-checks"></a>Määritä jälkeen päin päivitetyt sekit

[!include [banner](../../includes/banner.md)]

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
18. Valitse Tallenna.
19. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]