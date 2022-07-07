---
title: Lykkäyskirjausmenetelmät
description: Tässä artikkelissa kuvataan tuotto- ja kululykkäysten kirjausmenetelmien väliset erot tilauslaskutuksessa.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9019094"
---
# <a name="deferral-posting-methods"></a>Lykkäyskirjausmenetelmät

Tässä artikkelissa kuvataan tuotto- ja kululykkäysten kirjausmenetelmien väliset erot tilauslaskutuksessa.

**Tuoton ja kulujen lykkäysparametrit** -sivun lykkäyskirjausmenetelmät ovat **Tase** ja **Tulos**. Tämän artikkelin esimerkki sisältää tietoja näiden kahden menetelmän välisistä eroista ja valintaperusteista.

**Tase**-menetelmässä käytetään vain kahta tiliä. Tämän vuoksi asetuksia on tehtävä vain vähän. **Tulos**-menetelmässä on kaksi lisätiliä, jotka ovat **Alkuperäinen tunnustaminen** ja **Tuloutuksen vastakirjaus**. Niitä käytetään tuotossa, alennuksissa ja kustannuksissa tapahtumatyypistä riippuen. Nämä tilit määritetään **Lykkäyksen oletusarvot** -sivulla (**Tilauslaskutus \> Tuotto- ja kululykkäykset \> Asetukset**). Vaikka esimerkissä keskitytään lykättyyn tuottoon, samaa menetelmää voidaan käyttää lykätyissä alennuksissa ja kustannuksissa.

## <a name="example"></a>Esimerkki

Myyntilaskun 1 kokonaissumma on 3 000 $, ja sillä on lykättyä tuottoa. Seuraavissa taulukoissa näkyvät jaot, kun tämä myyntilasku kirjataan.

**Tase-menetelmä**

| Tyyppi | Tili | Veloitus | Hyvitys|
|---|---|---|---|
| Veloitus | Myyntireskontra | 3,000.00 | |
| Hyvitys | Viivästetty tuotto | | 3,000.00 |

**Tulos-menetelmä**

| Tyyppi | Tili | Veloitus | Hyvitys |
|---|---|---|---|
| Veloitus | Myyntireskontra | 3,000.00 | |
| Veloitus | Tuottokirjauksen vastakirjaus | 3,000.00 | |
| Hyvitys | Viivästetty tuotto | | 3,000.00 |
| Hyvitys | Alkuperäinen tuottokirjaus | | 3,000.00 |

Myyntilaskun 2 kokonaissumma on 2 000 $, ja sillä ei ole lykättyä tuottoa.

| Tyyppi | Tili | Määrä |
|---|---|---|
| Veloitus | Myyntireskontra | 3,000.00 |
| Hyvitys | Myyntituotto | 3,000.00 |

**Tase-menetelmä laskee yhteen myyntilaskun 1 ja 2**

| Tili | Veloitus | Hyvitys |
|---|---|---|
| Myyntireskontra | 5,000.00 | |
| Myyntituotto | | 2,000.00 |
| Viivästetty tuotto | | 3,000.00 |

Kun **Tase**-menetelmä on käytössä, kauden bruttotuottoa ei ole helppo nähdä. Osa tuotosta on kirjattu **Lykätty tuotto** -tilille. Muista, että koska lykätty tuotto kirjataan jokaisella kaudella, **Lykätty tuotto** -tilillä on useita debet- ja kredit-kirjauksia. Tietyn kauden bruttotuotto yhdistetään tuoton kirjauksen saapuvien ja lähtevien kirjausten kanssa.

**Tulos-menetelmä laskee yhteen myyntilaskun 1 ja 2**

| Tili | Veloitus | Hyvitys |
|---|---|---|
| Myyntireskontra | 5,000.00 | |
| Myyntituotto | | 5,000.00 |
| Tuoton vastakirjaus | 3,000.00 | |
| Viivästetty tuotto | | 3,000.00 |

Kaikki tuotto siirretään tuloksen **Tuotto**-tilille. Lykätty tuotto siirretään tuloslaskelmasta taseeseen. Bruttotuottoa voi tarkastella helposti, koska kaikki kirjataan **Tuotto**-tilille. Osa tästä bruttotuotosta kuitenkin lykätään. Tämän vuoksi se siirretään **Lykätty tuotto** -tilille ja kirjataan myöhemmin.

**Tulos**-menetelmässä voidaan tarkastella **Tuotto**- ja **Tuoton vastakirjaus** -tiliä, kun halutaan katsoa bruttotuottoa, joka on 5 000 $, ja nettotuottoa (lykättyjen nettosumma), joka on 2 000 $. Vaikka **Tulos**-menetelmä voi helpottaa raportointia, määritettäviä tilejä on enemmän kuin toisessa menetelmässä.
