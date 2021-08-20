---
title: Asiakkaiden ja toimittajien TDS-ryhmä-, PAN- ja TAN-tietojen määrittäminen
description: Tässä aiheessa kerrotaan, miten määritetään toimittajien ja asiakkaiden Vero vähennettynä lähteissä (TDS) -ryhmän tiedot, pysyvä tilinumero (PAN) ja verotilin numero (TAN).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b736838f1743a39d1f899f2679a31a2c0fe9a2b31e03b29d22af821314f329c9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745745"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Asiakkaiden ja toimittajien TDS-ryhmä-, PAN- ja TAN-tietojen määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten määritetään toimittajien ja asiakkaiden Vero vähennettynä lähteissä (TDS) -ryhmän tiedot, pysyvä tilinumero (PAN) ja verotilin numero (TAN).

1. Valitse **Ostoreskontra \> Toimittajat \> Kaikki toimittajat** tai **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.

    [![Kaikki toimittajat -sivu.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Valitse toimintoruudusta **Uusi**, jos haluat luoda toimittajan tai asiakkaan, ja syötä tarvittavat tiedot. Vaihtoehtoisesti voit valita aiemmin luodun toimittajan tai asiakkaan.
3. Määritä **Lasku ja toimitus** -pikavälilehden **Ennakonpidätys**-osassa **Laske ennakonpidätys** -asetuksen arvoksi **Kyllä**, kun haluat laskea toimittajan tai asiakkaan ennakonpidätyksen, TDS:n tai Lähteessä kerätyn veron (TCS).
4. Ostolaskun TDS-tiedot lasketaan toimittajalle tai asiakkaalle määritetyn TDS-oletusryhmän perusteella. Valitse **TDS-ryhmä**-kentässä oletusarvoinen TDS-ryhmä.

    > [!NOTE]
    > Kun valitset TDS-ryhmän **TDS-ryhmä**-kentässä, **Ennakonpidätysryhmä**- ja **TCS-ryhmä**-kentät eivät ole käytettävissä.

5. Valitse **Verotiedot**-pikavälilehden **PAN-tiedot**-osassa **Tila**-kentästä toimittajan tai asiakkaan pysyvä tilinumeron tila:

    - **Ei käytettävissä** – Toimittajalla tai asiakkaalla ei ole PAN-numeroa.
    - **Vastaanotettu** – Toimittajalla tai asiakkaalla on PAN-numero.
    - **Haettu** – Toimittaja tai asiakas on hakenut PAN-numeroa.
    - **Virheellinen** – Toimittajalla tai asiakkaalla on PAN-koodi, mutta se ei kelpaa.

6. Jos valitsit **Tila**-kentästä **Vastaanotettu**-kentässä ilmaistaksesi, että toimittajalla tai asiakkaalla on PAN-numero, kirjoita PAN **Numero**-kenttään. PAN-numerossa on oltava viisi aakkosmerkkiä, sitten neljä numeromerkkiä ja yksi aakkosmerkki. Tässä on esimerkki: **ABCDE1260A**.
7. Jos valitsit **Tila**-kentästä **Haettu**-kentässä ilmaistaksesi, että toimittaja tai asiakas on hakenut PAN-numeroa, kirjoita viitenumero **Viitenumero**-kenttään.
8. Valitse **Arvioitavan kohteen luonne** -kentässä arvioitavan kohteen luonteen luokka, johon toimittaja tai asiakas kuuluu:

    - Yhtiö
    - HUF
    - Vahvista
    - Henkilö
    - AOP
    - BOI
    - Paikallinen viranomainen
    - Muut

    [![Verotiedot-pikavälilehti.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. Toimintoruudun **Toimittaja**-välilehdessä **Rekisteröinti**-ryhmässä valitse **Rekisteröintitunnukset** avataksesi **Osoitteiden hallinta** -sivun.
10. Valitse **Osoitteiden hallinta** -sivulla **Verotiedot**-pikavälilehdellä **Lisää** tai **Muokkaa** avataksesi **Verotietojen hallinta** -sivun, jossa voit ylläpitää verorekisteröintimerkintää.
11. **Verotietojen hallinta** -sivulla **Ennakonpidätys**-pikavälilehdessä **Verotilin numero (TAN)** -kentässä syötä TAN. TAN-numerossa on oltava neljä aakkosmerkkiä, sitten viisi numeromerkkiä ja yksi aakkosmerkki. Tässä on esimerkki: **AFGH54821T**.
12. Sulje sivu.
