---
title: Palkanlaskennan työntekijän osoite
description: Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan työntekijän osoite -yksikölle Dynamics 365 Human Resourcesissa.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881974"
---
# <a name="payroll-worker-address"></a>Palkanlaskennan työntekijän osoite

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tämä ohjeaihe sisältää tietoja ja esimerkkikyselyn palkanlaskennan työntekijän osoite -yksikölle Dynamics 365 Human Resourcesissa.

## <a name="properties"></a>Ominaisuudet

| Ominaisuus<br>**Fyysinen nimi**<br>**_Laji_** | Käytä | kuvaus |
| --- | --- | --- |
| **Paikkakunta**<br>mshr_city<br>*Merkkijono* | Vain luku<br>Vaadittu | Osoitteessa määritetty paikkakunta.   |
| **Henkilöstönumero**<br>mshr_personnelnumber<br>*Merkkijono* | Vain luku<br>Vaadittu | Työntekijän yksilöivä henkilökuntanumero.  |
| **Maa alue**<br>mshr_countryregionid<br>*Merkkijono* | Vain luku<br>Vaadittu | Osoitteeseen määritetty maa tai alue  |
| **Voimassaolo alkaa**<br>mshr_postaladdressvalidfrom<br>*Päivämäärä aika siirros* | Vain luku <br>Vaadittu | Päivämäärä, josta alkaen osoite on voimassa. |
| **Työskenteli osoitteessa**<br>mshr_isworkedinaddressbr>*Int32* | Vain luku<br>Vaadittu | Osoittaa, onko osoite se, jossa työntekijä työskentelee. |
| **Lääni**<br>mshr_county<br>*Merkkijono* | Vain luku<br>Vaadittu | Osoitteessa määritetty maakunta.  |
| **Palkanlaskennan työntekijän osoitteen tunnus**<br>mshr_payrollworkeraddressentityid<br>*GUID* | Vaadittu<br>Järjestelmän luoma | Järjestelmän luoma GUID-arvo, jonka avulla osoite voidaan yksilöivästi tunnistaa.  |
| **Ensisijainen kenttä**<br>mshr_primaryfield<br>*Merkkijono* | Vain luku<br>Vaadittu |  |
| **Katu**<br>mshr_street<br>*Merkkijono* | Vain luku<br>Vaadittu | Osoitteessa määritetty katu. |
| **Voimassaolo päättyy**<br>mshr_postaladdressvalidto<br>*Päivämäärä aika siirros* | Vain luku <br>Vaadittu | Päivämäärä, johon asti osoite on voimassa.  |
| **Sijainnin tunnus**<br>mshr_locationidbr>*Merkkijono* | Vain luku <br>Vaadittu | Osoitteen tunnus.  |
| **Postinumero**<br>mshr_zipcode<br>*Merkkijono* | Vain luku <br>Vaadittu |Työntekijälle määritetty tunnusnumero.  |
| **Asui osoitteessa**<br>mshr_islivedinaddressbr>*merkkijono* | Vain luku<br>Vaadittu | Osoittaa, onko osoite se, jossa työntekijä asuu. |
| **Alue**<br>mshr_state<br>*Merkkijono* | Vain luku<br>Vaadittu | Osoitteessa määritetty osavaltio.  |

## <a name="example-query"></a>Esimerkkikysely

**Pyyntö**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Vastaus**

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
