---
title: Tallenna TDS-palautustodistuksen numerot
description: Tässä aiheessa kuvataan, kuinka Palautustodistukset-sivulla tallennetaan todistusnumerot ja -päivämäärät tietylle toimittajalle, asiakkaalle tai kirjanpitoon vastaanotettavat Vero vähennettynä lähteissä (TDS) -todistuksista.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023194"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Tallenna TDS-palautustodistuksen numerot

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka **Palautustodistukset**-sivulla tallennetaan todistusnumerot ja -päivämäärät tietylle toimittajalle, asiakkaalle tai kirjanpitoon vastaanotettavat Vero vähennettynä lähteissä (TDS) -todistuksista. Voit päivittää tälle sivulle TDS-tapahtumiin tallennetut TDS-todistusnumerot ja -päivämäärät valitsemalla **Päivitä sertifikaatti** -sivu (**Kirjanpito \> Kausittainen \> Ennakonpidätys \> Päivitä sertifikaatti**). Kun olet lopettanut TDS-sertifikaattien numeroiden päivittämisen, sulje ne.

Tallenna TDS-todistusnumerot ja -päivämäärät noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Vero \> Välillinen vero \> Ennakonpidätys \> Palautustodistukset**.

    [![Palautustodistukset-sivu](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Valitse **Palautustodistukset**-sivun **Verotyyppi**-kentässä valitse **TDS**.
3. Luo tietue valitsemalla **Uusi**.
4. Kirjoita **Todistusnumero**-kenttään TDS-huojennustodistuksen numero.
5. Valitse **Tilityyppi**-kentässä tilityyppi, jota varten TDS-todistus vastaanotetaan: **Toimittaja**, **Asiakas** tai **Kirjanpito**.
6. Valitse **Tili**-kentässä toimittaja-, asiakas- tai kirjanpitotilinumero valitsemasi tilityypin mukaan. **Nimi**-kentässä näkyy toimittajan, asiakkaan tai kirjanpitotilin nimi.
7. Syötä **Todistuksen summa** -kenttään TDS-todistuksen summa.
8. Kirjoita **Päivämäärä**-kenttään todistusnumeron todistuspäivämäärä.
9. Avaa **Todistustapahtumat**-sivu valitsemalla **Kyselyt**. Sivulla voit tarkastella TDS-tapahtumia, joille TDS-sertifikaatin numero ja päivämäärä päivitetään. Nämä tiedot voidaan päivittää **Päivitä sertifikaatti** -sivulla (**Vero \> Ilmoitukset \> Ennakonpidätys \> Päivitä sertifikaatti**).

    **Päivitä sertifikaatti** -sivulla näkyvät seuraavat tiedot kutakin TDS-tapahtumaa varten:

    - **Päivämäärä** – TDS-tapahtuman kirjauspäivämäärä.
    - **Tosite** – TDS-tapahtuman tositenumero.
    - **Lähde** – Moduuli, jolle TDS-tapahtuma luotiin.
    - **Tili** – Toimittajan, asiakkaan tai kirjanpitotilin numero, jota varten TDS-tapahtuma luotiin.
    - **Nimi** – Toimittajan, asiakkaan tai kirjanpitotilin nimi, jota varten TDS-tapahtuma luotiin.
    - **Summa** – Laskun summa, jonka perusteella TDS laskettiin.
    - **Veron summa** – Tapahtumalle laskettu TDS-veron summa.
    - **Todistuspäivämäärä** – TDS-todistuksen päivämäärä, joka päivitettiin TDS-tapahtumaa varten.
    - **Todistusnumero** – TDS-todistuksen numero, joka päivitettiin TDS-tapahtumaa varten.

10. Valitse **Palautustodistukset** -sivulla **Suljettu**-valintaruutu, jos haluat sulkea TDS-todistuksen numeron sen jälkeen, kun olet päivittänyt sen TDS-tapahtumille **Päivitä sertifikaatti** -sivulla.

    Voit valita sivun kaikkien tietueiden **Suljettu**-valintaruudun valitsemalla **Merkitse kaikki**.

    > [!NOTE]
    > TDS-todistuksen numerot, joille **Suljettu**-valintaruutu on valittuna, eivät ole käytettävissä **Päivitä sertifikaatti** -sivulla.
