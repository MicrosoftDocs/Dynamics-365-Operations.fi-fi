---
title: Määritä arvonlisäveron tilityskaudet
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisävero tilityskaudet Dynamics 365 Financessa.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 197b85fb88f966b0a13fc061e2e780dd84e74acb
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735811"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Määritä arvonlisäveron tilityskaudet

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisäveron täsmäytyskaudet. Arvonlisäveron tilityskaudet sisältävät tietoja kausiväleistä, joilta arvonlisävero on raportoitava ja maksettava. Tilitysprosessi voidaan suorittaa tietyn päivämäärävälin tilityskaudelle. Kaikki tilityskauteen liittyvät verokoodit on tilitettävä. Liittyvän arvonlisäveroviranomaisen määrityksestä riippuen verovelka kirjataan joko toimittajan tilille tai kirjanpitotilille.

Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Vero > Välilliset verot > Arvonlisävero > Arvonlisäveron tilityskaudet**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Tilityskausi**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Viranomainen**-kentästä arvonlisäveroviranomainen, joka vastaanottaa tilityskaudelle luodut raportit ja maksut.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Valitse **Maksuehdot**-kentässä avattavasta valikosta haluamasi tietue. Liittyvä arvonlisäveroviranomainen voidaan määrittää toimittajaksi. Arvonlisäveron tilitys luo avoimen toimittajan laskun. Maksuehdot määrittävät avoimen toimittajan laskun eräpäivän.  
8. Valitse tilityskauden välien tyyppi.
9. Syötä kausivälien yksiköiden määrä kautta kohti. Esimerkiksi neljännesvuosi sisältää 3 kuukautta.
10. Valitse **Käytä arvonlisäveron tilitykseen eräprosessia** -valintaruutu tai poista sen valinta. Tilityskauden tilitysprosessi voidaan käsitellä taustalla erätyönä. Tätä suositellaan, jos kausiväli sisältää paljon verotapahtumia.
11. Valitse **Estä verotapahtumien vastakirjauksien luonti** -valintaruutu tai poista sen valinta. Järjestelmä luo oletusarvoisesti verotapahtumien vastakirjauksia selvitysprosessin aikana, mikä voi heikentää suorituskykyä, jos kausiväliin sisältyy suuri määrä verotapahtumia. Estä verotapahtumien vastakirjauksien luonti valitsemalla tämä valintaruutu.
12. Laajenna **Kausivälit**-välilehti.
13. Valitse **Lisää**.
14. Kirjoita päivämäärä uuden rivin **Päivämäärästä**-kenttään.
15. Kirjoita päivämäärä **Päivämäärään**-kenttään.
16. Valitse **Uusi kausiväli**. Kun ensimmäinen kausiväli on syötetty, uudet kaudet voidaan luoda automaattisesti. Voit siirtyä takaisin ja lisätä tarvittaessa uusia kausivälejä.  
17. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
