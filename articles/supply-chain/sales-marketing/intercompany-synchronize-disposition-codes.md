---
title: Käsittelykoodien synkronointi
description: Tässä aiheessa käsitellään konsernin sisäisen kaupankäynnin käsittelykoodien synkronointia
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 04a25324e79a1f9cb30a7da19d648bda995ba7b2
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548233"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Konsernin sisäisten käsittelykoodien synkronointi

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management tukee konsernin sisäisiä palautuksia antamalla mahdollisuuden yhdistää ulkoisesti määritetyt käsittely niitä vastaaviin sisäisiin käsittelykoodeihin. Kun konsernin sisäinen ketju määritetään, käsittelykoodien on oltava samat toisiinsa yhdistetyissä yrityksissä. Jos käsittelykoodit eivät ole samat, synkronointiprosessi epäonnistuu.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Tietoja kolmen osapuolen suorien palautusten käsittelykoodeista

Käsittelykoodit synkronoidaan konsernin sisäiseltä myyntitilausriviltä alkuperäiselle myyntitilausriville. Synkronointi vaikuttaa kuitenkin alkuperäisellä myyntirivillä heti vain yhdellä tavalla. Kyseinen vaikutus on se, että muut rivikulut poistetaan yrityksessä A määritetyn käsittelykoodin ja muiden kulujen perusteella. Yritys A on palautustilauksen luova yritys.

Kolmen osapuolen suorassa toimitusketjussa kaikkia käsittelytapahtumia tuetaan konsernin sisäisellä myyntitilausrivillä. Jos tuote kuitenkin palautetaan asiakkaalle, on varmistettava, että palautustilauksen toimitusosoite vastaa alkuperäisessä tilauksessa määritettyä asiakkaan toimitusosoitetta.

> [!NOTE]
> Ostotilauksissa ei käytetä käsittelykoodeja. Tämän vuoksi synkronointi on suoritettava myyntitilauksesta myyntitilaukseen, kun käsittelykoodeja synkronoidaan konsernin sisäisestä myyntitilauksesta alkuperäiseen palautustilaukseen .

## <a name="replacing-returned-items"></a>Palautettujen nimikkeiden korvaaminen

Jos palautettu nimike korvataan ja korvaava tilaus on jo luotu yrityksessä B, käsittely ei voi valita eikä korvaavaa tilausta voi luoda yrityksessä A.

## <a name="rules-for-intercompany-direct-deliveries"></a>Konsernin sisäisten suoratoimitusten säännöt

Seuraavat yleiset säännöt koskevat konsernin sisäisten suoratoimitusten alkuperäisiä palautustilauksia:

- Jos perustana oleva alkuperäisen myyntitilauksen käsittelytoiminto on Hyvitys ja hävikki, Hyvitys tai Palautus asiakkaalle, käytettävä käsittelytehtävä on Hyvitys. Palautus asiakkaalle -toimintokoodi määrittää kuitenkin aiemmin luodun rivin ja uuden, konsernin sisäisestä myyntitilauksesta synkronoidun rivin nettosummaksi 0 (nolla). Hävikkirivejä ei sen sijaan synkronoida koskaan. Kun rivi lisätään konsernin sisäiseen myyntitilaukseen, sitä ei koskaan synkronoida myyntitilaukseen, jolla on positiivinen määrä ja jonka käsittelytoimintona on hävikki (kuten Hyvitys ja hävikki tai Korvaus ja hävikki).
- Hyvitys ja korvaus tai Hävikki ja korvaus -toiminnon perustana olevaa käsittelytoimintoa ei ohiteta. Sitä käsitellään Hyvitys ja korvaus tai Hävikki ja korvaus -toiminnon käsittelytoimintona. Tätä sääntöä käytetään, vaikka yrityksessä A ei luoda hävikkiriviä eikä yrityksessä B (palautetun nimikkeen vastaanottava yritys) korvaavaa tilausta. Korvaava tilaus luodaan yrityksessä A vain, kun pakkausluettelo päivitetään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
