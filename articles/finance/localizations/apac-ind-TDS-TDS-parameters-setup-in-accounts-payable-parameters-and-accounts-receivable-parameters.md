---
title: Määritä myyntireskontran ja ostoreskontran TDS-parametrit
description: Tässä ohjeaiheessa on tietoja ostoreskontran ja myyntireskontran parametrien määrittämisestä niin, että ne tukevat Vero vähennettynä lähteissä (TDS) -vähennyksiä.
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023208"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>Määritä myyntireskontran ja ostoreskontran TDS-parametrit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja ostoreskontran ja myyntireskontran parametrien määrittämisestä niin, että ne tukevat Vero vähennettynä lähteissä (TDS) -vähennyksiä.

1. Valitse **Vero \> Asetukset \> Parametrit \> Myyntireskontran parametrit**.
2. Valitse **Päivitykset**-välilehdessä **Päivitä tilausrivit** avataksesi **Päivitä tilausrivit** -valintaikkuna.
3. Määritä **TDS-ryhmä**-osan **Päivitä TDS-ryhmä** -kentässä menetelmä, jolla TDS-ryhmä päivitetään rivitasolla. Tätä asetusta käytetään, kun TDS-ryhmä päivitetään tilauksen otsikkoon. Käytettävissä ovat seuraavat asetukset:

    - **Ei koskaan** – TDS-ryhmää ei päivitetä tilausriveille, kun se päivitetään tilauksen otsikkoon.
    - **Aina** – TDS-ryhmä päivitetään automaattisesti tilausriveille, kun se päivitetään tilauksen otsikkoon.
    - **Kehote** – Käyttäjät saavat sanoman, joka kehottaa heitä päivittämään TDS-ryhmän tilausriveille.
4. Valitse **OK**.

    [![Päivitä tilausrivit -valintaikkuna](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Valitse **Vero \> Asetukset \> Parametrit \> Ostoreskontran parametrit**.
6. **Yleiset**-välilehdessä **Jako toimitustietojen perusteella** -pikavälilehdessä määritä **Tuotteen vastaanotto** -kohdan asetukseksi **Kyllä**, kun haluat kirjata ja jakaa tuotteen vastaanoton, jolla on eri toimitusosoitteet ja verotilien numerot (TAN). Jos tämän asetuksen arvoksi on määritetty **Ei**, et voi kirjata oston pakkausluetteloa, jolla on eri toimitusosoitteet ja TAN-numerot.
7. Määritä **Lasku**-asetuksen arvoksi **Kyllä**, jos haluat kirjata ja jakaa ostolaskun, jolla on eri toimitusosoitteet ja TAN-numerot.

    [![Jako toimitustietojen perusteella -pikavälilehti](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Sulje sivu.
