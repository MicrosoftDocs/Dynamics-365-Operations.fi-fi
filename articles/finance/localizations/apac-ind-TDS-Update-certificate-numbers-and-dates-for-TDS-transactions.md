---
title: Päivitä sertifikaattinumerot ja päivämäärät TDS-tapahtumille
description: Tässä aiheessa kuvataan, kuinka palautustodistuksen numerot ja päivämäärät, jotka on tallennettu toimittajalle, asiakkaalle tai kirjanpitotileille Vero vähennettynä lähteissä (TDS) -tapahtumille.
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023204"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Päivitä sertifikaattinumerot ja päivämäärät TDS-tapahtumille

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka palautustodistuksen numerot ja päivämäärät, jotka on tallennettu toimittajalle, asiakkaalle tai kirjanpitotileille Vero vähennettynä lähteissä (TDS) -tapahtumille. Voit tarkastella TDS-tapahtumien todistuksia **Palautustodistukset**-sivulla. Voit päivittää todistukset **Päivitä todistukset** -sivulla.

Päivitä TDS-tapahtumien todistusnumerot ja -päivämäärät noudattamalla seuraavia vaiheita.

1. Valitse **Vero \> Ilmoitukset \> Ennakonpidätys \> Päivitä todistus**.

    [![Päivitä todistus -sivu](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Valitse **Päivitä todistus** -sivun **Valitse**-osassa **Verotyyppi**-kentässä **TDS**.
3. Valitse **Todistusnumero**-kentässä asiakkaan tai toimittajan TDS-todistuksen numero.

    > [!NOTE]
    > **Todistusnumero**-kentässä luetellaan vain ne TDS-todistusten numerot, joissa **Suljettu**-valintaruudun valinta on poistettu **Palautustodistukset**-sivulla.

    **Todistuspäivämäärä**-kentässä on näkyvissä todistuspäivämäärä. **Tilityyppi**-kentässä näkyy tilityyppi, jota varten TDS-todistusnumero vastaanotetaan, ja nimikentässä näkyy tilin **Nimi**.

5. Valitse **Päivämäärästä**- ja **Päivämäärään**-kentissä sen kauden alkamis- ja päättymispäivät, joille TDS-tapahtumat näytetään.
6. Valitse **Näytä tiedot**, jos haluat tarkastella valitulla kaudella kirjattuja TDS-tapahtumia.

    Yläruudun **Yhteenveto**-välilehdessä näkyy seuraavat tiedot kaikista toimittajalle tai asiakkaalle valitun kauden aikana kirjatuista TDS-tapahtumista:

    - **Tosite** – TDS-tapahtuman tositenumero.
    - **Päivämäärä** – TDS-tapahtuman päivämäärä.
    - **Summa** – Laskun summa, jonka perusteella TDS laskettiin.
    - **Veron summa** – Tapahtumalle laskettu TDS-veron summa.

7. Jos haluat siirtää tiettyjä TDS-tapahtumia ylemmästä ruudukosta alempaan ruudukkoon, valitse tapahtumat ja valitse sitten **Sisällytä**. Vaihtoehtoisesti voit siirtää kaikki TDS-tapahtumat ylemmästä ruudukosta alempaan ruudukkoon valitsemalla **Sisällytä kaikki**.

    Jos haluat siirtää tiettyjä TDS-tapahtumia tai kaikki TDS-tapahtumat alemmasta ruudukosta yläruudukkoon, käytä **Sulje pois**- tai **Sulje pois kaikki** -painiketta.

8. Valitse **Päivitä** päivittääksesi **Todistusnumero**- ja **Todistuspäivämäärä**-kentät TDS-tapahtumille alemmassa ruudukossa.
10. Valitse **Vero \> Välilliset verot \> Ennakonpidätys \> Palautustodistus** ja valitse **Kysely**, jos haluat tarkastella päivitettyjä tapahtumarivejä, joissa on uudet todistusnumerot **Todistustapahtumat**-sivulla.

    [![Todistustapahtumat-sivu](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
