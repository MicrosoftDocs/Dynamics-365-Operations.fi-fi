---
title: Raja-arvo ja poikkeusraja-arvo
description: Tässä artikkelissa kuvataan Vero vähennettynä lähteissä (TDS) raja- ja poikkeusraja-arvot.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: aceebad08b5454b64059e7ef374b9634bad35c37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877933"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Raja-arvo ja poikkeusraja-arvo

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan Vero vähennettynä lähteissä (TDS) raja- ja poikkeusraja-arvot. Laskujen ja maksujen TDS-tiedot lasketaan aina ottaen huomioon **Ennakonpidätyksen komponentit** -sivulla TDS-verokomponenteille määritetty raja- ja poikkeusraja. TDS-verokomponentit liitetään TDS-verokoodeihin, jotka sisältyvät TDS-veroryhmiin. TDS-veroryhmät liitetään toimittajiin ja asiakkaisiin TDS:n laskemiseksi lasku- tai maksutasolla.

TDS lasketaan, jos tapahtuman summa tai tietylle toimittajan TDS-ryhmälle kirjatut kumulatiiviset tapahtumat ylittävät **Ennakonpidätyksen komponentit** -sivulla määritetyn raja-arvon. TDS-tietoja ei lasketa, ennen kuin kumulatiivinen tapahtuman summa ylittää määritetyn raja-arvon.

Jos poikkeusraja-arvo määritetään yhdessä TDS-komponentin raja-arvon kanssa, TDS lasketaan, kun tietty tapahtumasumma ylittää poikkeusrajan, vaikka kumulatiivinen tapahtumasumma ei olisi määritettyä raja-arvoa suurempi.

### <a name="example"></a>Esimerkki
TDS-verokomponentti määritetään ja liitetään TDS-veroryhmään, jota kutsutaan alihankkijaksi. Raja-arvoksi on määritetty 50 000, ja TDS-verokomponentin poikkeusraja-arvoksi on määritetty 20 000. TDS-ryhmän alihankkija määritetään toimittajan 1 TDS-oletusryhmäksi.

Toimittajan 1 ostolasku 001 kirjataan arvolle 10 000. Laskulle ei lasketa TDS:ää, koska laskun summa ei ylitä raja-arvoa tai poikkeusraja-arvoa. Toimittajan 1 ostolasku 002 kirjataan arvolle 25 000. Laskulle lasketaan TDS, koska laskun summa ylittää poikkeusraja-arvon. Toimittajan 1 ostolasku 003 kirjataan arvolle 20 000. Laskulle lasketaan TDS, koska toimittajalle lähetettyjen kolmen laskun kokonaissumma ylittää raja-arvon. TDS lasketaan kaikista laskuista, jotka on lähetetty toimittajalle ja joille ei ole laskettu TDS:ää aiemmin. TDS lasketaan arvolle 30 000, joka on laskujen 001 ja 003 kokonaissumma.

Raja-arvoa ja poikkeusraja-arvoa ei oteta huomioon TDS-laskennassa, jos **Ohita raja** -valintaruutu on valittuna TDS-verokoodeille TDS-ryhmässä, joka on liitettynä tapahtumaan. Raja-arvoa ei käytetä TDS-ryhmän TDS-verokoodeissa, joita varten **Ohita raja** -valintaruutu on olemassa.

Jos tietylle TDS-ryhmälle on valittu **Ohita raja** -valintaruutu joillekin laskuille, mutta sitä ei valita muille tietylle toimittajalle tai asiakkaalle luoduille laskuille, TDS:n laskeminen niin, että raja-arvoa ei ohiteta muutamien laskujen osalta, tehdään ottaen huomioon kaikkien niiden laskujen kumulatiivinen summa, joille TDS:ää ei ole laskettu aiemmin.

Raja-arvo voi olla esimerkiksi 25 000. Seuraavat laskut on luotu toimittajalle A.

- Lasku 1 – 2 0000 – (**Ohita raja** -valintaruutua ei ole valittu): TDS:ää ei lasketa.

- Lasku 2 – 4 0000 – (**Ohita raja** -valintaruutu on valittuna): TDS lasketaan arvolle 4 000.

- Lasku 2 – 3 000 – (**Ohita raja** -valintaruutua ei ole valittu): TDS lasketaan kumulatiivisen laskun summana, eli 27 000 (20 000 + 4 000 + 3 000) ylittää raja-arvon. TDS lasketaan niiden laskujen kumulatiivisen summan perusteella, joiden osalta TDS:ää ei ole laskettu aiemmin eli 23 000 (20 000 + 3 000).
