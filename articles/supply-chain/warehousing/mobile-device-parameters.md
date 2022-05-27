---
title: Yleiset mobiililaitteen parametrit
description: Tässä aiheessa kuvataan, kuinka mobiililaitteen asetukset määritetään Varastonhallinnan parametrit -sivulla.
author: Mirzaab
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0ae04c86ff1eafb649fcef7c34ace66bdc3e5cb8
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679162"
---
# <a name="global-mobile-device-parameters"></a>Yleiset mobiililaitteen parametrit

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka määritetään yleiset varastonhallinnan parametrit, jotka vaikuttavat siihen, miten järjestelmä käy vuorovaikutusta mobiililaitteiden kanssa.

Lisätietoja siitä, miten varastotyöntekijät määritetään, löytyy kohdasta [Varastotyöntekijän hallinta](manage-warehouse-workers.md). Lisätietoja rekisterikilven käsittelystä mobiililaitteilla on kohdassa [Rekisterikilven vastaanotto Warehouse Managementin mobiilisovelluksen kautta](warehousing-mobile-device-app-license-plate-receiving.md). Lisätietoja inventoinnin prosesseista on kohdissa [Inventointi](cycle-counting.md) ja [Inventoinnin esimerkkiskenaariot](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Avaa varastonhallinnan parametrien sivu

Avataksesi **Varastonhallinnan parametrit** -sivun siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**. Tämän jälkeen voit määrittää mobiililaitteilla työskentelyyn liittyvät kentät tämän aiheen seuraavassa osassa kuvatulla tavalla.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Mobiililaite-pikavälilehti Yleiset-välilehdessä

Yleiset mobiililaiteasetukset löytyvät **Mobiililaite**-pikavälilehdestä **Yleiset**-välilehdessä **Varastonhallinnan parametrit** -sivulla. Seuraavat kentät ovat käytettävissä.

| Kenttä | kuvaus |
|---|---|
| Mobiililaitteen huomautustyyppi | Valitse tietotyyppi, joka näytetään työntekijöille myyntitilaustyön keräilyssä. |
| Skannatun määrän raja | Syötä nimikkeiden enimmäismäärä, jonka työntekijä voi skannata kunkin istunnon aikana, käyttämällä mobiililaitteen valikkonimikettä, jolla on **Työn luontiprosessi** -arvo kohdassa *Oikaisu sisään*. Tämä kenttä ei vaikuta skannauksiin, jotka on tehty muuntyyppisen valikkonimikkeen avulla. |
| Käytä mobiililaiteistunnon kirjausta lokiin | Määritä tämä vaihtoehto arvoon *Kyllä* säilyttääksesi työntekijän kirjautumishistorian lokin. Tarkastellaksesi lokia siirry kohtaan **Työn käyttäjäistunnot \> Kyselyt ja raportit \> Mobiililaitteiden lokit \> Työn käyttäjäistunnot**. |
| Tallennettujen virheiden määrä | Syötä virhetietueiden enimmäismäärä, jonka järjestelmän tulee tallentaa. Tarkastellaksesi virhelokia siirry kohtaan **Työn käyttäjäistunnot \> Kyselyt ja raportit \> Mobiililaitteiden lokit \> Työn käyttäjäistunnot**. |
| Varastosiirron oletuskirjauskansio | Valitse kirjauskansio, jota käytetään, kun työntekijät käyttävät mobiililaitetta tuotteiden siirtoon varastosta toiseen. |
| Salli ostotilausrivin rekisteröinti ulkoisessa tarkistuksessa | Määritä tämä vaihtoehto arvoon *Kyllä*, jos työntekijöillä tulee olla mahdollisuus käyttää mobiililaitetta rekisteröidäkseen tilausrivejä ostotilauksissa, joissa on **Hyväksymistila**-arvo kohdassa *Ulkoisessa tarkistuksessa*. Määritä tämä vaihtoehto arvoon *Ei* estääksesi työntekijöitä rekisteröimästä rivejä ostotilauksissa, jotka ovat ulkoisessa tarkistuksessa. |
| Ota RSAT-tuki käyttöön | Tämä kenttä ottaa käyttöön Warehouse Managementin mobiilisovelluksen tehtävävahvistajan, joka kirjaa lokin ja vahvistaa jokaisen vaiheen, jonka sovellus suorittaa. Koska tämä prosessi voi heikentää järjestelmän suorituskykyä merkittävästi, vahvistaja tulisi ottaa käyttöön vain testauksen aikana. Sitä ei tulisi ottaa koskaan käyttöön tuotantoympäristössä. |
